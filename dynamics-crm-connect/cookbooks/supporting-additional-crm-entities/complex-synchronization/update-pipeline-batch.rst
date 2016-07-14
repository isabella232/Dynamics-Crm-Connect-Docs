Update Pipeline Batch
============================================

Now that entries are being added to the work queue, the *pipeline batch* 
must be updated to processes the queue.

1.	Navigate to your tenant.
2.	Navigate to **Pipeline Batches > CRM Accounts to xDB Sync Pipeline Batch**.
3.	In the field **Pipelines**, add the following pipeline:

    **Pipelines > Process Contacts in Queue Pipeline**

4.	Set the order for the items in the field to the following:
    
    * Read CRM Accounts Pipeline
    * Process Contacts in Queue Pipeline

5.	Save the item.
