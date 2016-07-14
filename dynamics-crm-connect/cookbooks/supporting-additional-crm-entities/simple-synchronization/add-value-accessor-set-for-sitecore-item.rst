Add Value Accessor Set for Sitecore Item
=========================================

In order to be able to write values to the field on a Sitecore account 
item, a *value accessor set* is needed. This item identifies the fields 
from the Sitecore account that are available to Dynamics CRM Connect.

1.	Navigate to your tenant.
2.	Navigate to **Data Access > Value Accessor Sets > Providers > Sitecore**.
3.	Add the following item:

    +----------+--------------------------------------------+
    | Template | **Sitecore Item Field Value Accessor Set** |
    +----------+--------------------------------------------+
    | Name     | **Sitecore Account Item Fields**           |
    +----------+--------------------------------------------+

4.	Navigate to **Sitecore Account Item Fields**.
5.	Add the following item:

    +----------+----------------------------------------+
    | Template | **Sitecore Item Field Value Accessor** |
    +----------+----------------------------------------+
    | Name     | **Account Id**                         |
    +----------+----------------------------------------+

6.	Set the following field value:

    +----------+---------------------------------------------------------------------------------------------------------+
    | Field    | **Field**                                                                                               |
    +----------+---------------------------------------------------------------------------------------------------------+
    | Value    | **Templates > Data Exchange > Providers > Sitecore > Entities > External Account > Data > AccountId**   |
    +----------+---------------------------------------------------------------------------------------------------------+

7.	Save the item.
8.	Navigate to **Sitecore Account Item Fields**.
9.	Add the following item:

    +----------+----------------------------------------+
    | Template | **Sitecore Item Field Value Accessor** |
    +----------+----------------------------------------+
    | Name     | **Account Name**                       |
    +----------+----------------------------------------+

10.	Set the following field value:

    +----------+---------------------------------------------------------------------------------------------------------+
    | Field    | **Field**                                                                                               |
    +----------+---------------------------------------------------------------------------------------------------------+
    | Value    | **Templates > Data Exchange > Providers > Sitecore > Entities > External Account > Data > AccountName** |
    +----------+---------------------------------------------------------------------------------------------------------+

11.	Save the item.


