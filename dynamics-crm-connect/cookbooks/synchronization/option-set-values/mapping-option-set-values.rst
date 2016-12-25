Mapping Option Set Values
=======================================

.. warning::
    Please read this section carefully before trying to
    write option set values to Dynamics CRM.

Now, any :def-providers-crm-component:`entity value accessor set<data-access/value-accessor-sets/entity-attributes.html>` 
you have can be configured to write option set values to 
CRM entities. In order for Dynamics CRM Connect to treat 
the attribute value as an option set value, you must enable 
the field **Use Value Property** on the :def-providers-crm-component:`entity value accessor<data-access/value-accessors/entity-attribute-value.html>`
that represents the entity.

.. tip::

    Remember that the components you created do not convert string values 
    into the appropriate option set value. The option set value is always
    and integer.

    For example, Dynamics CRM uses an option set to indicate a contact's 
    gender. In the option set:
    
        * Male is represented by the value 1
        * Female is represented by the value 2

    If you want to change the gender of a contact, the value you map 
    to CRM must be either **1** or **2**.

    The field **Source Value Transformer** on the 
    :def-framework-component:`value mapping<data-mapping/value-mappings/value-mapping.html>`
    component provides a way for you to convert strings (and other values) into valid option 
    set values.
