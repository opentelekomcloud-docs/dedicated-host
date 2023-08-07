:original_name: deh_01_0055.html

.. _deh_01_0055:

Ultra-High I/O DeHs
===================

The flavor type for ultra-high I/O DeHs is i3. Ultra-high I/O DeHs use high-performance local NVMe SSDs to provide high storage input/output operations per second (IOPS) and low read/write latency. They are suitable for high-performance relational databases, NoSQL databases (e.g. Cassandra and MongoDB), and ElasticSearch.

Ultra-high I/O ECSs can be deployed on i3 and i3_pro DeHs.

DeH Specifications
------------------

.. table:: **Table 1** Specifications of i3 DeHs

   +-------------+-------------------+------------------+-----------------------------------------------------------------------------------+-----------+-------------------------------+
   | Flavor Type | Number of Sockets | Cores Per Socket | Hardware Specifications                                                           | vCPUs     | Total Capacity of Local Disks |
   +=============+===================+==================+===================================================================================+===========+===============================+
   | i3          | 2                 | 26               | CPU: Intel® Xeon® CascadedLake CPU (frequency: 2.6 GHz; Turbo frequency: 3.5 GHz) | 92        | 16 TB                         |
   |             |                   |                  |                                                                                   |           |                               |
   |             |                   |                  | Memory: 324 GB (=331,776 MB)                                                      |           |                               |
   +-------------+-------------------+------------------+-----------------------------------------------------------------------------------+-----------+-------------------------------+

.. table:: **Table 2** Specifications of i3_pro DeHs

   +-------------+-------------------+------------------+-----------------------------------------------------------------------------------+-----------+-------------------------------+
   | Flavor Type | Number of Sockets | Cores Per Socket | Hardware Specifications                                                           | vCPUs     | Total Capacity of Local Disks |
   +=============+===================+==================+===================================================================================+===========+===============================+
   | i3_pro      | 2                 | 26               | CPU: Intel® Xeon® CascadedLake CPU (frequency: 2.6 GHz; Turbo frequency: 3.5 GHz) | 80        | 16 TB                         |
   |             |                   |                  |                                                                                   |           |                               |
   |             |                   |                  | Memory: 640 GB (or 655,360 MB)                                                    |           |                               |
   +-------------+-------------------+------------------+-----------------------------------------------------------------------------------+-----------+-------------------------------+

.. note::

   Number of vCPUs = (Number of sockets x Number of cores x Number of single-core threads - CPU overheads) x CPU overcommitment ratio

   -  i3 DeHs

      Number of vCPUs = (2 x 26 x 2 - 12) x 1 = 92

   -  i3_pro DeHs

      Number of vCPUs = (2 x 26 x 2 - 24) x 1 = 80

ECSs Allowed on DeHs
--------------------

.. table:: **Table 3** ECS flavors allowed on i3 DeHs

   ============= ===== ==================
   ECS Flavor    vCPUs Memory (RAM in GB)
   ============= ===== ==================
   i3.2xlarge.4  8     32
   i3.4xlarge.4  16    64
   i3.8xlarge.4  32    128
   i3.12xlarge.4 48    192
   i3.16xlarge.4 64    256
   ============= ===== ==================

.. table:: **Table 4** ECS flavors allowed on i3_pro DeHs

   ============= ===== ==================
   ECS Flavor    vCPUs Memory (RAM in GB)
   ============= ===== ==================
   i3.2xlarge.8  8     64
   i3.4xlarge.8  16    128
   i3.8xlarge.8  32    192
   i3.12xlarge.8 48    256
   i3.16xlarge.8 64    512
   ============= ===== ==================
