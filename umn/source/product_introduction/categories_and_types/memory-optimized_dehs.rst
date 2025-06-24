:original_name: en-us_topic_0105897861.html

.. _en-us_topic_0105897861:

Memory-Optimized DeHs
=====================

Overview
--------

Memory-optimized DeHs are designed for processing large-scale data sets in the memory. They use the latest Intel Xeon Skylake CPUs, network acceleration engines, and Data Plane Development Kit (DPDK) to provide higher network performance. They provide a maximum of 512 GiB of DDR4 memory for high-memory computing applications.

Memory-optimized DeHs are classified into m3, m4, and m7n DeHs.

-  M3 ECSs can be deployed on m3 DeHs.
-  M4 ECSs can be deployed on m4 DeHs.
-  m7n DeHs can house M7n ECSs.

DeH Specifications
------------------

.. table:: **Table 1** Specifications of m3 DeHs

   +-------------+-------------------+----------------------------+---------------------------------------------------------------------+-----------------+
   | Flavor Type | Number of Sockets | Number of Cores per Socket | Hardware Specifications                                             | Number of vCPUs |
   +=============+===================+============================+=====================================================================+=================+
   | m3          | 2                 | 18                         | -  CPU: Intel® Xeon® Processor Gold 6151 (24.75M L3 Cache, 3.0 GHz) | 60              |
   |             |                   |                            | -  Memory: 512 GiB (or 524,288 MiB)                                 |                 |
   +-------------+-------------------+----------------------------+---------------------------------------------------------------------+-----------------+

.. table:: **Table 2** Specifications of m4 DeHs

   +-------------+-------------------+----------------------------+----------------------------------------------------------------------------------+-----------------+
   | Flavor Type | Number of Sockets | Number of Cores per Socket | Hardware Specifications                                                          | Number of vCPUs |
   +=============+===================+============================+==================================================================================+=================+
   | m4          | 2                 | 22                         | -  CPU: Intel Cascade Lake 6266 (frequency: 3.00 GHz; turbo frequency: 3.40 GHz) | 76              |
   |             |                   |                            | -  Memory: 608 GiB (or 622,592 MiB)                                              |                 |
   +-------------+-------------------+----------------------------+----------------------------------------------------------------------------------+-----------------+

.. table:: **Table 3** Specifications of m7n DeHs

   +-------------+--------------------------+--------------------------+---------------------------------------------------------------------------------------------------------+-----------------+
   | Flavor Type | Number of CPUs (Sockets) | Number of Physical Cores | Hardware Specifications                                                                                 | Number of vCPUs |
   +=============+==========================+==========================+=========================================================================================================+=================+
   | m7n         | 2                        | 28                       | -  CPU: 3rd Generation Intel® Xeon® Scalable Processor (frequency: 2.60 GHz; turbo frequency: 3.40 GHz) | 98              |
   |             |                          |                          | -  Memory: 784 GiB (or 802,816 MiB)                                                                     |                 |
   +-------------+--------------------------+--------------------------+---------------------------------------------------------------------------------------------------------+-----------------+

.. note::

   Number of vCPUs = (Number of sockets x Number of cores x Number of single-core threads - CPU overheads) x CPU overcommitment ratio

   -  m3 DeHs

      vCPUs = (2 x 18 x 2 - 12) x 1 = 60

   -  m4 DeHs

      vCPUs = (2 x 22 x 2 - 14) x 1 = 74

ECSs Allowed on DeHs
--------------------

.. table:: **Table 3** ECS flavors allowed on m3 DeHs

   ============= ===== ===================
   ECS Flavor    vCPUs Memory (RAM in GiB)
   ============= ===== ===================
   m3.large.8    2     16
   m3.xlarge.8   4     32
   m3.2xlarge.8  8     64
   m3.4xlarge.8  16    128
   m3.8xlarge.8  32    256
   m3.15xlarge.8 60    512
   ============= ===== ===================

.. table:: **Table 5** ECS flavors allowed on m4 DeHs

   ============= ===== ===================
   ECS Flavor    vCPUs Memory (RAM in GiB)
   ============= ===== ===================
   m4.large.8    2     16
   m4.xlarge.8   4     32
   m4.2xlarge.8  8     64
   m4.3xlarge.8  12    96
   m4.4xlarge.8  16    128
   m4.6xlarge.8  24    192
   m4.8xlarge.8  32    256
   m4.16xlarge.8 64    512
   ============= ===== ===================

.. table:: **Table 6** ECS flavors allowed on m7n DeHs

   ============== ===== ===================
   ECS Flavor     vCPUs Memory (RAM in GiB)
   ============== ===== ===================
   m7n.large.8    2     16
   m7n.xlarge.8   4     32
   m7n.2xlarge.8  8     64
   m7n.3xlarge.8  12    96
   m7n.4xlarge.8  16    128
   m7n.6xlarge.8  24    192
   m7n.8xlarge.8  32    256
   m7n.12xlarge.8 48    384
   m7n.16xlarge.8 64    512
   m7n.24xlarge.8 96    768
   ============== ===== ===================
