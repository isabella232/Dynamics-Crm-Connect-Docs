Schedule a Pipeline Batch
============================

Dynamics CRM Connect includes commands that can be run using Sitecore's task
scheduling features.

Tasks can be scheduled using Content Editor, under the item
**sitecore > system > Tasks > Schedules**. When you configure
a task you must select a command. The command describes what
should happen when the task runs.

When you install Dynamics CRM Connect, a folder is created at
**sitecore > system > Tasks > Commands > Data Exchange**. This 
is where the commands that control synchronization processes
are stored.

.. tip::
    The items used to configure the commands are created using templates
    provided with :def-root:`Data Exchange Framework documentation<index.html>`.
    You installed Data Exchange Framework when you installed Dynamics CRM Connect.

    The :def-framework-component:`available templates<sitecore-task-commands/index.html#framework-sitecore-task-commands-templates>`
    are described in the :def-root:`Data Exchange Framework documentation<index.html>`.
