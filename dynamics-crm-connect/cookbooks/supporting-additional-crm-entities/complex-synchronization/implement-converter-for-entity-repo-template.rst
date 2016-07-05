.. _implement-converter-for-entity-repo-template:

Implement Converter for Entity Repository Template
====================================================

A converter is needed to transform items created using the template from 
:ref:`add-template-for-entity-repo` into entity repository objects that 
can be used by Pipeline Step Processors.

1.	In Visual Studio, add the following class:

.. code-block:: c#

    using Examples.DynamicsCrm.Repositories;
    using Sitecore.Connect.Crm.DynamicsCrm.Repositories;
    using Sitecore.DataExchange.Converters;
    using Sitecore.DataExchange.Providers.DynamicsCrm.Models.ItemModels.Repositories;
    using Sitecore.DataExchange.Repositories;
    using Sitecore.Services.Core.Model;
    using System;

    namespace Examples.DynamicsCrm.Converters
    {
        public class XrmClientAccountMembershipRepositoryConverter : BaseItemModelConverter<ItemModel, XrmClientEntityRepository>
        {
            private static readonly Guid TemplateId = Guid.Parse("[TEMPLATE-ID]");
            public XrmClientAccountMembershipRepositoryConverter(IItemModelRepository repository) : base(repository)
            {
                this.SupportedTemplateIds.Add(TemplateId);
            }
            public override XrmClientEntityRepository Convert(ItemModel source)
            {
                if (!CanConvert(source))
                {
                    return null;
                }
                var repository = new XrmClientAccountMembershipRepository(base.GetStringValue(source, EntityRepositoryItemModel.EntityName));
                return repository;
            }
        }
    }

2.	Find the following line in the code:

.. code-block:: c#

    private static readonly Guid TemplateId = Guid.Parse("[TEMPLATE-ID]");

3.	Replace ``[TEMPLATE-ID]`` with the ID for the template from :ref:`add-template-for-entity-repo`.
4.	Compile the project.
5.	Deploy **Examples.DynamicsCrm.dll** to your Sitecore server.
