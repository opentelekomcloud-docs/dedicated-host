:original_name: deh_06_0002.html

.. _deh_06_0002:

Permissions and Supported Actions
=================================

This section describes fine-grained permissions management for your DeHs. If your account does not need individual IAM users, you may skip over this section.

By default, new IAM users do not have any permissions assigned. You need to add a user to one or more groups, and assign policies or roles to these groups. The user then inherits permissions from the groups it is a member of. This process is called authorization. After authorization, the user can perform specified operations on cloud services based on the permissions.

You can grant user permissions by using roles and policies.

-  Roles: A type of coarse-grained authorization mechanism that defines permissions related to user responsibilities. This mechanism provides only a limited number of service-level roles for authorization.
-  Policies: A type of fine-grained authorization mechanism that defines permissions required to perform operations on specific cloud resources under certain conditions. This mechanism allows for API-level policies for authorization, meeting requirements for secure access control.

.. note::

   Policy-based authorization is useful if you want to allow or deny the access to an API.

An account has all of the permissions required to call all APIs, but IAM users must have the required permissions specifically assigned. The permissions required for calling an API are determined by the actions supported by the API. Only users who have been granted permissions allowing the actions can call the API successfully. For example, if an IAM user queries the quota using an API, the user must have been granted permissions that allow the **deh:quotas:get** action.

Supported Actions
-----------------

DeH provides system-defined policies that can be directly used in IAM. You can also create custom policies to supplement system-defined policies for more refined access control. The following are related concepts:

-  Permissions: Allow or deny certain operations.
-  APIs: APIs that will be called for performing certain operations.
-  Actions: Operations that will be allowed or denied.
-  Dependent actions: When assigning permissions for an action, you also need to assign permissions for the dependent actions.
-  IAM projects or enterprise projects: Applicable scope of custom policies. For example, if an action supports both IAM and enterprise projects, the policy that contains this action will take effect for user groups assigned in IAM and Enterprise Management. If an action supports only IAM projects, the policy will take effect only for user groups assigned in IAM.

.. note::

   Y: supported; x: not supported
