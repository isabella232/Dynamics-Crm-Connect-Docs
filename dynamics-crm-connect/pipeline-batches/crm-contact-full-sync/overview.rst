Overview
==========================

This synchronization process is defined in the *pipeline batch*
**Full CRM Contacts to xDB Sync Pipeline Batch**.

This pipeline batch synchronizes the same data as the :doc:`../crm-contact-sync/index` 
and :doc:`../crm-marketinglist-sync/index`, only it does this as a single 
synchronization process.

+-------------------------------+--------------+---------------------+
| Pipeline batch                | Contact sync | Marketing list sync |
+===============================+==============+=====================+
| CRM Contacts to xDB Sync      | yes          | no                  |
+-------------------------------+--------------+---------------------+
| CRM Lists to xDB Sync         | no           | yes                 |
+-------------------------------+--------------+---------------------+
| Full CRM Contacts to xDB Sync | yes          | yes                 |
+-------------------------------+--------------+---------------------+

Both :doc:`../crm-contact-sync/index` and :doc:`../crm-marketinglist-sync/index` 
update xDB Contacts. Both of these processes update contacts work by 
storing the updated contacts in a work queue, and only updating xDB
after all of the contacts are read. This reduces the number of times
you have to explicitly write to xDB, which may improve performance.

The full contact synchronization process uses this same approach. 
It only updates xDB after the contacts are synchronized, and the 
marketing lists are synchronized. Again, the benefit is that, in 
general, the fewer times you have to write to xDB, the better the 
performance on your Sitecore servers.

.. note:: 

  This pipeline batch uses the same *pipelines* as the 
  :doc:`../crm-contact-sync/index` and :doc:`../crm-marketinglist-sync/index`.
  Any changes made to those pipelines will affect the other
  pipeline batches that use the same pipelines.  

