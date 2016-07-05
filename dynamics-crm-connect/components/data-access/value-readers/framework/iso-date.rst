.. _framework-iso-date-value-reader:

ISO Date
==========================================

This *value reader* is used to read a ``DateTime`` object as an ISO date.

.. tip:: 

    This value reader is usually used with a :ref:`framework-sequential-value-reader`. 

+-----------------+-----------------------------------------------------------+
| Template name   | **ISO Date Value Reader**                                 |
+-----------------+-----------------------------------------------------------+
| Base template   | :ref:`framework-generic-value-reader`                     |
+-----------------+-----------------------------------------------------------+

+--------------------------------+--------------------------------------------------------------------------+
| Field                          | Description                                                              |
+================================+==========================================================================+
| ``Convert date/time to UTC``   | Whether or not the ``DateTime`` object that is read is expressed as UTC. |
+--------------------------------+--------------------------------------------------------------------------+
| ``Include ticks``              | Whether or not the ``DateTime`` object includes ticks.                   |
+--------------------------------+--------------------------------------------------------------------------+
