:original_name: deh_01_0013.html

.. _deh_01_0013:

Deploying ECSs on DeHs
======================

Scenarios
---------

You can create ECSs of the supported flavors on your DeHs.

Prerequisites
-------------

Before creating an ECS on a DeH, ensure that you have:

-  Allocated a DeH.
-  Created a security group in the target region and added security group rules that meet your service requirements if you do not use the default security group.
-  Created a key pair in the target region if you select the key pair login mode when creating an ECS.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner and select the desired region and project.

#. Under **Computing**, click **Dedicated Host**.

   The **Dedicated Host** page is displayed.

#. In the list of DeHs, locate the DeH on which an ECS will be located and click **Create ECS** in the **Operation** column.

   The **Create ECS** page is displayed.

   For details, see `Creating an ECS <https://docs.otc.t-systems.com/en-us/usermanual/ecs/en-us_topic_0021831611.html>`__.

   .. note::

      -  To create an ECS without specifying a DeH, click Create ECS in the upper right corner of the page. Ensure that the auto placement function is enabled for at least one DeH.
      -  When selecting an ECS type, pay attention to mapping between the ECS type and the DeH type. If no matched DeH resources exist, ECSs cannot be created.

Results
-------

Click **Back to ECS List** and wait until the ECS is created. You can view information about the newly created ECS, including the name/ID, specifications, and IP address.

.. |image1| image:: /_static/images/en-us_image_0210485079.png
