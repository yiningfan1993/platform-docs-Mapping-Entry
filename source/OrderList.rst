**********************
Order List
**********************

Through partner order, users can create and place mapping project orders based on their own requirements. Different features can be extracted from the provided imagery. In addition, users can determine if the order processing is fully automated or requires human annotation at certain stages.

 .. figure:: /images/OrderListInterface.png
    :align: center
    :alt: OrderListInterface

    *General Interface of Order List*

Create Order
******************

Users can start a new order by clicking on the |CreateOrder| button located on the top-right of the interface. The following options will be available:

Service type:

    * Modeling & Annotation: the order will apply modeling and Ecopia annotation as the service;
    * Modeling: the order will apply modeling and users will annotate the vector result (if applicable) within their own organization.

Click on "Submit" after setting the order name and selecting service type, the order list page will jump to basic settings page for users to provide more detailed information. The settings page can also be opened by clicking |ViewDetails| in the action column of each order.

Action: Settings |ViewDetails|
*************************************

Users can view and edit details of the order by clicking on |ViewDetails| button in the action column. The page will jump to basic settings of the order by default. 

Basic Settings
===============

This page contains basic information about the order. Users can modify the name of the order, geography, industry, and delivery contaction information (Email) to an order that is not placed yet. Click on "Save & Continue" to apply the changes and continue to Extraction Settings.

 
Extraction Settings
====================

This space allows users to select desired features (Catetitle) to be extracted from the provided imagery.


#. Select Catetitle: by clicking on the checkbox next to each Catetitle

    * Catetitles are categorized into 3 different Categories:
        * **3D Buildings**: includes 3d_building, 3d_single_tree, DSM, and ortho_mosaic
        * **2D Landcover**: includes building, road, manmade and natural landcover features
        * **Advanced Transportation**: includes different types of centerlines, road marking, signs and other transportation features that can be used for guiding and navigation
    * For definition of each Catetitle, please refer to Glossary for more details.


#. Users can select the category in general or select second-tier categories to further differentiate the features
#. Selected Catetitles will be reflected in the **Selected Catetitles** section in the settings
#. To help Ecopia team better understand the extraction requirements, users can attach supporting document in the **Attached Document for Extraction Request** section.
#. Click on "Save & Continue" to apply the changes and continue to Area of Interest.

 .. figure:: /images/ExtractionSettings.png
    :align: center
    :alt: ExtractionSettings
    

    *Extraction Settings*

Area of Interest
====================

This section allows users to upload the area that the extraction needs to be done and add corresponding imagery data.

Order's AOI Data
------------------

By clicking on the space on the top right corner, users can upload the AOI file from local machine. Once uploaded, the AOI will be listed under **Order's AOI Data** section of the page.

.. note::
      The AOI file needs to be in zipped shapefile format and smaller than 4 MB.


AOI Actions
--------------------

Once the AOI and imagery data has been added to the order. The following actions needs to be completed before proceeding with the order.


Preview AOI |PreviewAOI|
+++++++++++++++++++++++++++++

By clicking |PreviewAOI| button, users can review the uploaded AOI file overlay with Google Maps.

Bind Dataset |binddataset|
+++++++++++++++++++++++++++++

By clicking |BindDataset| button, bind dataset prompt window will open and users can select from a list of existing imagery datasets to bind with the AOI. After locating the dataset that needs to be used, click on the :guilabel:`+` in the action column to bind the dataset.

.. figure:: /images/BindDatasetWindow.png
    :alt: BindDatasetWindow
    :align: center
    :height: 480

    *Bind Dataset Window*


Check Coverage |checkcoverage|
++++++++++++++++++++++++++++++++

Once the corresponding imagery dataset is processed and bound with target AOI properly, users can click |checkcoverage| button to review the coverage checking process in the coverage information window.

.. figure:: /images/CoverageInformationWindow.png
    :alt: Coverage Check Window
    :align: center
    :height: 480

    *Coverage Check Window*

The **AOI Status** and **Coverage** column will change accordingly based on the coverage check status.

.. list-table:: Coverage Check Status
   :widths: 30 30 70 70
   :header-rows: 1
   :class: tight-table

   * - Coverage Check
     - AOI Status
     - Coverage
     - Note
   * - Coverage check not started
     - AOI Init
     - Need to check
     - Click |CheckCoverage| button to start coverage check, or choose manual confirm
   * - Coverage check passed
     - Coverage Checked
     - |Passed|: Coverage check has passed
     - automatically switch to **Coverage Checked** Status
   * - Coverage check failed
     - AOI Init
     - Options:
        * |ViewCoverageReport|: Visualize AOI and missing area
        * |ManualConfirm|: Ignore missing area and proceed with current coverage
     - Email notification will be sent to order owner

Remove AOI |DeleteAOI|
++++++++++++++++++++++++++

AOI will be removed once click on the |DeleteAOI| button.

Imagery Timeline
---------------------------

 In order to have the system generate the most accurate estimate delivery time, users are required to provide **Expect Image Arrivel** time and confirm when the imagery actually arrives.


Order's Imagery Data
----------------------------

Imagery datasets that will be used for this order will be listed in this section. By clicking on the "Add Imagery" button in the **Order's Imagery Data** section, users can add imagery data to the order by providing the following information:

    * Name: name of the imagery data
    * Category: 2D or 3D imagery data
    * Imagery Type: Satellite or Aerial
    * Image Path: Ecopia provides different types of data transfer protocol. Users can select the one that best filt their needs from the protocol dropdown list.

.. figure:: /images/AddStandardImagery.png
    :alt: AddStandardImagery
    :align: center

    *Add Standard Imagery*

After the information is provided, click on "Submit". In the following window, bind the imagery data with AOI that will be used for feature extraction and click on "Confirm" to complete the imagery adding process.



Delivery Settings
====================

Users can define how the data should be delivered by providing the following information in the delivery settings section:

#. **Delivery Projection**: projection system that should be applied to the vector result. The following options are available:

    * WGS84
    * WGS84/UTM
    * OTHER
    * Provide EPSG and added as an option

#. **Delivery Format**: data format that the vector result will be delivered in
#. **Expect Delivery Date**: by clicking on the "Estimate Delivery" button to the right, users can obtain the earliest date that the system can deliver the vector results. Users can select any date after the system estimated earliest delivery date.
#. **Deliver Grid Size**: grid can be applied to the vector result to split larger polygon into smaller pieces. 

Click on "Save & Continue" to apply all changes and move to **Order Payment** section.

Order Payment
=====================

Users can follow the three stages of payment below to complete the payment process.

Payment is being Calculated
----------------------------
At this stage, Ecopia production admin has been notified and review the payment amount of the order.

.. figure:: /images/CalculatingPayment.png
    :alt: Calculating Payment
    :align: center

    *Payment is being Calculated*

Payment Can Be Made Now
----------------------------
At this stage, Ecopia production admin has reviewed and approved the order and amount to be paid. Order owner will be notified via Email once the order reach this stage.

.. figure:: /images/PayNow.png
    :alt: PayNow
    :align: center

    *Payment is Ready to be Made*

By clicking on the :guilabel:`Pay Now` button, the page will jump to checkout page where payment can be made.

.. figure:: /images/Checkout.png
    :alt: Checkout
    :align: center
    :height: 480

    *Checkout Page*

Order Has Been Paid
----------------------------
At this stage, the payment has been made and the vector result will be delivered once it is ready.


.. figure:: /images/PaidOrder.png
    :alt: PaidOrder
    :align: center

    *Order Has Been Paid*

Action: Delete Order |DeleteAOI|
*********************************
Users can delete an order by clicking on the |DeleteAOI| button in the action column.


Delivery |Delivery|
********************
Email notification will be sent to order owner once the vector result is delivered. By clicking on the |Delivery| button, users can view the deliveries and their path on the platform. To download the vector results


.. |CreateOrder| image:: /images/CreateOrder.png
    :height: 21

.. |ViewDetails| image:: /images/ViewDetails.png
    :height: 21

.. |binddataset| image:: /images/binddataset.png
    :height: 21

.. |checkcoverage| image:: /images/checkcoverage.png
    :height: 21

.. |ViewCoverageReport| image:: /images/ViewCoverageReport.png
      :height: 25

.. |ManualConfirm| image:: /images/ManualConfirm.png
      :height: 20

.. |Passed| image:: /images/GreenCheck.png
      :height: 20

.. |PreviewAOI| image:: /images/PreviewAOI.png
      :height: 25

.. |DeleteAOI| image:: /images/DeleteAOI.png
      :height: 32

.. |Delivery| image:: /images/Delivery.png
      :height: 30