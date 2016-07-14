Set Maximum Number of CRM Contacts to Read
===============================================

By default, all active contacts are read from Dynamics CRM. You can
also set a limit for the number of contacts that are handled.

.. note::
  This setting is used in addition to the option to include inactive
  campaigns (see :doc:`/pipeline-batches/crm-contact-sync/read-inactive-contacts`)
  and the option to use a filter expression (see :doc:`/components/crm-filter-expressions/index`).

.. note::
  This setting does not restrict the number of contacts that are read
  from Dynamics CRM. The number of contacts that are read is determined
  by a combination of the expression that is used and the page size that
  is specified.

#. In Content Editor, navigate to your *tenant*.
#. Navigate to **Pipelines > CRM Contact Pipelines**.
#. Navigate to **Read CRM Contacts Pipeline > Read CRM Contacts**.
#. In the field **Maximum number of entities to read**, enter the maximum number of contacts you want to handle.
#. Save the item.

This setting will take affect the next time the synchronization process runs.

.. note::
  This setting will affect the CRM contacts are read in the future.
  CRM contacts that have already been synchronized will not be
  removed from Sitecore.
