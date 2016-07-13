.. _framework-pipeline-step-base-resolve-object-from-queue:

Base Resolve Object from Queue
==========================================

This template is the base template for any *pipeline step* that 
uses an *endpoint* to search for an existing object that matches 
an identifier value.

.. include:: ../../../../common/base-template-always-inherit-notice.txt

+--------------------------------+--------------------------------------------------------------------------+
| Template name                  | **Base Resolve Object from Queue Pipeline Step**                         |
+--------------------------------+--------------------------------------------------------------------------+
| Base template                  | :ref:`framework-pipeline-step-base-resolve-object`                       | 
+--------------------------------+--------------------------------------------------------------------------+

+--------------------------------+--------------------------------------------------------------------------+
| Field                          | Description                                                              |
+================================+==========================================================================+
| ``Endpoint from``              | The *work queue* endpoint used to search for the identifier value.       |
+--------------------------------+--------------------------------------------------------------------------+
