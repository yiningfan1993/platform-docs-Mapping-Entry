**********************
Annotator
**********************

Other than managing the mapping projects, the admin user is also responsible for managing the users that will be participating in the projects, ie. the :dfn:`Annotators`. To support this, the following tools are provided under the Annotator tab.

   * :ref:`add-annotator`
   * :ref:`Annotator:List of Annotator`

      * :ref:`disable-annotator`
      * :ref:`disabled-annotators`
      * :ref:`change-annotator-role`
      * :ref:`show-or-change-annotator-tags`
   * :ref:`annotator-tags`

.. figure:: /images/AnnotatorTabContent.png
   :width: 1000
   :align: center
   :alt: Annotator Management Tab

   *Annotator Management Tab*

.. _add-annotator:

Add Annotator |AddAnnotatorButton|
============================================================
To allow a new user to start participating in the mapping annotation projects, the admin user can use the |AddAnnotatorButton| button to manually add an **existing** platform user to the Vector Annotator Application by specifying their email and annotator role.

.. figure:: /images/AddAnnotatorPopUp.png
   :width: 400
   :align: center
   :alt: Add Annotator Pop-Up

   *Add Annotator Pop-Up*


.. _annotator-requests:

Annotator Requests |ShowRequestsButton|
============================================================
The Admin user can use the |ShowRequestsButton| button to obtain a list of historical requests that users have submitted to register as an Annotator through the :ref:`tools:Annotator Role Registration` tool. That includes the approved, rejected, and pending requests. The Admin user will be able to approve or reject a pending request.



List of Annotator
============================================================
A list of the current Annotators are listed under the Annotator Management tab, with their :dfn:`Name`, :dfn:`Email`, and :dfn:`Role`. The Admin user can filter on search for Annotators and also use the |AnnotatorDetailsButton| to view more details of an Annotator.

Other than viewing information about Annotators, the following actions can be performed on each Annotator:

   * :ref:`disable-annotator`
   * :ref:`change-annotator-role`
   * :ref:`show-or-change-annotator-tags`

.. figure:: /images/AnnotatorList.png
   :width: 1000
   :align: center
   :alt: Annotator List

   *Annotator List*

.. _disable-annotator:

Disable Annotator |DisableUserButton|
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Clicking on the |DisableUserButton| button disables the target Annotator. The Annotator will not be able to access mapping entry nor any of the mapping projects. The Admin user can use the |ShowDisabledButton| :ref:`disabled-annotators` tool to see a complete list of disabled Annotators and re-enable them if needed.


.. _disabled-annotators:

Disabled Annotators |ShowDisabledButton|
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
The Admin user can click the |ShowDisabledButton| button to bring up a list of Annotators that had been disabled. They can also use the |ReEnableButton| button to re-enable an Annotator if they wish.

.. figure:: /images/DisabledAnnotators.png
   :width: 500
   :align: center
   :alt: List of Disabled Annotators

   *List of Disabled Annotators*


.. _change-annotator-role:

Change Annotator Role |UpdateRoleButton|
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
The :ref:`role<annotator-roles>` of an Annotator can be changed at any time by the Admin user using the |UpdateRoleButton| button.

.. _show-or-change-annotator-tags:

Show or Change Annotator Tags |ShowTagsButton|
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
:ref:`Annotator tags<annotator-tags>` can be created for easier access management. The Admin user can also view or chnage the Annotation tag of any user using the |ShowTagsButton| tool.

.. figure:: /images/ShowAnnotatorTags.png
   :width: 400
   :align: center
   :alt: Annotator Tags of an Example Annotator

   *Annotator Tags of an Example Annotator*


.. _annotator-tags:

Manage Annotator Tags |AnnotatorTagsButton|
============================================================
All the Annotator Tags are displayed and can be managed with the |AnnotatorTagsButton| tool.

.. figure:: /images/ManageAnnotatorTags.png
   :width: 800
   :align: center
   :alt: Annotator Tags Management

   *Annotator Tags Management*
..

   * Use |BlueNewButton| to add a new tag.
   * Click on the name of an existing tag for more actions:

      * Use |DeleteTagButton| to delete the selected tag.
      * Use |RenameTagButton| to rename the selected tag.
      * Use |ShowMembersButton| to display a table of all Annotators with the selected tag on the right panel.
      * Use |HideMembersButton| to hide the table of tagged Annotators on the right panel.

   * When a table of tagged Annotators is displayed on the right panel:

      * Use |AddUsersButton| to add one or multiple Annotators under the selected tag.
      * Use the checkboxes to select one or multiple Annotators and click |RemoveUsersButton| to remove the selected tag for them.


.. |AddAnnotatorButton| image:: /images/AddAnnotatorButton.png
      :height: 20

.. |ShowRequestsButton| image:: /images/ShowRequestsButton.png
      :height: 20

.. |AnnotatorDetailsButton| image:: /images/AnnotatorDetailsButton.png
      :height: 20

.. |DisableUserButton| image:: /images/DisableUserButton.png
      :height: 20

.. |ReEnableButton| image:: /images/ReEnableButton.png
      :height: 20

.. |UpdateRoleButton| image:: /images/UpdateRoleButton.png
      :height: 20

.. |ShowTagsButton| image:: /images/ShowTagsButton.png
      :height: 20

.. |AnnotatorTagsButton| image:: /images/AnnotatorTagsButton.png
      :height: 20

.. |BlueNewButton| image:: /images/BlueNewButton.png
      :height: 20

.. |RenameTagButton| image:: /images/RenameTagButton.png
      :height: 20

.. |ShowMembersButton| image:: /images/ShowMembersButton.png
      :height: 20

.. |HideMembersButton| image:: /images/HideMembersButton.png
      :height: 20

.. |AddUsersButton| image:: /images/AddUsersButton.png
      :height: 20

.. |RemoveUsersButton| image:: /images/RemoveUsersButton.png
      :height: 20

.. |ShowDisabledButton| image:: /images/ShowDisabledButton.png
      :height: 20

.. |DeleteTagButton| image:: /images/DeleteTagButton.png
      :height: 20