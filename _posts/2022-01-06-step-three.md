---
layout: default
title:  "Step Three"
date:   2022-01-06 12:00:00 -0400
categories: jekyll update
---
## Create the Excel Spreadsheet

Power Apps can connect with data from a variety of sources. One such source is Microsoft Excel. All product information will be store within an Excel spreadsheet that'll be converted into a table. The spreadsheet should contain the following product information:

- Product name
- Path to the product's 3D model
- Price
- Description
- Category
- Path to the product's image

Power Apps will use the product information within the table alongside the image and model folders that were created in the prior step to display Contoso Furnishings' products in the app.

**Note**: The format and structure of the Excel spreadsheet is **very** important and must be created in the order and format as explained. If you have trouble viewing the product information in the Contoso Furnishings app, come back to this step and ensure that all steps were followed as they're written.

## Instructions

Complete the steps below to create the product information Excel spreadsheet and table.

1. In the browser, navigate to [portal.office.com/onedrive](https://portal.office.com/onedrive).
1. Inside the **Workshop** folder, click **+ New** and select **Excel workbook**. A new Excel workbook will open in the browser.
1. At the top right of the Excel workbook, click **Book - Saved** and change the **File Name** to **products**.

    ![A screenshot of the Excel window. The file name is highlighted.]({{ site.baseurl }}/images/4-file-name.jpg)

1. In the spreadsheet, create the following headers (**Note**: These headers are case sensitive):
	- Name
	- 3DModel [image]
	- Price
	- Description
	- Category
	- Picture [image]
1. In the spreadsheet, add the following product information below the headers:

    |Name  |3DModel [image]  |Price |Description  |Category |Picture [image]|
    |---------|---------|---------|---------|--------|--------|
    |Bookcase     |.\Models\bookshelf_modern.glb         |   695      |    Lorem ipsum dolor sit amet.     |  Office      |  .\Photos\bookshelf_modern.png      |
    |Coffee Grinder     | .\Models\coffee_grinder.glb        |  129       |   Lorem ipsum dolor sit amet.      |  Kitchen      |  .\Photos\coffee_grinder.png      |
    |Espresso Machine     | .\Models\espresso_machine.glb        |   150      |  Lorem ipsum dolor sit amet.       |   Kitchen     |  .\Photos\espresso_machine.png      |
    |Industrial Table    | .\Models\industrial_table.glb        | 375        |  Lorem ipsum dolor sit amet.       |   Office     |   .\Photos\industrial_table.png     |
    |Arm Chair     | .\Models\modern_armchair.glb        |   299      |    Lorem ipsum dolor sit amet.     |   Living Room     |  .\Photos\modern_armchair.png      |
    |Sofa     |  .\Models\modern_sofa.glb       |   650      |  Lorem ipsum dolor sit amet.       |   Living Room     |  .\Photos\modern_sofa.png      |
    |Night Stand     | .\Models\nightstand.glb        |   230      |   Lorem ipsum dolor sit amet.      |   Bedroom     |    .\Photos\nightstand.png    |
    |Standing Desk     |  .\Models\standing_desk.glb       |  300       |   Lorem ipsum dolor sit amet.      |  Office      |  .\Photos\standing_desk.png      |

    **Note**: If you are manually typing the 3DModel [image] and Picture [image], be sure to override Excel's suggestions for formatting. These two columns are using relative links which references the Models and Photos folders within the Workshop folder. If the paths are entered incorrectly, the product's 3D model and/or image will not display properly in the Contoso Furnishings app.

1. After the rows are complete, highlight all the columns and rows that contain data.
1. At the top of the Excel browser, click **Insert** > **Table** to create a table of the data.
1. In the **Create Table** pop-up that appears, confirm that your data range is correct (ex: A1:F9) and check the **My table has headers** box.

    ![A screenshot of the create table window. The my table has headers field is highlighted.]({{ site.baseurl }}/images/4-create-table.jpg)

1. In the **Create Table** pop-up, click **OK**.
1. After the table is created, click **Table Design** within the top of the Excel browser (this may be next to **Help**).
	
    **Note**: If you do not see **Table Design**, click on any of the cells containing data. This will activate the tab.
1. At the top far left of the Excel browser, change the table name to **Products**.

    ![A screenshot of the Excel window. The table name is highlighted.]({{ site.baseurl }}/images/4-table-name.jpg)

<ul class="actions">
<li><a href="https://aprilspeight.github.io/workshop-mr-powerapps/jekyll/update/2022/01/07/step-two.html" class="button special">Back</a></li>
<li><a href="https://aprilspeight.github.io/workshop-mr-powerapps/jekyll/update/2022/01/05/step-four.html" class="button">Next</a></li>
</ul>