**********************
Interface Walkthrough
**********************

Once users entered the Workflow Assembler Application, they will see the interface below, which contains the following main functions.

 .. figure:: /images/GeneralInterface.png
    :align: center
    :alt: General Interface

    *General Interface of Workflow Assembler App*

Sort
########

Sort function allows users to sort the items in the workflow element list based on the following criteria:

      #. **Alphabetic** |Alphabetic|: sort item list based on alphabetic order. This is the default order for all lists.
      #. **Created Time** |CreateTime|: sort item list based on time the items are created in descending order.


Item Types Dropdown
#######################

Users can switch the list among three workflow items:

      #. Gallery
      #. Workflow/Space
      #. Worker

Users can also use the search function below the dropdown to quickly locate the target item in the list.

Create New Item
##################

By clicking on the :guilabel:`Create` button, users can create a new workflow element with other customizations.

To create a new gallery, the following information needs to be provided:

      #. **Type**: Gallery
      #. **DAG Class**: Select between 2D and 3D
      #. **Name**: Name for the newly created Gallery. Can only contain letters, numbers and "_".
      #. **Advanced Config (optional)**: Set advanced configuration for this gallery if necessary.

 .. figure:: /images/CreateNewGallery.png
    :align: center
    :alt: Create New Gallery

    *Create New Gallery*

|


To create a new workflow/space, the following information needs to be provided:

      #. **Type**: Workflow/Space
      #. **Sub Type**: Select between workflow and space
      #. **Name**: Name for the workflow/space. Can only contain letters, numbers and "_".
      #. **Workflow Type**: Specify the workflow type (new workflow only)
      #. **Advanced Configuration (optional)**: Set advanced configuration for this gallery if necessary.

 .. figure:: /images/CreateNewWorkflowSpace.png
    :align: center
    :alt: Create New Workflow/Space

    *Create New Workflow/Space*

Item List
#############

All existing items will be listed in the item list. The list can be swtiched based on different types of items in the :ref:`tools:Item Types Dropdown`.

      #. By clicking on the title of the items in the list, the item details will be displayed in the :ref:`tools:DAG Graph Area`.
      #. By hovering the cursor over the title of the item in the list, users can click |Copy| to copy the name of the item.
      #. By clicking on the |Delete| button next to the item title, the item can be deleted from the list.

 .. figure:: /images/ItemList.png
    :align: center
    :alt: Item List
    :height: 300

    *Item List*


DAG Graph Area
################

DAG graph area depicts the workflow of selected item. Users can also customize the working item by adding or re-directing the process flow in the graph area.

View-Only Mode
****************

In view-only mode, users can view details of each node of the workflow by double-clicking on the dot that represents the node in the DAG graph.

 .. figure:: /images/ViewNodeDetail.gif
    :align: center
    :alt: View Node Detail

    *View Node Detail*

Users can go back to the previous workflow by clicking on the name in the hierarchy.

 .. figure:: /images/GoBacktoWorkflow.gif
    :align: center
    :alt: Go Back to Workflow

    *Go Back to Workflow*



To view more details of the workflow, the following actions are available:

    #. **Dragging Node**: Users can hold-click to drag the nodes inside of the DAG graph to gain better view of the workflow.
    #. **Panning Graph**: Users can pan to different area of the graph by hold-click on the empty space of the graph.
    #. **Zoom In/Out**: Users can zoom in/out in the graph area by scrolling the mouse wheel.



Edit Mode
************

By clicking on the |Edit| button on the top-right corner of the window, the edit mode is activated.

Under edit mode, users can perform following actions in the DAG graph.

Add/Remove Node
=================

By clicking the :guilabel:`+` button on top of the DAG graph area, users can add new node into the DAG graph. 

In the prompt window, users can either filter the selections using the **Filter Tags** or directly type the node name in the dropdown below to quickly locate the target note.

 .. figure:: /images/AddNode.png
    :align: center
    :alt: Add Node to DAG Graph
    :height: 300

    *Add Node to DAG Graph*

By clicking :guilabel:`OK` button, a new node will be added to the graph without any connection to the existing nodes.

 .. figure:: /images/AddNode.gif
    :align: center
    :alt: Add Node to DAG Graph

    *Add Node to DAG Graph*

After clicking on the target node and it is highlighted in blue, the selected node can be removed by clicking :guilabel:`-`. 

 .. figure:: /images/RemoveNode.gif
    :align: center
    :alt: Remove Node from DAG Graph

    *Remove Node from DAG Graph*

Create/Remove Connection Between Nodes
======================================================

There is no connection from or to the new node that is added to the graph. To create a connection to other node in the graph:

      #. Single-click on the starting node to highlight it.
      #. Double-click on the destination nodes, note that an arrow appears between the starting node to destination node, which means the connection is established. 

 .. figure:: /images/EstablishConnection.gif
    :align: center
    :alt: Establish a New Connection Between Nodes

    *Establish a New Connection Between Nodes*

To remove am existing connection, 
      
      #. Single-click on the connection line to highlight the connection.
      #. Click on :guilabel:`-`, same as one that removes node, on top of the DAG graph area to remove the connection. 
      #. In the prompt window, click :guilabel:`OK` to confirm the action. Notice that the connection between two nodes is removed.

 .. figure:: /images/RemoveConnection.gif
    :align: center
    :alt: Remove an Existing Between Nodes

    *Remove an Existing Between Nodes*

JSON Detail for Selected Item
#################################

This panel provides detailed description for selected item in JSON format. 

Users can:

      #. Navigate and expand the JSON file to see more details;
      #. Use copy to clipboard function to copy the whole or part of the JSON snippet out.

Advanced Configuration for Selected Item
##########################################

Users can view adavanced configuration for the selected items if it is available.

Add or Remove Items in Graph
##############################

After clicking |Edit| button on the top-right corner of the application to activate the editing mode


Actions: Edit, Save, Lock, Copy and Cancel Edit
#################################################

After users open an item from the list panel, the following tools are activated for users to modify the selected item. 


      #. **Edit**: By clicking on the |Edit| button, the editing mode is activated and users can edit the links/nodes in the DAG graph. Users can also cancel current editings by clicking on |CancelEdit| button.
      #. **Save**: By clicking on the |Save| button, all edits will be saved to the selected item that the user is currently working on.
      #. **Lock**: By clicking on the |Lock| button, users can lock current item and the current item cannot be edited unless it is unlocked by clicking |Unlock| button.
      #. **Copy**: By clicking on the |Copy| button, the currently selected item will be duplicated. By default, the duplicated item will have "_cp" in its name.
            
            .. figure:: /images/CopyItems.gif
                  :alt: Copy Item
                  :align: center

      #. **Full-screen**: By clicking on the |FullScreen| button, the DAG graph, JSON details and advanced configuration panels will enter full screen mode. Users can exit full-screen mode by clicking |ExitFullScreen|.




Current Breadcrumb Navigation
##############################

The breadcrumb navigation section indicates the hierarchy among gallery, workflow/space and worker. Users can navigate from gallery to worker or view any items in the hierarchy by clicking on the titles.

.. figure:: /images/BreadcrumbNavigation.gif
    :alt: Copy Item
    :align: center



.. |Edit| image:: /images/Edit.png
    :height: 21

.. |CancelEdit| image:: /images/CancelEdit.png
    :height: 21

.. |Save| image:: /images/Save.png
    :height: 21

.. |Lock| image:: /images/Lock.png
    :height: 21

.. |Unlock| image:: /images/Unlock.png
    :height: 21

.. |Copy| image:: /images/Copy.png
    :height: 21

.. |FullScreen| image:: /images/FullScreen.png
    :height: 21

.. |ExitFullScreen| image:: /images/ExitFullScreen.png
    :height: 21

.. |Delete| image:: /images/Delete.png
    :height: 21

.. |Alphabetic| image:: /images/Alphabetic.png
    :height: 21

.. |CreateTime| image:: /images/CreateTime.png
    :height: 21