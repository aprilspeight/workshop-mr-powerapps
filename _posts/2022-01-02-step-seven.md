---
layout: default
title:  "Step Seven"
date:   2022-01-02 12:00:00 -0400
categories: jekyll update
---
## Create Product Information Screen

Once a customer selects a product from the Gallery page, they should be taken to a Product Information screen which displays more information about the product such as:

- Product name
- Product description
- Price

## Instructions

Complete the steps below to create the Product Information screen.

### Create a Product Information Screen with Navigation

1. In the top navigation menu, click **New Screen** > **Blank**.
1. In the left panel, rename the new screen **ProductInformation**.
1. In the top navigation, click **Insert** > **Icons** and select the **Back** icon.
1. In the left panel, rename the **Icon** component **BackButton**.

    ![A screenshot of the tree view. The Back Button component is highlighted.]({{ site.baseurl }}/images/7-back-button-name.jpg)

1. Move the **BackButton** to align to the top left of the screen.

    ![A screenshot of the canvas app. The back button is aligned at the top left of the app.]({{ site.baseurl }}/images/7-back-button-icon.jpg)

1. In the formula bar, for **OnSelect** enter `Navigate(Home,ScreenTransition.Fade)`.
1. Test the app to confirm that the button navigates back to the **Home** screen.

### Create Navigation to the Product Information Screen

1. In the **Tree View** tab, select the **Home** screen.
1. In the first row of the **ProductGallery** click the **>** icon.

    ![A screenshot of the home screen for the canvas app. The right arrow icon is highlighted.]({{ site.baseurl }}/images/7-arrow-icon.jpg)

1. In the **formula bar**, for **OnSelect** enter `Navigate(ProductInformation,ScreenTransition.Fade)`.
1. Test the app to confirm that the button navigates to the **Product Information** screen.

### Add the Product Information

1. In the **Tree View** tab, select the **ProductInformation** screen.
1. In the **Insert** tab, click **Text label** to add a label for the product name.
1. Rename the **Text label** component **ProductName**.
1. In the formula bar, for **Text** enter `ProductGallery.Selected.Name`.
1. In the **Insert** tab, click **Text label** to add a label for the product description.
1. Rename the **Text label** component **ProductDescription**.
1. In the formula bar, for **Text** enter `ProductGallery.Selected.Description`.
1. In the **Insert** tab, click **Text label** to add a label for the product's price.
1. Rename the **Text label** component **ProductPrice**.
1. In the formula bar, for **Text** enter `"$" & ProductGallery.Selected.Price`.
1. Move and rearrange all the labels to display on the bottom half of the screen. Feel free to change text properties for the labels (ex: font, size, etc.).

    The **Tree view** should reflect the following:

    ![A screenshot of the tree view. The product information components are highlighted.]({{ site.baseurl }}/images/7-product-information-elements.jpg)

    The **ProductInformation** screen should reflect the following:

    ![A screenshot of the product information screen for the canvas app. The screen consists of a back button, the product name, the product description, and the product price.]({{ site.baseurl }}/images/7-product-information.jpg)

1. Test the app to confirm that depending on the selected product, the correct information displays on the **ProductInformation** screen.

<ul class="actions">
<li><a href="https://aprilspeight.github.io/workshop-mr-powerapps/jekyll/update/2022/01/03/step-six.html" class="button special">Back</a></li>
<li><a href="https://aprilspeight.github.io/workshop-mr-powerapps/jekyll/update/2022/01/01/step-eight.html" class="button">Next</a></li>
</ul>