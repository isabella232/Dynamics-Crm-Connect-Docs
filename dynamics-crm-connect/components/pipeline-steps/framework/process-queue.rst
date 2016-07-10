.. _framework-pipeline-step-process-queue:

Process Queue
=============================

This *pipeline step* is used to process the items in a *work queue* 
using a *queue processor*.

+-----------------+-----------------------------------------------------------+
| Template name   | **Process Queue Pipeline Step**                           |
+-----------------+-----------------------------------------------------------+
| Base template   | :ref:`framework-pipeline-step-base`                       |
+-----------------+-----------------------------------------------------------+

+-----------------------------------------------+-----------------------------------------------------------+
| Field                                         | Description                                               |
+===============================================+===========================================================+
| ``Queue processor``                           | | The queue processor to use.                             |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Post-process pipeline batches``             | | The *pipeline batches* to run after all of the queue    |
|                                               | | entries have been processed.                            |
+-----------------------------------------------+-----------------------------------------------------------+
