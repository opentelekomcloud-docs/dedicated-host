:original_name: deh_01_0054.html

.. _deh_01_0054:

Disk-Intensive DeHs
===================

Overview
--------

Disk-intensive DeHs are classified as d1 DeHs. d1 DeHs provide high-performance hardware and large-capacity hard disk drives (HDDs), so that ECSs created on such type of DeHs can efficiently and sequentially read and write ultra-large data sets stored on local storage.

Disk-intensive ECSs can be deployed on d1 DeHs.

.. note::

   If a DeH is faulty, the data stored in local disks cannot be completely restored. Therefore, do not store important data in local disks.

DeH Specifications
------------------

.. table:: **Table 1** Specifications of d1 DeHs

   +-------------+-------------------+----------------------------+-------------------------------------------------------------------+-----------------+-------------------------------+
   | Flavor Type | Number of Sockets | Number of Cores per Socket | Hardware Specifications                                           | Number of vCPUs | Total Capacity of Local Disks |
   +=============+===================+============================+===================================================================+=================+===============================+
   | d1          | 2                 | 12                         | -  CPU: Intel® Xeon® Processor E5-2690 v3 (30 MB Cache, 2.60 GHz) | 40              | SAS disks: 24 x 1800 GB       |
   |             |                   |                            | -  Memory: 328 GB (or 335,872 MB)                                 |                 |                               |
   +-------------+-------------------+----------------------------+-------------------------------------------------------------------+-----------------+-------------------------------+

.. note::

   Number of vCPUs = (Number of sockets x Number of cores x Number of single-core threads - CPU overheads) x CPU overcommitment ratio

   -  d1 DeHs

      vCPUs = (2 x 12 x 2 - 8) x 1 = 40

ECSs Allowed on d1 DeHs
-----------------------

.. table:: **Table 2** ECS flavors allowed on d1 DeHs

   ========== ===== ================== =====================
   ECS Flavor vCPUs Memory (RAM in GB) Number of Local Disks
   ========== ===== ================== =====================
   d1.xlarge  4     32                 3
   d1.2xlarge 8     64                 6
   d1.4xlarge 16    128                12
   d1.8xlarge 36    256                24
   ========== ===== ================== =====================
