:original_name: deh_01_0052.html

.. _deh_01_0052:

Creating a Custom Policy
========================

Custom policies can be created to supplement the system-defined policies of DeH.

You can create custom policies in either of the following ways:

-  Visual editor: Select cloud services, actions, resources, and request conditions. This does not require knowledge of policy syntax.
-  JSON: Edit JSON policies from scratch or based on an existing policy.

For details, see section "Creating a Custom Policy" in *Identity and Access Management User Guide*. The following section contains examples of common DeH custom policies.

Example Custom DeH Policies
---------------------------

-  Example 1: Authorize users to purchase and release DeHs.

   .. code-block::

      {
            "Version": "1.1",
            "Statement": [
                  {
                        "Effect": "Allow",
                        "Action": [
                              "deh:dedicatedHosts:create",
                              "deh:dedicatedHosts:create"
                        ]
                  }
            ]
      }

-  Example 2: Deny the DeH release request.

   A deny policy must be used together with other policies. If the permissions assigned to a user contain both "Allow" and "Deny", the "Deny" permission takes precedence over the "Allow" permission.

   If you assign the DeH FullAccess system policy to a user but do not want the user to have the permission to release DeHs, you can create a policy to deny the release of DeHs and grant both the DeH FullAccess policy and the created policy to the user. In this case, the "Deny" policy takes precedence and the user can perform all operations except DeH release. The following is an example of a deny policy:

   .. code-block::

      {
              "Version": "1.1",
              "Statement": [
                      {
                              "Action": [
                                      "deh:dedicatedHosts:delete"
                              ],
                              "Effect": "Deny"
                      }
              ]
      }
