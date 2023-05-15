:original_name: deh_01_0006.html

.. _deh_01_0006:

General-Purpose DeHs
====================

Overview
--------

General-purpose DeHs can accommodate ECSs with regular workloads and short-term workload surges. They use a CPU-unbound scheduling scheme. vCPUs are randomly allocated to idle CPU hyper threads based on the system loads. If traffic loads are light, the computing performance is high. However, if traffic loads are heavy, vCPUs of different ECSs compete for physical CPU resources, resulting in unstable computing performance.

General-purpose DeHs are classified into s2, s2-medium, and s3 types.

-  DeHs of the s2 type can be used to deploy the S2 ECSs. The s2 DeHs use the latest-generation Intel® Xeon® Skylake CPUs, providing better cost-effectiveness.
-  The s2-medium DeHs are similar to s2 DeHs and can be used to deploy the S2 ECSs.
-  S3 ECSs can be deployed on s3 DeHs.

DeH Specifications
------------------

.. table:: **Table 1** Specifications of s2 DeHs

   +-------------+-------------------+----------------------------+---------------------------------------------------------------------+-----------------+
   | Flavor Type | Number of Sockets | Number of Cores per Socket | Hardware Specifications                                             | Number of vCPUs |
   +=============+===================+============================+=====================================================================+=================+
   | s2          | 2                 | 22                         | -  CPU: Intel® Xeon® Processor Gold 6161 (30.25 MB Cache, 2.20 GHz) | 144             |
   |             |                   |                            | -  Memory: 704 GB (or 720,896 MB)                                   |                 |
   +-------------+-------------------+----------------------------+---------------------------------------------------------------------+-----------------+

.. table:: **Table 2** Specifications of s2-medium DeHs

   +-------------+-------------------+----------------------------+-----------------------------------------------------------------------+-----------------+
   | Flavor Type | Number of Sockets | Number of Cores per Socket | Hardware Specifications                                               | Number of vCPUs |
   +=============+===================+============================+=======================================================================+=================+
   | s2-medium   | 2                 | 12                         | -  CPU: Intel® Xeon® Processor Gold 5118 (16.5 MB L3 Cache, 2.30 GHz) | 72              |
   |             |                   |                            | -  Memory: 328 GB (or 335,872 MB)                                     |                 |
   +-------------+-------------------+----------------------------+-----------------------------------------------------------------------+-----------------+

.. table:: **Table 3** Specifications of s3 DeHs

   +-------------+-------------------+----------------------------+----------------------------------------------------------------------------------+-----------------+
   | Flavor Type | Number of Sockets | Number of Cores per Socket | Hardware Specifications                                                          | Number of vCPUs |
   +=============+===================+============================+==================================================================================+=================+
   | s3          | 2                 | 26                         | -  CPU: Intel Cascade Lake 6278 (frequency: 2.60 GHz, Turbo frequency: 3.50 GHz) | 264             |
   |             |                   |                            | -  Memory: 702 GB (or 718,848 MB)                                                |                 |
   +-------------+-------------------+----------------------------+----------------------------------------------------------------------------------+-----------------+

.. note::

   Number of vCPUs = (Number of sockets x Number of cores x Number of single-core threads - CPU overheads) x CPU overcommitment ratio

   -  s2 DeHs

      vCPUs = (2 x 22 x 2 - 16) x 2 = 144

   -  s2-medium DeHs

      vCPUs = (2 x 12 x 2 - 12) x 2 = 72

   -  s3 DeHs

      vCPUs = (2 x 26 x 2 - 16) x 3 = 264

ECSs Allowed on DeHs
--------------------

.. table:: **Table 4** ECS flavors allowed on s2 DeHs

   ============ ===== ==================
   ECS Flavor   vCPUs Memory (RAM in GB)
   ============ ===== ==================
   s2.medium.1  1     1
   s2.large.1   2     2
   s2.xlarge.1  4     4
   s2.2xlarge.1 8     8
   s2.4xlarge.1 16    16
   s2.8xlarge.1 32    32
   s2.medium.2  1     2
   s2.large.2   2     4
   s2.xlarge.2  4     8
   s2.2xlarge.2 8     16
   s2.4xlarge.2 16    32
   s2.8xlarge.2 32    64
   s2.medium.4  1     4
   s2.large.4   2     8
   s2.xlarge.4  4     16
   s2.2xlarge.4 8     32
   s2.4xlarge.4 16    64
   s2.8xlarge.4 32    128
   s2.medium.8  1     8
   s2.large.8   2     16
   s2.xlarge.8  4     32
   s2.2xlarge.8 8     64
   s2.4xlarge.8 16    128
   s2.8xlarge.8 32    256
   ============ ===== ==================

.. table:: **Table 5** ECS flavors allowed on s2-medium DeHs

   ============ ===== ==================
   ECS Flavor   vCPUs Memory (RAM in GB)
   ============ ===== ==================
   s2.medium.1  1     1
   s2.large.1   2     2
   s2.xlarge.1  4     4
   s2.2xlarge.1 8     8
   s2.4xlarge.1 16    16
   s2.8xlarge.1 32    32
   s2.medium.2  1     2
   s2.large.2   2     4
   s2.xlarge.2  4     8
   s2.2xlarge.2 8     16
   s2.4xlarge.2 16    32
   s2.8xlarge.2 32    64
   s2.medium.4  1     4
   s2.large.4   2     8
   s2.xlarge.4  4     16
   s2.2xlarge.4 8     32
   s2.4xlarge.4 16    64
   s2.8xlarge.4 32    128
   s2.medium.8  1     8
   s2.large.8   2     16
   s2.xlarge.8  4     32
   s2.2xlarge.8 8     64
   s2.4xlarge.8 16    128
   s2.8xlarge.8 32    256
   ============ ===== ==================

.. table:: **Table 6** ECS flavors allowed on s3 DeHs

   ============ ===== ==================
   ECS Flavor   vCPUs Memory (RAM in GB)
   ============ ===== ==================
   s3.medium.1  1     1
   s3.large.1   2     2
   s3.xlarge.1  4     4
   s3.2xlarge.1 8     8
   s3.4xlarge.1 16    16
   s3.8xlarge.1 32    32
   s3.medium.2  1     2
   s3.large.2   2     4
   s3.xlarge.2  4     8
   s3.2xlarge.2 8     16
   s3.4xlarge.2 16    32
   s3.8xlarge.2 32    64
   s3.medium.4  1     4
   s3.large.4   2     8
   s3.xlarge.4  4     16
   s3.2xlarge.4 8     32
   s3.4xlarge.4 16    64
   s3.8xlarge.4 32    128
   s3.medium.8  1     8
   s3.large.8   2     16
   s3.xlarge.8  4     32
   s3.2xlarge.8 8     64
   s3.4xlarge.8 16    128
   s3.8xlarge.8 32    256
   ============ ===== ==================
