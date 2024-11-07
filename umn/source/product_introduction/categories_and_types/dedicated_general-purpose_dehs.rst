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

.. note::

   c3 DeHs: Number of vCPUs = (Number of sockets x Number of cores x Number of single-core threads - CPU overheads) x CPU overcommitment ratio

   vCPUs = (2 x 18 x 2 - 12) x 1 = 60

ECSs Allowed on c3 DeHs
-----------------------

.. table:: **Table 2** ECS flavors allowed on c3 DeHs

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
