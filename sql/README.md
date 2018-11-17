# SQL 

Online practice: https://www.db-fiddle.com

[Sql - Structured Query Language](https://en.wikipedia.org/wiki/SQL)

Common databases: MySQL, PostgresSQL

```sql
CREATE TABLE users 
( 
  id INT PRIMARY KEY AUTO_INCREMENT, 
  email CHAR(50) NOT NULL,
  name CHAR(50),
  `password` CHAR(50)
);
```
```sql
INSERT INTO users (email, name, `password`) 
VALUE ('user@example.com', 'Simple user', 'simple password'); 
```
```sql
INSERT INTO users (email, name, `password`) 
VALUES('tony@stark.com', 'Tony Stark', 'awesome'),
('ironman@stark.com', 'Iron Man', 'strong password'),
('hulk@mit.com', 'Bruce Banner', 'anger'),
('loki@asgard.space', 'Loki', 'ghost'),
('thor@asgard.space', 'Thor', 'god of thunder!');
```
INSERT INTO users (email, name, `password`)  - password is a key word, email and name are not key words
Key word - is a specific word 

Keywords - https://dev.mysql.com/doc/refman/5.7/en/keywords.html

SELECT * FROM USERS;  - Query Error: Error: ER_NO_SUCH_TABLE: Table 'test.USERS' doesn't exist - MySQLis case sensitive for tables

SELECT name, id FROM users; - correct word order for making request (SELECT [column names separated with comma or * for all columns] FROM [table name])

SELECT name, id FROM users ORDER BY name; - to sort by spesific order use ORDER BY and the name of a column

SELECT name, id FROM users ORDER BY name DESC; - to sort in descendent order use DESC

SELECT name, id FROM users ORDER BY name ASC; - to sort in ascendent order use ASC

-- SELECT name, id FROM users ORDER BY name ASC; - to prevent from execution (to comment a line)

```sql
-- To make a simple select from users table with all rows - this is a simple comment, that will not be executed
SELECT * FROM users; 
```

Comment Syntax - https://dev.mysql.com/doc/refman/5.7/en/comments.html

With `LIKE` you can use the following wildcard character in the pattern: 

`SELECT * FROM users WHERE email LIKE '%com';` - it finds everything that ends with **com**

`SELECT * FROM users WHERE email LIKE '%com%';` - it finds everything that contains only **com**

`SELECT * FROM users WHERE email LIKE 'com%';` - it finds everything that begins with **com**


