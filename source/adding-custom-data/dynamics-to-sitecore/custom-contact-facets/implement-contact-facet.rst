Implement Contact Facet
===================================================
Each Salesforce contact is associated with an account.
In order to store the account name on a contact, a 
contact facet is needed.

1. In Visual Studio, add the following class:

.. code-block:: c#

    using Sitecore.XConnect;
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;

    namespace Examples.Connect.Dynamics
    {
        [FacetKey(DefaultFacetKey)]
        [Serializable]
        public class DynamicsAccountInformationFacet : Facet
        {
            public const string DefaultFacetKey = "DynamicsAccount";
            public string AccountName { get; set; }
            public DynamicsAccountInformationFacet()
            {
            }
        }
    }
