:original_name: deh_02_0022.html

.. _deh_02_0022:

Querying ECSs on a DeH
======================

Function
--------

This API is used to query information about deployed ECSs on a DeH.

URI
---

GET /v1.0/{project_id}/dedicated-hosts/{dedicated_host_id}/servers

:ref:`Table 1 <deh_02_0022__table572214121015>` describes the parameters.

.. _deh_02_0022__table572214121015:

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

.. table:: **Table 2** Request parameters

   +-----------+-------+--------+-----------+----------------------------------------------------------------------------------------------------------------------------+
   | Parameter | In    | Type   | Mandatory | Description                                                                                                                |
   +===========+=======+========+===========+============================================================================================================================+
   | limit     | query | String | No        | Specifies the number of records displayed per page.                                                                        |
   +-----------+-------+--------+-----------+----------------------------------------------------------------------------------------------------------------------------+
   | marker    | query | String | No        | Specifies the ID of the last record on the previous page. If the **marker** value is invalid, status code 400 is returned. |
   +-----------+-------+--------+-----------+----------------------------------------------------------------------------------------------------------------------------+

Response
--------

.. table:: **Table 3** Response parameters

   +-----------+------+------------------+-------------------------------------------------------------------------------------------------+
   | Parameter | In   | Type             | Description                                                                                     |
   +===========+======+==================+=================================================================================================+
   | servers   | body | Array of objects | Specifies the server object. For details, see :ref:`Table 4 <deh_02_0022__table1296218281715>`. |
   +-----------+------+------------------+-------------------------------------------------------------------------------------------------+

.. _deh_02_0022__table1296218281715:

.. table:: **Table 4** **servers** field description

   +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter             | Type                  | Description                                                                                                                                                                                                                                                              |
   +=======================+=======================+==========================================================================================================================================================================================================================================================================+
   | addresses             | Map<String, Object>   | Specifies the network addresses of an ECS.                                                                                                                                                                                                                               |
   |                       |                       |                                                                                                                                                                                                                                                                          |
   |                       |                       | The structure is Map<String, Object>.                                                                                                                                                                                                                                    |
   |                       |                       |                                                                                                                                                                                                                                                                          |
   |                       |                       | -  The key indicates the VPC subnet ID.                                                                                                                                                                                                                                  |
   |                       |                       | -  The value indicates the network attributes specified in :ref:`Table 5 <deh_02_0022__table08001321809>`.                                                                                                                                                               |
   +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | created               | String                | Specifies the time when the ECS was created.                                                                                                                                                                                                                             |
   +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | flavor                | Object                | Specifies the ECS flavor. For details, see :ref:`Table 6 <deh_02_0022__table13112134716015>`.                                                                                                                                                                            |
   +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | id                    | String                | Specifies the ECS ID in UUID format.                                                                                                                                                                                                                                     |
   +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | name                  | String                | Specifies the ECS name.                                                                                                                                                                                                                                                  |
   +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | status                | String                | Specifies the ECS status.                                                                                                                                                                                                                                                |
   |                       |                       |                                                                                                                                                                                                                                                                          |
   |                       |                       | Options:                                                                                                                                                                                                                                                                 |
   |                       |                       |                                                                                                                                                                                                                                                                          |
   |                       |                       | **ACTIVE**, **BUILD**, **DELETED**, **ERROR**, **HARD_REBOOT**, **MIGRATING**, **PASSWORD**, **PAUSED**, **REBOOT**, **REBUILD**, **RESIZE**, **REVERT_RESIZE**, **SHUTOFF**, **SHELVED**, **SHELVED_OFFLOADED**, **SOFT_DELETED**, **SUSPENDED**, and **VERIFY_RESIZE** |
   +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | tenant_id             | String                | Specifies the ECS tenant ID in UUID format.                                                                                                                                                                                                                              |
   +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | updated               | String                | Specifies the time when the ECS was updated last time.                                                                                                                                                                                                                   |
   +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | user_id               | String                | Specifies the ID of the user who has created the ECS. The value is in UUID format.                                                                                                                                                                                       |
   +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | task_state            | String                | Specifies the ECS task status.                                                                                                                                                                                                                                           |
   +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | image                 | Object                | Specifies the ECS image. For details, see :ref:`Table 7 <deh_02_0022__table92838016115>`.                                                                                                                                                                                |
   +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | metadata              | Object                | Specifies the ECS metadata. For details, see :ref:`Table 8 <deh_02_0022__table74181471712>`.                                                                                                                                                                             |
   +-----------------------+-----------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

.. _deh_02_0022__table08001321809:

.. table:: **Table 5** Data structure of the network to which an ECS accesses

   +-------------------------+-----------------------+-----------------------------------------------------------------------------------------+
   | Parameter               | Type                  | Description                                                                             |
   +=========================+=======================+=========================================================================================+
   | addr                    | String                | Specifies the IP address.                                                               |
   +-------------------------+-----------------------+-----------------------------------------------------------------------------------------+
   | version                 | Integer               | Specifies the type of an IP address. The value of this parameter can be **4** or **6**. |
   |                         |                       |                                                                                         |
   |                         |                       | -  **4**: The type of the IP address is IPv4.                                           |
   |                         |                       | -  **6**: The type of the IP address is IPv6.                                           |
   +-------------------------+-----------------------+-----------------------------------------------------------------------------------------+
   | OS-EXT-IPS-MAC:mac_addr | String                | Specifies the MAC address. This is an extended attribute.                               |
   +-------------------------+-----------------------+-----------------------------------------------------------------------------------------+
   | OS-EXT-IPS:type         | String                | Specifies the IP address assignment mode. This is an extended attribute.                |
   +-------------------------+-----------------------+-----------------------------------------------------------------------------------------+

.. _deh_02_0022__table13112134716015:

.. table:: **Table 6** **flavor** field description

   ========= ====== ========================
   Parameter Type   Description
   ========= ====== ========================
   id        String Specifies the flavor ID.
   ========= ====== ========================

.. _deh_02_0022__table92838016115:

.. table:: **Table 7** **image** field description

   ========= ====== =========================
   Parameter Type   Description
   ========= ====== =========================
   id        String Specifies the image UUID.
   ========= ====== =========================

.. _deh_02_0022__table74181471712:

.. table:: **Table 8** **metadata** field description

   ========= ====== ======================
   Parameter Type   Description
   ========= ====== ======================
   os_type   String Specifies the OS type.
   ========= ====== ======================

Example Request
---------------

Query ECSs on the DeH **ab910cf0daebca90c4001**.

.. code-block:: text

   GET https://{Endpoint}/v1.0/9c53a566cb3443ab910cf0daebca90c4/dedicated-hosts/ab910cf0daebca90c4001/servers

Example Response
----------------

.. code-block::

   {
       "servers": [
           {
             "addresses": {
                   "68269e6e-4a27-441b-8029-35373ad50bd9": [
                       {
                           "addr": "192.168.0.3",
                           "version": 4,
                           "OS-EXT-IPS-MAC:mac_addr": "fa:16:3e:1b:35:78",
                           "OS-EXT-IPS:type": "fixed"
                       }
                   ]
               },
               "created": "2012-09-07T16:56:37Z",
               "flavor": {
                   "id": "1"
               },
               "id": "05184ba3-00ba-4fbc-b7a2-03b62b884931",
               "metadata": {
                   "os_type": "Linux"
               },
               "name": "new-server-test",
               "status": "ACTIVE",
               "tenant_id": "a90b2728805d4240a72cc2eeb4e1244d",
               "updated": "2012-09-07T16:56:37Z",
               "user_id": "fake",
               "task_state": "",
               "image": {
                   "id": "1ce5800a-e487-4c1b-b264-3353a39e2b4b"
               }
           }
       ]
   }

Status Code
-----------

See :ref:`Status Codes <deh_02_0016>`.
