Add Pipelines to Handle Single CRM Account
============================================

Each account membership entity read from CRM is mapped to a Sitecore 
contact. A Pipeline is used to define the logic that resolves the 
Sitecore contact and applies data from the CRM entity.

1.	Navigate to your tenant.
2.	Navigate to **Pipelines > CRM Account Pipelines**.
3.	Add the following item:

    +-------------+-----------------------------------------------------------+
    | Template    | **Pipeline**                                              |
    +-------------+-----------------------------------------------------------+
    | Name        | **CRM Account Membership to xDB Contact Sync Pipeline**   |
    +-------------+-----------------------------------------------------------+

4.	Navigate to **CRM Account Membership to xDB Contact Sync Pipeline**.
5.	Add the following item:

    +-------------+-----------------------------------------------------------+
    | Template    | **Resolve xDB Contact from Repository Pipeline Step**     |
    +-------------+-----------------------------------------------------------+
    | Name        | **Resolve xDB Contact from Repository**                   |
    +-------------+-----------------------------------------------------------+

6.	Set the following field value:

    +-------------+-----------------------------------------------------------+
    | Field       | **Endpoint From**                                         |
    +-------------+-----------------------------------------------------------+
    | Value       | **Sitecore > Local xDB Contacts Endpoint**                |
    +-------------+-----------------------------------------------------------+

7.	Set the following field value:

    +-------------+------------------------------------------------------------------------------------------+
    | Field       | **Identifier Value Accessor**                                                            |
    +-------------+------------------------------------------------------------------------------------------+
    | Value       | **Value Accessor Sets > Providers > Dynamics CRM > CRM Contact Attributes > Email**      |
    +-------------+------------------------------------------------------------------------------------------+

8.	Set the following field value:

    +-------------+-----------------------------------------------------------+
    | Field       | **Identifier Object Location**                            |
    +-------------+-----------------------------------------------------------+
    | Value       | **Pipeline Context Source**                               |
    +-------------+-----------------------------------------------------------+

9.	Set the following field value:

    +-------------+-----------------------------------------------------------+
    | Field       | **Resolved Object Location**                              |
    +-------------+-----------------------------------------------------------+
    | Value       | **Pipeline Context Target**                               |
    +-------------+-----------------------------------------------------------+

10.	Save the item.
11.	Navigate to **CRM Account Membership to xDB Contact Sync Pipeline**.
12.	Add the following item:

    +-------------+-----------------------------------------------------------+
    | Template    | **Resolve xDB Contact from Queue Pipeline Step**          |
    +-------------+-----------------------------------------------------------+
    | Name        | **Resolve xDB Contact from Queue**                        |
    +-------------+-----------------------------------------------------------+

13.	Set the following field value:

    +-------------+-----------------------------------------------------------+
    | Field       | **Endpoint From**                                         |
    +-------------+-----------------------------------------------------------+
    | Value       | **Endpoints > Common > Queue Endpoint**                   |
    +-------------+-----------------------------------------------------------+

14.	Set the following field value:

    +-------------+----------------------------------------------------------------------------------------------------+
    | Field       | **Identifier Value Accessor**                                                                      |
    +-------------+----------------------------------------------------------------------------------------------------+
    | Value       | **Value Accessor Sets > Providers > Sitecore > xDB Contact Properties > xDB Contact Identifier**   |
    +-------------+----------------------------------------------------------------------------------------------------+

15.	Set the following field value:

    +-------------+-----------------------------------------------------------+
    | Field       | **Identifier Object Location**                            |
    +-------------+-----------------------------------------------------------+
    | Value       | **Pipeline Context Target**                               |
    +-------------+-----------------------------------------------------------+

16.	Set the following field value:

    +-------------+-----------------------------------------------------------+
    | Field       | **Resolved Object Location**                              |
    +-------------+-----------------------------------------------------------+
    | Value       | **Pipeline Context Target**                               |
    +-------------+-----------------------------------------------------------+

17.	Save the item.
18.	Navigate to **CRM Account Membership to xDB Contact Sync Pipeline**.
19.	Add the following item:

    +-------------+-----------------------------------------------------------+
    | Template    | **Apply Mapping Pipeline Step**                           |
    +-------------+-----------------------------------------------------------+
    | Name        | **Apply Mapping**                                         |
    +-------------+-----------------------------------------------------------+

20.	Set the following field value:

    +-------------+----------------------------------------------------------------------+
    | Field       | **Mapping Set**                                                      |
    +-------------+----------------------------------------------------------------------+
    | Value       | **Value Mapping Sets > CRM Account Membership to xDB Contact**       |
    +-------------+----------------------------------------------------------------------+

21.	Save the item.
22.	Navigate to **CRM Account Membership to xDB Contact Sync Pipeline**.
23.	Change the order of the child items to the following:

    * Resolve xDB Contact from Repository
    * Resolve xDB Contact from Queue
    * Apply Mapping
