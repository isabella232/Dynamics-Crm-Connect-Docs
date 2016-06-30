Disable Item Buckets for Campaigns
===================================

Dynamics CRM campaign are exposed as Sitecore campaigns that are created
under a campaign category item whose name matches the *tenant* used to
define the synchronization process.

Since it is possible that a large number of CRM campaigns are synchronized,
Dynamics CRM Connect makes this campaign category item bucketable. This
results in the individual campaign items being added to an item bucket.

.. note::
  By default, Sitecore campaigns are not bucketable. Dynamics CRM Connect
  extends Sitecore so that campaign items can be bucketed.

If you do not want the Campaign items to be added to an item bucket, you
must do the following:

#. In Content Editor, navigate to your tenant.
#. Navigate to **Pipelines > CRM Campaign Pipelines**.
#. Navigate to **CRM Campaign to Sitecore Campaign Pipeline**.
#. Navigate to **Resolve Campaign Category**.
#. In the field **Make campaign category item bucketable**, untick the box.
#. Save the item.
#. Navigate to **sitecore > system > Marketing Control Panel > Campaigns**.
#. If a campaign category item exists for your tenant, delete that item.
#. If prompted with a warning about **breaking links**, select the option to **leave links**.

  .. note::
    It is important to select the option to **leave links**.
    When you re-run the campaign synchronization process, the campaign items
    are created with the same Sitecore item ID as the campaign items you
    deleted in the previous step. Leaving links ensures that anywhere those
    campaigns are used will continue to work as expected.

9.	Navigate to your tenant.
#.	Navigate to **Pipelines Tasks > CRM Campaigns Sync Pipeline Batch**.
#.	Run the pipeline batch.

When the pipeline batch finishes, the Sitecore campaigns will be bucketed.
