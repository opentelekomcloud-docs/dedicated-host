:original_name: deh_01_0053.html

.. _deh_01_0053:

High-Performance DeHs
=====================

Overview
--------

High-performance DeHs are classified as h1 DeHs. h1 DeHs provide high-performance hardware and stable system running environment for ECSs that occupy a large number of compute and memory resources and have high-throughput storage systems.

High-performance ECSs can be deployed on h1 DeHs.

DeH Specifications
------------------

.. table:: **Table 1** Specifications of h1 DeHs

   +-------------+-------------------+----------------------------+-----------------------------------------------------------------+-----------------+
   | Flavor Type | Number of Sockets | Number of Cores per Socket | Hardware Specifications                                         | Number of vCPUs |
   +=============+===================+============================+=================================================================+=================+
   | h1          | 2                 | 12                         | -  CPU:                                                         | 36              |
   |             |                   |                            |                                                                 |                 |
   |             |                   |                            |    -  Intel® Xeon® Processor E5-2690 v3 (30 MB Cache, 2.60 GHz) |                 |
   |             |                   |                            |    -  Intel® Xeon® Processor E5-2690 v4 (35 MB Cache, 2.60 GHz) |                 |
   |             |                   |                            |                                                                 |                 |
   |             |                   |                            | -  Memory: 264 GB (or 270,336 MB)                               |                 |
   +-------------+-------------------+----------------------------+-----------------------------------------------------------------+-----------------+

.. note::

   Number of vCPUs = (Number of sockets x Number of cores x Number of single-core threads - CPU overheads) x CPU overcommitment ratio

   -  h1 DeHs

      vCPUs = (2 x 12 x 2 - 12) x 1 = 36

ECSs Allowed on h1 DeHs
-----------------------

.. table:: **Table 2** ECS flavors allowed on h1 DeHs

   ============ ===== ==================
   ECS Flavor   vCPUs Memory (RAM in GB)
   ============ ===== ==================
   h1.large     2     4
   h1.xlarge    4     8
   h1.2xlarge   8     16
   h1.4xlarge   16    32
   h1.8xlarge   32    64
   h1.large.4   2     8
   h1.xlarge.4  4     16
   h1.2xlarge.4 8     32
   h1.4xlarge.4 16    64
   h1.8xlarge.4 32    128
   h1.large.8   2     16
   h1.xlarge.8  4     32
   h1.2xlarge.8 8     64
   h1.4xlarge.8 16    128
   h1.8xlarge.8 32    256
   ============ ===== ==================
