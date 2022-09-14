:original_name: deh_05_0801.html

.. _deh_05_0801:

Querying API Versions
=====================

Function
--------

This API is used to query all API versions available to the DeH service.

URI
---

GET /

Request
-------

-  Request parameters

   None

-  Example request

   .. code-block:: text

      GET /

Response
--------

-  Response parameters

   .. table:: **Table 1** Response parameters

      ========= ================ ===========================
      Parameter Type             Description
      ========= ================ ===========================
      versions  Array of objects Specifies the API versions.
      ========= ================ ===========================

   .. table:: **Table 2** **versions** field description

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
      | updated               | String                | Specifies the API version update time, which must be UTC time.                                                                                                                                               |
      +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | version               | String                | If the APIs of this version support micro-versions, set this parameter to the maximum micro-version supported. If not, leave this parameter blank.                                                           |
      +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

   .. table:: **Table 3** **links** field description

      ========= ====== =====================================
      Parameter Type   Description
      ========= ====== =====================================
      href      String Specifies the URL of the API version.
      rel       String Specifies the API URL dependency.
      ========= ====== =====================================

-  Example response

   .. code-block::

      {
          "versions": [
              {
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
          ]
      }

Status Code
-----------

See :ref:`Status Codes <deh_02_0016>`.
