Schedule a Pipeline Batch
============================

Dynamics CRM Connect includes commands that can be run using Sitecore's task
scheduling features.

Tasks can be scheduled using Content Editor, under the item
**sitecore > system > Tasks > Schedules**.

When you install Dynamics CRM Connect, a folder is created at
**sitecore > system > Tasks > Commands > Data Exchange**. The following 
templates can be used to create commands that can be scheduled as tasks:

+--------------------------+---------------------------------------------------+
| Command template         | Description                                       |
+==========================+===================================================+
| Run All Pipeline         | | Allows you to select a folder that contains     |
| Batches Command          | | pipeline batches. When the command is run,      |
|                          | | each of the pipeline batches in the folder      |
|                          | | are run in the order they appear under the      |
|                          | | folder.                                         |
+--------------------------+---------------------------------------------------+
| Run Selected Pipeline    | | Allows you to select specific                   |
| Batches Command          | | pipeline batches. When the command is run,      |
|                          | | each selected pipeline batch is run in the      |
|                          | | order it was selected.                          |
+--------------------------+---------------------------------------------------+

.. hint:: 

    These templates are described in detail in the :doc:`/components/sitecore-task-commands/index` 
    section.
