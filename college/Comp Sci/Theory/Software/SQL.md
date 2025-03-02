Structured Query Language
Keywords must be in capitals for OCR but will still work in modern SQL
Database languages are divided into DDL (Data Definition Language) and DML (Data Manipulation Language)
DDL defines the database e.g. create table and links between them
An underscore represents a single character while a percentage sign represents multiple, as in LIKE 'A%' would search for any record that starts with a capital A and LIKE '%a' would search for any records that end with a lowercase a.

The **GROUP BY** clause is used with **SLELECT** to arrange data into groups, it is written like; 
SELECT column_name(s)
FROM table_name
GROUP BY column_name(s);
