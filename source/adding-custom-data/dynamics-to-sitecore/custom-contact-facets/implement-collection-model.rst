Implement Collection Model
===================================================
In xConnect, a collection model defines which contact 
facets are available. Before you can store data in a 
custom contact facet, you need a collection model that 
includes the custom contact facet.

1. In Visual Studio, add the following class:

.. code-block:: c#

    using Sitecore.DataExchange.Tools.DynamicsConnect.Models;
    using Sitecore.XConnect;
    using Sitecore.XConnect.Schema;
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;

    namespace Examples.Connect.Dynamics
    {
        public class DynamicsConnectCollectionModelEx
        {
            public DynamicsConnectCollectionModelEx()
            {
            }
            static DynamicsConnectCollectionModelEx()
            {
                _model = BuildModel();
            }
            private static XdbModel _model = null;
            public static XdbModel Model { get { return _model; } }
            private static XdbModel BuildModel()
            {
                var builder = new XdbModelBuilder(typeof(DynamicsConnectCollectionModelEx).FullName, new XdbModelVersion(1, 0));
                builder.DefineFacet<Contact, DynamicsAccountInformationFacet>(DynamicsAccountInformationFacet.DefaultFacetKey);
                builder.ReferenceModel(DynamicsConnectCollectionModel.Model);
                return builder.BuildModel();
            }
        }
    }
