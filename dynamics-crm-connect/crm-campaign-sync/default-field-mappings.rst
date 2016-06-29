.. _default-field-mappings-crm-campaign:

Default Field Mappings
=========================

By default, the campaign synchronization process maps the following values
from the CRM campaign to the Sitecore campaign.

These mappings are defined in the *value mapping set* named
**CRM Campaign to Sitecore Campaign**.

.. csv-table:: 
   :header: "CRM Campaign", "Sitecore Campaign", "Description"

    ``campaignid``, ``Id``, "Unique identifier in CRM"
    ``name``, ``Name``,  "Campaign name"
    ``actualstart``, ``StartDate``, "Campaign start date"
    ``actualend``, ``EndDate``, "Campaign end date"
    ``createdon``, ``CreatedDate``, "Date the campaign was created in CRM"
    ``modifiedon``, ``LastModifiedDate``, "Date the campaign was last modified in CRM"
    ``description``, ``Description``, "Campaign description"
