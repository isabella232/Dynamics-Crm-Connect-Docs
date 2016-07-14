Add Pipelines to Handle CRM Accounts
============================================

For each CRM account you must read the CRM contacts who are associated 
with the CRM account. A *pipeline* is used to define the logic that reads 
the CRM contacts that are associated with the CRM account and iterates 
those CRM contacts.

.. note:: 

    You have not yet configured the pipeline that will read the entities 
    from CRM. The pipeline that handles each entity is used in the 
    pipeline that reads the entities, so the pipeline that handles 
    each entity is configured first.

1.	Navigate to your tenant.
2.	Navigate to **Pipelines > CRM Account Pipelines**.
3.	Add the following item:

    +-------------+-----------------------------------------------------------+
    | Template    | **Pipeline**                                              |
    +-------------+-----------------------------------------------------------+
    | Name        | **Read Members from Single CRM Account Pipeline**         |
    +-------------+-----------------------------------------------------------+

4.	Navigate to **Read Members from Single CRM Account Pipeline**.
5.	Add the following item:

    +-------------+-----------------------------------------------------------+
    | Template    | **Read CRM Account Membership Pipeline Step**             |
    +-------------+-----------------------------------------------------------+
    | Name        | **Read Members from Single CRM Account**                  |
    +-------------+-----------------------------------------------------------+

6.	Set the following field value:

    +-------------+-----------------------------------------------------------+
    | Field       | **Endpoint for Dynamics CRM entity repository**           |
    +-------------+-----------------------------------------------------------+
    | Value       | **Dynamics CRM > Dynamics CRM Entity Endpoint**           |
    +-------------+-----------------------------------------------------------+

7.	Set the following field value:

    +-------------+-----------------------------------------------------------+
    | Field       | **Entity name**                                           |
    +-------------+-----------------------------------------------------------+
    | Value       | **accountmembership**                                     |
    +-------------+-----------------------------------------------------------+

8.	Set the following field value:

    +-------------+---------------------------------------------------------------------+
    | Field       | **Attributes to read**                                              |
    +-------------+---------------------------------------------------------------------+
    | Value       | **Common CRM Entity Attributes, CRM Contact Attributes Minimal**    |
    +-------------+---------------------------------------------------------------------+

9.	Save the item.
10.	Navigate to **Read Members from Single CRM Account Pipeline**.
11.	Add the following item:

    +-------------+-----------------------------------------------------------+
    | Template    | **Iterate Data and Run Pipelines Pipeline Step**          |
    +-------------+-----------------------------------------------------------+
    | Name        | **Iterate CRM Members and Run Pipelines**                 |
    +-------------+-----------------------------------------------------------+

12.	Set the following field value:

    +-------------+-----------------------------------------------------------+
    | Field       | **Pipelines**                                             |
    +-------------+-----------------------------------------------------------+
    | Value       | **CRM Account Membership to xDB Contact Sync Pipeline**   |
    +-------------+-----------------------------------------------------------+

13.	Save the item.
14.	Navigate to **Read Members from Single CRM Account Pipeline**.
15.	Change the order of the child items to the following:

    * Read Members from Single CRM Account
    * Iterate CRM Members and Run Pipelines
