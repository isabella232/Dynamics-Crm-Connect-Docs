Assign Converter to Entity Repository Template
====================================================

The converter created in :doc:`implement-converter-for-entity-repo-template` 
is always used to convert items based on the template created in 
:doc:`add-template-for-entity-repo`. This can be set up on the template 
so the converter is assigned automatically when a new item is created.

1.	In Sitecore, open Template Manager.
2.	Navigate to **Templates > Data Exchange > Providers > Dynamics CRM > Repositories > XRM Client Account Membership Repository**.
3.	Add standard values to the template.
4.	Navigate to the standard values item.
5.	Set the following field value:

    +--------------+---------------------------+
    | Field name   | **Entity name**           |
    +--------------+---------------------------+
    | Value        | **accountmembership**     |
    +--------------+---------------------------+

6.	Set the following field value:

    +--------------+-------------------------------------------------------------------------------------------------------------+
    | Field name   | **Converter type**                                                                                          |
    +--------------+-------------------------------------------------------------------------------------------------------------+
    | Value        | **Examples.DynamicsCrm.Converters.XrmClientAccountMembershipRepositoryConverter, Examples.DynamicsCrm**     |
    +--------------+-------------------------------------------------------------------------------------------------------------+

7.	Save the item.
