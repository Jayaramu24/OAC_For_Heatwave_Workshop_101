As a very first step, save the project by clicking on Save As, provide a meaningful name and save it under My Folder (check the next screenshot). Post this step, set the project to ‘Auto Save’ so that, you would lost minimal work if the project is accidentally closed or the system shuts down. ‘Auto Save’ ensures that the system automatically saves the work regularly without you having to worry about saving the project after every logical step.

![image](https://user-images.githubusercontent.com/90479726/133126003-ce0f9ab8-52a6-42c0-9cf7-2021b7d3340c.png)

![image](https://user-images.githubusercontent.com/90479726/133126075-de9ad8d8-6c4d-4a0f-b635-952b42b1c6d5.png)

Once we are on the ‘Visualize’ screen, let us first create a calculated measure required for our dashboard. Right Click on ‘My Calculations’ and click on ‘Add Calculation’.

![image](https://user-images.githubusercontent.com/90479726/133126238-8605eeba-d397-4095-b058-596c97079ce3.png)

Once we are on the ‘Visualize’ screen, let us first create a calculated measure required for our dashboard. Right Click on ‘My Calculations’ and click on ‘Add Calculation’.

![image](https://user-images.githubusercontent.com/90479726/133126334-e4828bee-1b81-42a5-ab7a-2fda42254c46.png)

Name the measure as Total Order and create the calculation as shown below. It is a simple count of Order key from orders table. Once the formula is typed, click on ‘Validate’ to ensure there are no syntax errors and save.

![image](https://user-images.githubusercontent.com/90479726/133126838-7ba57ea0-48fb-48e2-a6b4-3ed9a5e48dc6.png)

Expand the 'orders' table, then expand the automatically created Order Date Hierarchy and drag and drop the ‘Year’ column on to ‘Click here or drag and drop to add a filter’ section. Once the filter is added, click on 1995 to set the year filter. You can observe there is a natural language based ‘Search’ option if the column has many values.

![image](https://user-images.githubusercontent.com/90479726/133126991-f78054ec-ea9a-4bd9-abd5-874510eb898a.png)

Once the filter is set, just double click the ‘Total Orders’ measure we just created. Observe that the system has intelligently and automatically has selected the ‘Tile’ visualization.

![image](https://user-images.githubusercontent.com/90479726/133127050-cd43724f-6b39-4a92-b241-a2921d0ee6bd.png)

It is very easy to create additional tiles. Click anywhere within the current tile, hover on top right corner of the tile to observe the 3 dots, on clicking, you will find and option to ‘Edit’ and on clicking, you will find an option to ‘Duplicate Visualization. Just select this option.

![image](https://user-images.githubusercontent.com/90479726/133127213-7e2198bb-fdc8-4d57-9028-b2dfe66b856c.png)

Now let us create another calculated measure as before. This time, we will create the distinct count of customers from the orders table. The formula and syntax is as shown.

![image](https://user-images.githubusercontent.com/90479726/133127297-df273bef-91e8-497c-904c-6a866fce188a.png)

Once the new measure is validated and saved, just select the duplicated tile by clicking anywhere on the screen. Then drag and drop the new measure onto the ‘Values’ section of the tile. Just let the system overwrite the previous metric on the ‘Values’ section.

![image](https://user-images.githubusercontent.com/90479726/133127403-5b99e1e7-cf16-44c4-8dac-cc54c2accfa2.png)

Similarly let us create the next tile by duplicating one of the created tiles and updating the ‘Values’ section to O_TOTALPRICE (Total Sales) from the orders table. Also this time, we will format the metric so that it is more legible. On the properties section of the tile on the left bottom, select the ‘#’ tab and then select the ‘Currency option’.

![image](https://user-images.githubusercontent.com/90479726/133127546-9d722152-9f88-4737-bc88-d5f5d4855cd2.png)

Then update the properties as shown below.

![image](https://user-images.githubusercontent.com/90479726/133127623-a8edaa7a-a465-483d-a175-636d6cf8272d.png)

Let us now create the Sales trend and forecast chart. On the left hand panel, ‘Control’ select O_TOTALPRICE and ‘Month’ columns from the orders table. Right Click and select ‘Pick Visualization’ on the pop-up that appears. (Observe that unlike last time where the system automatically selected the visual, this time we are selecting it ourselves). Select the line graph as shown.

![image](https://user-images.githubusercontent.com/90479726/133127696-c08cddc2-b575-4e35-bab6-9ab701af7a8b.png)

Based on the real estate available, the system automatically places the line graph below the metrics. Now let us add Forecast to it. Click on the ‘Growth’ arrow icon on the top left panel to view some of the drag and drop advanced statistics options available. Select the ‘Forecast’ option and drag and drop it on the line graph.

![image](https://user-images.githubusercontent.com/90479726/133127768-5333b323-82a4-4e6f-888a-6ab3eabaed97.png)

Observe that, by default the forecast is applied for next 3 periods using the Seasonal ARIMA model. You can change both the periods as well as the model based on the requirement. Currently 3 time-series based forecast models are supported: Seasonal ARIMA, ARIMA and ETS. Based on the knowledge gained so far, create another trend and forecast graph for Total Orders for Monthly Order Trend and Forecast.

![image](https://user-images.githubusercontent.com/90479726/133127899-e1638308-5ee3-4462-84ea-ca83887d81bf.png)

Let us now create a scatter plot for country-wise break up of Unique customers and Total Sales. ‘Control(ctrl)’ select O_TOTALPRICE from the orders table, N_NAME from the nation table and Unique Customers from the calculated measure, like before, Right Click -> Pick Visualization -> Scatter.

![image](https://user-images.githubusercontent.com/90479726/133127989-188ada2d-9d4f-4e25-b7b3-df18da30fab8.png)

To ensue good spread of the data in the scatter plot, On the properties panel on the left, select the ‘Axis’ icon, expand vertical and Horizontal value axes and change the ‘Start’ from ‘Auto’ to ‘Min Data’ for both axes.

![image](https://user-images.githubusercontent.com/90479726/133128124-62247ad5-c08f-4f8f-8104-d5eb006b6c1d.png)

Similarly, apply the ‘Min Data’ concept to both the Trend and Forecast charts and observe the changes. Also, to make the country-wise break up chart more colorful, add the N_NAME column to ‘Color’ section by dragging and dropping.

![image](https://user-images.githubusercontent.com/90479726/133128218-4acc4b7d-72b5-4dd5-9721-8d541c2ec15c.png)

Let us now create the ‘Top 10 Selling Products’ visual. For this we will use ‘Tag Cloud’ option. First select P_NAME from part table, Right Click -> Pick Visualization -> Tag Cloud.

![image](https://user-images.githubusercontent.com/90479726/133128489-1977b70c-cfbd-499e-b971-5a801236ee6a.png)

Another interesting feature about the tool is that, while we can set the dashboard level filter like the ‘Year’, we can also set filters to individual visuals on the dashboard. Drag and drop L_QUANTITY from line item table on to the filter section of the Tag Cloud visual and then select Filter Type as ‘Top Bottom N’ as shown. By default Top 10 filters are selected. (You could also try ‘Bottom’ filter and changing the number from 10 to any other you like to get a feel of how this feature works.)

![image](https://user-images.githubusercontent.com/90479726/133128602-dab99592-a1e1-4ef7-8435-214bc9d42736.png)

You can also add the P_NAME column to the ‘Color’ section to make the visual more colorful. Ensure that L_QUANTITY is also added to the ‘Values’ section so that you can observe the size difference among the names based on the quantity sold. (You could also try creating a similar visual for Top 10 products by total price by using Total Price column in the orders table similar to the quantity column.) 

![image](https://user-images.githubusercontent.com/90479726/133128685-6ae39ccc-9b6b-4a76-9968-5dc624b12577.png)

On similar lines to creating other charts, let us also create a map chart by ‘Control(ctrl)’ selecting N_NAME from nation table and L_QUANTITY from ‘lineitem’ table and then selecting the ‘Map’ as the visual.

![image](https://user-images.githubusercontent.com/90479726/133129079-bffb4b2e-045f-4604-b2ea-4197e692978a.png)

Another very interesting feature which greatly enhances the dashboard interactivity is the using the attributes in a visual as a filter. Hover on the top left corner of any visual to observe the appearance of ‘Filter’ icon and select it. Once selected all attributes in the visual behave like filters. In this case, select the ‘Filter’ icon on the map chart. Then click any country that has data and the entire dashboard will be filtered for that country.

![image](https://user-images.githubusercontent.com/90479726/133129174-6f8797af-1656-46eb-b8f4-5ed27cca4c09.png)

In the below screenshot, India is selected as the filter by clicking on it on the map chart. As you will observer all the visuals are showing the respective information for India now.Another point: If you have noticed the bottom left corner in the previous screenshots, the individual dashboard known as ‘Canvas’ in OAC has a meaningful name to it. This is done by Double Clicking on the canvas name, typing a meaningful title and saving by clicking the ‘Tick’ icon as shown.

![image](https://user-images.githubusercontent.com/90479726/133129332-28bd31ca-c084-4a67-815e-dee186c0cfb5.png)

Let us now create a drill-down dashboard to this summary dashboard. For this, click on the ‘+’ icon next to the Canvas name in the bottom left corner and name it as ‘Product & Supplier Details’.

![image](https://user-images.githubusercontent.com/90479726/133129437-fce9762c-255d-4e08-9b06-49d8f20e918a.png)

Once the new empty canvas opens up, 
- Create a simple ‘Table’ visual for Product Details as shown with the mentioned columns in the ‘Rows’ section. 
- Similarly, create another ‘Table’ visual for Product-Supplier Details by selecting S_NAME from the ‘supplier’ table and PS_AVAILQTY, PS_SUPPLYCOST & S_ACCTBAL from the ‘partsupp’ table. 
- Also ensure that you have setup a dashboard filter P_NAME and default it first value to avoid overloading of the dashboard as the dataset is huge.

- If you have noticed, the individual visuals/charts are also having meaningful titles. This is done by selecting the first ‘Pinion’ icon in the visual properties panel on the bottom left, changing the ‘Title’ from ‘Auto’ to ‘Custom’ and typing a meaningful title to the visual. Kindly ensure all visuals have meaningful names by following the same process.

![image](https://user-images.githubusercontent.com/90479726/133129757-1400dc08-d3d1-4ea6-a5cd-d8185912f1d2.png)

While we have created a drill-down dashboard, we need to set-up the drill-down option in the summary chart so that when you Right Click on any of the product names in the ‘Tag Cloud’ visual, you will have an option to drill-down to its corresponding details in the drill-down dashboard. For this, click on the 3 dots next to the ‘traffic signal’ icon in the top right corner of the canvas below the black bar, select the ‘Data Actions’ option and set it up exactly as shown in the screenshot.

![image](https://user-images.githubusercontent.com/90479726/133129880-82a8fa6e-ac12-412e-92ff-cd79e3dd2386.png)

Now when you Right Click any of the product names in the ‘Tag Cloud’ visual, you will see a ‘Product & Supplier Drilldown’ option. And on clicking the option, you will be routed to the drill-down chart where you will be able to see the Product & its supplier details for the product you had Right clicked earlier. This is the approach to setup availability of required detailed information from a summary dashboard.

![image](https://user-images.githubusercontent.com/90479726/133129985-852a89b7-c8b9-4ee8-91be-949ae5d893c2.png)

Observe that the dashboard filter would have been updated for the Product selected from the previous screen and all the information available in this dashboard would be specific to the product. Alternatively, you could also select any other product from the filter itself to view similar details of that product.

![image](https://user-images.githubusercontent.com/90479726/133130085-50b060f5-c173-4d97-81af-a18f1eef8550.png)

Congratulations! Let us now check if we have achieved all the objectives we had set for ourselves initially.

**Order Summary needs to be prepared for 1995 with:**

**Following key Metrics:** 
Total Sales, Total Orders, Total Quantity Ordered, Items Returned, Unique Customers.

**Following Charts / Visuals:**
- Monthly Sales Trend & Forecast for next 3 months
- Monthly Orders Trend & Forecast for next 3 months
- Country-wise Break-up of Sales & Customers
- Country-wise Break-up of Orders
- Top 10 selling Products

Drill-down into top selling Products to view:
- Rest of the Product Details like; Type, Manufacturer, Brand, Shipping Container etc
- Product Supplier Details like; Supplier names, Available quantities with them, their cost and Supplier financial health if you need to procure additional products from them.

You will observe that the metrics ‘Total Quantity Ordered’ and ‘Items Returned’ have not been created as metrics. This is a DIY acitivity.

- Hint for ‘Items Returned’: During data preparation, we have updated return status to ‘Returned’. This needs to be used as a filter on an appropriate metric to arrive at this metric. ‘Total Quantity Ordered’ is pretty straight forward.

