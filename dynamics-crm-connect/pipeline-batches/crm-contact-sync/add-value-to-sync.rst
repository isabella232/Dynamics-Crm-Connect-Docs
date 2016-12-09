Add Value to Synchronize
==========================

The default value mappings are described in the :doc:`/pipeline-batches/crm-contact-sync/default-value-mappings`
section. These mappings can be changed, and new mappings can be added.

.. contents:: Steps
  :local:
  :depth: 2

In order to add a new field, you must know the attribute from the CRM contact
that you want to read, and the property on the xDB contact that you want
to write.

Identify CRM Contact Attribute
----------------------------------

Your CRM administrator is able to provide you with the names of the attributes
that are available in your CRM.

Identify xDB Contact Property
-------------------------------------

Values are stored on xDB contacts through contact facets. The contact facets
that are available on your Sitecore server depend on how your system has been
configured.

Your Sitecore administrator is able to provide you with the information about
the available contact facets and the values stored on each.

Define Value Accessors
------------------------

A *value accessor* represents a value that can be read or written during the
synchronization process. Two value accessor items must be created: one for
the CRM campaign attribute and the xDB contact property identified in
the previous steps.

.. _crm-contact-add-value-crm-value-accessor:

Value Accessor for CRM Contact
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The value accessor for the CRM contact is used to read the attribute 
whose value is written to the xDB contact.

#. In Content Editor, navigate to your *tenant*.
#. Navigate to **Data Access > Value Accessor Sets > Providers**.
#. Navigate to **Dynamics CRM > CRM Contact Attributes**.
#. Insert a new item using the template **Entity Attribute Value Accessor**.
#. In the field **Attribute name**, enter the name of the attribute from the section `Identify CRM Contact Attribute`_.
#. Save the item.

.. _crm-contact-add-value-xdb-value-accessor:

Value Accessor for xDB Contact
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The value accessor for the xDB contact is used to write the value read 
from the CRM contact to the xDB contact.  

Defining the value accessor for the xDB contact is more complicated than 
the one for the CRM contact. There is a much greater variety of ways that
data can be stored on an xDB contact than on a CRM contact. 

As a result, you must select the appropriate template for the value 
accessor. 

.. tip::
  The :def-providers-sitecore-component:`available templates<data-access/value-accessors/index.html#sitecore-provider-value-accessors-xdb-templates>`
  are described in the :def-root:`Data Exchange Framework documentation<index.html>`.

#. Navigate to your tenant.
#. Navigate to **Data Access > Value Accessor Sets > Providers**.
#. Navigate to **Sitecore > xDB Contact Entity Fields**.
#. Insert a new item using the template that is appropriate for the value identified in the section `Identify xDB Contact Property`_.
#. Set the required fields.
#. Save the item.

.. _crm-contact-add-value-define-value-mapping:

Define Value Mapping
---------------------

A *value mapping* associates the *value accessor* used to read a value
with the value accessor used to write a value.

In this case, the value mapping associates the value accessor used
read the attribute value from a CRM contact with the value accessor
used to write the property value to an xDB contact.

#. In Content Editor, Navigate to your *tenant*.
#. Navigate to **Value Mapping Sets > CRM Contact to xDB Contact**.
#. Insert a new item using the template **Value Mapping**.
#. In the field **Value accessor for source object**, select the :ref:`crm-contact-add-value-crm-value-accessor`.
#. In the field **Value accessor for target object**, select the :ref:`crm-contact-add-value-xdb-value-accessor`.
#. Save the item.

This setting will take affect the next time the synchronization process runs.
