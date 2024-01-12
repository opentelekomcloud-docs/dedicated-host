:original_name: deh_05_0903.html

.. _deh_05_0903:

Querying Tags of a DeH
======================

Function
--------

-  This API is used to query tags of a DeH.

-  Tag Management Service (TMS) uses this API to query all tags of a DeH.

URI
---

GET /v1.0/{project_id}/dedicated-host-tags/{dedicated_host_id}/tags

:ref:`Table 1 <deh_05_0903__table291625114015>` describes the parameters.

.. _deh_05_0903__table291625114015:

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
   |                   |                 |                 | You can obtain the value from the DeH console or using the API in :ref:`Querying DeHs <deh_02_0020>`.                                                               |
   +-------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Request
-------

None

Response
--------

.. table:: **Table 2** Response parameters

   +-----------------------+-----------------------+---------------------------------------------------------------------+
   | Parameter             | Type                  | Description                                                         |
   +=======================+=======================+=====================================================================+
   | tags                  | Array of objects      | Specifies the list of tags.                                         |
   |                       |                       |                                                                     |
   |                       |                       | For details, see :ref:`Table 3 <deh_05_0903__table20667652184712>`. |
   +-----------------------+-----------------------+---------------------------------------------------------------------+

.. _deh_05_0903__table20667652184712:

.. table:: **Table 3** **tag** field description

   ========= ====== ========================
   Parameter Type   Description
   ========= ====== ========================
   key       String Specifies the tag key.
   value     String Specifies the tag value.
   ========= ====== ========================

Example Request
---------------

.. code-block:: text

   GET https://{Endpoint}/v1.0/9c53a566cb3443ab910cf0daebca90c4/dedicated-host-tags/74259164-e63a-4ad9-9c77-a1bd2c9aa187/tags

Example Response
----------------

.. code-block::

   {
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

Status Code
-----------

See :ref:`Status Codes <deh_02_0016>`.
