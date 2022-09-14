:original_name: deh_01_0010.html

.. _deh_01_0010:

Constraints
===========

-  ECSs automatically created by Auto Scaling (AS) will not be dispatched to DeHs, while ECSs created on DeHs can be manually added to AS groups.
-  Special ECSs, such as those with local disks or GPUs, cannot be migrated between DeHs or between the public resource pool and DeHs.
