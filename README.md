show databases;

use vit;

create table category(c_id int primary key,c_details varchar(30));

insert into category values(101,'AC'),(102,'Fridge'),(103,'Chair'),(104,'TV');



show tables;

desc category;

create table product (p_id int primary key,

p_details varchar(30),

c_id int,

foreign key(c_id) references category(c_id)

);



INSERT INTO product VALUES 

(1, 'SAMSUNG', 101),

(2, 'LG', 102);

desc product;

INSERT INTO category VALUES (1, 'Electronics'), (2, 'Appliances');

INSERT INTO product VALUES 

(101, 'SAMSUNG', 1),

(102, 'LG', 2);

select * from product;

select * from category;

delete from category where c_id=1;

CREATE TABLE product (

    p_id INT PRIMARY KEY,

    p_details VARCHAR(30),

    c_id INT,

    FOREIGN KEY (c_id) REFERENCES category(c_id) ON DELETE CASCADE

);

select * from category;

insert into category values(10,'computer');



UPDATE category

SET c_id = 1

WHERE c_details = 'computer';

create table cont(f_name varchar(30) not null,m_name varchar(30),l_name varchar(30),m_no int unique);

insert into cont values ('hardhik','padey',' ',6547),('rohith','shrma','babu',53784);

select * from cont;

insert into cont values(' ','pushapa','rajjj',3433);

insert into cont values('','pushapa','rajjj',9434);

insert into cont values(null,'pushapa','rajjj',3433);



alter table category

drop primary key;



create table details(

name varchar(20),

m_no int UNIQUE,

address_country varchar(30) DEFAULT 'INDIA'

);

select * from details;

insert into details values ('ramu',4837,'ASIA');

insert into details values ('ramu',65378,null);
