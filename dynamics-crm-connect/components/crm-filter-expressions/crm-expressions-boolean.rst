.. _crm-expressions-boolean:

Boolean Condition Expression
======================================

A Boolean condition expression is used to compare the value of an 
attribute to either ``true`` or ``false``.

+-----------------+-----------------------------------------------------------+
| Template name   | **Boolean Condition Expression**                          |
+-----------------+-----------------------------------------------------------+
| Base template   | :ref:`crm-expressions-base-attribute`                     |
+-----------------+-----------------------------------------------------------+

+-------------------------------------+---------------------------------------------------------------------+
| Field                               | Description                                                         |
+=====================================+=====================================================================+
| ``Is``                              | The value - ``true`` or ``false`` - that is used in the expression. |
+-------------------------------------+---------------------------------------------------------------------+

.. note:: 
    
    Boolean condition expression items are converted into instances of the 
    type ``Microsoft.Xrm.Sdk.Query.ConditionExpression``. For more information 
    about how this type works, see `<https://msdn.microsoft.com/en-us/library/gg334419.aspx>`_.
