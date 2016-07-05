.. _framework-generic-value-accessor:

Generic
==========================================

This *value accessor* allows a value reader and/or value writer 
to be set explicitly.

+-----------------+-----------------------------------------------------------+
| Template name   | **Value Accessor**                                        |
+-----------------+-----------------------------------------------------------+
| Base template   | none                                                      |
+-----------------+-----------------------------------------------------------+

.. note::

    This template is the base template for all value accessors.
    In most cases, items based on templates that inherits from 
    this template are used to configure a *value accessor set*. 
    It is rare for items to be created using this template directly.

+-----------------------------------------------+-----------------------------------------------------------+
| Field                                         | Description                                               |
+===============================================+===========================================================+
| ``Value reader``                              | | Value reader used to read a value.                      |
|                                               | |                                                         |
|                                               | | Most templates that inherit from this template use      |  
|                                               | | other fields to provide information that is used to     |
|                                               | | automatically determine the appropriate value reader.   |
|                                               | |                                                         |
|                                               | | This field makes it possible for the value reader on    |
|                                               | | a specific item to be set explicitly. This field is     |
|                                               | | not used often.                                         |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Value writer``                              | | Value writer used to write a value.                     |
|                                               | |                                                         |
|                                               | | Most templates that inherit from this template use      |  
|                                               | | other fields to provide information that is used to     |
|                                               | | automatically determine the appropriate value writer.   |
|                                               | |                                                         |
|                                               | | This field makes it possible for the value writer on    |
|                                               | | a specific item to be set explicitly. This field is     |
|                                               | | not used often                                          |
+-----------------------------------------------+-----------------------------------------------------------+



