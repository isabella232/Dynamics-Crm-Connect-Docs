Read Inactive CRM Contacts
=============================

By default, only active contacts are read from Dynamics CRM. In order to
include inactive contacts, you must do the following:

#. In Content Editor, navigate to your *tenant*.
#. Navigate to **Pipelines > CRM Contact Pipelines**.
#. Navigate to **Read CRM Contacts Pipeline > Read CRM Contacts**.
#. In the field **Exclude active filter**, tick the box.
#. Save the item.

This setting will take affect the next time the synchronization process runs.

.. caution::
  If you run the synchronization process with this option enabled, xDB
  contacts will be created for inactive CRM contacts. There is no
  *disabled* property on xDB contacts, so you will not be able to
  distinguish CRM contacts that are active from CRM contacts that are
  inactive.

.. note::
  This setting will affect the CRM contacts are read in the future.
  CRM contacts that have already been synchronized will not be
  removed from xDB.