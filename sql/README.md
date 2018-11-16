# SQL 

Online practice: https://www.db-fiddle.com

[Sql - Structured Query Language](https://en.wikipedia.org/wiki/SQL)

Common databases MySQL, PostgresSQL

CREATE TABLE users 
( 
  id INT PRIMARY KEY AUTO_INCREMENT, 
  email CHAR(50) NOT NULL,
  name CHAR(50),
  `password` CHAR(50)
);

INSERT INTO users (email, name, `password`) 
VALUE
	('user@example.com', 'Simple user', 'simple password'),
    ('user2@example.com', 'Simple user2', '12345')
; 

INSERT INTO users (email, name, `password`) 
VALUES('tony@stark.com', 'Tony Stark', 'awesome'),
('ironman@stark.com', 'Iron Man', 'strong password'),
('hulk@mit.com', 'Bruce Banner', 'anger'),
('loki@asgard.space', 'Loki', 'ghost'),
('thor@asgard.space', 'Thor', 'god of thunder!');
