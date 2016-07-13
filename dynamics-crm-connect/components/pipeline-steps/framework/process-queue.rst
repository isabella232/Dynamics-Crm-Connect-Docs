.. _framework-pipeline-step-process-queue:

Process Queue
=============================

This *pipeline step* is used to process the items in a *work queue* 
using a *queue processor*, which can run additional *pipeline batches*
after the queue entries have been processed.

Template Information
-----------------------------

+--------------------------------+--------------------------------------------------------------------------+
| Template name                  | **Process Queue Pipeline Step**                                          |
+--------------------------------+--------------------------------------------------------------------------+
| Base template                  | :ref:`framework-pipeline-step-base`                                      |
+--------------------------------+--------------------------------------------------------------------------+

+-----------------------------------------------+-----------------------------------------------------------+
| Field                                         | Description                                               |
+===============================================+===========================================================+
| ``Queue processor``                           | | The queue processor to use.                             |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Post-process pipeline batches``             | | The pipeline batches to run after all of the queue      |
|                                               | | entries have been processed.                            |
+-----------------------------------------------+-----------------------------------------------------------+

Plugin Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| ``ParentPipelineContextSettings`` | | Provides access to the current pipeline context to the pipeline     | 
|                                   | | batches specified in the ``Post-process pipeline batches`` field.   | 
|                                   | |                                                                     |
|                                   | | This pipeline step creates this plugin and adds it to the new       |
|                                   | | pipeline context that is passed to the specified pipeline batches.  |
+-----------------------------------+-----------------------------------------------------------------------+
