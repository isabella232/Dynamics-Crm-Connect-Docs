Value Accessors
=======================

A *value accessor* associates the component used to read a value 
(*value reader*) with the component used to write a value (*value writer*).

The following comparison might be helpful:

+-------------------------+------------------+
| Data Exchange Framework | C#               |
+=========================+==================+
| Value accessor          | Property         |
+-------------------------+------------------+
| Value reader            | Property getter  |
+-------------------------+------------------+
| Value writer            | Property setter  |
+-------------------------+------------------+

Value accessors are used to configure *value mappings*. One value 
accessor identifies the component used to read a value from the 
source object, and another value accessor identifies the component
used to write a value to the target object.

.. toctree::
    :name: value-accessors-templates
    :caption: Templates 
    :titlesonly:
    :maxdepth: 2

    framework/index
    sitecore/index
    crm/index
    