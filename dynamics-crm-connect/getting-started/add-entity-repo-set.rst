Add Entity Repository Set
==========================

An *entity repository set* is the component that controls the interactions with
the CRM. You must create a new entity repository set in order to read data
from, and write data to, the CRM.

The entity repository set is the object that uses the connection string described
in :doc:`Add CRM Connection String </getting-started/add-crm-connection-string>`.

#. Navigate to your tenant.
#. Navigate to  **Tenant Settings > Dynamics CRM > Repository Sets**.
#. Add the following item:

    +--------------+---------------------------------------+
    | **Template** | XRM Client Entity Repository Set      |
    +--------------+---------------------------------------+
    | **Name**     | mycrm                                 |
    +--------------+---------------------------------------+

    .. tip::
      It is recommended that the name describe your CRM server.

#.	In the field **Connection string name**, enter the connection string name for the Dynamics CRM server.
#.	Save the item.

.. hint::
    
    Use the button **Test Connection** to test the connection. A message will indicate whether or not a connection could be made.

    .. image:: _static/test-connection.png

    |

    If an error message is displayed, the Sitecore log may contain a
    more detailed description of the problem.
