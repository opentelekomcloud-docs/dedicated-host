:original_name: deh_01_0051.html

.. _deh_01_0051:

Creating a User and Granting Permissions
========================================

This section describes how to use Identity and Access Management (IAM) to implement fine-grained permissions control for your DeH resources. With IAM, you can:

-  Create IAM users for employees based on your enterprise's organizational structure. Each IAM user will have their own security credentials for accessing DeH resources.
-  Grant only the permissions required for users to perform a specific task.
-  Use IAM to entrust a cloud account or cloud service to perform efficient O&M on your DeH resources.

If your cloud account does not require individual IAM users, skip over this section.

This section describes the procedure for granting permissions (see :ref:`Figure 1 <deh_01_0051__fig1515164216142>`).

Prerequisites
-------------

Learn about the permissions (see :ref:`Permissions <deh_01_0009>`) supported by DeH and choose policies or roles according to your requirements. For the permissions of other services, see `Permissions <https://docs.otc.t-systems.com/additional/permissions.html>`__.

Authorization Process
---------------------

.. _deh_01_0051__fig1515164216142:

.. figure:: /_static/images/en-us_image_0259246060.jpg
   :alt: **Figure 1** Process for granting DeH permissions

   **Figure 1** Process for granting DeH permissions

#. .. _deh_01_0051__li527593485415:

   `Creating a User Group and Assigning Permissions <https://docs.otc.t-systems.com/identity-access-management/umn/getting_started/creating_a_user_group_and_assigning_permissions.html>`__

   Create a user group on the IAM console, and assign the DeH ReadOnlyAccess permission to the group.

#. `Creating a User and Adding the User to a User Group <https://docs.otc.t-systems.com/identity-access-management/umn/getting_started/creating_a_user_and_adding_the_user_to_a_user_group.html>`__

   Create a user on the IAM console and add the user to the group created in :ref:`1 <deh_01_0051__li527593485415>`.

#. Log in and verify permissions.

   Log in to the management console using the created user, and verify that the user only has read permissions for DeH.

   -  Click **Service List** and choose **Computing** > **Dedicated Host**. On the displayed page, click **Buy DeH** in the upper right corner. If you cannot buy a DeH (after the DeH ReadOnlyAccess permission is assigned), the DeH ReadOnlyAccess permission has already taken effect.
   -  Choose any other service in the **Service List**. If a message appears indicating that you have insufficient permissions to access the service, the DeH ReadOnlyAccess policy has already taken effect.
