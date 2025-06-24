:original_name: deh_01_0033.html

.. _deh_01_0033:

Migrating ECSs
==============

Scenarios
---------

ECSs can be migrated between DeHs or between a DeH and a public resource pool. You can:

-  Migrate an ECS on a DeH to another DeH.
-  Migrate an ECS on a DeH to a public resource pool.
-  Migrate an ECS in a public resource pool to a DeH.

   .. note::

      Operations in this scenario need to be performed on the ECS console. For details, see Migrating an ECS in the *Elastic Cloud Server User Guide*.

Notes
-----

Only a stopped ECS can be migrated.

**Procedure**
-------------

#. Log in to the management console.

#. Click |image1| in the upper left corner, and select a region and a project.

#. Under **Computing**, click **Dedicated Host**.

   The **Dedicated Host** page is displayed.

#. Click the name of the target DeH.

   The DeH details page is displayed.

#. On the **ECSs on the DeH** tab, view the status of the ECS to be migrated.

#. Only a stopped ECS can be migrated. If the ECS is not stopped, click **More** and select **Stop** in the **Operation** column.

#. After the ECS status changes to **Stopped**, click **More** and select **Migrate ECS** in the **Operation** column.

#. On the **Migrate ECS** page, select the destination where you would like to migrate the ECS.

   -  If you want to migrate the ECS to another DeH, set **Migrated** to **To another DeH**.
   -  If you want to migrate the ECS from a DeH to a public resource pool, set **Migrated** to **Out of DeH**.

#. Click **OK**.

   .. note::

      The ECS status changes from **Resizing** to **Stopped** during migration.

.. |image1| image:: /_static/images/en-us_image_0000001850888056.png
