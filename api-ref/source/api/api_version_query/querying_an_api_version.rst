:original_name: deh_05_0802.html

.. _deh_05_0802:

Querying an API Version
=======================

Function
--------

This API is used to query a specified API version.

URI
---

GET /{api_version}

:ref:`Table 1 <deh_05_0802__table46110007>` describes the parameters.

.. _deh_05_0802__table46110007:

.. table:: **Table 1** Parameters description

   =========== ========= =============================================
   Parameter   Mandatory Description
   =========== ========= =============================================
   api_version Yes       Specifies the API version, for example, v1.0.
   =========== ========= =============================================

Request
-------

-  Request parameters

   None

-  Example request

   .. code-block:: text

      GET /v1.0

Response
--------

-  Response parameters

   .. table:: **Table 2** Response parameters

      ========= ====== ====================================================
      Parameter Type   Description
      ========= ====== ====================================================
      version   Object Specifies information about a specified API version.
      ========= ====== ====================================================

   .. table:: **Table 3** **version** field description

      +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter             | Type                  | Description                                                                                                                                                                                                  |
      +=======================+=======================+==============================================================================================================================================================================================================+
      | id                    | String                | Specifies the ID of the API version.                                                                                                                                                                         |
      +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | links                 | Array of objects      | Specifies the URL of the API version.                                                                                                                                                                        |
      +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | min_version           | String                | Specifies the microversion. If the APIs of this version support micro-versions, set this parameter to the supported minimum micro-version. If the microversion is not supported, leave this parameter blank. |
      +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | status                | String                | Specifies the API version status.                                                                                                                                                                            |
      |                       |                       |                                                                                                                                                                                                              |
      |                       |                       | -  **CURRENT**: indicates a primary version.                                                                                                                                                                 |
      |                       |                       | -  **SUPPORTED**: indicates an earlier version which is still supported.                                                                                                                                     |
      |                       |                       | -  **DEPRECATED**: indicates a deprecated version which may be deleted later.                                                                                                                                |
      +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | updated               | String                | Specifies the API version update time.                                                                                                                                                                       |
      +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | version               | String                | If the APIs of this version support micro-versions, set this parameter to the maximum micro-version supported. If not, leave this parameter blank.                                                           |
      +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

   .. table:: **Table 4** **links** field description

      ========= ====== =====================================
      Parameter Type   Description
      ========= ====== =====================================
      href      String Specifies the URL of the API version.
      rel       String Specifies the API URL dependency.
      ========= ====== =====================================

-  Example response

   .. code-block::

      {
          "version": {
              "id": "v1.0",
              "links": [
                  {
                      "href": "https//deh.xxx.com/v1.0/",
                      "rel": "self"
                  }
              ],
              "min_version": "",
              "status": "SUPPORTED",
              "updated": "2016-12-01T11:33:21Z",
              "version": ""
          }
      }

Status Code
-----------

See :ref:`Status Codes <deh_02_0016>`.
