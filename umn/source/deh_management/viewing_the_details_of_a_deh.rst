:original_name: deh_01_0017.html

.. _deh_01_0017:

Viewing the Details of a DeH
============================

Scenarios
---------

You can view the basic information about a DeH, including the status, total resources, and usage, on the DeH console.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner, and select a region and a project.

#. Under **Computing**, click **Dedicated Host**.

   The **Dedicated Host** page is displayed.

#. Locate the target DeH and view the following information:

   -  **Name**: DeH name
   -  **Type**: DeH type
   -  **AZ**: AZ where DeHs are located
   -  **Auto Placement**: Whether **Auto Placement** is enabled.
   -  **Status**: DeH status

      .. table:: **Table 1** Status

         +-----------+------------------------------------------------------------------------------------------------------------------------------+
         | Status    | Description                                                                                                                  |
         +===========+==============================================================================================================================+
         | Available | The DeH is running normally, and the instance can be started on the DeH.                                                     |
         +-----------+------------------------------------------------------------------------------------------------------------------------------+
         | Pending   | The DeH cannot be used to deploy new instances because the host is being initialized.                                        |
         +-----------+------------------------------------------------------------------------------------------------------------------------------+
         | Released  | The DeH has been released and cannot be used.                                                                                |
         +-----------+------------------------------------------------------------------------------------------------------------------------------+
         | Fault     | The DeH is faulty, and new instances cannot be started on the DeH. The O&M personnel need to replace the DeH with a new one. |
         +-----------+------------------------------------------------------------------------------------------------------------------------------+

   -  **vCPUs**: Total number of vCPUs and available vCPUs
   -  **Memory(GiB)**: Total memory and available memory
   -  **Sockets**: Number of physical CPU sockets
   -  **Cores**: Number of physical cores

Related Operations
------------------

-  :ref:`Changing the Name of a DeH <deh_01_0018>`
-  :ref:`Configuring Auto Placement for DeHs <deh_01_0019>`

.. |image1| image:: /_static/images/en-us_image_0000001850888056.png
