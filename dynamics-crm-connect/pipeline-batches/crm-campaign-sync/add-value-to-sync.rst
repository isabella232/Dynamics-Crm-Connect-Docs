Add Value to Synchronize
==========================

The default value mappings are described in the :doc:`/pipeline-batches/crm-campaign-sync/default-value-mappings`
section. These mappings can be changed, and new mappings can be added.

.. contents:: Steps:
  :local:
  :depth: 2

In order to add a new field, you must know the attribute from the CRM campaign
that you want to read, and the property on the Sitecore campaign that you want
to write.

Identify CRM Campaign Attribute
----------------------------------

Your CRM administrator is able to provide you with the names of the attributes
that are available in your CRM.

Identify Sitecore Campaign Property
-------------------------------------

Dynamics CRM Connect interacts with Sitecore campaigns using the following type:

``Sitecore.Marketing.Campaigns.Services.Model.CampaignEntity, Sitecore.Marketing.Campaigns.Services``

Your Sitecore administrator is able to provide you with the names of the
properties that are available on this type.

Define Value Accessors
------------------------

A *value accessor* represents a value that can be read or written during the
synchronization process. Two value accessor items must be created: one for
the CRM campaign attribute and the Sitecore campaign property identified in
the previous steps.

Value Accessor for CRM Campaign
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The value accessor for the CRM campaign is used to read the attribute whose 
value is written to the Sitecore campaign.

#. In Content Editor, navigate to your *tenant*.
#. Navigate to **Data Access > Value Accessor Sets > Providers**.
#. Navigate to **Dynamics CRM > CRM Campaign Attributes**.
#. Insert a new item using the template **Entity Attribute Value Accessor**.
#. In the field **Attribute name**, enter the name of the attribute from the section `Identify CRM Campaign Attribute`_.
#. Save the item.

.. tip::
  For more information on the value accessor used with CRM entity 
  attributes, see :def-providers-crm-component:`Entity Attribute Value<data-access/value-accessors/entity-attribute-value.html>`. 

Value Accessor for Sitecore Campaign
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The value accessor for the Sitecore campaign is used to write the value 
read from the CRM campaign to the Sitecore campaign.

#. Navigate to your tenant.
#. Navigate to **Data Access > Value Accessor Sets > Providers**.
#. Navigate to **Sitecore > Sitecore Campaign Entity Fields**.
#. Insert a new item using the template **Property Value Accessor**.
#. In the field **Property name**, enter the name of the property from the section `Identify Sitecore Campaign Property`_.
#. Save the item.

.. tip::
  For more information on the value accessor used with CRM entity 
  attributes, see :def-providers-crm-component:`Entity Attribute Value<data-access/value-accessors/entity-attribute-value.html>`. 

Define Value Mapping
---------------------

A *value mapping* associates the *value accessor* used to read a value
with the value accessor used to write a value.

In this case, the value mapping associates the value accessor used
read the attribute value from a CRM campaign with the value accessor
used to write the property value to Sitecore campaign.

#. In Content Editor, Navigate to your *tenant*.
#. Navigate to **Value Mapping Sets > CRM Campaign to Sitecore Campaign**.
#. Insert a new item using the template **Value Mapping**.
#. In the field **Value accessor for source object**, select the `Value Accessor for CRM Campaign`_.
#. In the field **Value accessor for target object**, select the `Value Accessor for Sitecore Campaign`_.
#. Save the item.

This setting will take affect the next time the synchronization process runs.
