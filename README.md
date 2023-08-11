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
![hw_2_2(1)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_2(2).png) ![hw_2_2(3)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_2(3).png)   

3. Вывести только Id пользователей

```
select id from public.students;
```
![hw_2_3(1)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_3(1).png)![hw_2_3(2)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_3(2).png)

4. Вывести только имя пользователей

```
select name from students;
```

5. Вывести только email пользователей

```
select email from students;
```

![hw_2_5(1)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_5(1).png)![hw_2_5(2)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_5(2).png)  

6. Вывести имя и email пользователей

```
select name, email from students;
```
![hw_2_6(1)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_6(1).png)![hw_2_6(2)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_6(2).png)  

7. Вывести id, имя, email и дату создания пользователей

```
select id, name, email, created_on from students;
```
![hw_2_7(1)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_7(1).png)![hw_2_7(2)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_7(2).png)

8. Вывести пользователей где password 12333

```
select name from students 
where password = '12333';
```
![hw_2_8](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_8.png)

9. Вывести пользователей которые были созданы 2021-03-26 00:00:00

```
select name from students
where created_on = '2021-03-26 00:00:00';
```
![hw_2_9](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_9.png)

10. Вывести пользователей где в имени есть слово Анна

```
select name from students
where name like '%Анна%';

select name from students
where name like '%Anna%';
```
![hw_2_10(1)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_10(1).png)![hw_2_10(2)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_10(2).png)

11. Вывести пользователей где в имени в конце есть 8

```
select name from students
where name like '%8';
```
![hw_2_11](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_11.png)

12. Вывести пользователей где в имени в есть буква а

```
select name from students
where name like '%a%';
```

![hw_2_12(1)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_12(1).png)![hw_2_12(2)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_12(2).png)![hw_2_12(3)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_12(3).png)

13. Вывести пользователей которые были созданы 2021-07-12 00:00:00

```
select name from students 
where created_on = '2021-07-12 00:00:00';
```

![hw_2_13](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_13.png)





