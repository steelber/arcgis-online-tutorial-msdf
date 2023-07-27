
← [Creating a Web Map](/sections/03-creating-a-web-map.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Customizing Pop-Ups](/sections/05-customizing-pop-ups.md) →

---

# Importing and Styling Layers
What’s a layer? A layer is a collection of specific geographic data added to your map. Maps can have multiple layers that can be shown concurrently or hidden as needed to allow you to interrogate the interactions of multiple datasets or to focus where you need to.

## Adding Layers
There are several different ways to add layers – for the purposes of this tutorial, you will be importing your hosted feature layer to your map. 

1. Click the **Layers** icon in the sidebar menu.
2. Click the **Add** button.
3. Search for your feature layer under **My Content** using the search bar, and click **+Add** to add it to your map.

Your layer will appear on the map with its location points, and the layer's Properties pane will pop up on the right-hand side of the map, along with the layer options menu. 

![Screenshot of a layer on an ArcGIS online map, with panes of information on either side of the map](/images/AO-new-layer-added.png)

You can use the eye icon that appears when you hover over a layer’s name to show/hide layers as needed.

From top to bottom:
* **Properties** (like transparency, visibility levels...)
* **Styles**: select and style the attributes you want to map
* **Filter**: filter your map based on attributes to show only certain points
* **Effects**: select from a variety of visual effects you can turn on for the entire layer or certain features (drop shadow, saturation, sepia...)
* **Aggregation**: enable point aggregation for dense maps
* **Pop-ups**: customize the pop-up that appears when a viewer clicks a point on the map
* **Fields**: edit the display names for data fields
* and more!

## Duplicating Layers
You may find it helpful to make copies of your layers, so you can use the separate copies to analyze different aspects of the data or filter out specific facets. To do so, simply click the “more options” button next to the layer’s name when you hover over it, and select **Duplicate**. You can rename your copy using the **Rename** option under the same more options menu.

![Screenshot of the ArcGIS Online layer options](/images/AO-new-layer-options.png)

## Customizing and Styling Layers
There are a variety of options for you in customizing your layers, depending on the attribute upon which you want to focus. Choose an attribute from the your spreadsheet and play around with how you want to visualize it! ArcGIS Online lets you customize most aspects of the visualization. Click the **Styles** button in the right-hand layer menu. (Feel free to duplicate your layer first if you want to play around with a couple of different attributes or viewing options.)

You can choose either **+ Field** to map a particular attribute from your spreadsheet or **+ Expression** to write a mathematical script based on your attributes that returns a value (for example, percent of a total). The latter is likely less applicable for your Spanish detective novel dataset.

For textual/categorical Data (race, jobs, schooling, heritage…):
* Types (Unique symbols), which shows different categories as different colors
* Location (Single symbol), which simply shows the location of your data (as a point or as a polygon)
The visual aspects (like size, color, symbol, transparency) can be customized by clicking the **Style options** button.

For numeric data (acreage, ages, number of people in a household, number of grandparents born in Iowa or in the US…):
* Counts and Amounts (Size), which uses symbol size to represent your numeric data
* Counts and Amounts (Color), which uses a color scheme to represent your numeric data
* Color and Size, which allows you to use both symbol size and color scheme
* Location (Single symbol), which simply shows the location of your data (as a point or as a polygon)
* Types (Unique symbols), which shows different categories as different colors
* and for points data, Heat Map, which shows areas of high activity in colors that appear “hotter”

Click the **Style options** button under the selected drawing style to customize the visualization on your map. Each of the options outlined can be customized – both the visual aspects (like size, color, symbol, transparency) and some of the numeric aspects (such as data classification and breakpoints).

![Screenshot of an ArcGIS Online map with Symbol Style and Style options panes open on the right.](/images/AO-new-layer-styling.png)

After selecting an attribute from the dropdown, you can click the **+ Field** button again to add a second attribute, if certain conditions are met: namely, one of the attributes must be a numeric one and the other must be a categorical one. You can then customize the appearances of both. You can use this feature to map two attributes at once, for example Category and Exactness. If the two attributes you want to map cannot be mapped together on a single layer, you can create multiple layers and adjust their transparencies to show overlap or showcase them in separate map images. Once you’re finished customizing, make sure to click the blue **Done** button at the bottom of the right-hand viewing pane to make sure your changes are saved.

![Screenshot of an ArcGIS Online layer with two attributes mapped](/images/AO-new-two-attributes.png)

> Let’s reflect:
> What do you notice about your visualization as you change its drawing style and customize its appearance?
> What is gained and what is lost with different visualization options?

---

← [Creating a Web Map](/sections/03-creating-a-web-map.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Customizing Pop-Ups](/sections/05-customizing-pop-ups.md) →
