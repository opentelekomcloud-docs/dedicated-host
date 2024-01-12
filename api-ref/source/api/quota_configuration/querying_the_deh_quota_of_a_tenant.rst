:original_name: deh_02_0028.html

.. _deh_02_0028:

Querying the DeH Quota of a Tenant
==================================

Function
--------

This API is used to query the DeH quota of a tenant.

URI
---

GET /v1.0/{project_id}/quota-sets/{tenant_id}

:ref:`Table 1 <deh_02_0028__table291625114015>` describes the parameters.

.. _deh_02_0028__table291625114015:

.. table:: **Table 1** Parameters description

   +-----------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter       | Type            | Mandatory       | Description                                                                                                                                                         |
   +=================+=================+=================+=====================================================================================================================================================================+
   | project_id      | String          | Yes             | Specifies the project ID.                                                                                                                                           |
   |                 |                 |                 |                                                                                                                                                                     |
   |                 |                 |                 | For details about how to obtain the project ID, see `Obtaining Required Information <https://docs.otc.t-systems.com/en-us/api/apiug/apig-en-api-180328009.html>`__. |
   +-----------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | tenant_id       | String          | Yes             | Specifies the tenant ID.                                                                                                                                            |
   |                 |                 |                 |                                                                                                                                                                     |
   |                 |                 |                 | You can obtain the value from the DeH console or using the API in :ref:`Querying DeHs <deh_02_0020>`.                                                               |
   +-----------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Request
-------

You can add the **resource** parameter to the URI. For example:

**/v1.0/{project_id}/quota-sets/{tenant_id}?resource={resource}**

.. table:: **Table 2** Request parameters

   ========= ======== ====== ========= ============================
   Parameter Location Type   Mandatory Description
   ========= ======== ====== ========= ============================
   resource  query    String No        Specifies the resource type.
   ========= ======== ====== ========= ============================

Response
--------

.. table:: **Table 3** Response parameters

   +-----------------------+-----------------------+-------------------------------------------------------------------+
   | Parameter             | Type                  | Description                                                       |
   +=======================+=======================+===================================================================+
   | quota_set             | Array of objects      | Specifies the quota set of a DeH.                                 |
   |                       |                       |                                                                   |
   |                       |                       | For details, see :ref:`Table 4 <deh_02_0028__table379913618427>`. |
   +-----------------------+-----------------------+-------------------------------------------------------------------+

.. _deh_02_0028__table379913618427:

.. table:: **Table 4** **quota_set** field description

   +-----------------------+-----------------------+----------------------------------------------------------+
   | Parameter             | Type                  | Description                                              |
   +=======================+=======================+==========================================================+
   | resource              | String                | Specifies the resource type.                             |
   +-----------------------+-----------------------+----------------------------------------------------------+
   | hard_limit            | Integer               | Specifies the quota limit.                               |
   |                       |                       |                                                          |
   |                       |                       | **-1** indicates that the resource quota is not limited. |
   +-----------------------+-----------------------+----------------------------------------------------------+
   | used                  | Integer               | Specifies the used amount of the quota.                  |
   +-----------------------+-----------------------+----------------------------------------------------------+

Example Request
---------------

.. code-block:: text

   GET https://{Endpoint}/v1.0/9c53a566cb3443ab910cf0daebca90c4/quota-sets/45df5566cb3443ab910cf0daebcapoi8

Example Response
----------------

.. code-block::

   {
    "quota_set": [
     {
      "used": 0,
      "resource": "c4",
      "hard_limit": 5
     },
     {
      "used": 0,
      "resource": "m4",
      "hard_limit": 5
     }]
   }

Status Code
-----------

See :ref:`Status Codes <deh_02_0016>`.
