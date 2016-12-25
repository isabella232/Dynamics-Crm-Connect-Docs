Add Value Writer
==========================

As of Dynamics CRM Connect 1.2, no *value writer* is included that is 
able to set values on attributes on CRM entities that are option sets.
You must add a component to do this.

1.	In Visual Studio, create a new project:

    +-------------------+--------------------------+
    | Project template  | **Class Library**        |
    +-------------------+--------------------------+
    | Name              | **Examples.DynamicsCrm** |
    +-------------------+--------------------------+

2.	Add references to following NuGet packages:

    * Sitecore.DataExchange.Providers.DynamicsCrm

3.	Add the following class:

.. code-block:: c#

    using Microsoft.Xrm.Sdk;
    using Sitecore.DataExchange.DataAccess;
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Reflection;
    using System.Text;
    using System.Threading.Tasks;

    namespace Examples.DynamicsCrm
    {
        public class EntityAttributeOptionSetValueWriter : IValueWriter
        {
            public EntityAttributeOptionSetValueWriter(string attributeName)
            {
                this.AttributeName = attributeName;
            }
            public string AttributeName { get; private set; }

            public CanWriteResult CanWrite(object target, object value, DataAccessContext context)
            {
                var canWrite = false;
                var isGuess = false;
                if (value != null && value is int)
                {
                    if (target is Entity)
                    {
                        canWrite = true;
                        isGuess = true;
                    }
                }
                return new CanWriteResult { CanWriteValue = canWrite, IsGuess = isGuess};
            }
            public bool Write(object target, object value, DataAccessContext context)
            {
                if (value != null && value is int)
                {
                    var entity = target as Entity;
                    if (entity != null)
                    {
                        if (entity.Attributes.ContainsKey(this.AttributeName))
                        {
                            if (entity.Attributes[this.AttributeName] is OptionSetValue)
                            {
                                var value2 = entity.Attributes[this.AttributeName] as OptionSetValue;
                                value2.Value = (int)value;
                                return true;
                            }
                        }
                        else
                        {
                            entity.Attributes[this.AttributeName] = new OptionSetValue((int)value);
                            return true;
                        }
                    }
                }
                return false;
            }
        }
    }
