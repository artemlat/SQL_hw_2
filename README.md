# SQL second homework  
*Here I continued to work with sql requests.*  

```CREATE TABLE public.students (
	id serial4 NOT NULL,
	"name" varchar(50) NOT NULL,
	email varchar(50) NOT NULL,
	"password" varchar(50) NOT NULL,
	created_on timestamp NOT NULL,
	CONSTRAINT students_email_key UNIQUE (email),
	CONSTRAINT students_pkey PRIMARY KEY (id)
);
```

*Then import data to public.students table from another database or from .csv file*  

1. Вывести все поля и все строки.

```
select * from public.students;
```
![hw_2_1(1)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_1(1).png)  
![hw_2_1(2)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_1(222).png)
![hw_2_1(3)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_1(3).png)
![hw_2_1(4)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_1(4).png)
2. Вывести всех студентов в таблице

```
select name from students;
```


