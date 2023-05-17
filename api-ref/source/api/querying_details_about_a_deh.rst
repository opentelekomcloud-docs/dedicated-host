:original_name: deh_02_0021.html

.. _deh_02_0021:

Querying Details About a DeH
============================

Function
--------

This API is used to query details about a DeH.

URI
---

GET /v1.0/{project_id}/dedicated-hosts/{dedicated_host_id}

:ref:`Table 1 <deh_02_0021__table572214121015>` describes the parameters.

.. _deh_02_0021__table572214121015:

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

   None

-  Example request

   .. code-block:: text

      GET https://{Endpoint}/v1.0/9c53a566cb3443ab910cf0daebca90c4/dedicated-hosts/ab910cf0daebca90c4001

Response
--------

-  Response parameters

   .. table:: **Table 2** Response parameters

      +-----------------+-----------------+-----------------+----------------------------------------------------------------+
      | Parameter       | In              | Type            | Description                                                    |
      +=================+=================+=================+================================================================+
      | dedicated_host  | body            | Object          | Specifies the DeH object.                                      |
      |                 |                 |                 |                                                                |
      |                 |                 |                 | For details, see :ref:`Table 1 <deh_02_0018__dedicated_host>`. |
      +-----------------+-----------------+-----------------+----------------------------------------------------------------+

-  Example response

   .. code-block::

      {
          "dedicated_host": {
              "dedicated_host_id": "ab910cf0daebca90c4001",
              "name": "win_2008 servers",
              "auto_placement": "off",
              "availability_zone": "az1",
              "host_properties": {
                  "vcpus": 36,
                  "cores": 12,
                  "sockets": 2,
                  "memory": 1073741824,
                  "host_type": "h1",
                  "host_type_name": "High performance",
                  "available_instance_capacities": [
                      {
                          "flavor": "h1.large"
                      },
                      {
                          "flavor": "h1.2large"
                      },
                      {
                          "flavor": "h1.4large"
                      },
                      {
                          "flavor": "h1.8large"
                      }
                  ]
              },
              "state": "available",
              "project_id": "9c53a566cb3443ab910cf0daebca90c4",
              "available_vcpus": 20,
              "available_memory": 1073201821,
              "instance_total": 2,
              "allocated_at": "2016-10-10T14:35:47Z",
              "released_at": null,
              "instance_uuids": [
                  "erf5th66cb3443ab912ff0daebca3456",
                  "23457h66cb3443ab912ff0daebcaer45"
              ]
          }
      }

Status Code
-----------

See :ref:`Status Codes <deh_02_0016>`.
