Limit Mapped Values
======================

Synchronizing values from a CRM contact involves reading attributes from CRM
and then mapping those values to the xDB Contact. If you want to limit the
values that are synchronized, you must disable the *value mapping*, and
potentially prevent the CRM contact attribute from being read.

.. contents:: Steps:
  :local:
  :depth: 2

Disable Value Mapping
------------------------

Existing value mappings can be disabled or deleted. However, disabling a
value mapping is often preferable to deleting a value mapping because
you may, in the future, decide that you want the value mapping after all.

#. Navigate to your *tenant*.
#. Navigate to **Value Mapping Sets > CRM Contact to xDB Contact**.
#. Select the value mapping item you want to disable.
#. For the field **Enabled**, untick the box.
#. Save the item.

This setting will take affect the next time the synchronization process runs.

.. note::
  This setting will affect the CRM contacts are read in the future.
  Values that are already mapped will not be removed from Sitecore.

Limit Attributes Read from CRM
--------------------------------

By disabling the value mapping, you will prevent the value from being set
on the xDB contact. You will not, however, prevent Dynamics CRM Connect from
reading the attribute from the CRM.

In order to ensure the attribute does not get read from the CRM, you must
disable the *value accessor* that corresponds to the attribute.

#. Navigate to your tenant.
#. Navigate to **Data Access > Value Accessor Sets > Providers**.
#. Navigate to **Dynamics CRM > CRM Contact Attributes**.
#. Select the value accessor.
#. For the field **Enabled**, untick the box.
#. Save the item.

This setting will take affect the next time the synchronization process runs.

.. caution::
  If you disable the value accessor without disabling the corresponding
  value mapper, an error will occur when you run the synchronization
  process.


