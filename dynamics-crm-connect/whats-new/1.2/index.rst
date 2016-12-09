v1.2
=================================================

.. contents:: What's new in version 1.2
   :depth: 1
   :local:

.. include:: ../../../common/def-documentation-notice.txt

New features 
-------------------------------------------------

New pipeline steps
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * Read multiple items from a Sitecore database.

        .. note::
            This pipeline step is not currently used in any of the 
            default pipeline batches. It is available for you to use
            in custom pipelines you design.

            For more information on this pipeline step, see 
            :def-providers-sitecore-component:`Read Sitecore Items<pipeline-steps/read-sitecore-items.html>`. 

Improved control over pipeline batches
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * Added button to Sitecore Content Editor to allow a user to stop
      a *pipeline batch* that is currently running.
    * Controls to prevent a pipeline batch from running multiple times
      concurrently.

Performance improvements 
-------------------------------------------------

:doc:`../../pipeline-batches/crm-campaign-sync/index`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * Queuing is used when multiple campaigns are updated in Sitecore.
    * Logic to resolve campaign category in Sitecore only runs once per execution.
    * *Mappings applied actions* are used to minimize the number of 
      Sitecore campaigns that need to be updated.   


:doc:`../../pipeline-batches/xdb-contact-sync/index`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * Queuing is used when multiple contacts are updated in Dynamics CRM.
    * *Mappings applied actions* are used to minimize the number of 
      CRM contacts that need to be updated.   


