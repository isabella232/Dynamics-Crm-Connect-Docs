Email Event
===================================================
This section describes how email activities from Dynamics 
are mapped to events in Sitecore.

.. contents:: In this topic:
   :local:

Format in Dynamics
-------------------------------------------------
In Dynamics, a contact can be associated with multiple
email activities. Each activity is a separate entity
that is linked to the contact.

.. note::

    Only completed activities are read from Dynamics.

Format in Sitecore
-------------------------------------------------
In Sitecore, email activity details are stored in
an event. The event is associated with an interaction.

The following interaction facet is used to identify
that the interaction came from Dynamics:

.. |dynamics-activity-facet-type| replace:: ``Sitecore.DataExchange.Tools.DynamicsConnect.Facets.DynamicsActivityInteraction``

+---------------------------+-------------------------------------------------+
| Facet Name                | ``DynamicsInteraction``                         |
+---------------------------+-------------------------------------------------+
| Facet Type                | |dynamics-activity-facet-type|                  |
+---------------------------+-------------------------------------------------+

The following event type is used to store email activity details:

.. |dynamics-email-event-type| replace:: ``Sitecore.DataExchange.Tools.DynamicsConnect.Events.EmailEvent``

+---------------------------+-------------------------------------------------+
| Event Type                | |dynamics-email-event-type|                     |
+---------------------------+-------------------------------------------------+

Mapping Values
-------------------------------------------------
Separate mappings are needed for the interaction facet and the event.

.. |dynamics-email-interaction-mapping-location| replace:: **Dynamics to xConnect Interaction Mappings > Dynamics Activity to xConnect Dynamics Interaction Facet**
.. |dynamics-email-event-mapping-location| replace:: **Dynamics to xConnect Event Mappings > Dynamics Activity to xConnect Event**

+---------------------------+--------------------+-------------------------------------------------+
| Source objects            | interaction facet, | Activity entity from Dynamics                   |
|                           | event              |                                                 |
+---------------------------+--------------------+-------------------------------------------------+
| Target object             | interaction facet  | |dynamics-activity-facet-type|                  |
+---------------------------+--------------------+-------------------------------------------------+
| Mapping definition        | interaction facet  | |dynamics-email-interaction-mapping-location|   |
+---------------------------+--------------------+-------------------------------------------------+
| Target object             | event              | |dynamics-email-event-type|                     |
+---------------------------+--------------------+-------------------------------------------------+
| Mapping definition        | event              | |dynamics-email-event-mapping-location|         |
+---------------------------+--------------------+-------------------------------------------------+

.. image:: _static/email-activity.png
    :align: center