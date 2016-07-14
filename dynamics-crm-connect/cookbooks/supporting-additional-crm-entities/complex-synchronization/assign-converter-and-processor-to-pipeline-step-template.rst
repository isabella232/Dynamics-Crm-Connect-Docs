Assign Converter & Processor to Pipeline Step Template
=======================================================

The converter created in :doc:`implement-converter-for-read-members-pipeline-step` 
is always used to convert items based on the template created in 
:doc:`add-template-for-read-members-pipeline-step`. The processor 
created in section is always used to run the *pipeline step*. This 
can be set up on the template so the converter is assigned 
automatically when a new item is created.

1.	In Sitecore, open Template Manager.
2.	Navigate to **Templates > Data Exchange > Providers > Dynamics CRM > Pipeline Steps > Read CRM Account Membership Pipeline Step**.
3.	Add standard values to the template.
4.	Navigate to the standard values item.
5.	Set the following field value:

    +--------------+-------------------------------------------------------------------------------------------------------------+
    | Field name   | **Converter type**                                                                                          |
    +--------------+-------------------------------------------------------------------------------------------------------------+
    | Value        | **Examples.DynamicsCrm.Converters.ReadAccountMembershipStepConverter, Examples.DynamicsCrm**                |
    +--------------+-------------------------------------------------------------------------------------------------------------+

6.	Set the following field value:

    +--------------+-------------------------------------------------------------------------------------------------------------+
    | Field name   | **Processor type**                                                                                          |
    +--------------+-------------------------------------------------------------------------------------------------------------+
    | Value        | **Examples.DynamicsCrm.Processors.ReadAccountMembershipStepProcessor, Examples.DynamicsCrm**                |
    +--------------+-------------------------------------------------------------------------------------------------------------+

7.	Save the item.
