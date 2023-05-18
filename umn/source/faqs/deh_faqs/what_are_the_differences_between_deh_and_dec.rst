:original_name: deh_faq_0007.html

.. _deh_faq_0007:

What Are the Differences Between DeH and DeC?
=============================================

-  Scenario

   DeC can provide a complete resource isolation solution by using dedicated services, such as Dedicated Distributed Storage Service (DSS) Dedicated Enterprise Storage Service (DESS), and Bare Metal Server (BMS).

   DeH can provide only isolated compute hosts, which are more flexible and suitable for customers who have requirements for computing resource isolation and flexibility.

-  Function

   You need to apply for an independent DeC account before requesting DeC resources. DeC resources and public ECSs belong to different VPCs. Common ECSs cannot be migrated to a DeC, and ECSs in a DeC cannot be migrated to common resource pools.

   ECSs created on a DeH and ECSs in the public resource pool share the same VPC. So, stopped ECSs can be migrated between a DeH and a resource pool.
