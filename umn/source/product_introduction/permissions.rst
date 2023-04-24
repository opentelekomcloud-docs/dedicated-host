:original_name: deh_01_0009.html

.. _deh_01_0009:

Permissions
===========

Background
----------

If you need to assign different permissions to employees in your enterprise to access your DeH resources, IAM is a good choice for fine-grained permissions management. IAM provides identity authentication, permissions management, and access control, helping you securely manage access to your cloud resources.

With IAM, you can create IAM users under your account for your employees, and assign permissions to the users to control their access to specific resource types. For example, some software developers in your enterprise need to use DeH but should not be allowed to delete other DeH resources or perform any other high-risk operations. In this scenario, you can create IAM users for the software developers and grant them only the permissions required for using DeH resources.

If your account does not need individual IAM users for permissions management, you may skip over this chapter.

IAM is free. You pay only for resources purchased using your account. For more information about IAM, see Identity and Access Management User Guide.

DeH Permissions
---------------

By default, new IAM users do not have permissions assigned. You need to add a user to one or more groups, and attach permissions policies or roles to these groups. Users inherit permissions from their groups and can perform specified operations on cloud services.

DeH is a project-level service deployed in specific physical regions. When you grant DeH permissions to a user group, set **Scope** to **Region-specific projects** and then select projects for the permissions to take effect. If you select **All projects**, the permissions will take effect for the user group in all region-specific projects. When accessing DeH, the users need to switch to a region where they have been authorized to use this service.

You can grant users permissions by using roles and policies.

-  Roles: A type of coarse-grained authorization mechanism that defines permissions related to users responsibilities. Only a limited number of service-level roles for authorization are available. If one role has a dependency role required for accessing DeH, assign both roles to the users. Roles are not ideal for fine-grained authorization and secure access control.
-  Policies: A fine-grained authorization mechanism that defines permissions required to perform operations on specific cloud resources under certain conditions. This mechanism allows for more flexible policy-based authorization, meeting requirements for secure access control. For example, the account administrator can allow IAM users to perform specified management operations on a type of DeH resources.

:ref:`Table 1 <deh_01_0009__table0407109181314>` describes all system permissions of DeH.

.. _deh_01_0009__table0407109181314:

.. table:: **Table 1** DeH system permissions

   +--------------------+-------------------------------------------------------------------------------+-----------------------+
   | Role/Policy Name   | Description                                                                   | Category              |
   +====================+===============================================================================+=======================+
   | DeH FullAccess     | DeH administrator, who has all permissions of DeH                             | System-defined policy |
   +--------------------+-------------------------------------------------------------------------------+-----------------------+
   | DeH ReadOnlyAccess | Read-only permission on DeHs. Users with this permission can only query DeHs. | System-defined policy |
   +--------------------+-------------------------------------------------------------------------------+-----------------------+

:ref:`Table 2 <deh_01_0009__table15562229183816>` lists the common operations supported by each system-defined permission of DeH. Select the permissions as needed.

.. _deh_01_0009__table15562229183816:

.. table:: **Table 2** Common operations supported by each system-defined policy or role

   +-----------------------------------------------------------+----------------+----------------------+--------------------+
   | Operation                                                 | DeH FullAccess | DeH CommonOperations | DeH ReadOnlyAccess |
   +===========================================================+================+======================+====================+
   | DeHs                                                      | Y              | x                    | x                  |
   +-----------------------------------------------------------+----------------+----------------------+--------------------+
   | Releasing DeHs                                            | Y              | x                    | x                  |
   +-----------------------------------------------------------+----------------+----------------------+--------------------+
   | Querying DeHs                                             | Y              | Y                    | Y                  |
   +-----------------------------------------------------------+----------------+----------------------+--------------------+
   | Querying Details of a DeH                                 | Y              | Y                    | Y                  |
   +-----------------------------------------------------------+----------------+----------------------+--------------------+
   | Modifying DeH Attributes                                  | Y              | Y                    | x                  |
   +-----------------------------------------------------------+----------------+----------------------+--------------------+
   | Querying Available DeH Types                              | Y              | Y                    | Y                  |
   +-----------------------------------------------------------+----------------+----------------------+--------------------+
   | Querying DeH Resource Types                               | Y              | Y                    | Y                  |
   +-----------------------------------------------------------+----------------+----------------------+--------------------+
   | Querying DeH Resource Type Details                        | Y              | Y                    | Y                  |
   +-----------------------------------------------------------+----------------+----------------------+--------------------+
   | Querying Available DeH Types                              | Y              | Y                    | Y                  |
   +-----------------------------------------------------------+----------------+----------------------+--------------------+
   | Querying DeH Resource Types                               | Y              | Y                    | Y                  |
   +-----------------------------------------------------------+----------------+----------------------+--------------------+
   | Querying the AZ to Which a DeH Resource Type Is Bound     | Y              | Y                    | Y                  |
   +-----------------------------------------------------------+----------------+----------------------+--------------------+
   | Querying the Flavor to Which a DeH Resource Type Is Bound | Y              | Y                    | Y                  |
   +-----------------------------------------------------------+----------------+----------------------+--------------------+
   | Querying the Tenant Quota                                 | Y              | Y                    | Y                  |
   +-----------------------------------------------------------+----------------+----------------------+--------------------+
   | Creating a DeH Tag                                        | Y              | Y                    | x                  |
   +-----------------------------------------------------------+----------------+----------------------+--------------------+
   | Deleting a DeH Tag                                        | Y              | Y                    | x                  |
   +-----------------------------------------------------------+----------------+----------------------+--------------------+
   | Querying Tags of a DeH                                    | Y              | Y                    | Y                  |
   +-----------------------------------------------------------+----------------+----------------------+--------------------+
   | Querying DeH Tags Created by a Tenant                     | Y              | Y                    | Y                  |
   +-----------------------------------------------------------+----------------+----------------------+--------------------+
   | Querying DeHs by Tag                                      | Y              | Y                    | Y                  |
   +-----------------------------------------------------------+----------------+----------------------+--------------------+
   | Querying ECSs on a DeH                                    | Y              | Y                    | Y                  |
   +-----------------------------------------------------------+----------------+----------------------+--------------------+
