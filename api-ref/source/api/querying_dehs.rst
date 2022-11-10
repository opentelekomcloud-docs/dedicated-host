:original_name: deh_02_0020.html

.. _deh_02_0020:

Querying DeHs
=============

Function
--------

This API is used to query the DeH list.

URI
---

GET /v1.0/{project_id}/dedicated-hosts

:ref:`Table 1 <deh_02_0020__table572214121015>` describes the parameters.

.. _deh_02_0020__table572214121015:

.. table:: **Table 1** Parameters description

   +-----------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter       | Type            | Mandatory       | Description                                                                                                                                                         |
   +=================+=================+=================+=====================================================================================================================================================================+
   | project_id      | String          | Yes             | Specifies the project ID.                                                                                                                                           |
   |                 |                 |                 |                                                                                                                                                                     |
   |                 |                 |                 | For details about how to obtain the project ID, see `Obtaining Required Information <https://docs.otc.t-systems.com/en-us/api/apiug/apig-en-api-180328009.html>`__. |
   +-----------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Request
-------

-  Request parameters

   You can add parameters **host_type**, **host_type_name**, **flavor**, **dedicated_host_id**, **state**, **tenant**, **availability_zone**, **name**, **limit**, **marker**, **tags**, **instance_uuid**, **released_at**, or **changes-since** to the URI to filter the search result,

   for example, **/v1.0/{project_id}/dedicated-hosts?host_type={host_type}&state={state}**.

   .. table:: **Table 2** Request parameters

      +-------------------+-------------+-------------+-------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter         | In          | Type        | Mandatory   | Description                                                                                                                                                                           |
      +===================+=============+=============+=============+=======================================================================================================================================================================================+
      | dedicated_host_id | query       | String      | No          | Specifies the DeH ID.                                                                                                                                                                 |
      +-------------------+-------------+-------------+-------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | name              | query       | String      | No          | Specifies the DeH name.                                                                                                                                                               |
      +-------------------+-------------+-------------+-------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | host_type         | query       | String      | No          | Specifies the DeH type.                                                                                                                                                               |
      +-------------------+-------------+-------------+-------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | host_type_name    | query       | String      | No          | Specifies the name of the DeH type.                                                                                                                                                   |
      +-------------------+-------------+-------------+-------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | flavor            | query       | String      | No          | Specifies the flavor ID.                                                                                                                                                              |
      +-------------------+-------------+-------------+-------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | state             | query       | String      | No          | Specifies the DeH status.                                                                                                                                                             |
      |                   |             |             |             |                                                                                                                                                                                       |
      |                   |             |             |             | The value can be **available**, **fault**, or **released**.                                                                                                                           |
      +-------------------+-------------+-------------+-------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | tenant            | query       | String      | No          | The value can be a tenant ID or **all**.                                                                                                                                              |
      |                   |             |             |             |                                                                                                                                                                                       |
      |                   |             |             |             | Only users with the DeH administrator permissions can specify this parameter.                                                                                                         |
      +-------------------+-------------+-------------+-------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | availability_zone | query       | String      | No          | Specifies the AZ to which the DeH belongs.                                                                                                                                            |
      +-------------------+-------------+-------------+-------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | limit             | query       | String      | No          | Specifies the number of records displayed per page.                                                                                                                                   |
      +-------------------+-------------+-------------+-------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | marker            | query       | String      | No          | Specifies the ID of the last record on the previous page. If the **marker** value is invalid, status code 400 is returned.                                                            |
      +-------------------+-------------+-------------+-------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | tags              | query       | String      | No          | Specifies the DeH tags.                                                                                                                                                               |
      +-------------------+-------------+-------------+-------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | instance_uuid     | query       | String      | No          | Specifies the ID of the ECS on the DeH.                                                                                                                                               |
      +-------------------+-------------+-------------+-------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | released_at       | query       | String      | No          | Specifies the time when the DeH is released.                                                                                                                                          |
      +-------------------+-------------+-------------+-------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | changes-since     | query       | String      | No          | Filters the response by date and timestamp when the DeH status changes. To help keep track of changes, this parameter may also display recently deleted DeHs.                         |
      |                   |             |             |             |                                                                                                                                                                                       |
      |                   |             |             |             | The format of the date and timestamp is ISO 8601:                                                                                                                                     |
      |                   |             |             |             |                                                                                                                                                                                       |
      |                   |             |             |             | .. code-block::                                                                                                                                                                       |
      |                   |             |             |             |                                                                                                                                                                                       |
      |                   |             |             |             |    CCYY-MM-DDThh:mm:ss±hh:mm                                                                                                                                                          |
      |                   |             |             |             |                                                                                                                                                                                       |
      |                   |             |             |             | If the **hh:mm** value is included, the time zone is returned as the UTC offset, for example, **2015-08-27T09:49:58-05:00**. If you omit the time zone, the UTC time zone is assumed. |
      +-------------------+-------------+-------------+-------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

-  Example request

   .. code-block:: text

      GET https://{Endpoint}/v1.0/9c53a566cb3443ab910cf0daebca90c4/dedicated-hosts?state=available

Response
--------

-  Response parameters

   .. table:: **Table 3** Response parameters

      +-----------------+-----------------+------------------+----------------------------------------------------------------+
      | Parameter       | In              | Type             | Description                                                    |
      +=================+=================+==================+================================================================+
      | dedicated_hosts | body            | Array of objects | Specifies the DeHs that meet the search criteria.              |
      |                 |                 |                  |                                                                |
      |                 |                 |                  | For details, see :ref:`Table 1 <deh_02_0018__dedicated_host>`. |
      +-----------------+-----------------+------------------+----------------------------------------------------------------+
      | total           | body            | Integer          | Specifies the quantity of DeHs that meet the search criteria.  |
      +-----------------+-----------------+------------------+----------------------------------------------------------------+

-  Example response

   .. code-block::

      {
          "dedicated_hosts": [
              {
                  "dedicated_host_id": "ab910cf0daebca90c4001",
                  "name": "high performance servers1",
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
                  "released_at": null
                  },
              {
                  "dedicated_host_id": "ab910cf0daebca90c4002",
                  "name": "high performance servers2",
                  "auto_placement": "off",
                  "availability_zone": "az1",
                  "host_properties": {
                      "vcpus": 36,
                      "cores": 12,
                      "sockets": 2,
                      "host_type": "h1",
                      "host_type_name": "High performance",
                      "memory": 1073741824,
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
                  "available_memory": 1073101821,
                  "instance_total": 3,
                  "allocated_at": "2016-10-10T14:35:47Z",
                  "released_at": null
                  },
                  ],
          "total": 25
      }

Status Code
-----------

See :ref:`Status Codes <deh_02_0016>`.
