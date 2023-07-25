# arcgis-online-tutorial
This is a tutorial on the basics of mapping in ArcGIS Online, geared towards Grinnell College students, faculty, and staff. This guide focuses on the Classic Map Viewer.

## Table of Contents
1. [What is ArcGIS Online?](#what-is-arcgis-online)
2. [Web Maps](#web-maps)
3. [Layers](#layers)
4. [Map Accessibility](#map-accessibility)
5. [Additional Information](#additional-information)
6. [Resources](#resources)

## What Is ArcGIS Online?
ArcGIS Online is a cloud-based online mapping software that allows you to create complex digital maps for data analysis, as well as easily share them with others. ArcGIS Online replicates many of the functions of the ArcGIS software application, though it is not quite as powerful.

In this tutorial, you will learn how to use ArcGIS Online by mapping historical data from the [Iowa Township Project](https://dasil.sites.grinnell.edu/2019/04/land-census-and-digital-humanities-the-iowa-township-project/).

### Logging In
Everyone at Grinnell has access to ArcGIS Online through the College. You can access your account by logging in with your Grinnell College credentials at https://grinnell.maps.arcgis.com/home/index.html. It is used in the browser, so you do not need to download anything special onto your computer.

### Downloading Data
Download the [dataset](/Grinnell_1900_Geocoding_Result_Tidied.csv) for this tutorial from this repository. You’ll upload this data into ArcGIS Online in order to map and analyze it. This dataset is a CSV file that contains Town of Grinnell census data from 1900, cleaned and formatted for use. You can look at the [Iowa Townships Data Codebook](/2019-Codebook-Iowa-Townships-Data-Set.pdf) to learn more about what the different abbreviations in the dataset mean.

Spatial data can take many forms: for the purposes of this walkthrough, we are using a spreadsheet with location information in some of the columns (in this case, latitude and longitude). Another file format option for spatial data is shapefiles. Shapefiles are a file format for storing geographical location and attribute information data, and they are actually made up of a grouping of individual files, compressed into a single .zip file that is uploaded all at once to ArcGIS Online. You can play around with some spatial data in shapefile format in the optional Going Further section of this tutorial.

> Let’s reflect! Download the dataset CSV, look through it, and think about what you see…
> * What do you notice about this data?
> * What questions do you think this dataset might help to answer, if visualized on a map?

## Web Maps
What’s a web map? Esri, the company behind ArcGIS and ArcGIS Online, describes a web map as “an interactive display of geographic information that you can use to tell stories and answer questions” (source: [Web maps](https://doc.arcgis.com/en/arcgis-online/reference/what-is-web-map.htm)).

### Creating a New Map
Click **Map** in the top level menu of your ArcGIS Online homepage to create a new map. From there, you will be taken to a new blank map for you to make your own!

![Screenshot of the ArcGIS Online user homepage](/Images/AO-homepage.png)

*Note: for the purposes of this tutorial, we will use Map Viewer Classic, which allows us to upload data by file. The new Map Viewer does not have this feature yet. Click “Open in Map Viewer Classic” at the top right of the map menu to switch over.*

### Customizing Your Map’s Appearance
You can customize the way your map looks by clicking **Basemap** in the top level menu of the map view, and then selecting your chosen basemap. You can change this at any time, so can come back and make edits for the best base map for your purposes once your data has been added to the map.

![Screenshot of the ArcGIS Online basemap options](/Images/AO-Basemap.png)

> Let’s reflect: how might different basemaps influence a viewer’s experience of a digital map?

### Saving Your Map
Click the **Save** button on the top level menu of the map view, then click **Save As** to save a new map or a new copy of an existing map: you will be prompted to give your new map a title and tags (required, but you can choose any you would like), and to add a summary, if desired. If you are working with a pre-existing map, just click *Save* to keep saving it to the same place – *make sure to do this regularly while you are working so your changes are saved*. 

![Screenshot of the ArcGIS Online map menu](/Images/AO-Web-Maps-Menu.png)

### Returning to an Existing Map
Click *Content* in the top level menu (available when you click the *Home* button if you are currently viewing a map or other content) to see all your saved content and return to an existing map. Click the title of an existing map, then click the *Open in Map Viewer* button (top right) to continue editing.

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

## Map Accessibility
What is web accessibility? “Web accessibility is the inclusive practice of ensuring there are no barriers that prevent interaction with, or access to, websites on the World Wide Web by people with physical disabilities, situational disabilities, and socio-economic restrictions on bandwidth and speed.” (Source: [Wikipedia](https://en.wikipedia.org/wiki/Web_accessibility)). As you create your map, keep accessibility at the forefront of your mind:
* be careful in your use of color and ensure appropriate color contrasts and differentiation (basemap, layer colors…)
* consider how you can avoid using color alone to convey meaning: vary labels and color, utilize different shapes, change both size and color value of the same shape (source: [“Improving Accessibility with ArcGIS Online Web Mapping Apps”](https://www.doi.gov/ocio/section508/video3) presentation from Esri)
* be thoughtful about your text content (pop-ups, map descriptions, and more): break up walls of text, ensure appropriate typeface and font size when you are customizing, provide links that make sense out of context (i.e., no “click here”)

You can use these resources to check your work:
* check color contrasts with WebAIM’s [Contrast Checker](https://webaim.org/resources/contrastchecker/)
* check accessible color selection with Toptal’s [Colorblind Web Page Filter](https://www.toptal.com/designers/colorfilter), the [Color Oracle](https://colororacle.org/) software, or the [Colorblindly](https://chrome.google.com/webstore/detail/colorblindly/floniaahmccleoclneebhhmnjgdfijgg?hl=en) Chrome extension

> Let’s reflect: what choices do you make as map creators that impact the accessibility of your maps for your viewers? What are some concrete examples of accessible features on a web map? What else do you need to keep in mind?

## Additional Information
### Sharing Your Map
There are ways to directly share your map with others if you want to. You can do this in a couple of different ways, depending on your needs. There are several sharing levels:
* owner: visible only to you, the creator
* organization: visible to all members in our organization, Grinnell College
* everyone (public): visible to the wider community outside of Grinnell College

You can very easily a pull an ArcGIS Online map into a StoryMap to provide narrative and context relating to your map. You will still want your map sharing levels to be set to whatever sharing level your StoryMap will be.

It is also possible to create a “shared update” group for sharing, which allows multiple people to work on the same map at once (similar to the collaborative editing features in Office 365). You are not able to create “shared update” groups on your own: this must be done by an admin. You can make this request by putting in an ITS Help Desk ticket.

To be able to embed your map on an external website, you need to make sure it is set to the “public” sharing setting. Once you have done so, you can click the Embed in Website button to customize your embed settings. Your map does not need to be shared publicly to be shared more widely as a web app – more on that below.

### Analysis
There are powerful analysis features that can be enabled on your ArcGIS Online account upon request: simply request a Publisher account from an ArcGIS Online admin or put in an ITS Help Desk ticket. The Publisher account also allows you to host feature layers that can be updated as needed and used across multiple maps.

Some examples of analysis features include:
* the ability to “join” one dataset to another using a unique identifier column
* the ability to measure distances between points (in a straight line or via selected travel mode)
* the ability to analyze patterns
* and more!

See more on analysis from Esri’s help documentation: [Perform Analysis](https://doc.arcgis.com/en/arcgis-online/analyze/perform-analysis.htm).

### Creating a Web App
A web app allows you to share a customized and streamlined view of your map with external viewers. Changes made to your map are reflected on its web app version. If you are interested in playing around with this feature and sharing your map as a web app, you can follow these [web app instructions](https://doc.arcgis.com/en/arcgis-online/create-maps/create-map-apps.htm#ESRI_SECTION1_2F3804B3E2C849F997784C121868A242) from Esri.

![Screenshot of the ArcGIS Online "Create a New Web App" menu with various web app options](/Images/AO-Web-Apps-Options.png)

### New Map Viewer
Esri is in the process of releasing a new Map Viewer. For the purposes of this tutorial, you are using the older Classic Viewer, as the new viewer is still missing a few useful features. If you would like to learn more about the new viewer and some of its new features, you can read this article from Esri, [“New Map Viewer in General Availability.”](https://www.esri.com/arcgis-blog/products/arcgis-online/mapping/new-map-viewer-in-general-availability/) At this time, there are no concrete plans to sunset the Classic Viewer: this information will be pushed out if and as plans change.

## Going Further
If you want to go further in your exploration of ArcGIS Online, you can optionally try some of the following:
* Download some other Iowa Township Project datasets from this repository and try mapping them. There is a [CSV with 1920s data](/Grinnell_1920_Geocoding_Result_Tidied.csv) and [shapefiles](/Shapefiles) with additional data. Try comparing and contrasting historical data from 1900 and 1920.
* Try playing around with some of the [Analysis](https://doc.arcgis.com/en/arcgis-online/analyze/perform-analysis.htm) and other Publisher features, once your Publisher account has been enabled. Test out hosting the CSV or shapefile data as a [hosted layer](https://doc.arcgis.com/en/arcgis-online/manage-data/hosted-web-layers.htm) within ArcGIS Online, rather than adding the file directly to a map.
* Use ArcGIS Online’s [browse and search features](https://doc.arcgis.com/en/arcgis-online/reference/search.htm) under the “Add” section to add additional layers of content to your map: you can find data created and curated by a variety of other organizations (such as recent federal census data, for example).
* Try building out a StoryMap with additional content to contextualize your map, following these [Getting Started](https://doc.arcgis.com/en/arcgis-storymaps/get-started/what-is-arcgis-storymaps.htm) instructions from Esri.
* Try exploring the new [Map Viewer](https://doc.arcgis.com/en/arcgis-online/get-started/get-started-with-mv.htm) to get a feel for it.
* Try creating a [web app](https://doc.arcgis.com/en/arcgis-online/create-maps/create-map-apps.htm) to streamline your map’s functionality for your users (for example, try out some of the comparison web app features that let you compare two layers or two maps).

## Resources
Resources & Documentation
* ArcGIS Online [resources and tutorials](https://www.esri.com/en-us/arcgis/products/arcgis-online/resources) from Esri​
* ArcGIS Online [“getting started” documentation](https://doc.arcgis.com/en/arcgis-online/get-started/get-started.htm) from Esri​

Design & Accessibility
* [Best Practices for Map Design: An Introduction](https://proceedings.esri.com/library/userconf/fed16/papers/fed_86.pdf), Leff, Davis-Holland, & Ducey (2016 presentation)​
* [Improving Accessibility with ArcGIS Online Web Mapping Apps](https://www.doi.gov/ocio/section508/video3) (US Department of the Interior, 2019 presentation)​
