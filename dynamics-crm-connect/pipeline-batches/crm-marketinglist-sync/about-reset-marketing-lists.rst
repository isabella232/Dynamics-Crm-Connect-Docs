.. _about-rest-crm-marketinglist:

About Reset Marketing Lists
============================

The step in the CRM marketing list synchronization process where existing
marketing lists are reset is needed due to the way marketing list membership
is read.

A simplified description of the logic is:

#.	Read all marketing lists.
#.	For each marketing list, get the contacts who are members of the list.
#.	For each contact, add the marketing list to the collection of marketing lists on the contact.

An example is helpful to understand why the reset is necessary. Consider
when a contact is a member of multiple marketing lists:

+----------------------+-----------------------------+-----------------------------+
| Step	               | Contact value (before)      | Contact value (after)       |
+======================+=============================+=============================+
| Update with List A   | \-                          | ``List A``                  |
+----------------------+-----------------------------+-----------------------------+
| Update with List B   | ``List A``                  | ``List A, List B``          |
+----------------------+-----------------------------+-----------------------------+
| Update with List C   | ``List A, List B``          | ``List A, List B, List C``  |
+----------------------+-----------------------------+-----------------------------+

What happens if the contact is removed from ``List C``? The next time the
synchronization process runs, CRM reports the contact is a member of ``List A``
and ``List B``. How does ``List C`` get removed from the xDB contact?

The reset marketing lists step ensures that the contact value is empty
before the CRM data is applied:

+----------------------+-----------------------------+-----------------------------+
| Step	               | Contact value (before)      | Contact value (after)       |
+======================+=============================+=============================+
| Reset Lists          | ``List A, List B, List C``  | \-                          |
+----------------------+-----------------------------+-----------------------------+
| Update with List A   | \-                          | ``List A``                  |
+----------------------+-----------------------------+-----------------------------+
| Update with List B   | ``List A``                  | ``List A, List B``          |
+----------------------+-----------------------------+-----------------------------+

What happens if the reset marketing lists step does not run? The values
from the previous synchronization remain:

+----------------------+-----------------------------+-----------------------------+
| Step	               | Contact value (before)      | Contact value (after)       |
+======================+=============================+=============================+
| No Reset Lists       | ``List A, List B, List C``  | ``List A, List B, List C``  |
+----------------------+-----------------------------+-----------------------------+
| Update with List A   | ``List A, List B, List C``  | ``List A, List B, List C``  |
+----------------------+-----------------------------+-----------------------------+
| Update with List B   | ``List A, List B, List C``  | ``List A, List B, List C``  |
+----------------------+-----------------------------+-----------------------------+

.. note::
  Why is this approach used to read marketing list membership? In a word:
  performance.

  We found that the alternatives (such as reading the marketing list
  membership for a contact at the same time you read the other contact data)
  are much slower when dealing with more than a couple dozen contacts.

  It is fully within your control to change how any synchronization process
  works. If you prefer to use a different approach, you can implement it.

.. caution::
  This step is not selective in which contacts are reset. If you are
  synchronizing with multiple Dynamics CRM systems, or if you are using
  filters to limit the contacts that you are synchronizing, this part of the
  synchronization process may not work as expected.

.. note::
  Future versions of Dynamics CRM Connect will allow you to assign a
  filter to the step that reads contacts from xDB so that only contacts
  that have been synchronized with a specific Dynamics CRM server will
  be selected.

