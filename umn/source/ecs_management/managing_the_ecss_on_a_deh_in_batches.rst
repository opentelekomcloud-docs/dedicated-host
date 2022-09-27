:original_name: deh_01_0025.html

.. _deh_01_0025:

Managing the ECSs on a DeH in Batches
=====================================

Scenarios
---------

You can start, stop, restart, or delete multiple ECSs on a DeH at a time on the management console.

Procedure
---------

#. Log in to the management console.

#. Click |image1| in the upper left corner and select the desired region and project.

#. Under **Computing**, click **Dedicated Host**.

   The **Dedicated Host** page is displayed.

#. Click the name of the target DeH.

   The DeH details page is displayed.

#. On the **ECSs on the DeH** tab, select the target ECSs.

   You can select multiple ECSs by selecting the check box before the ECS name.

   .. note::

      Except the deletion operation, ECSs to be operated in batches must be in the same state.

#. Click the button above the list to manage ECSs in batches.

   The options are as follows:

   -  **Start** (allowed only when ECSs are stopped)
   -  **Stop** (allowed only when ECSs are running.)
   -  **Restart** (allowed only when ECSs are running)
   -  **Delete**

.. |image1| image:: /_static/images/en-us_image_0210485079.png
