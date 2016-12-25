Extend Value Accessor Converter
=======================================

The component responsible for converting a Sitecore item into 
a *value accessor* that can read and write CRM entity attributes
must be modified in order to use the *value writer* you created
in the previous step.

Add the following class to your Visual Studio project:

.. code-block:: c#

    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    using Sitecore.DataExchange.Repositories;
    using Sitecore.DataExchange.DataAccess;
    using Sitecore.Services.Core.Model;
    using Sitecore.DataExchange.Providers.DynamicsCrm.Converters.DataAccess.ValueAccessors;
    using Sitecore.DataExchange.Providers.DynamicsCrm.Models.ItemModels.DataAccess;

    namespace Examples.DynamicsCrm
    {
        public class EntityAttributeValueAccessorConverterEx : EntityAttributeValueAccessorConverter
        {
            public EntityAttributeValueAccessorConverterEx(IItemModelRepository repository) : base(repository)
            {
            }
            public override IValueAccessor Convert(ItemModel source)
            {
                var accessor = base.Convert(source);
                if (accessor != null && accessor.ValueWriter == null)
                {
                    var useValueProperty = base.GetBoolValue(source, EntityAttributeValueAccessorItemModel.UseValueProperty);
                    if (useValueProperty)
                    {
                        var attributeName = base.GetStringValue(source, EntityAttributeValueAccessorItemModel.AttributeName);
                        accessor.ValueWriter = new EntityAttributeOptionSetValueWriter(attributeName);
                    }
                }
                return accessor;
            }
        }
    }

2. In Sitecore, 