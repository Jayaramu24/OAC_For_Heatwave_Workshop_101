To check the performance of queries from Heatwave in OAC, drag and drop ‘Manual Query’ as shown.

![image](https://user-images.githubusercontent.com/90479726/133307946-0e409df4-cc16-48a3-84f9-5001e8e59686.png)

Once you are in the SQL Entry screen after Double Clicking the 'Manual Query', try the following queries first with Heatwave engine 'off' and then turning 'on' the engine. Observe the difference in speed of query execution.
- Note: Set the Data Access to ‘Live’ while executing the query.

Query1 -> Find the revenue by Ship Mode and list them in descending order:

`select /*+ SET_VAR(use_secondary_engine=off) */
count(*) as No_of_Records  
From tpch.lineitem`


Query2 -> A Pricing Summary Report:

`Select /*+ SET_VAR(use_secondary_engine=off) */ 
l_returnflag, l_linestatus, sum(l_quantity) as sum_qty,  
sum(l_extendedprice) as sum_base_price,  
sum(l_extendedprice*(1-l_discount)) as sum_disc_price,  
sum(l_extendedprice*(1-l_discount)*(1+l_tax)) as sum_charge,  
avg(l_quantity) as avg_qty,  
avg(l_extendedprice) as avg_price,  
avg(l_discount) as avg_disc,  
count(*) as count_order  
From tpch.lineitem  
Where l_shipdate <= date '1998-12-01‘  
group by l_returnflag, l_linestatus  
order by l_returnflag, l_linestatus`

![image](https://user-images.githubusercontent.com/90479726/133321604-404cfc50-50c8-41bb-9f04-d69b375bd194.png)


Similarly you could try multiple queries including joining multiple tables and check the performance with and without Heatwave engine on.
