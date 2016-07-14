Implement Processor for Read Members Pipeline Step
====================================================

A processor implements the logic for the *pipeline step*. A processor is 
needed to read members from a CRM account using the *entity repository*.

1.	In Visual Studio, add the following class:

.. code-block:: c#

    using Microsoft.Xrm.Sdk;
    using Sitecore.Connect.Crm.DynamicsCrm.Plugins;
    using Sitecore.Connect.Crm.Repositories;
    using Sitecore.DataExchange.Contexts;
    using Sitecore.DataExchange.Extensions;
    using Sitecore.DataExchange.Models;
    using Sitecore.DataExchange.Providers.DynamicsCrm.Processors.PipelineSteps;
    using System;

    namespace Examples.DynamicsCrm.Processors
    {
        public class ReadAccountMembershipStepProcessor : ReadEntitiesStepProcessor
        {
            protected override RepositoryOperationContext GetRepositoryOperationContext(Endpoint endpoint, PipelineStep pipelineStep, PipelineContext pipelineContext)
            {
                var opContext = base.GetRepositoryOperationContext(endpoint, pipelineStep, pipelineContext);
                if (opContext == null)
                {
                    return null;
                }
                var syncSettings = pipelineContext.GetSynchronizationSettings();
                if (syncSettings == null)
                {
                    return null;
                }
                var source = syncSettings.Source;
                if (source == null)
                {
                    return null;
                }
                var entity = source as Entity;
                if (entity == null)
                {
                    return null;
                }
                if (!entity.Attributes.ContainsKey("accountid"))
                {
                    return null;
                }
                var accountId = (Guid)entity.Attributes["accountid"];
                if (accountId == Guid.Empty)
                {
                    return null;
                }
                var settings = new MemberEntitiesSettings
                {
                    EntityId = accountId
                };
                opContext.Plugins.Add(settings);
                return opContext;
            }
        }
    }

2.	Compile the project.
3.	Deploy **Examples.DynamicsCrm.dll** to your Sitecore server.
