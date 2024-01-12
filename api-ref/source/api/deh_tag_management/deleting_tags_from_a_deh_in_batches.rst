:original_name: deh_05_0902.html

.. _deh_05_0902:

Deleting Tags from a DeH in Batches
===================================

Function
--------

-  This API is used to delete tags from a specified DeH in batches.

-  Tag Management Service (TMS) uses this API to batch delete tags from a DeH.

**Constraint**
--------------

A DeH allows a maximum of 10 tags.

URI
---

POST /v1.0/{project_id}/dedicated-host-tags/{dedicated_host_id}/tags/action

:ref:`Table 1 <deh_05_0902__table1127422643418>` describes the parameters.

.. _deh_05_0902__table1127422643418:

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

   +-----------------+------------------+-----------------+--------------------------------------------------------------------------------------------------------------------------+
   | Parameter       | Type             | Mandatory       | Description                                                                                                              |
   +=================+==================+=================+==========================================================================================================================+
   | tags            | Array of objects | Yes             | Specifies the tag list.                                                                                                  |
   |                 |                  |                 |                                                                                                                          |
   |                 |                  |                 | For details, see :ref:`Table 3 <deh_05_0902__table147261636184517>`.                                                     |
   +-----------------+------------------+-----------------+--------------------------------------------------------------------------------------------------------------------------+
   | action          | String           | Yes             | Specifies the operation. Only lowercase letters are supported. For example, **delete** indicates the deletion operation. |
   +-----------------+------------------+-----------------+--------------------------------------------------------------------------------------------------------------------------+

.. _deh_05_0902__table147261636184517:

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

Response
--------

N/A

Example Request
---------------

Delete two tags from a DeH in a batch. The keys and corresponding values for these two tags are as follows: **key1** and **value1**; **key2** and **value2**

.. code-block:: text

   POST https://{Endpoint}/v1.0/9c53a566cb3443ab910cf0daebca90c4/dedicated-host-tags/74259164-e63a-4ad9-9c77-a1bd2c9aa187/tags/action

.. code-block::

   {
       "action": "delete",
       "tags": [
           {
               "key": "key1",
               "value": "value1"
           },
           {
               "key": "key2",
               "value": "value2"
           }
       ]
   }

Example Response
----------------

N/A

Status Code
-----------

See :ref:`Status Codes <deh_02_0016>`.
