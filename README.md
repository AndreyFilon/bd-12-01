# Домашнее задание к занятию 1 "`«Базы данных»`" - `Филон Андрей`

Заказчик передал вам файл в формате Excel, в котором сформирован отчёт.  
На основе этого отчёта нужно выполнить следующие задания.

### Задание 1

Опишите не менее семи таблиц, из которых состоит база данных:  
    какие данные хранятся в этих таблицах;  
    какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.  

Приведите решение к следующему виду:  
Сотрудники (  
    идентификатор, первичный ключ, serial,  
    фамилия varchar(50),  
    ...  
    идентификатор структурного подразделения, внешний ключ, integer).  

### Ответ

#### 1) Таблица Сотрудники  

Идентификатор, PRIMARY KEY, INT, NOT NULL, AUTO_INCREMENT  
ФИО, VARCHAR(100), NOT NULL  
Адрес, VARCHAR(150), NOT NULL  
Идентификатор структурного подразделения, FOREIGN KEY, INT, NOT NULL  

#### 2) Таблица Структурные подразделения   

Идентификатор, PRIMARY KEY, INT, NOT NULL, AUTO_INCREMENT  
Наименование подразделения, VARCHAR(60), NOT NULL   

#### 3) Таблица Должности   

Идентификатор, PRIMARY KEY, INT, NOT NULL, AUTO_INCREMENT  
Наименование, VARCHAR(60), NOT NULL  
Оклад, DECIMAL(10,2), NOT NULL   

#### 4) Таблица Тип подразделения  

Идентификатор, PRIMARY KEY, INT, NOT NULL, AUTO_INCREMENT  
Наименование varchar(50), not null  

#### 5) Таблица Область  

Идентификатор, PRIMARY KEY, INT, NOT NULL, AUTO_INCREMENT  
Наименование, VARCHAR(50), NOT NULL 

#### 6) Таблица Город  

Идентификатор, PRIMARY KEY, INT, NOT NULL, AUTO_INCREMENT  
Наименование, VARCHAR(50), NOT NULL  

#### 7) Таблица Адрес  

Идентификатор, PRIMARY KEY, INT, NOT NULL, AUTO_INCREMENT  
Наименование, VARCHAR(200), NOT NULL   
 
#### 8) Таблица  Адрес филиала  

Идентификатор области, FOREIGN KEY, INT, NOT NULL  
Идентификатор города, FOREIGN KEY, INT, NOT NULL  
Идентификатор адреса, FOREIGN KEY, INT, NOT NULL  

#### 9) Таблица  Проекты

Идентификатор, PRIMARY KEY, INT, NOT NULL, AUTO_INCREMENT  
Наименование, VARCHAR(200), NOT NULL  

#### 10) Таблица Сотрудник/Тип подразделения/Структурное подразделение

Идентификатор сотрудника, FOREIGN KEY, INT, NOT NULL  
Идентификатор типа подразделения, FOREIGN KEY, INT, NOT NULL  
Идентификатор структурного подразделения, FOREIGN KEY, INT, NOT NULL
дата найма, DATE, NOT NULL  

---
