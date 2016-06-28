Add Fields to Synchronize
==========================

The default field mappings are described in the :doc:`Default Field Mappings <default-field-mappings>`
section. These mappings can be changed, and new mappings can be added.

.. contents:: Steps:
  :local:
  :depth: 2

In order to add a new field, you must know the attribute from the CRM campaign
that you want to read, and the property on the Sitecore campaign that you want
to write.

Identity CRM Campaign Attribute
----------------------------------

Your CRM administrator is able to provide you with the names of the attributes
that are available in your CRM.

Identity Sitecore Campaign Property
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

#. In Content Editor, navigate to your *tenant*.
#. Navigate to **Data Access > Value Accessor Sets > Providers**.
#. Navigate to **Dynamics CRM > CRM Campaign Attributes**.
#. Insert a new item using the template **Entity Attribute Value Accessor**.
#. In the field **Attribute name**, enter the name of the attribute from the section `Identity CRM Campaign Attribute`_.
#. Save the item.
#. Navigate to your tenant.
#. Navigate to **Data Access > Value Accessor Sets > Providers**.
#. Navigate to **Sitecore > Sitecore Campaign Entity Fields**.
#. Insert a new item using the template **Property Value Accessor**.
#. In the field **Property name**, enter the name of the property from the section `Identity Sitecore Campaign Property`_.
#. Save the item.

Define Value Mapping
---------------------

A *value mapping* associates the *value accessor* used to read a value
with the value accessor used to write a value.

In this case, the value mapping associates the value accessor used
read the attribute value from a CRM campaign with the value accessor
used to write the property value to a Sitecore campaign.

#. In Content Editor, Navigate to your *tenant*.
#. Navigate to **Value Mapping Sets > CRM Campaign to Sitecore Campaign**.
#. Insert a new item using the template **Value Mapping**.
#. In the field **Value accessor for source object**, select the item you created under **Data Access > Value Accessor Sets > Providers > Dynamics CRM > CRM Campaign Attributes**.
#. In the field **Value accessor for target object**, select the item you created under **Data Access > Value Accessor Sets > Providers > Sitecore > Sitecore Campaign Entity Fields**.
#. Save the item.

This setting will take affect the next time the synchronization process runs.
