Map Contact Facet To Contact
===================================================

1. In Sitecore, open Content Editor.
2. Navigate to **sitecore > system > Data Exchange**

.. image:: _static/root-for-def.png

3. Select your tenant.

.. image:: _static/tenant.png

4. Navigate to **Data Access > Value Accessor Sets > Providers > xConnect > xConnect Contact**

.. image:: _static/value-accessor-set-for-xconnect-contact.png

5. Add the following item:

+---------------------------+---------------------------------------------------------------------+
| Template                  | **xConnect Entity Facet Value Accessor**                            |
+---------------------------+---------------------------------------------------------------------+
| Item name                 | **Dynamics Account Information Facet on xConnect Contact**          |
+---------------------------+---------------------------------------------------------------------+

6. Select the new item.

.. image:: _static/value-accessor-for-dynamics-account-information-facet-on-xconnect-contact.png

7. Set the following field values:

.. |field-value-for-facet-definition| replace:: **Collection Models > Custom Models > Custom Collection Model for Dynamics > Facets > Contact > DynamicsAccount**
.. |field-value-for-mapping-set| replace:: **Value Mapping Sets > Dynamics to xConnect Contact Mappings > Dynamics Contact to xConnect Contact Dynamics Account Information Facet**

+---------------------------+---------------------------------------------------------------------+
| Field                     | Value                                                               |
+===========================+=====================================================================+
| Facet Definition          | |field-value-for-facet-definition|                                  |
+---------------------------+---------------------------------------------------------------------+
| Mapping Set               | |field-value-for-mapping-set|                                       |
+---------------------------+---------------------------------------------------------------------+

8. Save the item.
9. Select your tenant.
10. Navigate to **Value Mapping Sets > Dynamics to xConnect Contact Mappings > Dynamics Contact to Contact Model**

.. image:: _static/mapping-set-for-contact.png

11. Add the following item:

+---------------------------+---------------------------------------------------------------------+
| Template                  | **Value Mapping**                                                   |
+---------------------------+---------------------------------------------------------------------+
| Item name                 | **Dynamics Account Information Facet**                              |
+---------------------------+---------------------------------------------------------------------+

12. Select the new item.

.. image:: _static/mapping-for-salesforce-account-information-facet.png

13. Set the following field values:

.. |source-accessor-for-custom-facet-mapping| replace:: **Data Access > Value Accessors > Common > Value Accessor with Raw Value Reader Set**
.. |target-accessor-for-custom-facet-mapping| replace:: **Data Access > Value Accessor Sets > Providers > xConnect > xConnect Contact > Dynamics Account Information Facet on xConnect Contact**

+---------------------------+---------------------------------------------------------------------+
| Field                     | Value                                                               |
+===========================+=====================================================================+
| Source Accessor           | |source-accessor-for-custom-facet-mapping|                          |
+---------------------------+---------------------------------------------------------------------+
| Target Accessor           | |target-accessor-for-custom-facet-mapping|                          |
+---------------------------+---------------------------------------------------------------------+

14. Save the item.