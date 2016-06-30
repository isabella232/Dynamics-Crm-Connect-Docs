.. _default-value-mappings-crm-marketinglist:

Default Value Mappings
==============================

In CRM, a marketing list consists of two things: the marketing list itself,
and the list of members of the marketing list. Both of these things are
represented in Sitecore.

Marketing List
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
By default, the marketing list synchronization process maps the following
values from the CRM marketing list to the Sitecore item.

These mappings are defined in the *value mapping set* named
**CRM List to Sitecore Item**.

.. note::
  The following template is used to represent CRM marketing lists in Sitecore:

  **Templates > Data Exchange > Providers > Sitecore > Entities > External Marketing List**

.. csv-table:: 
   :header: "CRM Marketing List", "Sitecore Field", "Description"

    ``listid``, ``MarketingListId``, "Unique identifier in CRM"
    ``listname``, ``MarketingListName``, "Marketing list name"

Marketing List Membership
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
By default, the marketing list synchronization process maps the following
values from the CRM marketing list to the xDB contacts that are members
of the marketing list.

These mappings are defined in the value mapping set named
**CRM List Membership to xDB Contact**.

.. csv-table:: 
   :header: "CRM Marketing List", "xDB Contact Facet", "Facet Property", "Description"

    ``listid``, ``DynamicsCrm``, ``MarketingLists``, "Unique identifier in CRM"

