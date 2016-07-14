Implement Entity Repository for Account Membership
====================================================

The default entity repository is able to read entities from Dynamics CRM. 
If you are only reading attributes from the entity, the default entity 
repository can be used. But in cases where you need to read data from 
multiple entities, you need to create a custom entity repository.

For this example, you need an entity repository that is able to read the 
contacts associated with an account.

1.	In Visual Studio, add the following references to the project:

  *	Sitecore.Connect.Crm.dll
  *	Sitecore.Connect.Crm.DynamicsCrm.dll
  *	Sitecore.DataExchange.dll
  *	Sitecore.DataExchange.Providers.DynamicsCrm.dll
  *	Sitecore.Services.Core.dll

2.	Add a reference to the following NuGet packages:

  * Microsoft.CrmSdk.CoreAssemblies (version 7.1.1)

3.	Add the following class:

.. code-block:: c#

  using Microsoft.Xrm.Sdk;
  using Microsoft.Xrm.Sdk.Query;
  using Sitecore.Connect.Crm.DynamicsCrm.Extensions;
  using Sitecore.Connect.Crm.DynamicsCrm.Repositories;
  using Sitecore.Connect.Crm.Repositories;
  using System;
  using System.Collections.Generic;

  namespace Examples.DynamicsCrm.Repositories
  {
      public class XrmClientAccountMembershipRepository : BaseXrmClientMemberEntitiesRepository
      {
          public XrmClientAccountMembershipRepository(string entityName) : base(entityName)
          {
          }
          protected override IEnumerable<Entity> ReadMembers(Guid entityId, RepositoryOperationContext context)
          {
              var query = new QueryExpression("contact");
              var settings = context.GetReadEntityRepositoryOperationSettings();
              if (settings != null)
              {
                  query.ColumnSet = settings.ColumnSet;
              }
              var accountEntity = new LinkEntity("contact", "account", "parentcustomerid", "accountid", JoinOperator.Inner);
              accountEntity.Columns = new ColumnSet("accountid", "name");
              accountEntity.EntityAlias = "account";
              query.LinkEntities.Add(accountEntity);
              query.Criteria.Conditions.Add(new ConditionExpression("parentcustomerid", ConditionOperator.Equal, entityId));
              return ReadEntities(query, context);
          }
      }
  }

4.	Compile the project.
5.	Deploy **Examples.DynamicsCrm.dll** to your Sitecore server.
