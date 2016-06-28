Default Field Mappings
----------------------

By default, the campaign synchronization process maps the following values
from the CRM campaign to the Sitecore campaign.

These mappings are defined in the *value mapping set* named
**CRM Campaign to Sitecore Campaign**.

+-----------------+-----------------------+------------------------------------+
| CRM Campaign    | Sitecore Campaign     | Description                        |
+=================+=======================+====================================+
| ``campaignid``  | ``Id``                | Unique identifier for the          |
|                 |                       | campaign in the CRM                |
+-----------------+-----------------------+------------------------------------+
| ``name``        | ``Name``              | Campaign name                      |
+-----------------+-----------------------+------------------------------------+
| ``actualstart`` | ``StartDate``         | Campaign start date                |
+-----------------+-----------------------+------------------------------------+
| ``actualend``   | ``EndDate``           | Campaign end date                  |
+-----------------+-----------------------+------------------------------------+
| ``createdon``   | ``CreatedDate``       | Date the campaign was created      |
|                 |                       | in the CRM                         |
+-----------------+-----------------------+------------------------------------+
| ``modifiedon``  | ``LastModifiedDate``  | Ddate the campaign was last        |
|                 |                       | modified in the CRM                |
+-----------------+-----------------------+------------------------------------+
| ``description`` | ``Description``       | Campaign description               |
+-----------------+-----------------------+------------------------------------+
