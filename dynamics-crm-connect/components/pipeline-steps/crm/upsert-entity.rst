.. _crm-pipeline-step-upsert-entity:

Upsert CRM Entity
=============================

This *pipeline step* is used to upsert an entity in Dynamics CRM. If the entity
already exists in CRM, the entity is updated. If the entity does not exist in
CRM, the entity is inserted.

Template Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Upsert Entity Pipeline Step**                                       |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :ref:`framework-pipeline-step-base`                                   |
+-----------------------------------+-----------------------------------------------------------------------+

.. |endpoint| replace:: :ref:`crm-endpoint-entities`
.. |post-pipelines| replace:: ``Pipelines to run after a new entity is inserted``

+-------------------------------------------------+---------------------------------------------------------+
| Field                                           | Description                                             |
+=================================================+=========================================================+
| ``Endpoint for Dynamics CRM entity repository`` | | The |endpoint| *endpoint* to upsert the entity to.    |
+-------------------------------------------------+---------------------------------------------------------+
| ``Entity name``                                 | | Name of the entity to upsert to CRM.                  |
|                                                 | |                                                       |
|                                                 | | The *entity repository set* assigned to the           | 
|                                                 | | endpoint must be configured to support the            |
|                                                 | | specified entity.                                     | 
+-------------------------------------------------+---------------------------------------------------------+
| ``Entity id attribute name``                    | | Name of the attribute on the entity to use as the     |
|                                                 | | identifier in CRM.                                    |
|                                                 | |                                                       |
|                                                 | | This value is used to build a query to determine      |
|                                                 | | whether or not the entity already exists in CRM.      |
|                                                 | | If the entity already exists, an update command       |
|                                                 | | is used, otherwise an insert command is used.         |
+-------------------------------------------------+---------------------------------------------------------+
| |post-pipelines|                                | | The pipelines to run if the entity is inserted.       |
|                                                 | |                                                       |
|                                                 | | The selected pipelines do not run if the entity       |
|                                                 | | already exists in CRM.                                |
|                                                 | |                                                       |
|                                                 | | The inserted entity is passed to the selected         |
|                                                 | | pipelines as the *source object* on the               |
|                                                 | | *pipeline context*.                                   |
+-------------------------------------------------+---------------------------------------------------------+

Plugin Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Plugin type                       | Description                                                           |
+===================================+=======================================================================+
| ``SynchronizationSettings``       | | For each entity that is inserted, a new pipeline context is         |
|                                   | | created. This pipeline context is passed to each of the pipelines   |
|                                   | | specified in the |post-pipelines|                                   |
|                                   | | field.                                                              |
|                                   | |                                                                     |
|                                   | | The inserted entity is set as the source object on this plugin.     |
|                                   | |                                                                     |
|                                   | | This pipeline step creates this plugin and adds it to the new       |
|                                   | | pipeline context that is passed to the specified pipelines.         |
+-----------------------------------+-----------------------------------------------------------------------+
| ``ParentPipelineContextSettings`` | | Provides access to the current pipeline context to the pipelines    | 
|                                   | | specified in the |post-pipelines|                                   | 
|                                   | | field.                                                              |
|                                   | |                                                                     |
|                                   | | This pipeline step creates this plugin and adds it to the new       |
|                                   | | pipeline context that is passed to the specified pipelines.         |
+-----------------------------------+-----------------------------------------------------------------------+
