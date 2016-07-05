.. _add-pipelines-to-read-crm-entities:

Add Pipelines to Read CRM Entities
=====================================

A *pipeline* is needed to read accounts from CRM and to pass each account 
to the pipeline configured in :ref:`add-pipelines-to-handle-crm-entity`. 

1.	Navigate to your tenanr.
2.	Navigate to **Pipelines > CRM Account Pipelines**.
3.	Add the following item:

    +----------+---------------------------------------------------+
    | Template | **Pipeline**                                      |
    +----------+---------------------------------------------------+
    | Name     | **Read CRM Accounts Pipeline**                    |
    +----------+---------------------------------------------------+

4.	Navigate to **Read CRM Accounts Pipeline**.
5.	Add the following item:

    +----------+---------------------------------------------------+
    | Template | **Read CRM Entities Pipeline Step**               |
    +----------+---------------------------------------------------+
    | Name     | **Read CRM Accounts**                             |
    +----------+---------------------------------------------------+

6.	Set the following field value:

    +----------+---------------------------------------------------+
    | Field    | **Endpoint for Dynamics CRM entity repository**   |
    +----------+---------------------------------------------------+
    | Value    | **Dynamics CRM > Dynamics CRM Entity Endpoint**   |
    +----------+---------------------------------------------------+

7.	Set the following field value:

    +----------+---------------------------------------------------+
    | Field    | **Entity name**                                   |
    +----------+---------------------------------------------------+
    | Value    | **account**                                       |
    +----------+---------------------------------------------------+

8.	Set the following field value:

    +----------+----------------------------------------------------------+
    | Field    | **Attributes to read**                                   |
    +----------+----------------------------------------------------------+
    | Value    | **Common CRM Entity Attributes, CRM Account Attributes** |
    +----------+----------------------------------------------------------+

9.	Save the item.
10.	Navigate to **Read CRM Accounts Pipeline**.
11.	Add the following item:

    +----------+---------------------------------------------------+
    | Template | **Iterate Data and Run Pipelines**                |
    +----------+---------------------------------------------------+
    | Name     | **Iterate CRM Accounts and Run Pipelines**        |
    +----------+---------------------------------------------------+

12.	Set the following field value:

    +----------+---------------------------------------------------+
    | Field    | **Pipelines**                                     |
    +----------+---------------------------------------------------+
    | Value    | **CRM Account to Sitecore Account Sync Pipeline** |
    +----------+---------------------------------------------------+

13.	Save the item.
14.	Navigate to **Read CRM Accounts Pipeline**.
15.	Reorder the child items so they are in the following order:

    a)	**Read CRM Accounts**
    b)	**Iterate CRM Accounts and Run Pipelines**
