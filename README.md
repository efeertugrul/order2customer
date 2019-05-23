# order2customer
This is a heuristic implementation for combining orders in the same factory for the same customer.

The csv files must be encoded with UTF-8

Columns of the each csv file is written below

## Order Customer Matches
OrderCustomer = [Order No, Customer Id]

## Order Product Matches
In this file the products are sorted by their order numbers. The order number should not be included in the columns.
Just sort the orders by their order no.
<br/>OrderProduct = [Product Code, Weight]

## Empty Freight Costs
Each intersection of columns and rows represents the empty freight cost from city to warehouse#
<br/>Empty = [cityindex, warehouse1, warehouse2, warehouse3, warehouse4]

## Full Freight Costs
Each intersection of columns and rows represents the full freight cost from warehouse# to city
<br/>Full = [cityindex, warehouse1, warehouse2, warehouse3, warehouse4]

## Warehouse information
This includes the city of the warehouse and Cost, Insurance & Freight number of that warehouse
<br/>WarehouseFrame = [City,CIF.1]

## Customer City Matches
Ids of the customers and plate codes of their cities
<br/>Customer = [Customer ID, cityindex]

## Product Warehouse Matches
ProductWarehouse = [Product Code, warehouse1, warehouse2, warehouse3, warehouse4]
#### Ex: Product A, 1, 0, 0, 1
#### This row represents that "Product A" is accessible from warehouse1 and warehouse4

## Traveltime from Warehouses to Other Cities
Each row represents the travel time from a city to warehouses
<br/>traveltime = [cityindex, warehouse1, warehouse2, warehouse3, warehouse4]

## Order Day Matches
Each row represents the Order No and the Day the order has received
#### index equals to Order No - 1.

<br/>orderday = [index,Order No,Day]

#### Ex: 0, 1, 1
