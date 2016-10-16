Simple Synchronization
=======================================

No custom development is needed to read entities from CRM and to represent 
those entities in Sitecore, provided Sitecore already has a data structure 
that can be used to store the data. In this example, we are reading entities 
from CRM (accounts) and are representing those entities in an existing data 
structure (Sitecore items). 

.. note:: 

    Associating an xDB contact with a CRM account will require custom code, 
    because it is doing more than reading entities (it is reading a 
    relationship between the contact and account entities) and is storing 
    that data in a data structure that must be created (a custom contact facet). 
    :doc:`../complex-synchronization/index` covers how to implement this.

.. toctree::
    :name: simple-sync-steps
    :caption: Steps
    :numbered:
    :titlesonly:

    confirm-crm-privileges
    add-templates-for-crm-entity-data
    add-entity-repository
    add-value-accessor-set-for-crm-entity
    add-value-accessor-set-for-sitecore-item
    add-value-mapping-set
    add-pipelines-to-handle-crm-entity
    add-pipelines-to-read-crm-entities
    add-pipeline-batch
    run-pipeline-batch
