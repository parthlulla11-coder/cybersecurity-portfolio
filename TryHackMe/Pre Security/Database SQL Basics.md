**Learning Objectives** 

*Understand what data is and why it matters
*Explain what a database is and why it is used
*Understand what SQL is and what it is used for
*Identify tables, rows, and columns
*Write simple SQL queries to retrieve information


View Everything in a Table (Select + From) - 

*SELECT * FROM Orders; see every order currently stored in the database. 

<img width="1906" height="916" alt="image" src="https://github.com/user-attachments/assets/a799a10a-5eca-45ec-aba3-f10e5c479cd0" />

** Show Only Specific Columns (Select Drink, Price)**

SELECT drink, price FROM Orders; - This will display only the drink and price columns.

<img width="1042" height="779" alt="image" src="https://github.com/user-attachments/assets/9ac4b512-1741-4455-a7ec-a355fc0d3ce4" />

**Filter Results (Where)** (The (WHERE) keyword filters rows. It keeps only rows that match a condition.)
 
 Query - SELECT * FROM Orders WHERE drink = 'Coffee'; 

 Function - Filter Results - If the database contains coffee orders, you will now see only those rows.

 <img width="1007" height="669" alt="image" src="https://github.com/user-attachments/assets/ba949cfc-5af6-4aea-a6b2-4a9d93b074ce" />

 Sort Results (Order By) - (The ORDER BY keyword sorts results by a column. By default, results are sorted in ascending order (lowest to highest).)

 Query - SELECT * FROM Orders ORDER BY price;

Function - To sort in reverse order (highest to lowest), add DESC.

Ex - <img width="1150" height="858" alt="image" src="https://github.com/user-attachments/assets/6a2e126f-e8b0-4c0b-a0c5-6c72729d9421" />

**Combine Filtering + Sorting**

Query - SELECT * FROM Orders WHERE drink = 'Coffee' ORDER BY price DESC;

Function - filter to keep only one drink type and then sort by price.

Ex - <img width="1030" height="678" alt="image" src="https://github.com/user-attachments/assets/0d7f923a-943e-405b-8600-21241938988f" />



**Skills Learned** 

*Understanding what a database is
*Knowing what tables, rows, and columns are
*Asking simple questions using SQL
*Reading results returned by a database

**SQL Queries Learned**

*SELECT – choose what data to display

*FROM – choose where the data comes from

*WHERE – filter records based on a condition

*ORDER BY – sort results
