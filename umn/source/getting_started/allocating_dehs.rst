:original_name: deh_01_0012.html

.. _deh_01_0012:

Allocating DeHs
===============

Scenarios
---------

You will allocate a DeH for the first time or allocate more DeHs as required.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner and select the desired region and project.

#. Under **Computing**, click **Dedicated Host**.

   The **Dedicated Host** page is displayed.

#. Click **Allocate DeH**.

   The **Allocate DeH** page is displayed.

#. Configure the DeH parameters.

   .. table:: **Table 1** Parameter description

      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                                                                          |
      +===================================+======================================================================================================================================================================================================================================+
      | Region                            | A region is a geographic area where your DeHs are located. Select the region closest to your services to reduce the latency and improve the download speed.                                                                          |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | AZ                                | An AZ is a physical region where resources use independent power supply and networks. AZs are physically isolated but interconnected through an internal network. To enhance application availability, create DeHs in different AZs. |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | DeH Category and DeH Type         | For details about the available DeH categories and types, see :ref:`Overview <deh_01_0005>`.                                                                                                                                         |
      |                                   |                                                                                                                                                                                                                                      |
      |                                   | .. note::                                                                                                                                                                                                                            |
      |                                   |                                                                                                                                                                                                                                      |
      |                                   |    Pay attention to the following when configuring the DeH type:                                                                                                                                                                     |
      |                                   |                                                                                                                                                                                                                                      |
      |                                   |    -  The DeH type determines the flavors and quantity of ECSs that can run on the DeH.                                                                                                                                              |
      |                                   |    -  The **Supported ECS Flavors** area shows the ECS flavors supported by the DeH type. You can create an ECS of the listed flavor only after the DeH is created successfully.                                                     |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Auto Placement                    | When **Auto Placement** is disabled for a DeH, new ECSs with auto placement selected will not be created on the DeH. When **Auto Placement** is enabled for a DeH, new ECS with auto placement selected may be created on the DeH.   |
      |                                   |                                                                                                                                                                                                                                      |
      |                                   | During ECS creation, you can still manually select DeHs with auto placement disabled to create ECSs on them.                                                                                                                         |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Tag                               | Tags are identifiers of DeHs. Adding tags to DeHs helps you better identify and manage your DeHs. You can add a maximum of 10 tags to a DeH.                                                                                         |
      |                                   |                                                                                                                                                                                                                                      |
      |                                   | For details about tag operations, see :ref:`Tag Management <deh_01_0038>`.                                                                                                                                                           |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | DeH Name                          | You can specify the DeH name, which contains a maximum of 64 characters, including only letters, digits, underscores (_), periods (.), and hyphens (-).                                                                              |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Quantity                          | When you allocate multiple DeHs, the system will add a suffix to each DeH name, for example, **my_DeH-001** and **my_DeH-002**.                                                                                                      |
      +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

   Check the total price. If you have any questions about the price details, click **Price Calculator** to view more information.

#. Click **Allocate Now**.

#. Confirm the configuration information, and click **SubmitAllocate Now**.

Results
-------

You can view the newly created DeH on the **Dedicated Host** page. If the DeH is not displayed immediately, refresh the page and wait for a while. If the status of the DeH changes to Available, you can use the DeH.

Follow-up Operations
--------------------

After a DeH is provisioned, you can perform the following operations as needed:

-  :ref:`Deploying ECSs on DeHs <deh_01_0013>`
-  :ref:`Migrating ECSs to DeHs <deh_01_0033>`

.. |image1| image:: /_static/images/en-us_image_0210485079.png

