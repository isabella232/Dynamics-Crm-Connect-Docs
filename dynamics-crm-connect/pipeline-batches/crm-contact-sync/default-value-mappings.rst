Default Value Mappings
==============================

By default, the contact synchronization process maps the following values
from the CRM contact to the xDB contact.

These mappings are defined in the *value mapping set* named
**CRM Contact to xDB Contact**.

The following values are written to the xDB contact's identifiers: 

.. csv-table:: 
   :header: "Property", "Description"

   ``IdentificationLevel``, "The value that indicates the contact is known: ``2``"
   ``Identifier``, "The value of the CRM contact attribute ``emailaddress1``"

The following values are mapped from the CRM contact to the xDB contact:

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

In addition, the following values are written to the xDB contact.

.. csv-table:: 
   :header: "xDB Contact Facet", "Facet Property", "Description"

    ``DynamicsCrm``, ``LastSynced``, "The date/time when the value mappings were last applied."
    ``DynamicsCrm``, ``CrmName``, "The tenant name."
