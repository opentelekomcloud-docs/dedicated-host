:original_name: deh_02_0025.html

.. _deh_02_0025:

Querying Available DeH Types
============================

Function
--------

This API is used to query available DeH types in an AZ.

URI
---

Get /v1.0/{project_id}/availability-zone/{availability_zone}/dedicated-host-types

:ref:`Table 1 <deh_02_0025__table572214121015>` describes the parameters.

.. _deh_02_0025__table572214121015:

.. table:: **Table 1** Parameters description

   +-------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter         | Type            | Mandatory       | Description                                                                                                                                                         |
   +===================+=================+=================+=====================================================================================================================================================================+
   | project_id        | String          | Yes             | Specifies the project ID.                                                                                                                                           |
   |                   |                 |                 |                                                                                                                                                                     |
   |                   |                 |                 | For details about how to obtain the project ID, see `Obtaining Required Information <https://docs.otc.t-systems.com/en-us/api/apiug/apig-en-api-180328009.html>`__. |
   +-------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | availability_zone | String          | Yes             | Specifies the AZ.                                                                                                                                                   |
   +-------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Request
-------

None

Response
--------

.. table:: **Table 2** Response parameters

   +----------------------+------+------------------+-------------------------------------------------------------------------------------------------------+
   | Parameter            | In   | Type             | Description                                                                                           |
   +======================+======+==================+=======================================================================================================+
   | dedicated_host_types | body | Array of objects | Specifies the available DeH types. For details, see :ref:`Table 3 <deh_02_0025__table1790111341615>`. |
   +----------------------+------+------------------+-------------------------------------------------------------------------------------------------------+

.. _deh_02_0025__table1790111341615:

.. table:: **Table 3** **dedicated_host_types** field description

   ============== ====== ===================================
   Parameter      Type   Description
   ============== ====== ===================================
   host_type      String Specifies the DeH type.
   host_type_name String Specifies the name of the DeH type.
   ============== ====== ===================================

Example Request
---------------

.. code-block:: text

   GET https://{Endpoint}/v1.0/9c53a566cb3443ab910cf0daebca90c4/availability-zone/az1/dedicated-host-types

Example Response
----------------

.. code-block::

   {
    "dedicated_host_types": [
     {
      "host_type": "c4",
      "host_type_name": "dedicated_general_purpose"
     },
     {
      "host_type": "m4",
      "host_type_name": "memory_optimized"
     }
    ]
   }

Status Code
-----------

See :ref:`Status Codes <deh_02_0016>`.
