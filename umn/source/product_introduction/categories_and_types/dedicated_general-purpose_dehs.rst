:original_name: deh_01_0049.html

.. _deh_01_0049:

Dedicated General-Purpose DeHs
==============================

Overview
--------

Dedicated general-purpose DeHs are classified as c3, c4, and c7n DeHs. DeHs of c3, c4, and c7n types can be used to deploy C3, C4, and C7n ECSs. The C3, C4, and C7n ECSs use high-performance networks to improve comprehensive performance and stability, meeting the requirements of enterprise-level applications for high service stability and computing performance.

DeH Specifications
------------------

.. table:: **Table 1** Specifications of c3 DeHs

   +-----------------+-------------------+----------------------------+---------------------------------------------------------------------+-----------------+
   | **Flavor Type** | Number of Sockets | Number of Cores per Socket | Hardware Specifications                                             | Number of vCPUs |
   +=================+===================+============================+=====================================================================+=================+
   | c3              | 2                 | 18                         | -  CPU: Intel® Xeon® Processor Gold 6151 (24.75M L3 Cache, 3.0 GHz) | 60              |
   |                 |                   |                            | -  Memory: 256 GiB (or 262,144 MiB)                                 |                 |
   +-----------------+-------------------+----------------------------+---------------------------------------------------------------------+-----------------+

.. table:: **Table 2** Specifications of c4 DeHs

   +-------------+-------------------+----------------------------+----------------------------------------------------------------------------------+-----------------+
   | Flavor Type | Number of Sockets | Number of Cores per Socket | Hardware Specifications                                                          | Number of vCPUs |
   +=============+===================+============================+==================================================================================+=================+
   | c4          | 2                 | 22                         | -  CPU: Intel Cascade Lake 6266 (frequency: 3.00 GHz; turbo frequency: 3.40 GHz) | 74              |
   |             |                   |                            | -  Memory: 296 GiB (or 303,104 MiB)                                              |                 |
   +-------------+-------------------+----------------------------+----------------------------------------------------------------------------------+-----------------+

.. table:: **Table 3** Specifications of c7n DeHs

   +-------------+--------------------------+--------------------------+----------------------------------------------------------------------------------------------------+-----------------+
   | Flavor Type | Number of CPUs (Sockets) | Number of Physical Cores | Hardware Specifications                                                                            | Number of vCPUs |
   +=============+==========================+==========================+====================================================================================================+=================+
   | c7n         | 2                        | 28                       | CPU: 3rd Generation Intel® Xeon® Scalable Processor (frequency: 2.6 GHz; turbo frequency: 3.4 GHz) | 98              |
   |             |                          |                          |                                                                                                    |                 |
   |             |                          |                          | Memory: 392 GiB (or 401,408 MiB)                                                                   |                 |
   +-------------+--------------------------+--------------------------+----------------------------------------------------------------------------------------------------+-----------------+

.. note::

   DeHs: Number of vCPUs = (Number of sockets x Number of cores x Number of single-core threads - CPU overheads) x CPU overcommitment ratio

   -  c3 DeHs: vCPUs = (2 x 18 x 2 - 12) x 1 = 60
   -  c4 DeHs: vCPUs = (2 x 22 x 2 - 14) x 1 = 74
   -  c7n DeHs: vCPUs = (2 x 28 x 2 - 14) x 1 = 98

ECSs Allowed on DeHs
--------------------

.. table:: **Table 4** ECS flavors allowed on c3 DeHs

   ============= ===== ===================
   ECS Flavor    vCPUs Memory (RAM in GiB)
   ============= ===== ===================
   c3.large.2    2     4
   c3.xlarge.2   4     8
   c3.2xlarge.2  8     16
   c3.4xlarge.2  16    32
   c3.8xlarge.2  32    64
   c3.15xlarge.2 60    128
   c3.large.4    2     8
   c3.xlarge.4   4     16
   c3.2xlarge.4  8     32
   c3.4xlarge.4  16    64
   c3.8xlarge.4  32    128
   c3.15xlarge.4 60    256
   ============= ===== ===================

.. table:: **Table 5** ECS flavors allowed on c4 DeHs

   ============= ===== ===================
   ECS Flavor    vCPUs Memory (RAM in GiB)
   ============= ===== ===================
   c4.large.2    2     4
   c4.xlarge.2   4     8
   c4.2xlarge.2  8     16
   c4.3xlarge.2  12    24
   c4.4xlarge.2  16    32
   c4.6xlarge.2  24    48
   c4.8xlarge.2  32    64
   c4.16xlarge.2 64    128
   c4.large.4    2     8
   c4.xlarge.4   4     16
   c4.2xlarge.4  8     32
   c4.3xlarge.4  12    48
   c4.4xlarge.4  16    64
   c4.6xlarge.4  24    96
   c4.8xlarge.4  32    128
   c4.16xlarge.4 64    256
   ============= ===== ===================

.. table:: **Table 6** ECS flavors allowed on c7n DeHs

   ============== ===== ============
   ECS Flavor     vCPUs Memory (GiB)
   ============== ===== ============
   c7n.large.2    2     4
   c7n.xlarge.2   4     8
   c7n.2xlarge.2  8     16
   c7n.3xlarge.2  12    24
   c7n.4xlarge.2  16    32
   c7n.6xlarge.2  24    48
   c7n.8xlarge.2  32    64
   c7n.12xlarge.2 48    96
   c7n.16xlarge.2 64    128
   c7n.24xlarge.2 96    192
   c7n.large.4    2     8
   c7n.xlarge.4   4     16
   c7n.2xlarge.4  8     32
   c7n.3xlarge.4  12    48
   c7n.4xlarge.4  16    64
   c7n.6xlarge.4  24    96
   c7n.8xlarge.4  32    128
   c7n.12xlarge.4 48    192
   c7n.16xlarge.4 64    256
   c7n.24xlarge.4 96    384
   ============== ===== ============
