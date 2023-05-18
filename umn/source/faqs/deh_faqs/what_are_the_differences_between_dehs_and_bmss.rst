:original_name: deh_faq_0006.html

.. _deh_faq_0006:

What Are the Differences Between DeHs and BMSs?
===============================================

Bare metal servers and dedicated hosts are physically-isolated servers dedicated to individual tenants. Their differences are as follows:

-  DeH: A dedicated host is fully exclusive for your ECSs, but cannot be directly used for running workloads. You can deploy ECSs for running workloads on a dedicated host.
-  BMS: A BMS is used as a server and can be directly used for running your services.


.. figure:: /_static/images/en-us_image_0000001441682817.png
   :alt: **Figure 1** Differences between DeHs and BMSs

   **Figure 1** Differences between DeHs and BMSs

.. table:: **Table 1** Differences between DeHs and BMSs

   +--------------------------+----------------------------------------------------------------------------------+-------------------------+
   | Item                     | DeH                                                                              | BMS                     |
   +==========================+==================================================================================+=========================+
   | Virtualization provided  | Yes                                                                              | No                      |
   +--------------------------+----------------------------------------------------------------------------------+-------------------------+
   | Usage                    | Provisioning of multiple ECSs on a DeH                                           | Used as a whole server  |
   +--------------------------+----------------------------------------------------------------------------------+-------------------------+
   | Supported specifications | Specifications of physical servers running DeHs and supported ECS specifications | Only BMS specifications |
   +--------------------------+----------------------------------------------------------------------------------+-------------------------+
   | Supported images         | ECS images                                                                       | Only BMS images         |
   +--------------------------+----------------------------------------------------------------------------------+-------------------------+
