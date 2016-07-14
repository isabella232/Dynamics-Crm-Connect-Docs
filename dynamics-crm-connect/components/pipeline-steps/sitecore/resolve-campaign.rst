Resolve Campaign
=============================

This *pipeline step* is used to find a marketing campaign in 
Sitecore using the campaign identifier.

Template Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Resolve Marketing Campaign Pipeline Step**                          |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`base-resolve-object`                                            |
+-----------------------------------+-----------------------------------------------------------------------+

.. include:: ../../../../common/no-template-fields-added.txt

Plugin Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Plugin type                       | Description                                                           |
+===================================+=======================================================================+
| ``CampaignRepositorySettings``    | | Subsequent pipeline steps use this plugin to access the repository  |
|                                   | | used to resolve the campaign.                                       |
|                                   | |                                                                     |
|                                   | | This step adds this plugin to the pipeline context.                 |
+-----------------------------------+-----------------------------------------------------------------------+
