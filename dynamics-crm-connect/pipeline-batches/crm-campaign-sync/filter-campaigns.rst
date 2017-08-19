Filter CRM Campaigns
========================

By default, all active campaigns are read from Dynamics CRM. You can define
an expression that provides a greater amount of control over which campaigns
are read.

.. note::
  This setting is used in addition to the option to include inactive
  campaigns described in the section :doc:`/pipeline-batches/crm-campaign-sync/read-inactive-campaigns`.

#. In Content Editor, navigate to your *tenant*.
#. Navigate to **Tenant Settings > Dynamics CRM > Filter Expressions > Campaign Filter Expressions**.
#. Insert a new item using the template **Filter Expression**.
#. Configure the item.

    .. tip::
        For more information on how to configure filter expresions, see 
        :def-framework-component:`Filter Expressions<filter-expressions/index.html>`. 

5. Navigate to your tenant.
#. Navigate to **Pipelines > CRM Campaign Pipelines**.
#. Navigate to **Read CRM Campaigns Pipeline > Read CRM Campaigns**.
#. In the field **Filter expression**, select the expression you created.
#. Save the item.

This setting will take affect the next time the synchronization process runs.

.. note::
  This setting will affect the CRM campaigns are read in the future.
  CRM campaigns that have already been synchronized will not be
  removed from Sitecore.
