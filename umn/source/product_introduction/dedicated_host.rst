:original_name: deh_01_0003.html

.. _deh_01_0003:

Dedicated Host
==============

A Dedicated Host (DeH) is a physical server fully dedicated for your use to ensure isolation, security, and performance for your ECSs. You can bring your own license (BYOL) to DeH to reduce the costs on software licenses and facilitate the independent management of ECSs.

:ref:`Figure 1 <deh_01_0003__fig184871050515>` shows the differences between DeHs and common ECSs.

.. _deh_01_0003__fig184871050515:

.. figure:: /_static/images/en-us_image_0161118470.png
   :alt: **Figure 1** Differences between DeHs and common ECSs

   **Figure 1** Differences between DeHs and common ECSs

The physical resources of the DeH are not shared with others. You can obtain the detailed information on the DeH, such as sockets, physical cores, CPU type, and memory size. So, you can create ECSs of specified flavors based on the DeH flavor.

ECS Deployment Modes
--------------------

When deploying an ECS, you can:

-  Select a DeH to deploy ECSs.

   Directly create ECSs on an existing DeH or select a DeH you want to deploy ECSs on when creating ECSs.

-  Configure the system to automatically deploy ECSs on a DeH.

   Enable **Auto Placement** for DeHs to let the system automatically deploy ECSs on the DeH with the highest available memory based on load balancing requirements.

You can use either of the above methods to deploy ECSs on a DeH. This helps you ensure isolation, security, and compliance for deployed applications, improves resource utilization, and optimizes the ECS performance.
