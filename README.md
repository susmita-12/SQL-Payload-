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

- ' ORDER BY 1--
- ' ORDER BY 2--
- ' ORDER BY 3--
etc.

- ' UNION SELECT NULL--
- ' UNION SELECT NULL,NULL--
- ' UNION SELECT NULL,NULL,NULL--
etc

#Finding columns with a useful data type in an SQL injection UNION attack
The reason for performing an SQL injection UNION attack is to be able to retrieve the results from an injected query. Generally, the interesting data that you want to retrieve will be in string form, so you need to find one or more columns in the original query results whose data type is, or is compatible with, string data.

Having already determined the number of required columns, you can probe each column to test whether it can hold string data by submitting a series of UNION SELECT payloads that place a string value into each column in turn. For example, if the query returns four columns, you would submit:

- ' UNION SELECT 'a',NULL,NULL,NULL--
- ' UNION SELECT NULL,'a',NULL,NULL--
- ' UNION SELECT NULL,NULL,'a',NULL--
- ' UNION SELECT NULL,NULL,NULL,'a'--

#Retrieving multiple values within a single column
- ' UNION SELECT username || '~' || password FROM users--

#Blind SQL injection vulnerabilities
Blind SQL injection arises when an application is vulnerable to SQL injection, but its HTTP responses do not contain the results of the relevant SQL query or the details of any database errors.

With blind SQL injection vulnerabilities, many techniques such as UNION attacks, are not effective because they rely on being able to see the results of the injected query within the application's responses. It is still possible to exploit blind SQL injection to access unauthorized data, but different techniques must be used.


