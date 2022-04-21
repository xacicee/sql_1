# sql_1
create table  accounts(
    user_id serial PRIMARY KEY ,
    user_name VARCHAR(60) UNIQUE NOT NULL ,
    password VARCHAR(40) NOT NULL ,
    email VARCHAR(110) UNIQUE NOT NULL ,
    created_on TIMESTAMP NOT NULL ,
    last_login timestamp
);

INSERT INTO  accounts(user_name, password, email, created_on, last_login)
VALUES ('gizem','gizemiko1','info@gizo.net', current_timestamp, current_timestamp );


insert into accounts (user_name,password,email,created_on,last_login)
values ('sena', 'sena_bir', 'info@sena.net', current_timestamp, current_timestamp);


insert into accounts (user_name, password, email, created_on, last_login)
values ('zehra', 'zehra_1', 'info@zehra.net', current_timestamp, current_timestamp);


insert into accounts(user_name, password, email, created_on, last_login)
values('ayşe', 'ayse_23', 'info@ayse.net', current_timestamp, current_timestamp);


insert into accounts (user_name, password, email, created_on, last_login)
values ('kemal', 'kemal_01', 'info@kemal.net', current_timestamp, current_timestamp);

select*from accounts ; 

select user_name from accounts ;

select password from accounts ;

select email from accounts ;

select created_on from accounts ;

select last_login from accounts ;

select*from accounts where user_id=1;

select*from accounts where user_id=8;

select* from accounts where user_name='ayşe';

select*from accounts where user_name like '%zehra%';

select*from accounts  where user_name like '%kemal';

select*from accounts where user_name is not null and user_name like '%zehra';

select*from accounts where user_id>1;

select*from accounts where user_id in(1,4,5,8);

select *from accounts where user_id between 3 and 5;

select*from accounts where user_id =1 or user_id=10;

select*from accounts where user_id<>1;

select *from accounts where user_id!=1;

select *from accounts where user_id is not null;

select *from accounts where user_id>2;

select*from accounts where length(user_name) between 1 and 11 order by user_name asc;

select*from accounts where length(user_name) between 1 and 11 order by user_name desc;



alter table accounts add COLUMN birth_year INT;

update accounts set birth_year=2001 where user_name='ayşe';

update accounts set birth_year=1999 where user_name='zehra';

update accounts set birth_year=2016 where user_name='kemal';


