Add Value Accessor Set for CRM Entity
=======================================

In order to be able to read attributes from a CRM account entity, 
a *value accessor set* is needed. This item identifies the attributes 
from the CRM account that are available to Dynamics CRM Connect.

1.	Navigate to your tenant.
2.	Navigate to **Data Access > Value Accessor Sets > Providers > Dynamics CRM**.
3.	Add the following item:

    +----------+-------------------------------------+
    | Template | **Entity Value Accessor Set**       |
    +----------+-------------------------------------+
    | Name     | **CRM Account Attributes**          |
    +----------+-------------------------------------+

4.	Navigate to CRM Account Attributes.
5.	Add the following item:

    +----------+-------------------------------------+
    | Template | **Entity Attribute Value Accessor** |
    +----------+-------------------------------------+
    | Name     | **Account Id**                      |
    +----------+-------------------------------------+

6.	Set the following field value:

    +----------+-------------------------------------+
    | Field    | **Attribute name**                  |
    +----------+-------------------------------------+
    | Value    | **accountid**                       |
    +----------+-------------------------------------+

7.	Save the item.
8.	Navigate to **CRM Account Attributes**.
9.	Add the following item:

    +----------+-------------------------------------+
    | Template | **Entity Attribute Value Accessor** |
    +----------+-------------------------------------+
    | Name     | **Account Name**                    |
    +----------+-------------------------------------+

10.	Set the following field value:

    +----------+-------------------------------------+
    | Field    | **Attribute name**                  |
    +----------+-------------------------------------+
    | Value    | **name**                            |
    +----------+-------------------------------------+

11.	Save the item.
