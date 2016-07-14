Add to Full CRM Contacts to xDB Sync Pipeline Batch
======================================================

If you want, you can add the CRM account synchronization process to the 
process that synchronizes CRM contact and marketing list data.

1.	Navigate to your tenant.
2.	Navigate to **Pipeline Batches > Full CRM Contacts to xDB Sync Pipeline Batch**.
3.	In the field **Pipelines**, add the following pipeline:

    **Pipelines > CRM Account Pipelines > Read CRM Accounts Pipeline**

4.	Set the order for the items in the field to the following:
    
    * Reset Existing xDB Contacts Pipeline
    * Read CRM Lists Pipeline
    * Read CRM Contacts Pipeline
    * Read CRM Accounts Pipeline
    * Process Contacts in Queue Pipeline

5.	Save the item.

If you run the pipeline batch you should see the CRM account ID included in the Sitecore contact.

