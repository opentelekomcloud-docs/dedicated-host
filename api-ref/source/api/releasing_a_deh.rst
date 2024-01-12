:original_name: deh_02_0024.html

.. _deh_02_0024:

Releasing a DeH
===============

Function
--------

This API is used to release a DeH.

Constraints
-----------

A DeH accommodating ECSs cannot be released.

URI
---

DELETE /v1.0/{project_id}/dedicated-hosts/{dedicated_host_id}

:ref:`Table 1 <deh_02_0024__table572214121015>` describes the parameters.

.. _deh_02_0024__table572214121015:

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

None

Example Request
---------------

.. code-block:: text

   DELETE https://{Endpoint}/v1.0/9c53a566cb3443ab910cf0daebca90c4/dedicated-hosts/74259164-e63a-4ad9-9c77-a1bd2c9aa187

Example Response
----------------

.. code-block::

   Http Response Code: 204

Status Code
-----------

.. table:: **Table 2** Returned error codes

   ============ ============================================
   Error Code   Description
   ============ ============================================
   409 Conflict A DeH accommodating ECSs cannot be released.
   ============ ============================================

For more status codes, see :ref:`Status Codes <deh_02_0016>`.
