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

-  Request parameters

   None

-  Example request

   .. code-block:: text

      GET https://{Endpoint}/v1.0/9c53a566cb3443ab910cf0daebca90c4/availability-zone/az1/dedicated-host-types

Response
--------

-  Response parameters

   .. table:: **Table 2** Response parameters

      +----------------------+------+------------------+-------------------------------------+
      | Parameter            | In   | Type             | Description                         |
      +======================+======+==================+=====================================+
      | dedicated_host_types | body | Array of objects | Specifies the available DeH types.  |
      +----------------------+------+------------------+-------------------------------------+
      | host_type            | body | String           | Specifies the DeH type.             |
      +----------------------+------+------------------+-------------------------------------+
      | host_type_name       | body | String           | Specifies the name of the DeH type. |
      +----------------------+------+------------------+-------------------------------------+

-  Example response

   .. code-block::

      {
          "dedicated_host_types": [
              {
                  "host_type": "General",
                  "host_type_name": "General Computing"
              },
              {
                  "host_type": "m1",
                  "host_type_name": "Memory-optimized"
              },
              {
                  "host_type": "h2",
                  "host_type_name": "High performance"
              },
              {
                  "host_type": "d1",
                  "host_type_name": "Disk intensive"
              }
          ]
      }

Status Code
-----------

See :ref:`Status Codes <deh_02_0016>`.
