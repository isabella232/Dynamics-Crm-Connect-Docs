Add Value Accessor Set for CRM Account
======================================

In order to be able to read attributes from a CRM *accountmembership* 
entity, a *value accessor set* is needed. This item identifies the 
attributes from the CRM *accountmembership* that are available to 
Dynamics CRM Connect.

1.	Navigate to your tenant.
2.	Navigate to **Data Access > Value Accessor Sets > Providers > Dynamics CRM**.
3.	Add the following item:

    +-------------+-----------------------------------------------------------+
    | Template    | **Entity Value Accessor Set**                             |
    +-------------+-----------------------------------------------------------+
    | Name        | **CRM Account Membership Attributes**                     |
    +-------------+-----------------------------------------------------------+

4.	Navigate to **CRM Account Membership Attributes**.
5.	Add the following item:

    +-------------+-----------------------------------------------------------+
    | Template    | **Entity Attribute Value Accessor**                       |
    +-------------+-----------------------------------------------------------+
    | Name        | **Account Id**                                            |
    +-------------+-----------------------------------------------------------+

6.	Set the following field value:

    +-------------+-----------------------------------------------------------+
    | Field       | **Use value property**                                    |
    +-------------+-----------------------------------------------------------+
    | Value       | **ticked**                                                |
    +-------------+-----------------------------------------------------------+

7.	Set the following field value:

    +-------------+-----------------------------------------------------------+
    | Field       | **Attribute name**                                        |
    +-------------+-----------------------------------------------------------+
    | Value       | **account.accountid**                                     |
    +-------------+-----------------------------------------------------------+

8.	Save the item.
9.	Navigate to **CRM Account Membership Attributes**.
10.	Add the following item:

    +-------------+-----------------------------------------------------------+
    | Template    | **Entity Attribute Value Accessor**                       |
    +-------------+-----------------------------------------------------------+
    | Name        | **Account Name**                                          |
    +-------------+-----------------------------------------------------------+

11.	Set the following field value:

    +-------------+-----------------------------------------------------------+
    | Field       | **Use value property**                                    |
    +-------------+-----------------------------------------------------------+
    | Value       | **ticked**                                                |
    +-------------+-----------------------------------------------------------+

12.	Set the following field value:

    +-------------+-----------------------------------------------------------+
    | Field       | **Attribute name**                                        |
    +-------------+-----------------------------------------------------------+
    | Value       | **account.accountname**                                   |
    +-------------+-----------------------------------------------------------+

13.	Save the item.
