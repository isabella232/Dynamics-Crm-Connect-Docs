.. _extend-contact-aggregator:

Extend Contact Aggregator
======================================

When an xDB contact is changed, the aggregation process runs. 
The aggregation process ensures the contact is reindexed. 

A component called a contact aggregator is responsible for 
creating the indexable contact from the xDB contact. In other 
words, the contact aggregator converts the xDB contact into an 
instance of the class you created in :ref:`extend-indexable-contact`.

You must create a custom contact aggregator that uses the 
indexable contact class.

1.	In Visual Studio, add the following references to the project:

    * Sitecore.Analytics.Aggregation.dll
    * Sitecore.Kernel.dll

2.	Add the following class:

.. code-block:: c#

    using Examples.DynamicsCrm.Search;
    using Sitecore.Analytics.Aggregation.Pipelines.ContactProcessing;
    using Sitecore.Analytics.DynamicsCrm.Aggregators;
    using Sitecore.ContentSearch;
    using Sitecore.ContentSearch.Analytics.Models;
    using System;
    using System.Collections.Generic;

    namespace Examples.DynamicsCrm.Aggregators
    {
        public class ContactChangeContactAggregatorEx2 : ContactChangeContactAggregatorEx
        {
            public ContactChangeContactAggregatorEx2(string name) : base(name) { }
            protected override IEnumerable<IContactIndexable> ResolveIndexables(ContactProcessingArgs args)
            {
                if (args == null)
                {
                    throw new ArgumentNullException("args");
                }
                var changeEventReason = this.GetChangeEventReason(args);
                var contact = args.GetContact();
                if (contact != null)
                {
                    yield return new ContactChangeIndexable(
                        new ContactIndexableEx2(contact), 
                        changeEventReason);
                }
                else
                {
                    yield return new ContactChangeIndexable(
                        new IndexableUniqueId<Guid>(args.ContactId.Guid), 
                        changeEventReason);
                }
            }
        }
    }

3.	Compile the project.
4.	Deploy **Examples.DynamicsCrm.dll** to your Sitecore server.
