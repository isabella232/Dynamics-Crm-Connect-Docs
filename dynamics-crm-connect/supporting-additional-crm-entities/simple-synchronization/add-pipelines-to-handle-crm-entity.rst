.. add-pipelines-to-handle-crm-entity:

Add Pipelines to Handle CRM Entity
=====================================

Each account entity read from CRM is represented in Sitecore by an item. 
A *pipeline* is used to define the logic involved in creating the Sitecore item.

.. note:: 
    You have not yet configured the pipeline that will read the entities from CRM. 
    The pipeline that handles each entity is used in the pipeline that reads the 
    entities, so the pipeline that handles each entity is configured first.

1.	Navigate to your tenant.
2.	Navigate to **Pipelines**.
3.	Add the following item:

    +----------+---------------------------------------------------+
    | Template | **Pipelines Folder**                              |
    +----------+---------------------------------------------------+
    | Name     | **CRM Account Pipelines**                         |
    +----------+---------------------------------------------------+

4.	Navigate to **CRM Account Pipelines**.
5.	Add the following item:

    +----------+---------------------------------------------------+
    | Template | **Pipelines**                                     |
    +----------+---------------------------------------------------+
    | Name     | **CRM Account to Sitecore Account Sync Pipeline** |
    +----------+---------------------------------------------------+

6.	Navigate to **CRM Account to Sitecore Account Sync Pipeline**.
7.	Add the following item:

    +----------+---------------------------------------------------+
    | Template | **Resolve Sitecore Item Pipeline Step**           |
    +----------+---------------------------------------------------+
    | Name     | **Resolve Sitecore Item**                         |
    +----------+---------------------------------------------------+

8.	Set the following field value:

    +----------+------------------------------------------------------------------------------------------------------------+
    | Field    | **Template for new item**                                                                                  |
    +----------+------------------------------------------------------------------------------------------------------------+
    | Value    | **Templates > Data Exchange > Providers > Sitecore > Entities > External Account**                         |
    +----------+------------------------------------------------------------------------------------------------------------+

9.	Set the following field value:

    +----------+------------------------------------------------------------------------------------------------------------+
    | Field    | **Value accessor for name for new item**                                                                   |
    +----------+------------------------------------------------------------------------------------------------------------+
    | Value    | **Templates > Data Exchange > Providers > Dynamics CRM > CRM Account Attributes > Account**                |
    +----------+------------------------------------------------------------------------------------------------------------+

10.	Set the following field value:

    +----------+------------------------------------------------------------------------------------------------------------+
    | Field    | **Endpoint to read data from**                                                                             |
    +----------+------------------------------------------------------------------------------------------------------------+
    | Value    | **Sitecore > Sitecore Item Model Repository Endpoint**                                                     |
    +----------+------------------------------------------------------------------------------------------------------------+

11.	Set the following field value:

    +----------+------------------------------------------------------------------------------------------------------------+
    | Field    | **Identifier value accessor**                                                                              |
    +----------+------------------------------------------------------------------------------------------------------------+
    | Value    | **Value Accessor Sets > Providers > Dynamics CRM > CRM Account Attributes > Account Id**                   |
    +----------+------------------------------------------------------------------------------------------------------------+

12.	Set the following field value:

    +----------+------------------------------------------------------------------------------------------------------------+
    | Field    | **Identifier object location**                                                                             |
    +----------+------------------------------------------------------------------------------------------------------------+
    | Value    | **Pipeline Context Source**                                                                                |
    +----------+------------------------------------------------------------------------------------------------------------+

13.	Set the following field value:

    +----------+------------------------------------------------------------------------------------------------------------+
    | Field    | **Resolved object location**                                                                               |
    +----------+------------------------------------------------------------------------------------------------------------+
    | Value    | **Pipeline Context Target**                                                                                |
    +----------+------------------------------------------------------------------------------------------------------------+

14.	Set the following field value:

    +----------+------------------------------------------------------------------------------------------------------------+
    | Field    | **Parent for item to resolve**                                                                             |
    +----------+------------------------------------------------------------------------------------------------------------+
    | Value    | **sitecore > system > Data Exchange > mycrm > Tenant Settings > Dynamics CRM > Accounts**                  |
    +----------+------------------------------------------------------------------------------------------------------------+

15.	Set the following field value:

    +----------+------------------------------------------------------------------------------------------------------------+
    | Field    | **Value accessor for Sitecore item field used to match the identifier value**                              |
    +----------+------------------------------------------------------------------------------------------------------------+
    | Value    | **Data Access > Value Accessor Sets > Providers > Sitecore > Sitecore Account Item Fields > Account Id**   |
    +----------+------------------------------------------------------------------------------------------------------------+

16.	Save the item.
#.	Navigate to your tenant.
#.  Navigate to **Pipelines > CRM Account Pipelines > CRM Account to Sitecore Account Sync Pipeline**.
#.	Add the following item:

    +----------+---------------------------------------------------+
    | Template | **Apply Mapping Pipeline Step**                   |
    +----------+---------------------------------------------------+
    | Name     | **Apply Mapping**                                 |
    +----------+---------------------------------------------------+

20.	Set the following field value:

    +----------+------------------------------------------------------------------------------------------------------------+
    | Field    | **Mapping set**                                                                                            |
    +----------+------------------------------------------------------------------------------------------------------------+
    | Value    | **Value Mapping Sets > CRM Account to Sitecore Item**                                                      |
    +----------+------------------------------------------------------------------------------------------------------------+

21.	Save the item.
22.	Navigate to **CRM Account to Sitecore Account Sync Pipeline**.
23.	Add the following item:

    +----------+---------------------------------------------------+
    | Template | **Update Sitecore Item Pipeline Step**            |
    +----------+---------------------------------------------------+
    | Name     | **Update Sitecore Item**                          |
    +----------+---------------------------------------------------+

24.	Set the following field value:

    +----------+------------------------------------------------------------------------------------------------------------+
    | Field    | **Endpoint for Sitecore item model repository**                                                            |
    +----------+------------------------------------------------------------------------------------------------------------+
    | Value    | **Sitecore > Sitecore Item Model Repository Endpoint**                                                     |
    +----------+------------------------------------------------------------------------------------------------------------+

25.	Save the item.
26.	Navigate to **CRM Account to Sitecore Account Sync Pipeline**.
27.	Change the order of the child items to the following:

    a)	**Resolve Sitecore Item**
    b)	**Apply Mapping**
    c)	**Update Sitecore Item**
