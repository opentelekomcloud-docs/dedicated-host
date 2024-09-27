:original_name: deh_01_0055.html

.. _deh_01_0055:

Ultra-High I/O DeHs
===================

Ultra-high I/O DeHs use high-performance local NVMe SSDs to provide high storage input/output operations per second (IOPS) and low read/write latency. They are suitable for high-performance relational databases, NoSQL databases (e.g. Cassandra and MongoDB), and ElasticSearch.

Ultra-high I/O ECSs can be deployed on i3, i3_pro, and i3m DeHs.

DeH Specifications
------------------

.. table:: **Table 1** Specifications of i3 DeHs

   +-------------+-------------------+------------------+-----------------------------------------------------------------------------------+-----------------+-------------------------------+
   | Flavor Type | Number of Sockets | Cores Per Socket | Hardware Specifications                                                           | Number of vCPUs | Total Capacity of Local Disks |
   +=============+===================+==================+===================================================================================+=================+===============================+
   | i3          | 2                 | 26               | CPU: Intel® Xeon® CascadedLake CPU (frequency: 2.6 GHz; turbo frequency: 3.5 GHz) | 80              | 32 TB                         |
   |             |                   |                  |                                                                                   |                 |                               |
   |             |                   |                  | Memory: 324 GB (or 331,776 MB)                                                    |                 |                               |
   +-------------+-------------------+------------------+-----------------------------------------------------------------------------------+-----------------+-------------------------------+

.. table:: **Table 2** Specifications of i3_pro DeHs

   +-------------+-------------------+------------------+-----------------------------------------------------------------------------------+-----------------+-------------------------------+
   | Flavor Type | Number of Sockets | Cores Per Socket | Hardware Specifications                                                           | Number of vCPUs | Total Capacity of Local Disks |
   +=============+===================+==================+===================================================================================+=================+===============================+
   | i3_pro      | 2                 | 26               | CPU: Intel® Xeon® CascadedLake CPU (frequency: 2.6 GHz; turbo frequency: 3.5 GHz) | 80              | 32 TB                         |
   |             |                   |                  |                                                                                   |                 |                               |
   |             |                   |                  | Memory: 640 GB (or 655,360 MB)                                                    |                 |                               |
   +-------------+-------------------+------------------+-----------------------------------------------------------------------------------+-----------------+-------------------------------+

.. table:: **Table 3** Specifications of i3m DeHs

   +-----------+-------------------+------------------+--------------------------------------------------------------------------------------------+-----------------+-------------------------------+
   | Host Type | Number of Sockets | Cores Per Socket | Hardware Specifications                                                                    | Number of vCPUs | Total Capacity of Local Disks |
   +===========+===================+==================+============================================================================================+=================+===============================+
   | i3m       | 2                 | 18               | CPU: Intel® Xeon® Skylake-SP Xeon Gold 6151 (frequency: 2.6 GHz; turbo frequency: 3.5 GHz) | 64              | 12.8 TB                       |
   |           |                   |                  |                                                                                            |                 |                               |
   |           |                   |                  | Memory: 512 GB (or 524,288 MB)                                                             |                 |                               |
   +-----------+-------------------+------------------+--------------------------------------------------------------------------------------------+-----------------+-------------------------------+

ECSs Allowed on DeHs
--------------------

.. table:: **Table 4** ECS flavors allowed on i3 DeHs

   ============= ===== ===================
   ECS Flavor    vCPUs Memory (RAM in GiB)
   ============= ===== ===================
   i3.2xlarge.4  8     32
   i3.4xlarge.4  16    64
   i3.8xlarge.4  32    128
   i3.12xlarge.4 48    192
   i3.16xlarge.4 64    256
   ============= ===== ===================

.. table:: **Table 5** ECS flavors allowed on i3_pro DeHs

   ============= ===== ===================
   ECS Flavor    vCPUs Memory (RAM in GiB)
   ============= ===== ===================
   i3.2xlarge.8  8     64
   i3.4xlarge.8  16    128
   i3.8xlarge.8  32    192
   i3.12xlarge.8 48    256
   i3.16xlarge.8 64    512
   ============= ===== ===================

.. table:: **Table 6** ECS flavors allowed on i3m DeHs

   ============== ===== ===================
   Flavor Name    vCPUs Memory (RAM in GiB)
   ============== ===== ===================
   i3m.2xlarge.8  8     64
   i3m.4xlarge.8  16    128
   i3m.8xlarge.8  32    256
   i3m.12xlarge.8 48    384
   i3m.16xlarge.8 64    512
   ============== ===== ===================
