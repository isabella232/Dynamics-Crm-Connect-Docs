.. _extend-dynamics-crm-contact-facet:

Extend Dynamics CRM Contact Facet
======================================

The default contact facet used to store CRM data on an xDB contact does not 
have the ability to store any account information. However, you can extend 
the contact facet so that it can.

.. note:: 
    You can also create an entirely new contact facet, if you prefer. 
    But since only a single value is going to be stored, there is not 
    much value in creating a new contact facet.

1.	In Visual Studio, create a new project:

    +-------------------+--------------------------+
    | Project template  | **Class Library**        |
    +-------------------+--------------------------+
    | Name              | **Examples.DynamicsCrm** |
    +-------------------+--------------------------+

2.	Add the following references to the project:

    * Sitecore.Analytics.DynamicsCrm.dll
    * Sitecore.Analytics.Model.dll

3.	Add the following interface:

.. code-block:: c#

    using Sitecore.Analytics.DynamicsCrm.Models;
    using System;
    namespace Examples.DynamicsCrm.Models
    {
        public interface ICrmContactDataEx : ICrmContactData
        {
            Guid AccountId { get; set; }
        }
    }

4.	Add the following class:

.. code-block:: c#

    using Sitecore.Analytics.DynamicsCrm.Models;
    using System;

    namespace Examples.DynamicsCrm.Models
    {
        public class CrmContactDataEx : CrmContactData, ICrmContactDataEx
        {
            public CrmContactDataEx()
            {
                base.EnsureAttribute<Guid>(nameof(AccountId));
            }
            public Guid AccountId
            {
                get
                {
                    return base.GetAttribute<Guid>(nameof(AccountId));
                }
                set
                {
                    base.SetAttribute<Guid>(nameof(AccountId), value);
                }
            }
        }
    }
