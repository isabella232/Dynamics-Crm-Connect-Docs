Add Value Accessor Set for Sitecore Contact
============================================

In order to be able to write values to the Sitecore contact, a 
*value accessor set* is needed. This item identifies the fields 
from the Sitecore contact that are available to Dynamics CRM Connect.

1.	Navigate to your tenant.
2.	Navigate to **Data Access > Value Accessor Sets > Providers > Sitecore**.
3.	Add the following item:

  +----------------+----------------------------------------------------------+
  | Template       | **xDB Contact Value Accessor Set**                       |
  +----------------+----------------------------------------------------------+
  | Name           | **xDB Contact Properties for Account Membership**        |
  +----------------+----------------------------------------------------------+

4.	Navigate to **xDB Contact Properties for Account Membership**.
5.	Add the following item:

  +----------------+----------------------------------------------------------+
  | Template       | **xDB Contact Facet Property Value Accessor**            |
  +----------------+----------------------------------------------------------+
  | Name           | **Account Id**                                           |
  +----------------+----------------------------------------------------------+

6.	Set the following field value:

  +----------------+----------------------------------------------------------+
  | Field          | **Contact facet name**                                   |
  +----------------+----------------------------------------------------------+
  | Vallue         | **DynamicsCrm**                                          |
  +----------------+----------------------------------------------------------+

7.	Set the following field value:

  +----------------+----------------------------------------------------------+
  | Field          | **Property name**                                        |
  +----------------+----------------------------------------------------------+
  | Vallue         | **AccountId**                                            |
  +----------------+----------------------------------------------------------+

8.	Save the item.
