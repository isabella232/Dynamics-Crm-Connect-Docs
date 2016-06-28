Read Inactive CRM Campaigns
=============================

By default, only active campaigns are read from Dynamics CRM. In order to
include inactive campaigns, you must do the following:

#. In Content Editor, navigate to your *tenant*.
#. Navigate to **Pipelines > CRM Campaign Pipelines**.
#. Navigate to **Read CRM Campaigns Pipeline > Read CRM Campaigns**.
#. In the field **Exclude active filter**, tick the box.
#. Save the item.

This setting will take affect the next time the synchronization process runs.

.. caution::
  If you run the synchronization process with this option enabled, Sitecore
  campaigns will be created for inactive CRM campaigns. There is no
  **disabled** property on Sitecore campaigns, so you will not be able to
  distinguish CRM campaigns that are active from CRM campaigns that are
  inactive.

.. note::
  This setting will affect the CRM campaigns are read in the future.
  CRM campaigns that have already been synchronized will not be
  removed from Sitecore.
