Deploy the Extension
=======================================

Next you need to deploy the extension and configure Sitecore to use
the components you developed.

#. Compile the Visual Studio project.
#. Deploy the *dll* to your Sitecore server.
#. In Sitecore, open Template Manager.
#. Navigate to **Templates > Data Exchange > Providers > Dynamics CRM > Data Access > Value Accessors > Entity Attribute Value Accessor > __Standard Values**.
#. Set the following field value:

    +--------------+----------------------------------------------------------------------------------------+
    | Field name   | **Converter Type**                                                                     |
    +--------------+----------------------------------------------------------------------------------------+
    | Value        | **Examples.DynamicsCrm.EntityAttributeValueAccessorConverterEx, Examples.DynamicsCrm** |
    +--------------+----------------------------------------------------------------------------------------+

    .. note::
        Since you are making this change to the *standard values* item,
        this change will affect all existing items based on this template.

#. Save the item.