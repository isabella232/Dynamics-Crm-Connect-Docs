.. add-templates-for-crm-entity-data:

Add Templates for CRM Entity Data
===================================

You have configured the ability for an xDB contact to be associated with a CRM account. Now you must create a Sitecore template that can be used to store information about the CRM account.

Having Sitecore items that represent CRM accounts will allow your users to configure rules based on account membership. For example, a marketer will be able to personalize a web page based on whether or not a visitor is associated with a specific account.

The marketer must be able to select from a list of available accounts. This is the purpose of exposing CRM accounts as Sitecore items.

#.	In Sitecore, open Template Manager.
#.	Navigate to **Templates > Data Exchange > Providers > Dynamics CRM > Folders**.
#.	Add a new template named **Accounts Folder**.
#.	Set the icon for this template to ``Office/32x32/folder_open.png``.
#.	Navigate to **Templates > Data Exchange > Providers > Sitecore > Entities**.
#.	Add a new template named **External Account**.
#.	Set the icon for this template to ``Office/32x32/office_building2.png``.
#.	Add a section named **Data**.
#.	Add the following field:

    +--------+--------------------------------+
    | Name   | **AccountName**                |
    +--------+--------------------------------+
    | Type   | **Single-Line Text**           |
    +--------+--------------------------------+
    | Shared | **ticked**                     |
    +--------+--------------------------------+

10.	Navigate to **Templates > Data Exchange > Providers > Sitecore > Entities > External Account > Data > AccountName**.
#.	Set the following field value:

    +--------+--------------------------------+
    | Field  | **Title**                      |
    +--------+--------------------------------+
    | Value  | **Account name**               |
    +--------+--------------------------------+

12.	Save the item.
#.	Add the following field:

    +--------+--------------------------------+
    | Name   | **AccountId**                  |
    +--------+--------------------------------+
    | Type   | **Single-Line Text**           |
    +--------+--------------------------------+
    | Shared | **ticked**                     |
    +--------+--------------------------------+

14.	Navigate to **Templates > Data Exchange > Providers > Sitecore > Entities > External Account > Data > AccountId**.
#.	Set the following field value:

    +--------+--------------------------------+
    | Field  | **Title**                      |
    +--------+--------------------------------+
    | Value  | **Account ID**                 |
    +--------+--------------------------------+

16.	Save the item.
#.	Open Content Editor.
#.	Navigate to your tenant.
#.	Navigate to **Tenant Settings > Dynamics CRM**.
#.	Add the following item:

    +----------+--------------------------------------------------------------------------+
    | Template | **Data Exchange > Providers > Dynamics CRM > Folders > Accounts Folder** |
    +----------+--------------------------------------------------------------------------+
    | Name     | **Accounts**                                                             |
    +----------+--------------------------------------------------------------------------+

