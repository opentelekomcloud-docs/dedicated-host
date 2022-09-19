:original_name: en-us_topic_0105897861.html

.. _en-us_topic_0105897861:

Memory-Optimized DeHs
=====================

Overview
--------

Memory-optimized DeHs are designed for processing large-scale data sets in the memory. They use the latest Intel Xeon Skylake CPUs, network acceleration engines, and Data Plane Development Kit (DPDK) to provide higher network performance, providing a maximum of 512 GB DDR4 memory for high-memory computing applications.

Memory-optimized DeHs are classified into m3 and m4 DeHs.

-  M3 ECSs can be deployed on m3 DeHs.
-  M4 ECSs can be deployed on m4 DeHs.

DeH Specifications
------------------

.. table:: **Table 1** Specifications of m3 DeHs

   +-------------+-------------------+----------------------------+---------------------------------------------------------------------+-----------------+
   | Flavor Type | Number of Sockets | Number of Cores per Socket | Hardware Specifications                                             | Number of vCPUs |
   +=============+===================+============================+=====================================================================+=================+
   | m3          | 2                 | 18                         | -  CPU: Intel® Xeon® Processor Gold 6151 (24.75M L3 Cache, 3.0 GHz) | 60              |
   |             |                   |                            | -  Memory: 512 GB (or 524,288 MB)                                   |                 |
   +-------------+-------------------+----------------------------+---------------------------------------------------------------------+-----------------+

.. table:: **Table 2** Specifications of m4 DeHs

   +-------------+-------------------+----------------------------+----------------------------------------------------------------------------------+-----------------+
   | Flavor Type | Number of Sockets | Number of Cores per Socket | Hardware Specifications                                                          | Number of vCPUs |
   +=============+===================+============================+==================================================================================+=================+
   | m4          | 2                 | 22                         | -  CPU: Intel Cascade Lake 6266 (frequency: 3.00 GHz; Turbo frequency: 3.40 GHz) | 74              |
   |             |                   |                            | -  Memory: 592 GB ( or 606,208 MB)                                               |                 |
   +-------------+-------------------+----------------------------+----------------------------------------------------------------------------------+-----------------+

.. note::

   Number of vCPUs = (Number of sockets x Number of cores x Number of single-core threads - CPU overheads) x CPU overcommitment ratio

   -  m3 DeHs

      vCPUs = (2 x 18 x 2 - 12) x 1 = 60

   -  m4 DeHs

      vCPUs = (2 x 22 x 2 - 14) x 1 = 74

ECSs Allowed on DeHs
--------------------

.. table:: **Table 3** ECS flavors allowed on m3 DeHs

   ============= ===== ==================
   Flavor Name   vCPUs Memory (RAM in GB)
   ============= ===== ==================
   m3.large.8    2     16
   m3.xlarge.8   4     32
   m3.2xlarge.8  8     64
   m3.4xlarge.8  16    128
   m3.8xlarge.8  32    256
   m3.15xlarge.8 60    512
   ============= ===== ==================

.. table:: **Table 4** ECS flavors allowed on m4 DeHs

   ============= ===== ==================
   Flavor Name   vCPUs Memory (RAM in GB)
   ============= ===== ==================
   m4.large.8    2     16
   m4.xlarge.8   4     32
   m4.2xlarge.8  8     64
   m4.3xlarge.8  12    96
   m4.4xlarge.8  16    128
   m4.6xlarge.8  24    192
   m4.8xlarge.8  32    256
   m4.16xlarge.8 64    512
   ============= ===== ==================
