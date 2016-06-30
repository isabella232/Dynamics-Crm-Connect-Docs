Filter CRM Contacts
========================

By default, all active contacts with an email address are read from 
Dynamics CRM. This is actually a combination of two things:

* The built in filter for active contacts (which can be disabled as described in the section :ref:`read-inactive-crm-campaigns`)
* A pre-configured expression filter for contacts with email addresses.

The pre-configured expression filter is set on the following item under your *tenant*:

+-----------------+-------------------------------------------------------------------+
| Item path       | | **Pipelines > CRM Contact Pipelines >**                         |
|                 | | **Read CRM Contacts Pipeline > Read CRM Contacts**              |
+-----------------+-------------------------------------------------------------------+
| Field name      | | **Filter expression**                                           |
+-----------------+-------------------------------------------------------------------+
| Expression path | | **Tenant Settings > Dynamics CRM > Filter Expressions >**       |
|                 | | **Contact Filter Expressions > Contacts With Email Specified**  | 
+-----------------+-------------------------------------------------------------------+

This pre-configured expression filter can be changed or replaced as 
needed. Details on how to configure filter expressions are available
in the section :ref:`crm-filter-expressions`.

