Phone Numbers Facet
===================================================
This section describes how phone number information is
mapped from a contact in Dynamics to a contact in Sitecore.

.. contents:: In this topic:
   :local:

Format in Dynamics
-------------------------------------------------
In Dynamics, phone numbers are associated with a 
contact through attributes on the contact. 

Format in Sitecore
-------------------------------------------------
In Sitecore, phone numbers are associated with a 
contact through a contact facet:

.. |phone-numbers-facet-type| replace:: ``Sitecore.XConnect.Collection.Model.PhoneNumberList``

+---------------------------+-------------------------------------------------+
| Facet Name                | ``PhoneNumbers``                                |
+---------------------------+-------------------------------------------------+
| Facet Type                | |phone-numbers-facet-type|                      |
+---------------------------+-------------------------------------------------+

Mapping Values
-------------------------------------------------
The contact facet provides the ability to store multiple 
phone numbers. The standard mappings only handle a single
phone number, which is set as the preferred phone number
on the contact facet.

.. |phone-numbers-source-objects| raw:: html

    Contact entity from Dynamics,
    Tenant from Sitecore

.. |phone-numbers-mapping-location| replace:: **Dynamics to xConnect Contact Mappings > Dynamics Contact to xConnect Contact Phone Numbers Facet**

+---------------------------+-------------------------------------------------+
| Source objects            | |phone-numbers-source-objects|                  |
+---------------------------+-------------------------------------------------+
| Target object             | |phone-numbers-facet-type|                      |
+---------------------------+-------------------------------------------------+
| Mapping definition        | |phone-numbers-mapping-location|                |
+---------------------------+-------------------------------------------------+

.. image:: _static/phone-numbers.png
    :align: center