:original_name: deh_01_0028.html

.. _deh_01_0028:

Modifying Specifications of ECSs on DeHs
========================================

Scenarios
---------

When the specifications of ECSs on a DeH cannot meet service requirements, you can modify the ECS specifications including the vCPUs and memory. For some ECSs, you can change the ECS type when modifying the ECS specifications. You can change the specifications of a general-purpose ECS to that of an H1 ECS. You can change XEN instances to KVM instances.

.. note::

   XEN instances: indicate ECSs that are virtualized by XEN.

   KVM instances: indicate ECSs that are virtualized by KVM.

   Before changing a XEN instance to a KVM instance, manually install the desired driver on the ECS. Otherwise, the ECS will be unavailable after the modification is performed. For example, starting the OS will fail.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner and select the desired region and project.

#. Under **Computing**, click **Dedicated Host**.

   The **Dedicated Host** page is displayed.

#. Click the name of the target DeH.

   The DeH details page is displayed.

#. On the **ECSs on the DeH** tab, query the status of the target ECS.

#. Only the specifications of a stopped ECS can be modified. If the ECS is not stopped, click **More** and select **Stop** in the **Operation** column.

#. After the ECS status changes to **Stopped**, click **Modify Specifications** in the **Operation** column.

   The **Modify ECS Specifications** page is displayed. Modify the specifications by following the instructions described in Elastic Cloud Server User Guide.

.. |image1| image:: /_static/images/en-us_image_0210485079.png
