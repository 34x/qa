# SQL 

## What sql is

## Tables and how to create them

## Select, sort and conditional statements

## Update statements

## Delete statements


[Online practice](https://www.db-fiddle.com)

[Sql - Structured Query Language](https://en.wikipedia.org/wiki/SQL)

**Common SQL databases:** MySQL, PostgresSQL, SQLite

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

```INSERT INTO users (email, name, `password`)``` - password is a key word, email and name are not key words

**Key word** - is a specific word 

[Keywords MySQL](https://dev.mysql.com/doc/refman/5.7/en/keywords.html)

SELECT * FROM USERS;  - Query Error: Error: ER_NO_SUCH_TABLE: Table 'test.USERS' doesn't exist - MySQLis case sensitive for tables


`SELECT name, id FROM users;` - correct word order for making request (SELECT [column names separated with comma or * for all columns] FROM [table name])

`SELECT name, id FROM users ORDER BY name;` - to sort by spesific order use ORDER BY and the name of a column

`SELECT name, id FROM users ORDER BY name DESC;` - to sort in descendent order use DESC

`SELECT name, id FROM users ORDER BY name ASC;` - to sort in ascendent order use ASC

`-- SELECT name, id FROM users ORDER BY name ASC;` - to prevent from execution (to comment a line)

```sql
-- To make a simple select from users table with all rows - this is a simple comment, that will not be executed
SELECT * FROM users; 
```

[Comment Syntax](https://dev.mysql.com/doc/refman/5.7/en/comments.html)

With `LIKE` you can use the following wildcard character in the pattern: 

`SELECT * FROM users WHERE email LIKE '%com';` - it finds everything that ends with **com**

`SELECT * FROM users WHERE email LIKE '%com%';` - it finds everything that contains only **com**

`SELECT * FROM users WHERE email LIKE 'com%';` - it finds everything that begins with **com**

`SELECT * FROM users *WHERE email LIKE '%com';`* - WHERE is a condition 

`UPDATE users SET name = "Allmighty Loki" WHERE id = '5';` - the way to change the name

*In case of using sql injection:*

`SELECT name FROM users WHERE name LIKE '%Lo'; SELECT email, `password` FROM users; -- %';`

*The way to avoid sql injection* - code part
`SELECT * FROM users WHERE name LIKE '%\'%';`



## SQL Injections

Example html form: email, name, body.

Example table:

id | email | name | body |ip
---|-------|------|------|---
int|string |string|string|string

New post create query: 

```sql 
INSERT INTO post (id, email, name, body)
       VALUES(((SELECT count(*) FROM post) + 1), '$email', '$name', '$body')
```

SQL injection (written in the `body` field):


`a'); DELETE FROM post; -- wtf`

Search query: 

```sql
SELECT * FROM post WHERE email LIKE '%$term%' OR name LIKE '%$term%' OR body LIKE '%$term%' LIMIT 100;
```

SQL injection (written in the `search` field) that reveal user IP to anyone:

`text' UNION SELECT id, email, name, ip as body, ip FROM post; -- `
