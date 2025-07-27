CREATE TABLE AUTHORS (
Author_id int primary key,
name varchar(50),
country varchar(50)
);

CREATE TABLE BOOKS(
book_id int primary key,
title varchar(100),
author_id int,
foreign key(author_id) references Authors (author_id)
);

 describe authors;
 describe books;
 

 INSERT INTO AUTHORS VALUES (1, 'ASHISH', 'INDIA'),
(2, ,'SMARAN', 'USA'),
(3, 'VAIBHAV', 'UK');

INSERT INTO BOOKS VALUES (101, 'DATA SCIENCE BASICS', 1),
(102, 'AI IN EDUCATION', 2),
(103, 'SQL SIMPLIFIED',3);

SELECT * FROM AUTHORS;
SELECT * FROM BOOKS;


select b.title, a.name, a.country from authors a inner join Books b on a.author_id b.author_id;
