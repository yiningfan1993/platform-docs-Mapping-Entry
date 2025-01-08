**********************
Order List
**********************

Order list is a centralized space for users to create order, manage order, monitor order status and review deliverables. 

 .. figure:: /images/OrderListInterface.png
    :align: center
    :alt: OrderListInterface

    *General Interface of Order List*

Create Order
******************

Users can start a new order by clicking on the |CreateOrder| button located on the top-right of the interface. 

.. The following options will be available:

.. Service type:

..    * Modeling & Annotation: the order will apply modeling and Ecopia annotation as the service;
..    * Modeling: the order will apply modeling and users will annotate the vector result (if applicable) within their own organization.

Click on "Submit" after setting the order name, the order list page will jump to basic settings page for users to provide more detailed information. The settings page can also be opened by clicking |ViewDetails| in the action column of each order.

Action: Settings |ViewDetails|
*************************************

Users can view and edit details of the order by clicking on |ViewDetails| button in the action column. The order list page will jump to basic settings once a new order is created for users to provide more information about the order.

Input Data
===============

This page contains setting information for order's AOI and corresponding imagery data that will be used for production.

Order's AOI Data
------------------

Add AOI Data
++++++++++++++

By clicking :guilabel:`Add AOI` button on the top right corner, users can upload the AOI file from local machine or through S3 buckets. Once uploaded, the AOI will be listed under **AOI Data** section of the page.

 .. figure:: /images/AddAOILocalDrive.png
    :align: center
    :alt: AddAOILocalDrive

    *Add AOI via Local Drive*

 .. figure:: /images/AddAOIS3.png
    :align: center
    :alt: AddAOIS3

    *Add AOI via S3*

.. note::
      The AOI file needs to be in zipped shapefile format and smaller than 4 MB.


AOI Actions
++++++++++++++

The following actions are available for uploaded AOI files.


    #. Preview AOI |PreviewAOI|: By clicking |PreviewAOI| button, users can review the uploaded AOI file overlay with Google Maps.
    #. Remove AOI |DeleteAOI|: AOI will be removed once click on the |DeleteAOI| button.


Order's Imagery Data
----------------------------

Add Imagery
++++++++++++

Imagery datasets that will be used for this order are listed in this section. By clicking on the :guilabel:`Add Imagery` button in the **Imagery Data** section, users can add imagery data to the order by providing the following information:

    * Imagery Type:

        * Single View: single view imagery for 2D feature extraction
        * Multi View: multi-view imagery for 3D production

    * Location: 

        * Local Drive: upload by drag-and-drop or navigate to the location of the file on local machine
        * Cloud Service: S3 bucket that store the imagery data or through partnered imagery provider

            * Own S3: customers own S3 path with corresponding access key and secret access key
            * Ecopia S3: system generated Ecopia S3 bucket paired with access key and secret access key for users to upload imagery datasets to designated S3 buckets
            * Imagery Provider: download imagery through imagery provider by providing resolution (mandatory) and vintage (not mandatory).
    

.. figure:: /images/AddStandardImagery.png
    :alt: AddStandardImagery
    :align: center

    *Add Standard Imagery*

After the information is provided, click on :guilabel:`Submit`. The newly create imagery dataset will be listed in **Imagery Data** section. In the meantime, system will process the imagery automatically and run coverage check against the AOI. 

Imagery Data Action
+++++++++++++++++++++

The following actions are available for uploaded imagery datasets:

    #. Edit Imagery |Edit|: users can edit imagery datasets by adjusting the location information;
    #. Delete Imagery |DeleteAOI|: users can remove the uploaded imagery dataset by clicking on this button.


Coverage Check
-----------------
If the provided imagery failed to cover the entire provided AOI, the following notification will appear in the input data section. 

.. figure:: /images/CoverageCheck.png
    :alt: CoverageCheck
    :align: center

    *Coverage Check Notification*


Extraction Settings
====================

This space allows users to select desired features (Catetitle) to be extracted from the provided imagery.

#. A list of standard product packages are listed on top of the catetitles. Users can select one or multiple and corresponding catetiles will be automatically selected in the catetitle list below.
#. Select Catetitle: by clicking on the checkbox next to each Catetitle

    * Catetitles are categorized into 3 different Categories:
        * **Raster**: include DSM and orthomosaic data generated through production pipeline
        * **2D Landcover**: includes building, road, manmade and natural landcover features; height attribute can be selected to construct 3D landcover data
        * **Advanced Transportation**: includes different types of transportation related centerlines, polygons, points and other transportation features that can be used for guiding and navigation
        * **Non-Standard**: features that are not derived through modeling. Features have neem categorized into centerlines, road lines, polygons, and signs.
            
            * users can also define new categories by clicking on :guilabel:`+ Add Category` button. In the pop-up window, category name, geometry tyoe, definition, image example, and annotate rules are required to create this new category.

    * For definition of each Catetitle, please refer to Glossary for more details.


#. Users can select the category in general or select second-tier categories to further differentiate the features

    .. figure:: /images/SecondTier.png
        :alt: Second-Tier Categories
        :align: center

        *Example of Second-Tier Category*

#. Selected Catetitles will be reflected in the **Advanced settings for selected products** section in the settings
#. In the **Advanced settings for selected products** section, users can modify the catetitle name in the delivery shapefile.
    
    * Catetitle name in the delivery shapefile can be modified by clicking on the edit button;
    * Special capturing rules can be added to advance settings to provide production team with clear instructions.


        .. figure:: /images/catetitleAdvancedSettings.png
            :alt: Catetitle Advanced Settings
            :align: center

        *Catetitle Advanced Settings*


#. To help Ecopia team better understand the extraction requirements, users can attach supporting document in the **Attached Document for Extraction Request** section.
#. Click on "Save & Continue" to apply the changes and continue to Area of Interest.

 .. figure:: /images/ExtractionSettings.png
    :align: center
    :alt: ExtractionSettings
    

    *Extraction Settings*







Delivery Settings
====================

Users can define how the data should be delivered by providing the following information in the delivery settings section:

#. **Delivery Projection**: projection system that should be applied to the vector result. The following options are available:

    * WGS84
    * WGS84/UTM
    * OTHER
    * Provide EPSG and added as an option

#. **Delivery Format**: data format that the vector result will be delivered in
#. **Deliver Grid Size**: grid can be applied to the vector result to split larger polygon into smaller pieces. 

Click on "Save & Continue" to apply all changes and move to **Order Payment** section.

Quote & Place Order
=====================

Once the AOI information and extraction settings are provided through previous pages, users can obtain quote information and place order to put the order into production.

Quote
----------------------------
User can obtain quote information by clicking on the :guilabel:`Quote` button. At this stage, the system is calculating the quote for the order based on the extraction settings and size of the AOI. The process will normally take a few minutes to complete.

.. figure:: /images/CalculatingQuote.png
    :alt: Calculating Quote
    :align: center

    *Quote is being Calculated*

The following information will be provided:

    #. **Cost Quotation(USD)**: quotation for this prodction order in USD;
    #. **Delivery Days**: number of days required for production team to deliver the result;
    #. **Quotation Expired Time**: the expiration time of the current quote
    #. **Order Place Status**: current status of the order

        * Not Applied: the order has not been placed by the current users.
        * Order has been placed at ... : order has been placed at certain time stamp and system has sent notification to the production admin.

Place Order
----------------------------
Once the quote is calculated, users can place order by clicking on the :guilabel:`Place Order`. After the order is placed, the production team will receive notification and the production process will be triggered.

.. figure:: /images/PlaceOrder.png
    :alt: PayNow
    :align: center

    *Order is ready to be placed*


Action: Delete Order |DeleteAOI|
*********************************
Users can delete an order by clicking on the |DeleteAOI| button in the action column.


Action: Delivery |Delivery|
*********************************
Email notification will be sent to order owner once the vector result is delivered. By clicking on the |Delivery| button, users can view the deliveries and their path on the platform. To download the vector results


Action: Feedback |Feedback|
*********************************
Users can provide feedback to the current order based on the quality and timing of the delivery.



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

.. |Edit| image:: /images/Edit.png
      :height: 30

.. |Feedback| image:: /images/Feedback.png
      :height: 30