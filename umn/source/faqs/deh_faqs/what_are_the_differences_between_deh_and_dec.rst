:original_name: deh_faq_0007.html

.. _deh_faq_0007:

What Are the Differences Between DeH and DeC?
=============================================

-  Scenarios

   DeC provides a complete resource isolation solution by using dedicated services, such as Dedicated Distributed Storage Service (DSS) Dedicated Enterprise Storage Service (DESS), and Bare Metal Server (BMS).

   DeH provides only isolated compute hosts, which are more flexible and suitable for customers who demand computing resource isolation and flexibility.

-  Functions

   You need to apply for an independent DeC account before requesting DeC resources. DeC resources and public ECSs work in different VPCs. You cannot migrate public ECSs to a DeC or ECSs in a DeC to a public resource pool.

   ECSs created on a DeH and ECSs in the public resource pool share the same VPC. So, you can migrate a stopped ECS between a DeH and a resource pool.
