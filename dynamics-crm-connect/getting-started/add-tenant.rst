Add Tenant
===============

All of the settings that pertain to synchronizing your Sitecore server with
your CRM are grouped under an item called a *tenant*.

You must create a tenant in order to configure a connection to your CRM.

#. In Sitecore, open Content Editor.
#. Navigate to **sitecore > system > Data Exchange**.
#. Add the following item:

    +--------------+---------------------------------------+
    | **Template** | Data Exchange Tenant for Dynamics CRM |
    +--------------+---------------------------------------+
    | **Name**     | mycrm                                 |
    +--------------+---------------------------------------+

    .. tip::
      The name you choose for your tenant is used to identify data
      read from Dynamics CRM. You can change this value later.
