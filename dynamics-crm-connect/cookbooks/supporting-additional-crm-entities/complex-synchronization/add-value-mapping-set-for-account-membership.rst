Add Value Mapping Set for Account Membership
==============================================

In order to map values from the source object (CRM account membership 
entity) to a target object (Sitecore contact), you must define a 
*value mapping set*.

1.	Navigate to your tenant.
2.	Navigate to **Value Mapping Sets**.
3.	Add the following item:

  +----------------+----------------------------------------------------------+
  | Template       | **Value Mapping Set**                                    |
  +----------------+----------------------------------------------------------+
  | Name           | **CRM Account Membership to xDB Contact**                |
  +----------------+----------------------------------------------------------+

4.	Navigate to **CRM Account Membership to xDB Contact**.
5.	Add the following item:

  +----------------+----------------------------------------------------------+
  | Template       | **Value Mapping**                                        |
  +----------------+----------------------------------------------------------+
  | Name           | **Account Id**                                           |
  +----------------+----------------------------------------------------------+

6.	Set the following field value:

  +----------------+----------------------------------------------------------------------------------------------------------------------------+
  | Field          | **Value accessor for source object**                                                                                       |
  +----------------+----------------------------------------------------------------------------------------------------------------------------+
  | Value          | **Data Access > Value Accessor Sets > Providers > Dynamics CRM > CRM Account Membership Attributes > Account Id**          |
  +----------------+----------------------------------------------------------------------------------------------------------------------------+

7.	Set the following field value:

  +----------------+----------------------------------------------------------------------------------------------------------------------------+
  | Field          | **Value accessor for target object**                                                                                       |
  +----------------+----------------------------------------------------------------------------------------------------------------------------+
  | Value          | **Data Access > Value Accessor Sets > Providers > Sitecore > xDB Contact Properties for Account Membership > Account Id**  |
  +----------------+----------------------------------------------------------------------------------------------------------------------------+

8.	Set the following field value:

  +----------------+----------------------------------------------------------+
  | Field          | **Transformer for source value**                         |
  +----------------+----------------------------------------------------------+
  | Value          | **Value Readers > Common > Guid Value Reader**           |
  +----------------+----------------------------------------------------------+

9.	Save the item.
