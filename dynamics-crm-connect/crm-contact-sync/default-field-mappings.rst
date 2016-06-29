.. _default-field-mappings-crm-contact:

Default Field Mappings
==============================

By default, the contact synchronization process maps the following values
from the CRM contact to the xDB contact.

These mappings are defined in the *value mapping set* named
**CRM Contact to xDB Contact**.

.. csv-table:: 
   :header: "CRM Contact", "xDB Contact Facet", "Facet Property", "Description"

    ``contactid``, ``DynamicsCrm``, ``ContactId``, "Unique identifier in CRM"
    ``address1_city``, ``Addresses``, ``City``, "City"
    ``address1_country``, ``Addresses``, ``Country``, "Country"
    ``address1_line1``, ``Addresses``, ``StreetLine1``, "Street address (line 1)"
    ``address1_line2``, ``Addresses``, ``StreetLine2``, "Street address (line 2)"
    ``address1_line3``, ``Addresses``, ``StreetLine3``, "Street address (line 3)"
    ``address1_postalcode``, ``Addresses``, ``PostalCode``, "Postal code"
    ``address1_stateorprovince``, ``Addresses``, ``StateProvince``, "State or province"
    ``donotbulkemail``, ``Communication Profile``, ``ConsentRevoked``, "Bulk email opt-out"
    ``emailaddress1``, ``Emails``, ``SmtpAddress``, "Email address"
    ``firstname``, ``Personal``, ``FirstName``, "First name"
    ``jobtitle``, ``Personal``, ``JobTitle``, "Job title"
    ``lastname``, ``Personal``, ``Surname``, "Last name (surname)"
    ``telephone1``, ``Personal``, ``Number``, "Telephone number"
