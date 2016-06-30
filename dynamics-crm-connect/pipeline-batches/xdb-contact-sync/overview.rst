Overview
==========================

This synchronization process is defined in the *pipeline batch*
**xDB Contacts to CRM Sync Pipeline Batch**.

The contact synchronization process involves the following steps:

#.	Read contacts from xDB.
#.	Loop through the contacts from xDB. For each contact:

  a)	Get the CRM contact that corresponds to the xDB contact if one exists, otherwise create a new CRM contact.
  b)	Apply value mappings by reading values from the xDB contact and writing those values to the CRM contact.
  c)	Save the CRM contact.
  d)	If the CRM contact was created.

      i.	Get the xDB contact.
      ii.	Get the contact from the work queue that corresponds to the xDB contact if one exists, otherwise add the contact to the work queue.
      iii.	Apply value mappings by reading values the CRM contact and writing those values to the work queue contact.

      .. note::
        Writing data back to the xDB contact is needed so that the CRM contact id is set on the xDB contact. This facilitates future synchronization.

3.	Read contacts from work queue.
#.	Create a known contact set for the xDB bulk contact update API.
#.	Loop through the contacts from the work queue. For each contact:

   a) Add the contact to the known contact set.

6.	Submit the known contact set.

.. image:: _static/xdb-contacts-sequence-diagram-simple.png

.. note::
  A more detailed sequence diagram is available
  :download:`here <_static/xdb-contacts-sequence-diagram-detailed.png>`.
