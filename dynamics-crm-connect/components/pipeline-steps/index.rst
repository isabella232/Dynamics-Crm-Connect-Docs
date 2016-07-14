.. include:: ../../../common/stub-topic.txt

|stub-icon| Pipeline Steps
=======================================

A *pipeline step* represents a unit of work that is performed when 
a *pipeline* runs. Configuring pipeline steps, and ensuring those
steps are in the correct order, is one of the most important parts
of configuring a synchronization process.

At runtime, parameters are made available to a pipeline step through
*pipeline context plugins*. Knowing which plugins provide input to
a pipeline step - and which plugins are provide output from a 
pipeline step - is critical in order to be able to use a pipeline 
step.  

Templates
-------------

.. toctree::
    :titlesonly:
    :maxdepth: 2

    framework/index
    sitecore/index
    crm/index
        
    