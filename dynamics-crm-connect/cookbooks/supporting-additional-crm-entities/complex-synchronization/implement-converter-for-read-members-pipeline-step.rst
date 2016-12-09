Implement Converter for Read Members Pipeline Step
====================================================

A converter is needed to transform items created using the template from 
:doc:`add-template-for-read-members-pipeline-step` into entity repository 
objects that can be used by *pipeline step processors*.

1.	In Visual Studio, add the following class:

.. code-block:: c#

    using Sitecore.DataExchange.Attributes;
    using Sitecore.DataExchange.Providers.DynamicsCrm.Converters.PipelineSteps;
    using Sitecore.DataExchange.Repositories;
    using System;

    namespace Examples.DynamicsCrm.Converters
    {
        [SupportedIds("[TEMPLATE-ID")]
        public class ReadAccountMembershipStepConverter : ReadEntitiesStepConverter
        {
            public ReadAccountMembershipStepConverter(IItemModelRepository repository) : base(repository)
            {
            }
        }
    }

2.	Find the following line in the code:

.. code-block:: c#

    [SupportedIds("[TEMPLATE-ID")]

3.	Replace ``[TEMPLATE-ID]`` with the ID for the template from :doc:`add-template-for-read-members-pipeline-step`.
4.	Compile the project.
5.	Deploy **Examples.DynamicsCrm.dll** to your Sitecore server.
