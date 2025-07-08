:original_name: deh_faq_0029.html

.. _deh_faq_0029:

Why Is It Not Possible to Successfully Create an ECS on a DeH Even When There Are More Available Resources on the DeH Than What the ECS Requires?
=================================================================================================================================================

A DeH usually has multiple non-uniform memory access (NUMA) nodes. The available resources of a DeH displayed on the console represent the total resources available across all NUMA nodes.

In order to ensure optimal performance, ECSs of certain specifications cannot be deployed across NUMA nodes. If the resources of a single NUMA node are inadequate, the ECS creation will fail.

During ECS creation on a DeH:

-  The ECS will be successfully created if the remaining resources of a NUMA node meet or exceed the ECS specification requirement.
-  If the remaining resources of each NUMA node do not meet the ECS specification requirement, the creation of the ECS will fail.

For instance, if a DeH has 10 vCPUs and 20 GiB of available resources distributed across two NUMA nodes, attempting to create an ECS with 8 vCPUs and 16 GiB will fail. However, creating an ECS with 4 vCPUs and 8 GiB will be successful.


.. figure:: /_static/images/en-us_image_0000002179197409.png
   :alt: **Figure 1** Available DeH resources (example)

   **Figure 1** Available DeH resources (example)
