Update Pipeline that Reads CRM Accounts
============================================

Currently, the *pipeline* that reads accounts from CRM is only creating 
or updating the Sitecore items that correspond to those accounts. That 
pipeline must be changed so that it reads the account membership from CRM.

1.	Navigate to your tenant.
2.	Navigate to **Pipelines > CRM Account Pipelines > Read CRM Accounts Pipeline > Iterate CRM Accounts and Run Pipelines**.
3.	In the field **Pipelines**, add the following pipeline:

    **Pipelines > CRM Account Pipelines > Read Members from Single CRM Account Pipeline**
     
4.	Set the order for the items in the field to the following:

    * CRM Account to Sitecore Account Sync Pipeline
    * Read Members from Single CRM Account Pipeline

5.	Save the item.
