Configure Endpoint
=====================

An *endpoint* represents a system you can read data from or write data to. The
endpoint that represents your CRM system is already created. But it is not
connected to an *entity repository set*.

#.	Navigate to your *tenant*.
#.  Navigate to **Endpoints > Providers > Dynamics CRM > Dynamics CRM Entity Endpoint**.
#.	In the field **Entity repository set**, select the entity repository set you created in :doc:`Add Entity Repository Set </getting-started/add-entity-repo-set>`.
#.	Save the item.

.. note::
  It may seem redundant to have both an entity repository set and
  an endpoint. Why isn't it enough to have just an endpoint?

  Consider the configuration you just did. You had to create an entity
  repository set and then assign the entity repository set to an
  endpoint. Imagine how this would be different if there was no
  entity repository set, only an endpoint.

  The endpoint is used in many places within the tenant. If you look
  at the list of items that refer to the endpoint you will see that
  there are 6 items that reference the endpoint:

  Without the entity repository set, if you ever needed to change the
  endpoint (for example, if you wanted to change from using a
  connection string to using a connection string name), you would
  need to create a new endpoint and then change those 6 items.
  Instead, all you need to do is entity repository set on the
  endpoint. You are able to leave those 6 items untouched.

  .. image:: _static/configure-endpoint.png

