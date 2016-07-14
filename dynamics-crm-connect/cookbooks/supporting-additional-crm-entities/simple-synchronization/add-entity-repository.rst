Add Entity Repository
===========================

Each type of CRM entity you want to interact with must be defined  
on the Entity Repository Set that your Dynamics CRM Endpoint uses.

.. note:: 
    These instructions assume you have an entity repository set 
    named **mycrm entity repository set**. The name of your 
    repository set may be different, so you may need to adjust 
    some of the paths accordingly.

#.	In Sitecore, open Content Editor.
#.	Navigate to your tenant.
#.	Navigate to **Tenant Settings > Dynamics CRM > Repository Sets > mycrm entity repository set**.
#.	Add the following item:

    +----------+----------------------------------+
    | Template | **XRM Client Entity Repository** |
    +----------+----------------------------------+
    | Name     | **account**                      |
    +----------+----------------------------------+
