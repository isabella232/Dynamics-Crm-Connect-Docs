.. _crm-expressions-string:

String Condition Expression
======================================

A string condition expression is used to compare the value of an 
attribute to a string value. 

+-----------------+-----------------------------------------------------------+
| Template name   | **String Condition Expression**                           |
+-----------------+-----------------------------------------------------------+
| Base template   | :ref:`crm-expressions-base-attribute`                     |
+-----------------+-----------------------------------------------------------+

+-----------------------------------------------+-----------------------------------------------------------+
| Field                                         | Description                                               |
+===============================================+===========================================================+
| ``Condition operator``                        | The operator that is used in the expression.              |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Value``                                     | The string value that is used in the expression.          | 
+-----------------------------------------------+-----------------------------------------------------------+

.. note:: 
    
    String condition expression items are converted into instances of the 
    type ``Microsoft.Xrm.Sdk.Query.ConditionExpression``. For more information 
    about how this type works, see `<https://msdn.microsoft.com/en-us/library/gg334419.aspx>`_.
