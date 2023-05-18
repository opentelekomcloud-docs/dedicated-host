:original_name: deh_01_0031.html

.. _deh_01_0031:

General Computing-Plus DeHs
===========================

Overview
--------

Compared with general computing DeHs, general computing-plus DeHs provide dedicated vCPUs, featuring powerful performance. In addition, the DeHs use latest-generation network acceleration engines and Data Plane Development Kit (DPDK) to provide higher network performance, meeting requirements in different scenarios.

General computing-plus DeHs include only c4 DeHs.

-  C4 ECSs can be deployed on c4 DeHs.

DeH Specifications
------------------

.. table:: **Table 1** Specifications of c4 DeHs

   +-------------+--------------------------+--------------------------+----------------------------------------------------------------------------------+-------------+
   | Flavor Type | Number of CPUs (Sockets) | Number of Physical Cores | Hardware Specifications                                                          | vCPUs       |
   +=============+==========================+==========================+==================================================================================+=============+
   | c4          | 2                        | 22                       | -  CPU: Intel Cascade Lake 6266 (frequency: 3.00 GHz; Turbo frequency: 3.40 GHz) | 74          |
   |             |                          |                          | -  Memory: 296 GB (or 303,104 MB)                                                |             |
   +-------------+--------------------------+--------------------------+----------------------------------------------------------------------------------+-------------+

.. note::

   Number of vCPUs = (Number of sockets x Number of cores x Number of single-core threads - CPU overheads) x CPU overcommitment ratio

   -  c4 DeHs

      vCPUs = (2 x 22 x 2 - 14) x 1 = 74

ECSs Allowed on DeHs
--------------------

.. table:: **Table 2** ECS flavors allowed on c4 DeHs

   ============= ===== ==================
   Flavor Name   vCPUs Memory (RAM in GB)
   ============= ===== ==================
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
   ============= ===== ==================
