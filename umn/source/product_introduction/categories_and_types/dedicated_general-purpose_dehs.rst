:original_name: deh_01_0049.html

.. _deh_01_0049:

Dedicated General-Purpose DeHs
==============================

Overview
--------

Dedicated general-purpose DeHs are classified as c3 and c4 DeHs. DeHs of c3 and c4 types can be used to deploy C3 and C4 ECSs. The C3 and C4 ECSs use high-performance networks to improve comprehensive performance and stability, meeting the requirements of enterprise-level applications for high service stability and computing performance.

DeH Specifications
------------------

.. table:: **Table 1** Specifications of c3 DeHs

   +-----------------+-------------------+----------------------------+---------------------------------------------------------------------+-----------------+
   | **Flavor Type** | Number of Sockets | Number of Cores per Socket | Hardware Specifications                                             | Number of vCPUs |
   +=================+===================+============================+=====================================================================+=================+
   | c3              | 2                 | 18                         | -  CPU: Intel® Xeon® Processor Gold 6151 (24.75M L3 Cache, 3.0 GHz) | 60              |
   |                 |                   |                            | -  Memory: 256 GB (or 262,144 MB)                                   |                 |
   +-----------------+-------------------+----------------------------+---------------------------------------------------------------------+-----------------+

.. table:: **Table 2** Specifications of c4 DeHs

   +-------------+-------------------+----------------------------+----------------------------------------------------------------------------------+-------------+
   | Flavor Type | Number of Sockets | Number of Cores per Socket | Hardware Specifications                                                          | vCPUs       |
   +=============+===================+============================+==================================================================================+=============+
   | c4          | 2                 | 22                         | -  CPU: Intel Cascade Lake 6266 (frequency: 3.00 GHz; turbo frequency: 3.40 GHz) | 74          |
   |             |                   |                            | -  Memory: 296 GB (or 303,104 MB)                                                |             |
   +-------------+-------------------+----------------------------+----------------------------------------------------------------------------------+-------------+

.. note::

   DeHs: Number of vCPUs = (Number of sockets x Number of cores x Number of single-core threads - CPU overheads) x CPU overcommitment ratio

   -  c3 DeHs: vCPUs = (2 x 18 x 2 - 12) x 1 = 60
   -  c4 DeHs: vCPUs = (2 x 22 x 2 - 14) x 1 = 74

ECSs Allowed on DeHs
--------------------

.. table:: **Table 3** ECS flavors allowed on c3 DeHs

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

.. table:: **Table 4** ECS flavors allowed on c4 DeHs

   ============= ===== ===================
   Flavor Name   vCPUs Memory (RAM in GiB)
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
