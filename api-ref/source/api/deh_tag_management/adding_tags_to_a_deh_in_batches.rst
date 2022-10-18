:original_name: deh_05_0901.html

.. _deh_05_0901:

Adding Tags to a DeH in Batches
===============================

Function
--------

-  This API is used to add tags to a specified DeH in batches.

-  Tag Management Service (TMS) uses this API to batch add tags to a DeH.

**Constraint**
--------------

-  A DeH allows a maximum of 10 tags.

-  This API is idempotent.

   During tag creation, if a tag exists (both the key and value are the same as those of an existing tag), the tag is successfully processed by default.

-  A new tag will overwrite the original one if their keys are the same and values are different.

URI
---

POST /v1.0/{project_id}/dedicated-host-tags/{dedicated_host_id}/tags/action

:ref:`Table 1 <deh_05_0901__table1913014815289>` describes the parameters.

.. _deh_05_0901__table1913014815289:

.. table:: **Table 1** Parameters description

   +-------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter         | Type            | Mandatory       | Description                                                                                                                                                         |
   +===================+=================+=================+=====================================================================================================================================================================+
   | project_id        | String          | Yes             | Specifies the project ID.                                                                                                                                           |
   |                   |                 |                 |                                                                                                                                                                     |
   |                   |                 |                 | For details about how to obtain the project ID, see `Obtaining Required Information <https://docs.otc.t-systems.com/en-us/api/apiug/apig-en-api-180328009.html>`__. |
   +-------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | dedicated_host_id | String          | Yes             | Specifies the DeH ID.                                                                                                                                               |
   |                   |                 |                 |                                                                                                                                                                     |
   |                   |                 |                 | You can obtain the DeH ID from the DeH console or using the :ref:`Querying DeHs <deh_02_0020>` API.                                                                 |
   +-------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Request
-------

-  Request parameters

   .. table:: **Table 2** Request parameters

      +-----------+------------------+-----------+--------------------------------------------------------------------------------------------------------------------------+
      | Parameter | Type             | Mandatory | Description                                                                                                              |
      +===========+==================+===========+==========================================================================================================================+
      | tags      | Array of objects | Yes       | Specifies the tag list.                                                                                                  |
      +-----------+------------------+-----------+--------------------------------------------------------------------------------------------------------------------------+
      | action    | String           | Yes       | Specifies the operation. Only lowercase letters are supported. For example, **create** indicates the creation operation. |
      +-----------+------------------+-----------+--------------------------------------------------------------------------------------------------------------------------+

   .. table:: **Table 3** **resource_tag** field description

      +-----------------+-----------------+-----------------+----------------------------------------------------------------------+
      | Parameter       | Type            | Mandatory       | Description                                                          |
      +=================+=================+=================+======================================================================+
      | key             | String          | Yes             | Specifies the tag key.                                               |
      |                 |                 |                 |                                                                      |
      |                 |                 |                 | -  It contains a maximum of 36 Unicode characters.                   |
      |                 |                 |                 | -  The value cannot be empty.                                        |
      |                 |                 |                 | -  It cannot contain the following ASCII characters: ``=*<>\|/,``    |
      |                 |                 |                 | -  It can contain letters, digits, hyphens (-), and underscores (_). |
      +-----------------+-----------------+-----------------+----------------------------------------------------------------------+
      | value           | String          | Yes             | Specifies the tag value.                                             |
      |                 |                 |                 |                                                                      |
      |                 |                 |                 | -  It contains a maximum of 43 Unicode characters.                   |
      |                 |                 |                 | -  It cannot contain the following ASCII characters: ``=*<>\|/,``    |
      |                 |                 |                 | -  It can contain letters, digits, hyphens (-), and underscores (_). |
      +-----------------+-----------------+-----------------+----------------------------------------------------------------------+

-  Example request

   .. code-block:: text

      POST https://{Endpoint}/v1.0/9c53a566cb3443ab910cf0daebca90c4/dedicated-host-tags/74259164-e63a-4ad9-9c77-a1bd2c9aa187/tags/action

   .. code-block::

      {
          "action": "create",
          "tags": [
              {
                  "key": "key1",
                  "value": "value1"
              },
              {
                  "key": "key2",
                  "value": "value2"
              }
          ]
      }

Response
--------

N/A

Status Code
-----------

See :ref:`Status Codes <deh_02_0016>`.
