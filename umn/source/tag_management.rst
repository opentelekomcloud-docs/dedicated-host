:original_name: deh_01_0038.html

.. _deh_01_0038:

Tag Management
==============

Tags are identifiers of DeHs and can help you quickly identify your DeHs.

You can add a tag to a DeH when creating a DeH. Alternatively, you can add a tag to a DeH on the **Tags** tab of the DeH details page. A maximum of 10 tags can be added to a DeH.

A tag consists of a tag key and a tag value. :ref:`Table 1 <deh_01_0038__table204442131366>` lists the naming requirements for keys and values.

.. _deh_01_0038__table204442131366:

.. table:: **Table 1** Tag naming requirements

   +-----------------------+---------------------------------------------------------------------+-----------------------+
   | Parameter             | Requirement                                                         | Example Value         |
   +=======================+=====================================================================+=======================+
   | Tag key               | -  Cannot be left blank.                                            | Organization          |
   |                       | -  Must be unique for a specific DeH.                               |                       |
   |                       | -  Contains a maximum of 36 characters.                             |                       |
   |                       | -  Contains only digits, letters, hyphens (-), and underscores (_). |                       |
   +-----------------------+---------------------------------------------------------------------+-----------------------+
   | Tag value             | -  Contains a maximum of 43 characters.                             | Apache                |
   |                       | -  Contains only digits, letters, hyphens (-), and underscores (_). |                       |
   +-----------------------+---------------------------------------------------------------------+-----------------------+

Searching for DeHs
------------------

On the **Dedicated Host** page, you can search for the desired DeHs by tag key and tag value.

#. Log in to the management console.

#. Under **Computing**, click **Dedicated Host**.

   The **Dedicated Host** page is displayed.

#. In the upper right corner of the DeH list, click **Search by Tag** to show the search page.


   .. figure:: /_static/images/en-us_image_0181721054.png
      :alt: **Figure 1** Searching for DeHs by tag

      **Figure 1** Searching for DeHs by tag

#. Enter the tag key and tag value of the target DeH. Click **Search**.

   The system automatically searches for your desired DeHs.

#. Click |image1| to add a tag.

   You can add multiple tags to search for DeHs. The system will display DeHs that match all tags.

#. Click **Search**.

   The system searches for DeHs based on tag keys or tag values.

.. |image1| image:: /_static/images/en-us_image_0238393803.png
