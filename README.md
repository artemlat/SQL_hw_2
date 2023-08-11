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
*Result is like in the second task*

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

14. Вывести пользователей которые были созданы 2021-07-12 00:00:00 и имеют пароль 1m313

```
select name from students
where created_on = '2021-07-12 00:00:00' and password = '1m313';
```
![hw_2_14](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_14.png)

15. Вывести пользователей которые были созданы 2021-07-12 00:00:00 и у которых в имени
есть слово Andrey

```
select name from students
where created_on = '2021-07-12 00:00:00' and name like '%Andrey%';
```
![hw_2_15](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_15.png)

16. Вывести пользователей которые были созданы 2021-07-12 00:00:00 и у которых в имени есть цифра 8

```
select name from students
where created_on = '2021-07-12 00:00:00' and name like '%8%';
```
![hw_2_16](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_16.png)

17. Вывести пользователя у которых id равен 110

```
select name from students
where id = 110;
```
![hw_2_17](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_17.png)

18. Вывести пользователя у которых id равен 153

```
select name from students
where id = 153;
```
![hw_2_18](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_18.png)

19. Вывести пользователя у которых id больше 140

```
select name from students
where id > 140;
```
![hw_2_19(1)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_19(1).png)![hw_2_19(2)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_19(2).png)

20. Вывести пользователя у которых id меньше 130

```
select name from students
where id < 130;
```
![hw_2_20](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_20.png)

21. Вывести пользователя у которых id меньше 127 или больше 188

```
select name from students
where id < 127 or id > 188;
```
![hw_2_21(1)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_21(1).png)![hw_2_21(2)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_21(2).png)

22. Вывести пользователя у которых id меньше либо равно 137

```
select name from students
where id <= 137
order by id;
```
![hw_2_22](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_22.png)

23. Вывести пользователя у которых id больше либо равно 137

```
select name from students
where id >= 137;
```
![hw_2_23(1)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_23(1).png)![hw_2_23(2)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_23(2).png)

24. Вывести пользователя у которых id больше 180 но меньше 190

```
select name from students 
where id > 180 and id < 190;
```
![hw_2_24](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_24.png)

25. Вывести пользователя у которых id между 180 и 190

```
select name from students 
where id between 180 and 190;
```

![hw_2_25](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_25.png)

26. Вывести пользователей где password равен 12333, 1m313, 123313

```
select name from students 
where password in ('12333', '1m313', '123313');
```

![hw_2_26](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_26.png)

27. Вывести пользователей где created_on равен 2020-10-03 00:00:00, 2021-05-19 00:00:00, 
2021-03-26 00:00:00

```
select name from students 
where created_on in ('2020-10-03 00:00:00', '2021-05-19 00:00:00', '2021-03-26 00:00:00');
```
![hw_2_27](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_27.png)

28. Вывести минимальный id

```
select min(id) from students;
```
![hw_2_28](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_28.png)

29. Вывести максимальный id

```
select max(id) from students;
```
![hw_2_29](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_29.png)

30. Вывести количество пользователей

```
select count(*) from students;
```
![hw_2_30](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_30.png)

31. Вывести id пользователя, имя, дату создания пользователя. 
Отсортировать по порядку возрастания даты добавления пользоватлеля.

```
select id, name, created_on from students
order by created_on;
```
![hw_2_32(1)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_32(1).png)![hw_2_32(2)](https://github.com/artemlat/SQL_hw_2/blob/main/hw_2_32(2).png)












