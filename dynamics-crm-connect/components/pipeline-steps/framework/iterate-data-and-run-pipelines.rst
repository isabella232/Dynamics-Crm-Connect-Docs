.. _framework-pipeline-step-iterate-data-and-run-pipelines:

Iterate Data and Run Pipelines
==========================================

This *pipeline step* iterates a collection of objects and runs a set of 
*pipelines*, using the data object as the *source object*.

Template Information
-----------------------------

+-----------------+-----------------------------------------------------------+
| Template name   | **Iterate Data and Run Pipelines Pipeline Step**          |
+-----------------+-----------------------------------------------------------+
| Base template   | :ref:`framework-pipeline-step-base`                       |
+-----------------+-----------------------------------------------------------+

+-----------------------------------------------+-----------------------------------------------------------+
| Field                                         | Description                                               |
+===============================================+===========================================================+
| ``Pipelines``                                 | The pipelines to run.                                     |
+-----------------------------------------------+-----------------------------------------------------------+

Plugin Information
-----------------------------

+-----------------------------+-------------------------------------------------------------------+
| Plugin type                 | Description                                                       |
+=============================+===================================================================+
| ``PipelinesSettings``       | | Provides access to the collection of data objects that are      |
|                             | | passed to the pipelines.                                        |
+-----------------------------+-------------------------------------------------------------------+
| ``SynchronizationSettings`` | | Each data object is set as the source object on a new pipeline  |
|                             | | context which is used to run the pipelines.                     |
+-----------------------------+-------------------------------------------------------------------+

