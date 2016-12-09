Set Maximum Number of CRM Campaigns to Read
===============================================

By default, all active campaigns are read from Dynamics CRM. You can
also set a limit for the number of campaigns that are handled.

.. note::
  This setting is used in addition to the option to include inactive
  campaigns (see :doc:`/pipeline-batches/crm-campaign-sync/read-inactive-campaigns`)
  and the option to use a filter expression (see :def-providers-crm-component:`CRM Filter Expressions<crm-filter-expressions/index.html>`).

.. note::
  This setting does not restrict the number of campaigns that are read
  from Dynamics CRM. The number of campaigns that are read is determined
  by a combination of the expression that is used and the page size that
  is specified.

#. In Content Editor, navigate to your *tenant*.
#. Navigate to **Pipelines > CRM Campaign Pipelines**.
#. Navigate to **Read CRM Campaigns Pipeline > Read CRM Campaigns**.
#. In the field **Maximum number of entities to read**, enter the maximum number of campaigns you want to handle.
#. Save the item.

This setting will take affect the next time the synchronization process runs.

.. note::
  This setting will affect the CRM campaigns are read in the future.
  CRM campaigns that have already been synchronized will not be
  removed from Sitecore.
