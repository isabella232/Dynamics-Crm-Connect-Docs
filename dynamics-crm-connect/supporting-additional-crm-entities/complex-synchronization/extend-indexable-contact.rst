.. _extend-indexable-contact:

Extend Indexable Contact
======================================

The contact facet makes it possible to store the account ID on the 
xDB contact, but in order for this value to be usable within Sitecore, 
the account ID must be indexed.

Sitecore includes the type ``Sitecore.ContentSearch.Analytics.Models.ContactIndexable``. 
This type converts an xDB contact into a format where the contact 
data can be indexed.

Dynamics CRM Connect extends this type so that the properties on the
``Sitecore.Analytics.DynamicsCrm.Models.ICrmContactData`` contact facet 
are indexed. This is the purpose of the type 
``Sitecore.Analytics.DynamicsCrm.Search.ContactIndexableEx``.

You must extend ``ContactIndexableEx`` to include the account ID.

1.	In Visual Studio, add the following references to the project:

    * Sitecore.ContentSearch.dll
    * Sitecore.ContentSearch.Analytics.dll

2.	Add the following class:

.. code-block:: c#
   
    using Examples.DynamicsCrm.Models;
    using Sitecore.Analytics.DynamicsCrm.Search;
    using Sitecore.Analytics.Model.Entities;
    using System;

    namespace Examples.DynamicsCrm.Search
    {
        public class ContactIndexableEx2 : ContactIndexableEx
        {
            public ContactIndexableEx2(IContact contact) : base(contact)
            {
                LoadFields(contact);
            }
            private void LoadFields(IContact contact)
            {
                var data = contact.GetFacet<ICrmContactDataEx>("DynamicsCrm");
                if (data == null)
                {
                    return;
                }
                AddField<Guid>("crm.account", data.AccountId);
            }
        }
    }
