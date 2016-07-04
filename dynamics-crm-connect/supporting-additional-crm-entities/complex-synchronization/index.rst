.. _complex-sync-for-crm-entities:

Complex Synchronization
=======================================

In :ref:`complex-sync-for-crm-entities`, you configured a synchronization 
process that represents CRM accounts as Sitecore items. The real power of 
having access to CRM accounts is when you are able to associate an xDB 
contact with a CRM account.

Some custom development is required. By default, Sitecore does not provide 
a way to store account information and to associate an xDB contact with the
account. And since Sitecore does not store this information, Sitecore is 
not aware of this information.

Custom development is required for the following parts of the solution:

* Read the CRM contacts that are associated with an account from CRM
* Associate an xDB contact with an account
* Search for xDB contacts by account

In order to keep the instructions as simple as possible, a specific example 
is used to describe this configuration:

* This example builds on the example covered in :ref:`complex-sync-for-crm-entities`.
* Each CRM contact is a part of an account. You want to associate the 
Sitecore contact with the CRM account by setting a value on a custom 
contact facet.

.. note:: 
    The relationship between contacts and accounts is similar to the 
    relationship between contacts and marketing lists. The difference 
    is that a contact is associated with a single account, while a 
    contact may be associated with multiple marketing lists.

Steps
------

.. toctree::
    :numbered:
    :titlesonly:

    extend-dynamics-crm-contact-facet
    extend-indexable-contact
    extend-contact-aggregator
    
