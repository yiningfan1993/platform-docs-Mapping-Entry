**********************
Quotation
**********************


The :guilabel:`Quotation` function of the mapping entry contains an estimatation tool that allow users to quickly obatin information about the size of the area of interest (AOI) and number of buildings inside of this AOI.

.. figure:: /images/quotation/quotation_tab.png
    :align: center
    :alt: The Quotation Tab


    *The Quotation Function*

|


Quotation Table
########################

The following fields are included in the Quotation Table:
    1. **Package ID**: unique identifier for the quotes;
    2. **File ID**: unique identifier for the AOI files;
    3. **Location**: AOI file location; users can directly download previously uploaded AOI files from the table;
    4. **Submitted User**: usernames of the users who uploaded the file;
    5. **Job Status**: indicator for status of quotation generation;
    6. **Area (km2)**: size of the AOI in km2;
    7. **Buildings**: number of buildings inside of the AOI;
    8. **Group Column**: the field to group polygons in the AOI file. **Null** by default;
    9. **Area Column**: the field that indicates the size of the plygons in AOI file. **Null** by default;
    10. **Created**: creation time of the quotes

On the right hand side there are two functions that are available to the users:
    1. View Report |viewreportbutton|: by clicking |viewreportbutton|, a detailed quote report will be generated based on the selected AOI.
    2. Detele AOI |deleteaoibutton|: by clicking |deleteaoibutton|, the AOI and its corresponding quote entry will be removed from the quotation table.




Create New Quote
########################

New quotes can be created by clicking :guilabel:`+ New Quote` on the top right of the quotation table, a window will pop-up for users to upload the AOI file.

.. figure:: /images/quotation/Upload_Quotation_File.png
    :align: center
    :alt: Upload Quotation File
    :height: 360


    *Upload Quotation File*

In the **Select AOI File** area, click in the empty space to navigate to the location of zipped AOI shapefile on local machine or drag the zipped shapefile into the empty area.
Once the file is listed below, click on :guilabel:`Start Upload` to upload the zipped AOI file to the quotation tool.

.. figure:: /images/quotation/Uploaded_AOI.png
    :align: center
    :alt: Uploaded AOI
    :height: 360


    *Zipped AOI file uploaded to the quotation tool*

Once the upload is completed, users can click :guilabel:`Submit` to trigger the estimation process.

Obtain Quotes
########################

After clicking :guilabel:`Submit`, the interface will return to the quotation table. The newest quote will be listed at the top of the table. 
There are four different statuses for each quotation job:

    1. **Pending**: the quotation job is still running for the quote and the number of buildings in the AOI is still being generated;
    2. **Finished**: the quotation job is finished. Users can obtain area and building count information from the table or quotation report |viewreportbutton|;
    3. **Error**: the quotation job is failed. Users need to check the AOI file and re-run the quotation job;
    4. **Invalid**: the AOI file is invalid. Users need to check the validity of the AOI file, fix the AOI shapefile and re-run the quotation tool again.

The initial status of a new quote is **Pending** as the building count is being generated. Once the status turns to **Finished**, users can obtain the quote by using the quotation table or view quotation report |viewreportbutton|.

.. figure:: /images/quotation/QuotationReport.png
    :align: center
    :alt: The Quotation Report
    :height: 360


    *The Quotation Report*


.. |viewreportbutton| image:: /images/quotation/viewreportbutton.png
      :height: 30

.. |deleteaoibutton| image:: /images/quotation/detelebutton.png
      :height: 30