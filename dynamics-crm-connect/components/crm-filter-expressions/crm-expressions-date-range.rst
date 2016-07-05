.. _crm-expressions-date-range:

Date Range Condition Expression
======================================

A date range condition expression is used to determine whether or not 
the value of an attribute is within a date range. 

+-----------------+-----------------------------------------------------------+
| Template name   | **Date Range Condition Expression**                       |
+-----------------+-----------------------------------------------------------+
| Base template   | :ref:`crm-expressions-base-attribute`                     |
+-----------------+-----------------------------------------------------------+

+-----------------------------------------------+-----------------------------------------------------------+
| Field                                         | Description                                               |
+===============================================+===========================================================+
| ``Start date``                                | | The start date for the expression.                      |
|                                               | |                                                         |
|                                               | | If no value is specified, no lower bound is considered. |
+-----------------------------------------------+-----------------------------------------------------------+
| ``End date``                                  | | The end date for the expression.                        |
|                                               | |                                                         |
|                                               | | If no value is specified, no upper bound is considered. |
+-----------------------------------------------+-----------------------------------------------------------+

.. note:: 
    
    Date range condition expression items are converted into instances of the 
    type ``Microsoft.Xrm.Sdk.Query.ConditionExpression``. For more information 
    about how this type works, see `<https://msdn.microsoft.com/en-us/library/gg334419.aspx>`_.
