Disable Value Mapping
=============================

Existing *value mappings* can be disabled or deleted. However, disabling a
value mapping is often preferable to deleting a value mapping because
you may, in the future, decide that you want the value mapping after all.

#. Navigate to your *tenant*.
#. Navigate to **Value Mapping Sets > xDB Contact to CRM Contact**.
#. Select the value mapping item you want to disable.
#. For the field **Enabled**, untick the box.
#. Save the item.

This setting will take affect the next time the synchronization process runs.

.. note::
  This setting will affect the xDB contacts are read in the future.
  Values that are already mapped will not be removed from CRM.
