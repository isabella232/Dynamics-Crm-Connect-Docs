Add Value Mapping Set
===========================

In order to map values from the source object (CRM account entity) to a 
target object (Sitecore account item), you must define a *value mapping set*.

1.	Navigate to your tenant.
2.	Navigate to **Value Mapping Sets**.
3.	Add the following item:

    +----------+--------------------------------------------+
    | Template | **Value Mapping Set**                      |
    +----------+--------------------------------------------+
    | Name     | **CRM Account to Sitecore Item**           |
    +----------+--------------------------------------------+

4.	Navigate to **CRM Account to Sitecore Item**.
5.	Add the following item:

    +----------+--------------------------------------------+
    | Template | **Value Mapping**                          |
    +----------+--------------------------------------------+
    | Name     | **Account Id**                             |
    +----------+--------------------------------------------+

6.	Set the following field value:

    +----------+------------------------------------------------------------------------------------------------------------+
    | Field    | **Value accessor for source object**                                                                       |
    +----------+------------------------------------------------------------------------------------------------------------+
    | Value    | **Data Access > Value Accessor Sets > Providers > Dynamics CRM > CRM Account Attributes > Account Id**     |
    +----------+------------------------------------------------------------------------------------------------------------+

7.	Set the following field value:

    +----------+------------------------------------------------------------------------------------------------------------+
    | Field    | **Value accessor for target object**                                                                       |
    +----------+------------------------------------------------------------------------------------------------------------+
    | Value    | **Data Access > Value Accessor Sets > Providers > Sitecore > Sitecore Account Item Fields > Account Id**   |
    +----------+------------------------------------------------------------------------------------------------------------+

8.	Save the item.
9.	Navigate to **CRM Account to Sitecore Item**.
10.	Add the following item:

    +----------+--------------------------------------------+
    | Template | **Value Mapping**                          |
    +----------+--------------------------------------------+
    | Name     | **Account Name**                           |
    +----------+--------------------------------------------+

11.	Set the following field value:

    +----------+------------------------------------------------------------------------------------------------------------+
    | Field    | **Value accessor for source object**                                                                       |
    +----------+------------------------------------------------------------------------------------------------------------+
    | Value    | **Data Access > Value Accessor Sets > Providers > Dynamics CRM > CRM Account Attributes > Account Name**   |
    +----------+------------------------------------------------------------------------------------------------------------+

12.	Set the following field value:

    +----------+------------------------------------------------------------------------------------------------------------+
    | Field    | **Value accessor for target object**                                                                       |
    +----------+------------------------------------------------------------------------------------------------------------+
    | Value    | **Data Access > Value Accessor Sets > Providers > Sitecore > Sitecore Account Item Fields > Account Name** |
    +----------+------------------------------------------------------------------------------------------------------------+

13.	Save the item.

