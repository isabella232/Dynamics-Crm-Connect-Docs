Handling Large Numbers of Marketing Lists
============================================

By default, all CRM marketing lists for a *tenant* are stored as children
under a single item.

If you have more than 100 marketing lists in CRM that you are bringing into
Sitecore, it is recommended you set this item to be *bucketable*. This will
ensure Sitecore's item bucket feature is used, which will improve performance
and user experience within Sitecore.

#. In Content Editor, navigate to your tenant.
#. Navigate to **Tenant Settings > Dynamics CRM > Marketing Lists**.
#. In the Ribbon, under the tab **Configure**, click the button **Bucket**.

  .. image:: _static/bucket-button.png

4. Any child items already created will be moved into the item bucket
   structure. Any new items created (as a result of future synchronization)
   will be created in the item bucket structure.
