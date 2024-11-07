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
   |                   |                 |                 | You can obtain the value from the DeH console or using the API in :ref:`Querying DeHs <deh_02_0020>`.                                                               |
   +-------------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Request
-------

None

Response
--------

.. table:: **Table 2** Response parameters

   +-----------------+-----------------+-----------------+----------------------------------------------------------------+
   | Parameter       | In              | Type            | Description                                                    |
   +=================+=================+=================+================================================================+
   | dedicated_host  | body            | Object          | Specifies the DeH object.                                      |
   |                 |                 |                 |                                                                |
   |                 |                 |                 | For details, see :ref:`Table 1 <deh_02_0018__dedicated_host>`. |
   +-----------------+-----------------+-----------------+----------------------------------------------------------------+

Example Request
---------------

Query details about the DeH **ab910cf0daebca90c4001**.

.. code-block:: text

   GET https://{Endpoint}/v1.0/9c53a566cb3443ab910cf0daebca90c4/dedicated-hosts/ab910cf0daebca90c4001

Example Response
----------------

.. code-block::

   {
       "dedicated_host": {
           "dedicated_host_id": "d465d0ae-f859-4a83-a508-8db654c05e7e",
           "name": "DEH001",
           "auto_placement": "off",
           "availability_zone": "eu-de-01",
           "host_properties": {
               "vcpus": 74,
               "cores": 22,
               "sockets": 2,
               "memory": 303104,
               "host_type": "c4",
               "host_type_name": "dedicated_general_purpose",
               "available_instance_capacities": [
                   {
                       "flavor": "c4.large.4"
                   },
                   {
                       "flavor": "c4.xlarge.4"
                   },
                   {
                       "flavor": "c4.2xlarge.4"
                   },
                   {
                       "flavor": "c4.3xlarge.4"
                   },
                   {
                       "flavor": "c4.6xlarge.4"
                   },
                   {
                       "flavor": "c4.16xlarge.4"
                   }
               ]
           },
           "state": "available",
           "project_id": "9c53a566cb3443ab910cf0daebca90c4",
           "available_vcpus": 20,
           "available_memory": 81920,
           "instance_total": 5,
           "allocated_at": "2016-10-10T14:35:47Z",
           "released_at": "",
           "instance_uuids": [
               "erf5th66cb3443ab912ff0daebca3456",
               "23457h66cb3443ab912ff0daebcaer45"
           ]
       }
   }

Status Code
-----------

See :ref:`Status Codes <deh_02_0016>`.
