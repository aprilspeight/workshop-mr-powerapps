---
layout: default
title:  "Step Eight"
date:   2022-01-01 12:00:00 -0400
categories: jekyll update
---
## Add the View in 3D & View in MR Controls

To make the shopping experience interactive, the app is in need of Power Apps mixed reality controls that'll enable the customer to both view a 3D model of the product and view the 3D model within their own real-world environment. Power Apps provides two such mixed reality controls:

**View in 3D** - The View in 3D control enables you to view 3D content in the app. You can rotate and zoom into the model with simple gestures.

**View in Mixed Reality** - The View in MR control enables you to see how a particular item might fit within a specified space. The control creates a button in your app. When the customer clicks the button, it overlays the selected 3D model (in .glb, .stl, or .obj file formats) onto the live camera feed of their device.

Photos can be taken within the View in Mixed Reality control. Customers should be able to view photos taken within a gallery in the app.

## Instructions

Complete the steps below to add the View in 3D and View in MR controls to the Product Information screen.

### Add the View in 3D Control

1. In the left panel, click the **Tree View** icon, select the **ProductInformation** screen.
1. In the left panel, click the **Insert** icon and select **Media** > **View in 3D**.
1. On the **Select a data source** window that appears, select the **Products** data source.
1. In the formula bar, for **Source** enter `ProductGallery.Selected.'3DModel'`.
1. In the left panel, rename the **View in 3D** component **Product3D**.

    ![A screenshot of the tree view. The product 3 d control is highlighted.]({{ site.baseurl }}/images/8-product-3d.jpg)

1. Using the scale controls, resize the **Product3D** component to display between the **Back** icon and **product information**.

    ![A screenshot of the product information screen for the canvas app. The screen consists of a back button, the product name, the product description, the product price, and the product 3 d control.]({{ site.baseurl }}/images/8-view-3d.jpg)

1. Test the app to view the 3D model of the product.

### Add the View in MR Control

1. In the left panel, click the **Tree View** icon, select the **ProductInformation** screen.
1. In the left panel, click the **Insert** icon and select **Mixed Reality** > **View in MR**.
1. On the **Select a data source** window that appears, select the **Products** data source.
1. In the formula bar, for **Source** enter `ProductGallery.Selected.'3DModel'`.
1. In the left panel, rename the **View in 3D** component **ProductMR**.

    ![A screenshot of the tree view. The product m r control is highlighted.]({{ site.baseurl }}/images/8-product-mr.jpg)

1. In the right **View in MR** panel, change the **Display Type** to **Icon**.
1. Using the scale controls, resize the **ProductMR** component to the size of the icon and move the icon to display at the bottom left of the **ProductMR** control.

    ![A screenshot of the product information screen for the canvas app. The screen consists of a back button, the product name, the product description, the product price, the product 3 d control, and the product m r control.]({{ site.baseurl }}/images/8-canvas-view-mr.jpg)

1. Test the app to view the 3D model in Mixed Reality.

### Create a View in MR Photo Gallery Screen with Navigation

1. In the top navigation menu, click **New Screen** > **Blank**.
1. In the left panel, rename the new screen **ViewMRPhotos**.
1. In the top navigation, click **Insert** > **Icons** and select the **Back** icon.
1. In the left panel, rename the **Icon** component **BackButton**.

    ![A screenshot of the tree view. The back button control is highlighted.]({{ site.baseurl }}/images/8-view-mr-photo-back-button.jpg)

1. Move the **BackButton** to align to the top left of the screen.

    ![A screenshot of the m r photo gallery screen. The screen consists of a back button aligned at the top left of the screen.]({{ site.baseurl }}/images/8-mr-photo-gallery-screen.jpg)

1. In the formula bar, for **OnSelect** enter `Navigate(ProductInformation,ScreenTransition.Fade)`.
1. In the left panel, click the **Tree View** and select the **Product Information** screen.
1. In the left panel, click the **Insert** icon and select **Button**.
1. In the formula bar, for **Text** enter `"View Photos"`.
1. In the formula bar, for **OnSelect** enter `Navigate(ViewMRPhotos,Fade)`.
1. In the left panel, rename the button **ViewPhotos**.

    ![A screenshot of the tree view. The view photos control is highlighted.]({{ site.baseurl }}/images/8-view-photos.jpg)

1. Test the app to confirm that the **ViewPhotos** button navigates to the **ViewMRPhotos** screen. Once on the **ViewMRPhotos** screen, test the app to confirm that the **Back** navigation button navigates to the **ProductInformation** screen.

### Create View MR Photo Gallery

1. In the left panel, click **Tree View** and select the **ViewMRPhotos** screen.
1. In the left panel, click the **Insert** icon and select **Horizontal Gallery**.
1. In the formula bar, for **Items** enter `ProductMR.Photos`.
1. In the left panel, rename the **Gallery** component **ViewMRGallery**.

    ![A screenshot of the tree view. The view m r gallery component is highlighted.]({{ site.baseurl }}/images/8-view-mr-gallery.jpg)

1. In the left panel, expand the **ViewMRGallery** component to view it's elements. Rename the **Image** component to **PhotoTaken**.

    ![A screenshot of the tree view. The photo taken component is highlighted.]({{ site.baseurl }}/images/8-photo-taken.jpg)

1. Move and scale the **ViewMRGallery** to align with the height and width of the app screen below the **Back** navigation button.

    ![A screenshot of the m r photo gallery screen. The screen consists of a back button and a large blank rectangle for the gallery.]({{ site.baseurl }}/images/8-view-mr-gallery-scaled.jpg)

1. Test the app to confirm that photos taken while viewing a product in MR appears on the **ViewMRPhotos** screen.

### Create Zoom for Photo Gallery Photos

1. In the left panel, click **Tree View** and select the **ViewMRPhotos** screen.
1. In the left panel, click the **Insert** icon and select **Image**.
1. In the left panel, rename the **Image** component **ImageZoom**.

    ![A screenshot of the tree view. The image zoom component is highlighted.]({{ site.baseurl }}/images/8-photo-taken.jpg)

1. Move and scale the **ImageZoom** to align with the height and width of the app screen below the **Back** navigation button.

    ![A screenshot of the m r photo gallery screen. The screen consists of a back button and a large blank rectangle for the image zoom photo.]({{ site.baseurl }}/images/8-image-zoom.jpg)

1. In the formula bar, for **OnSelect** enter `UpdateContext({vVisibleImageZoom:false})`. When the image is pressed, the app will close the zoom of the image.
1. In the formula bar, for **Image** enter `ViewMRGallery.Selected.PhotoTaken`.
1. In the formula bar, for **Visible** enter `vVisibleImageZoom`.
1. In the left panel, expand the **ViewMRGallery** component to view it's elements.
1. Click the **PhotoTaken** element.
1. In the formula bar, for **OnSelect** enter `UpdateContext({vVisibleImageZoom:true})`. When the image is pressed, the app will display a larger view of the image.
1. Test the app to confirm that you can zoom to view the photos within the **ViewMRGallery** component.

<ul class="actions">
<li><a href="https://aprilspeight.github.io/workshop-mr-powerapps/jekyll/update/2022/01/02/step-seven.html" class="button special">Back</a></li>
<li><a href="https://aprilspeight.github.io/workshop-mr-powerapps/" class="button">Home</a></li>
</ul>