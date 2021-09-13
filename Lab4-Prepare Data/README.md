Drag and drop following tables:customers, lineitem, nation, orders, part, partsupp, supplier

![image](https://user-images.githubusercontent.com/90479726/133122834-e5dd2172-ac95-4b0d-bb6c-9de1c8cd74fc.png)

To start joining the tables, right click on linetem -> Join To -> partsupp

![image](https://user-images.githubusercontent.com/90479726/133122909-c2cd4093-0bf8-4214-9859-f4b73d1021b2.png)

From both the tables’ dropdowns, select PS_PARTKEY and PS_SUPPKEY

![image](https://user-images.githubusercontent.com/90479726/133123145-8e923dd8-d6f6-488b-a2a2-124d3db8145c.png)

If any key that needs to be joined is saved as a numerical value, the system will ask you to first convert it to an attribute since the numerical value is considered as a ‘Measure’ and ‘Measures’ cannot be joined.

![image](https://user-images.githubusercontent.com/90479726/133123345-310e93a5-71d4-4bb8-ba43-bb1a9177edc4.png)

Kindly follow the below join conditions:lineitem -> orders -> customer -> nationpartsupp -> lineitem (PartKey+SupplierKey)partsupp-> partpartsupp-> supplierNote: All joins to be inner joins

![image](https://user-images.githubusercontent.com/90479726/133123488-426de32b-ccc4-4d5f-ba52-61d81b514a00.png)

After the completion of joins, select lineitem table in the bottom to observe interactive visual data preparation screen.L_RETURNFLAG has values = N, R, A. To make them more understandable, double click on each one of them and update them to NA, Returned, Accepted respectively.Similarly updates values in L_LINESTATUS to Fulfilled and Ordered respectively.

![image](https://user-images.githubusercontent.com/90479726/133123652-3160c015-a848-4c23-b94c-008c23454a91.png)

Click any of the date columns to observe Machine Learning enrichment Recommendations to derive Year, Month, Quarter etc. For now let us skip them.

![image](https://user-images.githubusercontent.com/90479726/133123791-dd2cd5f5-02bf-4d8b-a892-9c06f9f45c56.png)

Similarly, if you navigate to nation table you will see a bunch of recommendations to enrich the N_NAME column.

![image](https://user-images.githubusercontent.com/90479726/133123914-e30a6721-f810-4ed0-9919-782ea1ff8fe8.png)

For any of the columns in any of the tables, the tool offers a rich set of data preparation options when you Right Click on any of the column names.

![image](https://user-images.githubusercontent.com/90479726/133124039-e2cb5e14-65be-4e3d-9d27-c12a016be0c1.png)

Clicking on ‘Edit Definition’ provides additional features of how you want to manage the data.

![image](https://user-images.githubusercontent.com/90479726/133124199-85ceb79e-9a64-4bcc-9418-d1d6b0312da0.png)

Depending on the use-case, you can set the connection to ‘Live’ or ‘Automatic Caching’. Brief explanation for both is provided right below the options.

![image](https://user-images.githubusercontent.com/90479726/133124297-49c610cb-b613-4057-b5b4-8eaec8538713.png)

You could also toggle the view to ‘Enter SQL’ to write custom queries either if required or if some data needs to be checked for validation. Once the query is written, you need to click ‘Get Preview Data’ to run the query.

![image](https://user-images.githubusercontent.com/90479726/133124425-fd401a72-e5d7-4e43-b9d2-56990c56e6fc.png)

Once the data preparation is complete and the data is ready for analysis, it needs to be saved as a dataset.

![image](https://user-images.githubusercontent.com/90479726/133124522-1349f280-382c-40ce-a4d5-f901f6a3bf2d.png)

Provide a meaningful name and save the dataset.

![image](https://user-images.githubusercontent.com/90479726/133124602-8b605cfa-4c71-4d09-8b8b-97dc08c45499.png)

Once the dataset is save ‘Create Project’ button gets activated.

![image](https://user-images.githubusercontent.com/90479726/133124705-9e58e6ff-1027-435a-97f7-2a2579db195f.png)

On clicking the ‘Create Project’ button, if the system asks you to save any changes, kindly save.

![image](https://user-images.githubusercontent.com/90479726/133124802-c9e94d1f-e8ae-4385-b534-a4d7b23796b8.png)

Congratulations! The data is now ready for dashboards and analyses.
