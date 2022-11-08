:original_name: deh_01_0003.html

.. _deh_01_0003:

Dedicated Host
==============

Dedicated Host (DeH) provides dedicated physical hosts to ensure isolation, security, and performance for your ECSs. You can bring your own license (BYOL) to DeH to reduce the costs on software licenses and facilitate the independent management of ECSs.

:ref:`Figure 1 <deh_01_0003__fig184871050515>` shows the differences between DeHs and common ECSs.

.. _deh_01_0003__fig184871050515:

.. figure:: /_static/images/en-us_image_0161118470.png
   :alt: **Figure 1** Differences between DeHs and common ECSs

   **Figure 1** Differences between DeHs and common ECSs

The physical resources of the DeH are not shared with others, while the physical resources of the ECS may be shared with others. You can obtain the detailed information on the DeH, such as sockets, physical cores, CPU type, and memory size. So, you can create ECSs of specified flavors based on the DeH flavor.

ECS Deployment Modes
--------------------

You can use your DeH resources by the following methods:

-  Select a DeH to deploy ECSs.

   Directly create ECSs on an existing DeH or select a DeH you want to deploy ECSs on when creating ECSs.

-  Configure the system to automatically deploy the ECS on a DeH.

   When you create an ECS, select **Auto Placement** for **DeH** to configure the system to automatically deploy the ECS on the DeH with the highest available memory.

The combination of these two methods guarantees the isolation, security, and regulation compliance for deployed applications, improves resource utilization, and optimizes the ECS performance.
