Resolve CRM Entity
=============================

This *pipeline step* is used to find an entity in Dynamics CRM by matching 
an attribute value.

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Resolve CRM Entity Pipeline Step**                                  |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../framework/base-resolve-object`                               |
+-----------------------------------+-----------------------------------------------------------------------+

.. |endpoint| replace:: :doc:`/components/endpoints/crm/crm-entities`
.. |attributes-to-read| replace:: :doc:`/components/data-access/value-accessor-sets/crm/entity-attributes`

+-------------------------------------------------+---------------------------------------------------------+
| Field                                           | Description                                             |
+=================================================+=========================================================+
| ``Endpoint for Dynamics CRM entity repository`` | | The |endpoint| *endpoint* to read an entity from.     |
+-------------------------------------------------+---------------------------------------------------------+
| ``Entity name``                                 | | Name of the entity to read from CRM.                  |
|                                                 | |                                                       |
|                                                 | | The *entity repository set* assigned to the endpoint  | 
|                                                 | | must be configured to support the specified entity.   |
+-------------------------------------------------+---------------------------------------------------------+
| ``Entity attribute for lookup``                 | | A query is built that looks for an entity with an     |
|                                                 | | attribute whose value matches the identifier value.   |
|                                                 | | This field specifies which attribute on the entity    |
|                                                 | | is used in the query.                                 |
|                                                 | |                                                       |
|                                                 | | The selected attribute must be defined on the entity. |
|                                                 | | If an attribute is selected that is not defined on    |
|                                                 | | the entity, an exception is thrown when the pipeline  |
|                                                 | | step runs.                                            |
+-------------------------------------------------+---------------------------------------------------------+
| ``Attributes to read``                          | | The attributes from the entities that are read from   |
|                                                 | | CRM.                                                  |
|                                                 | |                                                       |
|                                                 | | Attributes are specified by selecting one or more     |
|                                                 | | |attributes-to-read| *value accessor set* items.      |
|                                                 | |                                                       |
|                                                 | | The selected attributes must be defined on the        |
|                                                 | | entity. If an attribute is selected that is not       |
|                                                 | | defined on the entity, an exception is thrown when    |
|                                                 | | the pipeline step runs.                               |
+-------------------------------------------------+---------------------------------------------------------+
