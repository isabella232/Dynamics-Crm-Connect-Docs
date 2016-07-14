Base Process Queue from Endpoint
=================================================

.. |endpoint| replace:: :doc:`/components/endpoints/framework/queue`

This template is the base template for all *pipeline steps* that are used to 
interact with a |endpoint| *endpoint*.

.. include:: ../../../../common/base-template-always-inherit-notice.txt

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Base Process Queue from Endpoint Pipeline Step**                    |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`base-process-queue`                                             |
+-----------------------------------+-----------------------------------------------------------------------+

+-----------------------------------+-----------------------------------------------------------------------+
| Field                             | Description                                                           |
+===================================+=======================================================================+
| ``Queue endpoint``                | The |endpoint| endpoint to add entries to.                            |
+-----------------------------------+-----------------------------------------------------------------------+
