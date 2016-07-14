Default Value Mappings
==============================

By default, the contact synchronization process maps the following values
from the CRM contact to the xDB contact.

These mappings are defined in the *value mapping set* named
**xDB Contact to CRM Contact**.

.. csv-table:: 
   :header: "xDB Contact Facet", "Facet Property", "CRM Contact", "Description"

    ``Emails``, ``SmtpAddress``, ``emailaddress1``, "Email address"
    ``Personal``, ``FirstName``, ``firstname``, "First name"
    ``Personal``, ``Surname``, ``lastname``, "Last name (surname)"
