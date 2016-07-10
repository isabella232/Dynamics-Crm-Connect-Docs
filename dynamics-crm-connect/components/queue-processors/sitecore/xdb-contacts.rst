.. _sitecore-queue-processors-xdb-contacts:

xDB Contacts
==========================================

This *queue processor* is reads xDB contacts from the queue and writes 
those contacts to xDB using the bulk contact update API.

+-----------------+-----------------------------------------------------------+
| Template name   | **Queue Processor for xDB Contact**                       |
+-----------------+-----------------------------------------------------------+
| Base template   | :ref:`framework-queue-processor-base`                     |
+-----------------+-----------------------------------------------------------+

This queue processor handles the following types of queue entries:

    * ``Sitecore.Analytics.Model.Entities.IContactTemplate``