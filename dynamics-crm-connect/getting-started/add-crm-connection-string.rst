Add CRM Connection String
=============================

Dynamics CRM Connect uses a connection string to specify which CRM to 
connect to.

You must add the connection to the Sitecore connection strings file. 
This file is located on your Sitecore server:

**[web root]/App_Config/ConnectionStrings.config**

.. hint::
  Talk to your CRM administrator to get the proper value.

.. hint::
  Documentation on the supported format for this connection string is
  available from the Microsoft Developer Network (MSDN):

      https://msdn.microsoft.com/en-us/library/gg695810(v=crm.7).aspx#parameters

.. important::
  Dynamics CRM Connect does not currently support authentication using OAuth.

.. tip::
  The name of the connection string can be whatever you like, but it
  is recommended you use the name of the tenant.

  For example, if the tenant is named **mycrm**, the following
  connection string name is used:

    ::

      <add name="mycrm" connectionString="url=https://####/XRMServices/2011/Organization.svc;
           user id=####;password=####;organization=###;authentication type=2" />