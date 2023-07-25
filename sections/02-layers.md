← [Web Maps](/01-web-maps.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Map Accessibility](/03-map-accessibility.md) →

## Layers
What’s a layer? A layer is a collection of specific geographic data added to your map. Maps can have multiple layers that can be shown concurrently or hidden as needed to allow you to interrogate the interactions of multiple datasets or to focus where you need to.

### Adding Layers
There are a couple different ways to add layers – for the purposes of this tutorial, you will be adding layers of data by file. This data takes the form of a CSV. This CSV will show up on your map layers in the form of points. As previously mentioned, for this tutorial run-through you’ll work with the [Grinnell_1900_Geocoding_Result_Tidied.csv](/Grinnell_1900_Geocoding_Result_Tidied.csv), which is points data relating to the Town of Grinnell. (When using shapefiles, you want to make sure to keep the shapefile compressed in .zip format – some browsers try to open compressed files for you automatically, which is not helpful in this case.)

1. Click the **+Add** button at the left of the top-level menu.
2. Select **Add Layer from File**.
3. Upload the CSV file (or the entire .zip file, in the case of a shapefile).
4. Click the **Import Layer** button.
5. You now have the option of choosing what attribute to show, and how to customize the way your layer’s data is being visualized.
** To keep it simple to start, you can start by visualizing the total number of people in each household. Select the **TotalHH** attribute from the dropdown list, then select the default **Counts and Amounts (Size)** drawing style. You’ll customize this later.
** If you’re feeling adventurous, you can choose any of the attributes to visualize, and play around with how they appear on the map.
6. When you’re ready, click the **Done** button at the bottom.
7. You should now see the data added as a content layer, on the left-hand panel of your map.

Once a layer has been added to your map, a variety of options appear for you when you hover over a layer’s name in the Content menu of your map. You can use the checkbox by the layer’s name to show/hide layers as needed.

![Screenshot of the ArcGIS Online layer menu options](/Images/AO-Layer-Menu.png)

From left to right:
* The **Show Legend** button pops out your layer’s legend for you.
** Please note that the ArcGIS Online legend is automatically generated based on the titles of the attributes in your dataset. You cannot customize it from within your map.
* The **Show Table** button gives a preview of your data in table form, at the bottom of your map.
* The **Change Style** button allows you to customize your data visualization style – more on that below!
* In the case of points data, the **Cluster Points** button lets you [configure clustering](https://doc.arcgis.com/en/arcgis-online/create-maps/configure-clustering.htm) to better extract information from your data.
** Per Esri: “If your map has a layer with a large number of points, you can configure clustering to make it easier to visually extract meaningful information from your data.” (Source: [Configure clustering](https://doc.arcgis.com/en/arcgis-online/reference/configure-clustering.htm))
* The **More Options** button lets you select from a variety of other customization and viewing options, as needed.

![Screenshot of the ArcGIS Online layer menu "More Options"](/Images/AO-More-Options.png)

### Making Copies of Layers
You may find it helpful to make copies of your layers, so you can use the separate copies to analyze different aspects of the data. To do so, simply click the “more options” button under the layer’s name when you hover over it, and select **Copy**. You can rename your copy using the **Rename** option under the same more options menu.

### Customizing Layers
There are a variety of options for you in customizing your layers, depending on the attribute upon which you want to focus. Choose an attribute from the list (basically, one of the columns of census data in the data spreadsheet) and play around with how you want to visualize it! ArcGIS Online lets you customize most aspects of the visualization. Hover over the layer you’re working with and click the **Change Style** button (feel free to make a copy first if you want to play around with a couple of different viewing options). Choose an attribute to show from the dropdown, then select a drawing style underneath (different options appear depending on whether the attribute is numeric or textual/categorical).

You can also scroll down to the bottom and choose New expression to write a script that creates a custom expression to mathematically manipulate attributes in some way.

*For example, with the census data, you could combine the attributes for numbers of children of different genders and age groupings to get the total number of household members aged 17 and under, with a custom expression along the lines of $feature[“Male_Under_5”] + $feature[“Male_5_to_17”] + $feature[“Female_Under_5”] + $feature[“Fem_5_to_17”].*

For textual/categorical Data (race, jobs, schooling, heritage…):
* Types (Unique symbols), which shows different categories as different colors
* Location (Single symbol), which simply shows the location of your data (as a point or as a polygon)
The visual aspects (like size, color, symbol, transparency) can be customized.

For numeric data (acreage, ages, number of people in a household, number of grandparents born in Iowa or in the US…):
* Counts and Amounts (Size), which uses symbol size to represent your numeric data
* Counts and Amounts (Color), which uses a color scheme to represent your numeric data
* Location (Single symbol), which simply shows the location of your data (as a point or as a polygon)
* Types (Unique symbols), which shows different categories as different colors
* and for points data, Heat Map, which shows areas of high activity in colors that appear “hotter”

![Screenshot of an ArcGIS Online map. On the left, a pane with layer visualization choices, with Counts and Amounts (sizes) option selected. And on the right, a map with points plotted for the town of Grinnell in 1900.](/Images/AO-Layers-Counts-and-Amounts-Size-i-Dark.png)

Click the **Options** button at the center of the selected drawing style to customize the visualization on your map. Each of the options outlined can be customized – both the visual aspects (like size, color, symbol, transparency) and some of the numeric aspects (such as data classification and breakpoints).

![Screenshot of the options for customizing a data visualization option in ArcGIS Online](/Images/AO-Layers-Counts-and-Amount-Size-Options-i.png)

![Screenshot of the options for customizing a data visualization symbol in ArcGIS Online](/Images/AO-Layers-Counts-and-Amount-Size-Symbol-Options.png)

After selecting an attribute from the dropdown, you can click **Add attribute** to add a second attribute, if certain conditions are met: namely, one of the attributes must be a numeric one and the other must be a categorical one. You can then customize the appearances of both. You can use this feature to map two attributes at once, for example, Total Household size and whether the family owns or rents their home. If the two attributes you want to map cannot be mapped together on a single layer, you can create multiple layers and adjust their transparencies to show overlap or showcase them in separate map images. Once you’re finished customizing, make sure to click the blue **Done** button at the bottom of the viewing pane to make sure your changes are saved.

> Let’s reflect:
> What do you notice about your visualization as you change its drawing style and customize its appearance?
> In the case of numeric data, spend some time playing around with breakpoints using the **Classify Data** options – try out different types of breaks, and different numbers of classes. What makes sense for the attribute you’ve chosen?
> What is gained and what is lost with different visualization options?

### Configuring Pop-Ups
You can configure the pop-ups that appear when you click on your data points. By default, they show all of the information from that point’s row in your data table – but some or most of this information may not be needed depending on what you are trying to showcase with your map. To configure a pop-up, hover over the layer you’re working with and click the **More Options** button, then the **Configure Pop-Up** option.

![Screenshot of the ArcGIS Online configure pop-up options](/Images/AO-Layers-Configure-Pop-Up.png)

At the top of the pane, you can select a pop-up title based on an attribute. In the **Display** dropdown below, you can decide if you want to display:
* a list of attributes (which you can customize below using the **Configure Attributes** – you can choose which ones you want to appear)
* a description from one field
* a custom attribute display
* no attribute information

![Screenshot of the ArcGIS Online pop-up custom attribute display pane](/Images/AO-Layers-Custom-Pop-Up.png)

Don’t forget to click the **OK** button at the bottom of the pane when you’re done customizing your pop-up, to save your changes. In the case of a custom attribute display, you can click the green Configure button and lay out the information you want to display. You will see a basic text editor for formatting, and you can use the small + button to pull in the IDs of the attributes you want to display. When you’re finished, click the blue OK button at the bottom of your text box.

*For example, “The {Lastname} household has {TotalHH} members in total.” pulls in both the name and total household attributes as a sentence.*

In the case of this data, the attribute fields may be somewhat opaque to someone unfamiliar with the dataset, so if you were displaying this data more publicly, and focusing on some information in particular, it could make sense to customize the attribute display (and reduce the number of fields, since many might not be relevant to a casual viewer).

> Let’s reflect: how do external map elements like this pop-up influence the viewing experience? How do you think they could or should be used most effectively?

← [Web Maps](/01-web-maps.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Map Accessibility](/03-map-accessibility.md) →
