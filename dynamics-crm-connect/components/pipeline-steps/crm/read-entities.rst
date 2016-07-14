Read CRM Entities
=============================

This *pipeline step* is used to read entities from Dynamics CRM.

Template Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Read CRM Entities Pipeline Step**                                   |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../framework/pipeline-step`                                     |
+-----------------------------------+-----------------------------------------------------------------------+

.. |ep| replace:: :doc:`/components/endpoints/crm/crm-entities`
.. |attributes-to-read| replace:: :doc:`/components/data-access/value-accessor-sets/crm/entity-attributes`
.. |filters| replace:: :doc:`/components/crm-filter-expressions/index`

+-------------------------------------------------+---------------------------------------------------------+
| Field                                           | Description                                             |
+=================================================+=========================================================+
| ``Endpoint for Dynamics CRM entity repository`` | | The |ep| *endpoint* from which entities are read.     |   
+-------------------------------------------------+---------------------------------------------------------+
| ``Entity name``                                 | | Name of the entity to read from CRM.                  |
|                                                 | |                                                       |
|                                                 | | The *entity repository set* assigned to the endpoint  | 
|                                                 | | must be configured to support the specified entity.   |
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
| ``Page size``                                   | | The maximum number of entities that will be read      |
|                                                 | | from CRM at a time.                                   |
|                                                 | |                                                       |
|                                                 | | If the number of entities that can be read is larger  |
|                                                 | | than the page size, multiple calls to CRM are made.   |
+-------------------------------------------------+---------------------------------------------------------+
| ``Maximum number of entities to read``          | | The maximum number of entities that will be read      |
|                                                 | | from CRM.                                             |
+-------------------------------------------------+---------------------------------------------------------+
| ``Exclude active filter``                       | | By default, a filter is added to the CRM query that   |
|                                                 | | ensures only active entities are returned.            |
|                                                 | |                                                       |
|                                                 | | Ticking this option disables that filter, meaning     |
|                                                 | | that inactive entities may be read.                   |
+-------------------------------------------------+---------------------------------------------------------+
| ``Filter expression``                           | | The *filter expression* that controls which entities  | 
|                                                 | | are read from CRM.                                    | 
|                                                 | |                                                       | 
|                                                 | | See |filters| for more information.                   |
+-------------------------------------------------+---------------------------------------------------------+

Plugin Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Plugin type                       | Description                                                           |
+===================================+=======================================================================+
| ``IterableDataSettings``          | | Subsequent pipeline steps use this plugin to access the entities    |
|                                   | | read from CRM.                                                      |
|                                   | |                                                                     |
|                                   | | This step adds this plugin to the pipeline context.                 |
+-----------------------------------+-----------------------------------------------------------------------+
