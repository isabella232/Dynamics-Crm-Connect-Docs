Option Set Values
==========================

In Dynamics CRM, option sets are used to define lists of values from 
which one or more values can be selected. For example, option sets
are used to identify things like gender (male, female), the type of
entity a marketing list is made up of (accounts, contacts, leads) 
and so on.

As of Dynamics CRM Connect 1.2, option set values can be read from CRM, 
but they cannot be written back to CRM. This section explains how to
extend the Dynamics CRM Connect in order to support writing option set
values back to CRM. 

.. note:: 
    Support for option set values is planned to be included in Dynamics 
    CRM Connect 1.3. At that point, this section will become obsolete
    and will be removed from the documentation.

Steps
------

.. toctree::
    :name: option-set-values
    :numbered:
    :titlesonly:

    add-value-writer
    extend-value-accessor-converter
    deploy-the-extension
    mapping-option-set-values


