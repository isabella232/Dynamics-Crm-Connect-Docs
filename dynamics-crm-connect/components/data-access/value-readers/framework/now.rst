.. _framework-now-value-reader:

Now
==========================================

This *value reader* is used to read the current ``DateTime``.

+-----------------+-----------------------------------------------------------+
| Template name   | **Now Value Reader**                                      |
+-----------------+-----------------------------------------------------------+
| Base template   | :ref:`framework-generic-value-reader`                     |
+-----------------+-----------------------------------------------------------+

+--------------------------------+--------------------------------------------------------------------------+
| Field                          | Description                                                              |
+================================+==========================================================================+
| ``Get date/time as UTC``       | Whether or not the ``DateTime`` object that is read is expressed as UTC. |
+--------------------------------+--------------------------------------------------------------------------+

.. tip:: 

    This value reader is used to capture when the synchronization 
    process ran so this value can be stored on the xDB contact.
