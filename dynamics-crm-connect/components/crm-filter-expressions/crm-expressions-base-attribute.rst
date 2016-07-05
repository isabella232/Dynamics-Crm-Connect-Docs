.. _crm-expressions-base-attribute:

Base Entity Attribute Value Condition Expression
======================================================

This template is the base template for all CRM expression filters 
that involve an entity attribute.

+-----------------+-----------------------------------------------------------+
| Template name   | **Base Entity Attribute Value Condition Expression**      |
+-----------------+-----------------------------------------------------------+
| Base template   | none                                                      |
+-----------------+-----------------------------------------------------------+

+-----------------------------------------------+-----------------------------------------------------------+
| Field                                         | Description                                               |
+===============================================+===========================================================+
| ``Value accessor for entity attribute``       | | The value accessor that is used to read the value of    |
|                                               | | an attribute from an entity.                            |
|                                               | |                                                         |
|                                               | | It is important that the value accessor selected has    |
|                                               | | a field that identifies the attribute name. The         |
|                                               | | attribute name is used to build the filter for the      |
|                                               | | API call to Dynamics CRM.                               |
+-----------------------------------------------+-----------------------------------------------------------+
