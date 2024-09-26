:original_name: deh_05_0904.html

.. _deh_05_0904:

Querying DeHs by Tag
====================

Function
--------

-  This API is used to filter DeHs by tag and return the list of all tags of a DeH.

-  Tag Management Service (TMS) uses this API to filter the DeHs.

URI
---

POST /v1.0/{project_id}/dedicated-host-tags/resource_instances/action

:ref:`Table 1 <deh_05_0904__table291625114015>` describes the parameters.

.. _deh_05_0904__table291625114015:

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

.. table:: **Table 2** Request parameters

   +-----------------+------------------+-----------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Parameter       | Type             | Mandatory       | Description                                                                                                                                                                                                                          |
   +=================+==================+=================+======================================================================================================================================================================================================================================+
   | tags            | Array of objects | No              | Displays all DeHs with specified tags. For more information, see :ref:`Table 3 <deh_05_0904__table1646113155613>`.                                                                                                                   |
   |                 |                  |                 |                                                                                                                                                                                                                                      |
   |                 |                  |                 | -  A maximum of 10 keys can be included. Each key can have a maximum of 10 values.                                                                                                                                                   |
   |                 |                  |                 | -  The structure body must be included.                                                                                                                                                                                              |
   |                 |                  |                 | -  The tag key cannot be left blank or set to an empty string.                                                                                                                                                                       |
   |                 |                  |                 | -  A key must be unique.                                                                                                                                                                                                             |
   |                 |                  |                 | -  Values of the same key must be unique.                                                                                                                                                                                            |
   +-----------------+------------------+-----------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | not_tags        | Array of objects | No              | Displays the DeHs with none of specified tags. For more information, see :ref:`Table 3 <deh_05_0904__table1646113155613>`.                                                                                                           |
   |                 |                  |                 |                                                                                                                                                                                                                                      |
   |                 |                  |                 | -  A maximum of 10 keys can be included. Each key can have a maximum of 10 values.                                                                                                                                                   |
   |                 |                  |                 | -  The structure body must be included.                                                                                                                                                                                              |
   |                 |                  |                 | -  The tag key cannot be left blank or set to an empty string.                                                                                                                                                                       |
   |                 |                  |                 | -  Keys must be unique.                                                                                                                                                                                                              |
   |                 |                  |                 | -  Values of the same key must be unique.                                                                                                                                                                                            |
   +-----------------+------------------+-----------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | limit           | Integer          | No              | Limits the maximum number of queried DeHs. The value cannot be a negative number. The maximum value is 1000.                                                                                                                         |
   |                 |                  |                 |                                                                                                                                                                                                                                      |
   |                 |                  |                 | -  If the **action** value is **count**, this parameter is invalid.                                                                                                                                                                  |
   |                 |                  |                 | -  If the **action** value is **filter**, the default value is **1000**.                                                                                                                                                             |
   +-----------------+------------------+-----------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | offset          | Integer          | No              | Specifies the index position. The query starts from the next piece of data indexed by this parameter. The value must be a non-negative number.                                                                                       |
   |                 |                  |                 |                                                                                                                                                                                                                                      |
   |                 |                  |                 | You do not need to specify this parameter when querying resources on the first page. When you query resources on subsequent pages, set the value of **offset** to the location returned in the response body for the previous query. |
   |                 |                  |                 |                                                                                                                                                                                                                                      |
   |                 |                  |                 | -  If the **action** value is **count**, this parameter is invalid.                                                                                                                                                                  |
   |                 |                  |                 | -  If the **action** value is **filter**, the default value is **0**.                                                                                                                                                                |
   +-----------------+------------------+-----------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | action          | String           | Yes             | Specifies the operation, which can be **filter** or **count**.                                                                                                                                                                       |
   |                 |                  |                 |                                                                                                                                                                                                                                      |
   |                 |                  |                 | -  **filter**: Filters DeHs by tag and lists DeHs that meet the search criteria. Listed DeHs are queried by page.                                                                                                                    |
   |                 |                  |                 | -  **count**: Searches for DeHs by tag and returns the number of DeHs that meet the search criteria.                                                                                                                                 |
   +-----------------+------------------+-----------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | tags_any        | Array of objects | No              | Includes any of the specified tags. For more information, see :ref:`Table 3 <deh_05_0904__table1646113155613>`.                                                                                                                      |
   |                 |                  |                 |                                                                                                                                                                                                                                      |
   |                 |                  |                 | -  This field contains a maximum of 10 tag keys and each tag key has a maximum of 10 tag values. The tag value corresponding to each tag key can be an empty array but the structure cannot be missing.                              |
   |                 |                  |                 | -  Each key must be unique, and cannot contain duplicate values.                                                                                                                                                                     |
   |                 |                  |                 | -  The response returns resources containing the tags in this list. Keys in this list are in an OR relationship and values in each key-value structure are also in an OR relationship.                                               |
   |                 |                  |                 | -  If no tag filtering condition is specified, full data is returned.                                                                                                                                                                |
   +-----------------+------------------+-----------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | not_tags_any    | Array of objects | No              | Excludes any of the specified tags. For more information, see :ref:`Table 3 <deh_05_0904__table1646113155613>`.                                                                                                                      |
   |                 |                  |                 |                                                                                                                                                                                                                                      |
   |                 |                  |                 | -  This field contains a maximum of 10 tag keys and each tag key has a maximum of 10 tag values. The tag value corresponding to each tag key can be an empty array but the structure cannot be missing.                              |
   |                 |                  |                 | -  Each key must be unique, and cannot contain duplicate values.                                                                                                                                                                     |
   |                 |                  |                 | -  The response returns resources containing no tags in this list. Keys in this list are in an OR relationship and values in each key-value structure are also in an OR relationship.                                                |
   |                 |                  |                 | -  If no tag filtering condition is specified, full data is returned.                                                                                                                                                                |
   +-----------------+------------------+-----------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | matches         | Array of objects | No              | Specifies the search field, which is used to search for DeHs by condition.                                                                                                                                                           |
   |                 |                  |                 |                                                                                                                                                                                                                                      |
   |                 |                  |                 | Currently, only **resource_name** can be used for search. For more information, see :ref:`Table 4 <deh_05_0904__table159211739175717>`.                                                                                              |
   +-----------------+------------------+-----------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

.. _deh_05_0904__table1646113155613:

.. table:: **Table 3** **tag** field description

   +-----------------+------------------+-----------------+--------------------------------------------------------------------------------------------------+
   | Parameter       | Type             | Mandatory       | Description                                                                                      |
   +=================+==================+=================+==================================================================================================+
   | key             | String           | Yes             | Specifies the tag key.                                                                           |
   |                 |                  |                 |                                                                                                  |
   |                 |                  |                 | -  It contains a maximum of 127 Unicode characters.                                              |
   |                 |                  |                 | -  This field cannot be left blank.                                                              |
   +-----------------+------------------+-----------------+--------------------------------------------------------------------------------------------------+
   | values          | Array of strings | No              | Specifies the tag values.                                                                        |
   |                 |                  |                 |                                                                                                  |
   |                 |                  |                 | -  Each tag contains a maximum of 10 values.                                                     |
   |                 |                  |                 | -  Values of the same tag must be unique.                                                        |
   |                 |                  |                 | -  Each value can contain a maximum of 255 Unicode characters.                                   |
   |                 |                  |                 | -  If this parameter is not specified, any value can be used.                                    |
   |                 |                  |                 | -  The resources containing one or more values listed in **values** will be found and displayed. |
   +-----------------+------------------+-----------------+--------------------------------------------------------------------------------------------------+

.. _deh_05_0904__table159211739175717:

.. table:: **Table 4** **match** field description

   +-----------------+-----------------+-----------------+------------------------------------------------------------------------------+
   | Parameter       | Type            | Mandatory       | Description                                                                  |
   +=================+=================+=================+==============================================================================+
   | key             | String          | Yes             | Specifies the key parameter to be matched.                                   |
   |                 |                 |                 |                                                                              |
   |                 |                 |                 | -  The key must be unique, and the value is used for matching.               |
   |                 |                 |                 | -  The **key** field is a fixed dictionary value.                            |
   |                 |                 |                 | -  This field cannot be left blank.                                          |
   |                 |                 |                 |                                                                              |
   |                 |                 |                 | .. note::                                                                    |
   |                 |                 |                 |                                                                              |
   |                 |                 |                 |    The parameter value can only be **resource_name**, which is the DeH name. |
   +-----------------+-----------------+-----------------+------------------------------------------------------------------------------+
   | value           | String          | Yes             | Specifies the tag value.                                                     |
   |                 |                 |                 |                                                                              |
   |                 |                 |                 | -  Each value can contain a maximum of 255 Unicode characters.               |
   |                 |                 |                 | -  This field cannot be left blank.                                          |
   +-----------------+-----------------+-----------------+------------------------------------------------------------------------------+

Response
--------

.. table:: **Table 5** Response parameters

   +-------------+------------------+----------------------------------------------------------------------------------------------------+
   | Parameter   | Type             | Description                                                                                        |
   +=============+==================+====================================================================================================+
   | resources   | Array of objects | Specifies the returned DeH list. For details, see :ref:`Table 6 <deh_05_0904__table924792920312>`. |
   +-------------+------------------+----------------------------------------------------------------------------------------------------+
   | total_count | Integer          | Specifies the total number of resources.                                                           |
   +-------------+------------------+----------------------------------------------------------------------------------------------------+

.. _deh_05_0904__table924792920312:

.. table:: **Table 6** Description of the **resource** field

   +-----------------------+-----------------------+-----------------------------------------------------------------------+
   | Parameter             | Type                  | Description                                                           |
   +=======================+=======================+=======================================================================+
   | resource_id           | String                | Specifies the DeH ID.                                                 |
   +-----------------------+-----------------------+-----------------------------------------------------------------------+
   | resouce_detail        | String                | Specifies the DeH details.                                            |
   |                       |                       |                                                                       |
   |                       |                       | This field is used for future extension and is left empty by default. |
   +-----------------------+-----------------------+-----------------------------------------------------------------------+
   | tags                  | Array of objects      | Specifies the tag list.                                               |
   |                       |                       |                                                                       |
   |                       |                       | For details, see :ref:`Table 7 <deh_05_0904__table145631502043>`.     |
   +-----------------------+-----------------------+-----------------------------------------------------------------------+
   | resource_name         | String                | Specifies the resource name.                                          |
   +-----------------------+-----------------------+-----------------------------------------------------------------------+

.. _deh_05_0904__table145631502043:

.. table:: **Table 7** **tag** field description

   +-----------------------+-----------------------+------------------------------------------------------------------+
   | Parameter             | Type                  | Description                                                      |
   +=======================+=======================+==================================================================+
   | key                   | String                | Specifies the tag key.                                           |
   |                       |                       |                                                                  |
   |                       |                       | -  It contains a maximum of 36 Unicode characters.               |
   |                       |                       | -  This field cannot be left blank.                              |
   |                       |                       | -  It cannot contain the following ASCII characters:``=*<>\|/,`` |
   +-----------------------+-----------------------+------------------------------------------------------------------+
   | value                 | String                | Specifies the tag value.                                         |
   |                       |                       |                                                                  |
   |                       |                       | -  Each value contains a maximum of 43 Unicode characters.       |
   |                       |                       | -  This field can be left blank.                                 |
   |                       |                       | -  It cannot contain the following ASCII characters:``=*<>\|/,`` |
   +-----------------------+-----------------------+------------------------------------------------------------------+

Example Request
---------------

Filter DeHs by tag. From the first data record, query the DeH using the search field (field: **resource_name**; value: **resource1**) and the tag (key: **key1**; value: **value1**).

.. code-block:: text

   POST https://{Endpoint}/v1.0/9c53a566cb3443ab910cf0daebca90c4/dedicated-host-tags/resource_instances/action
   {
       "offset": "0",
       "limit": "100",
       "action": "filter",
       "matches": [
           {
               "key": "resource_name",
               "value": "resource1"
           }
       ],
       "tags": [
           {
               "key": "key1",
               "values": ["value1"]
           }
       ]
   }

Example Response
----------------

Response body when **action** is set to **filter**

.. code-block::

   {
       "resources": [
           {
               "resource_detail": null,
               "resource_id": "cdfs_cefs_wesas_12_dsad",
               "resource_name": "resource1",
               "tags": [
                   {
                       "key": "key1",
                       "value": "value1"
                   }
               ]
           }
       ],
       "total_count": 1
   }

Response body when **action** is set to **count**

.. code-block::

   {
       "total_count": 100
   }

Status Code
-----------

See :ref:`Status Codes <deh_02_0016>`.
