# SQL-BASIC-QUERIES
Through my process of learning SQL, these are some basic queries and notes that I thought were worthy of noting.

SELECT * FROM TABLENAME
--SELECT * allows us to display all columns and rows in table 'tblMyCDList'

SELECT COUNT (*) FROM TABLENAME
--counts number of rows (entries) in a table where the column is not null

SELECT * FROM TABLENAME WHERE CDID = 27
--Shows CDID 27 from table 'TABLENAME'

SELECT COUNT (*) FROM fake_apps WHERE price = 0;
--counts all column entries where price = 0

SELECT price, COUNT(*) FROM fake_apps GROUP BY price;
--This query is able to select the PRICE column, and count all of them
--in table 'fake_apps' then group them by each different price that was found

SELECT price, COUNT (*) FROM fake_apps WHERE downloads > 20000 GROUP BY price;
--SELECT price, selects the price column
--COUNT (*), in all table data
--FROM fake_apps, all table data in the table named fake_apps
--WHERE downloads > 20000, where all downloads exceed 20000
-- GROUP BY price, group all price amounts
--Then query allows us to find the price column, search all rows in the table 'fake_apps'
--That exceed 20000 dowloads, then group the results by price
/* OUTPUT FORMATED FOR READING
price	   COUNT (*)
0.0	     26
0.99	   17
1.99	   18
2.99	   7
3.99	   5
14.99	   5
*/
