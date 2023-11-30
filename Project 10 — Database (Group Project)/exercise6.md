Задание 6.

# Создание SQL-запросов

## Таблица Shippers

### Запрос №1: 
Находит всех грузоотправителей у которых в номере телефона: 98

SELECT * FROM Shippers

WHERE phone LIKE "%98%";

![Alt text](Shippers-9.png)

### Запрос №2: 
Находит номер телефона грузовой компании Federal Shipping

SELECT phone FROM Shippers

WHERE ShipperName = "Federal Shipping";

![Alt text](Shippers-10.png)

### Запрос №3: 
Находит первых двух грузоотправителей у которых в номере телефона есть "555" и сортирует их в алфавитном порядке по названию

SELECT * FROM Shippers

WHERE phone LIKE "%555%"

ORDER BY ShipperName LIMIT 2;

![Alt text](Shippers-11.png)

## Таблица Suppliers

### Запрос №1: 
Перечисляет количество поставщиков в каждой стране

SELECT COUNT (SupplierID), country 

FROM Suppliers GROUP BY country;

![Alt text](Suppliers-20.png)

### Запрос №2: 
Находит страны где поставщиков больше одного

SELECT COUNT (SupplierID), country 

FROM Suppliers GROUP BY country

HAVING COUNT (SupplierID) > 1;

![Alt text](Suppliers-21.png)

### Запрос №3: 
Находит страны в алфавитном порядке, в промежутке с А по К, с количеством поставщиков больше двух

SELECT COUNT (SupplierID), country FROM Suppliers

WHERE country BETWEEN "A%" AND "K%"

GROUP BY country

HAVING COUNT (SupplierID) > 2 ORDER BY country;

![Alt text](Suppliers-22.png)

## Таблица OrderDetails

### Запрос №1: 
Показывает, какое количество продукта под номером 4 было куплено в промежутке 10300 по 10400 номера заказов

SELECT SUM (Quantity),ProductID FROM OrderDetails

WHERE OrderID BETWEEN 10300 AND 10400

AND ProductID = 75;

![Alt text](OrderDetails-12.png)

### Запрос №2: 
Показывает количество продуктов у каждого заказа

SELECT OrderID, SUM (Quantity)

FROM OrderDetails GROUP BY OrderID;

![Alt text](OrderDetails-13.png)

### Запрос №3: 
Находит номер двух продуктов, который покупали меньше всех

SELECT ProductID, SUM (Quantity) FROM OrderDetails

GROUP BY ProductID

ORDER BY SUM (Quantity) LIMIT 1;

![Alt text](OrderDetails-14.png)

## Таблица Customers

### Запрос №1:  
Находит id  заказчиков из Парижа

SELECT Country,CustomerID FROM Customers

WHERE City = 'Paris'

![Alt text](Customers.png)

### Запрос №2:  
Отображает количество клиентов из страны Германия

SELECT * FROM Customers

WHERE Country ="Germany"

![Alt text](Customers-1.png)

### Запрос №3: 
Отображает выбор города, подсчитывает ID, как номера клиентов, где имя клиента отсутствует в "Around the Horn" Drachenblut Delikatessend, группировка по городам имеющий номер клиентов >= 5

SELECT City, count(CustomerID) AS number_of_clients FROM Customers

WHERE CustomerName NOT IN ('Around the Horn','Drachenblut Delikatessend')

GROUP BY City HAVING number_of_clients >= 5

![Alt text](Customers-2.png)

## Таблица Categories

### Запрос №1: 
Отображает запись в таблице, где в описании присутствует слово "сыры".

SELECT * FROM Categories

WHERE Description LIKE'Cheeses';

![Alt text](Categories-3.png)

### Запрос №2: 
Отображает количество категорий

SELECT count(CategoryName) AS category\_quantity FROM Categories;

![Alt text](Categories-4.png)

### Запрос №3: 
Этот запрос отображает выбор из таблицы "Категории", где название категории равно "Приправы" или название категории равно "Морепродукты"

SELECT * FROM Categories

WHERE CategoryName="Condiments"OR CategoryName="Seafood";

![Alt text](Categories-5.png)

## Таблица Employees

### Запрос №1: 
Отображает все строки резюме кроме имени 'Buchanan'.

SELECT * FROM Employees 

WHERE NOT LastName='Buchanan'

![Alt text](Employees-6.png)

### Запрос №2: 
Выбор резюме с номером ID >= 7

SELECT * FROM Employees

WHERE EmployeeID >=7;

![Alt text](Employees-7.png)

### Запрос №3: 
Выбрать индификатор сотрудника по фамилии и фото.

SELECT EmployeeID LastName, Photo 

FROM Employees

WHERE EmployeeID >=1;

![Alt text](Employees-8.png)

## Таблица Orders

### Запрос №1: 
Сортировка заказов за декабрь 1996 года.

SELECT * FROM Orders

WHERE OrderDate LIKE '%1996-12%';

![Alt text](Orders-15.png)

### Запрос №2: 
Сортировка заказов с номером сотрудника “1” и номером грузоотправителя “1” из всех пользователей.

SELECT * FROM Orders

WHERE EmployeeID LIKE "1" and ShipperID LIKE "1"

ORDER BY CustomerID;

![Alt text](Orders-16.png)

### Запрос №3: 
Выбор даты заказа, идентификатора отправителя из заказов, где ордер ID больше 10435.

SELECT OrderDate, ShipperID 

FROM Orders

WHERE OrderID > "10435";

![Alt text](Orders-17.png)

## Таблица Products

### Запрос №1: 
Просмотр продукта с минимальной ценой.

SELECT ProductID,ProductName,Unit,MIN(Price) 

FROM Products;

![Alt text](Products-18.png)

### Запрос №2: 
Выбор названия продукта и его цены, где цена >= 123,79

SELECT ProductName, Price 

FROM Products

WHERE Price >="123.79"

![Alt text](Products-19.png)

### Запрос №3:  
Отображает выбор прайса, подсчитывает 
ID, как номера клиентов, где имя клиента отсутствует 
в ('Thüringer Rostbratwurst','Scottish Longbreads'), 
группировка по прайсам, имеющий номер клиентов >= 5

SELECT Price, count(SupplierID) AS number_of_clients FROM Products

WHERE ProductName NOT IN ('Thüringer Rostbratwurst','Scottish Longbreads')

GROUP BY Price HAVING number_of_clients >= 3;

![Alt text](Products-23.png)

