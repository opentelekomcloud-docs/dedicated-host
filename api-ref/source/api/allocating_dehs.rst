:original_name: deh_02_0019.html

.. _deh_02_0019:

Allocating DeHs
===============

Function
--------

This API is used to allocate one or more DeHs and set required parameters, such as the flavor, AZ, and quantity.

Constraints
-----------

The number of allocatable DeHs depends on the DeH quota owned by the tenant.

URI
---

POST /v1.0/{project_id}/dedicated-hosts

:ref:`Table 1 <deh_02_0019__table572214121015>` describes the parameters.

.. _deh_02_0019__table572214121015:

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

   .. table:: **Table 2** Request parameters

      +-------------------+-------------+------------------+-------------+-------------------------------------------------------------------------------------------------------------------------+
      | Parameter         | In          | Type             | Mandatory   | Description                                                                                                             |
      +===================+=============+==================+=============+=========================================================================================================================+
      | name              | body        | String           | Yes         | Specifies the DeH name.                                                                                                 |
      +-------------------+-------------+------------------+-------------+-------------------------------------------------------------------------------------------------------------------------+
      | auto_placement    | body        | String           | No          | Specifies whether to allow an ECS to be placed on any available DeH if its DeH ID is not specified during its creation. |
      |                   |             |                  |             |                                                                                                                         |
      |                   |             |                  |             | The value can be **on** or **off**.                                                                                     |
      |                   |             |                  |             |                                                                                                                         |
      |                   |             |                  |             | The default value is **on**.                                                                                            |
      +-------------------+-------------+------------------+-------------+-------------------------------------------------------------------------------------------------------------------------+
      | availability_zone | body        | String           | Yes         | Specifies the AZ to which the DeH belongs.                                                                              |
      +-------------------+-------------+------------------+-------------+-------------------------------------------------------------------------------------------------------------------------+
      | host_type         | body        | String           | Yes         | Specifies the DeH type.                                                                                                 |
      +-------------------+-------------+------------------+-------------+-------------------------------------------------------------------------------------------------------------------------+
      | quantity          | body        | Integer          | Yes         | Specifies the number of allocatable DeHs.                                                                               |
      +-------------------+-------------+------------------+-------------+-------------------------------------------------------------------------------------------------------------------------+
      | tags              | body        | Array of objects | No          | Specifies the DeH tags.                                                                                                 |
      |                   |             |                  |             |                                                                                                                         |
      |                   |             |                  |             | For details, see :ref:`Table 3 <deh_02_0019__table17210121526>`.                                                        |
      +-------------------+-------------+------------------+-------------+-------------------------------------------------------------------------------------------------------------------------+

   .. _deh_02_0019__table17210121526:

   .. table:: **Table 3** **tag** field description

      +-----------------+-----------------+-----------------+----------------------------------------------------------------------+
      | Parameter       | Type            | Mandatory       | Description                                                          |
      +=================+=================+=================+======================================================================+
      | key             | String          | Yes             | Specifies the tag key.                                               |
      |                 |                 |                 |                                                                      |
      |                 |                 |                 | -  It contains a maximum of 36 Unicode characters.                   |
      |                 |                 |                 | -  The value cannot be empty.                                        |
      |                 |                 |                 | -  It cannot contain the following ASCII characters: ``=*<>\|/,``    |
      |                 |                 |                 | -  It can contain letters, digits, hyphens (-), and underscores (_). |
      +-----------------+-----------------+-----------------+----------------------------------------------------------------------+
      | value           | String          | Yes             | Specifies the tag value.                                             |
      |                 |                 |                 |                                                                      |
      |                 |                 |                 | -  It contains a maximum of 43 Unicode characters.                   |
      |                 |                 |                 | -  It cannot contain the following ASCII characters: ``=*<>\|/,``    |
      |                 |                 |                 | -  It can contain letters, digits, hyphens (-), and underscores (_). |
      +-----------------+-----------------+-----------------+----------------------------------------------------------------------+

-  Example request

   .. code-block:: text

      POST https://{Endpoint}/v1.0/9c53a566cb3443ab910cf0daebca90c4/dedicated-hosts
      {
           "availability_zone": "dc1.az1",
           "name": "high performance servers1",
           "auto_placement": "off",
           "host_type": "h1",
           "quantity": 2,
           "tags": [
               {
                   "key": "key1",
                   "value": "value1"
               }
           ]
      }

Response
--------

-  Response parameters

   .. table:: **Table 4** Response parameters

      +--------------------+------+------------------+---------------------------------------------------------------------------------------+
      | Parameter          | In   | Type             | Description                                                                           |
      +====================+======+==================+=======================================================================================+
      | dedicated_host_ids | body | Array of strings | Specifies a group of IDs of allocated DeHs. The tenant can create ECSs on these DeHs. |
      +--------------------+------+------------------+---------------------------------------------------------------------------------------+

-  Example response

   .. code-block::

      {
          "dedicated_host_ids": ["xxxxxxx1","xxxxxxx2"]
      }

Status Code
-----------

.. table:: **Table 5** Returned error codes

   +-----------------------------------+-----------------------------------+
   | Error Code                        | Description                       |
   +===================================+===================================+
   | 403 Forbidden                     | #. Insufficient quota.            |
   |                                   | #. The flavor is not supported.   |
   +-----------------------------------+-----------------------------------+
   | 404 FlavorNotFound                | Invalid flavor.                   |
   +-----------------------------------+-----------------------------------+

For more status codes, see :ref:`Status Codes <deh_02_0016>`.
