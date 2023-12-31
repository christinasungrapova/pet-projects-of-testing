# Баг-репорты

## Activities

### Баг №1. Неправильный код состояния ответа при отправке запроса POST​/api​/v1​/Activities.

***Автор:*** delmarbo(Inna).

***Окружение:*** Microsoft Edge Версия 117.0.2045.43.

***Серьезность:*** S3 Major (значительный).

***Приоритет:*** P2 Medium (средний).

***Предшествующие условия:***
- Открыт сайт https://fakerestapi.azurewebsites.net/index.html.
- Открыта секция Activities.
- Нажата строка POST​/api​/v1​/Activities.
- Нажата кнопка Try it out.

***Шаги:***  
1. Отправить POST запрос <https://fakerestapi.azurewebsites.net/api/v1/Activities>  с телом запроса:  
```
{  
 "id": 0,  
 "title": "string",  
 "dueDate": "2023-09-25T19:25:34.272Z",  
 "completed": true  
} 
``` 
2. Проверить код состояния ответа.

***Фактический результат:*** Код состояния ответа - 200 OK. 

***Ожидаемый результат:*** Код состояния ответа - 201 Created.   


### Баг №2. Неправильный код состояния ответа при отправке запроса DELETE​/api​/v1​/Activities​/{id}.

***Автор:*** delmarbo(Inna).

***Окружение:*** Microsoft Edge Версия 117.0.2045.43. 

***Серьезность:*** S3 Major (значительный).

***Приоритет:*** P2 Medium (средний).

***Предшествующие условия:***  
- Открыт сайт https://fakerestapi.azurewebsites.net/index.html.
- Открыта секция Activities.
- Нажата строка POST​/api​/v1​/Activities.
- Нажата кнопка Try it out.

***Шаги:***  
1. Отправить POST запрос <https://fakerestapi.azurewebsites.net/api/v1/Activities/5> с номером id = 5. 
2. Проверить код состояния ответа.    

***Фактический результат:***  Код состояния ответа - 200 OK.  

***Ожидаемый результат:***  Код состояния ответа - 204.


## Authors

### Баг №3. Неправильный код состояния ответа при отправке запроса POST/api/v1/Authors. 

***Автор:*** delmarbo(Inna).

***Окружение:*** Microsoft Edge Версия 117.0.2045.43. 

***Серьезность:*** S3 Major (значительный).

***Приоритет:*** P2 Medium (средний).

***Предшествующие условия:***   
- Открыт сайт https://fakerestapi.azurewebsites.net/index.html.
- Открыта секция Authors.
- Нажата строка POST​/api​/v1​/Authors.
- Нажата кнопка Try it out.

***Шаги:***  
1. Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/Authors с телом запроса:  
```
{  
 "id": 0,  
 "idBook": 0,  
 "firstName": "Лев",  
 "lastName": "Толстой"  
} 
```      
2. Проверить код состояния ответа.   

***Фактический результат:*** Код состояния ответа - 200 OK.  

***Ожидаемый результат:***  Код состояния ответа - 201 Created.  


### Баг №4. Неправильный код состояния ответа при отправке запроса DELETE/api/v1/Authors/{id}

***Автор:*** delmarbo(Inna).

***Окружение:*** Microsoft Edge Версия 117.0.2045.43. 

***Серьезность:*** S3 Major (значительный).

***Приоритет:*** P2 Medium (средний).

***Предшествующие условия:***
- Открыт сайт https://fakerestapi.azurewebsites.net/index.html.
- Открыта секция Authors.
- Нажата строка DELETE/api/v1/Authors/{id}.
- Нажата кнопка Try it out.

***Шаги:***  
1. Отправить DELETE запрос <https://fakerestapi.azurewebsites.net/api/v1/Authors/{id}> указав id=1 в пути запроса.  
2. Проверить код состояния ответа.

***Фактический результат:*** Код состояния ответа - 200 OK.

***Ожидаемый результат:*** Код состояния ответа - 204 No Content.  


## Books

### Баг №5. Неправильный код состояния ответа при отправке запроса POST/api/v1/Books.

***Автор:*** catherib(Кристина)

***Окружение:*** ПК Windows 10 Домашняя, Яндекс.Браузер (Версия
23.7.4.971 (64-bit)).

***Серьезность:*** S3 Major (значительный).

***Приоритет:*** P2 Medium (средний).

***Предшествующие условия:***
- Открыт сайт https://fakerestapi.azurewebsites.net/index.html.
- Открыта секция Authors.
- Нажата строка Нажата строка POST/api/v1/Books.
- Нажата кнопка Try it out.

***Шаги:*** 
1. Выбрать любой из 3-х заголовков запроса:
- application/json; v=1.0
- text/json; v=1.0
- application/*+json; v=1.0
2. Внести данные "id": 300 в тело запроса.
3. Нажать на кнопку “Execute”.
4. Проверить код состояния.

***Фактический результат:*** Код состояния ответа - 200 OK.  

***Ожидаемый результат:***  Код состояния ответа - 201 Created. 


## CoverPhotos

### Баг №6. Неправильный код состояния ответа при отправке запроса POST​/api​/v1​/CoverPhotos c неверным значением.

***Автор:*** leobaldg(Авелина).

***Окружение:*** Windows 10 Pro, Google Chrome Версия 117.0.5938.132.

***Серьезность:*** S3 Major (значительный).

***Приоритет:*** P2 Medium (средний).

***Предшествующие условия:***
- Открыт сайт https://fakerestapi.azurewebsites.net/index.html.
- Открыта секция CoverPhotos.
- Нажата строка Нажата строка POST​/api​/v1​/CoverPhotos.
- Нажата кнопка Try it out.

***Шаги:***
1. Отправить POST запрос <https://fakerestapi.azurewebsites.net/api​/v1​/CoverPhotos> с телом запроса:  
```
{
  "id": 93,
  "idBook": 0,
  "url": "0"
}
```
2. Проверить код состояния ответа.

***Фактический результат:*** Код состояния ответа - 200 OK.

***Ожидаемый результат:*** Код состояния ответа - 400 Bad Request.

### Баг №7. Неправильный код состояния ответа при отправке запроса PUT​/api​/v1​/CoverPhotos с неверным значением.

***Автор:*** leobaldg(Авелина).

***Окружение:*** Windows 10 Pro, Google Chrome Версия 117.0.5938.132.

***Серьезность:*** S3 Major (значительный).

***Приоритет:*** P2 Medium (средний).

***Предшествующие условия:***
- Открыт сайт https://fakerestapi.azurewebsites.net/index.html.
- Открыта секция CoverPhotos.
- Нажата строка Нажата строка PUT​/api​/v1​/CoverPhotos.
- Нажата кнопка Try it out.

***Шаги:***  
1. Отправить POST запрос <https://fakerestapi.azurewebsites.net//api​/v1​/CoverPhotos> с телом запроса:  
```  
{
  "id": 13,
  "idBook": 0,
  "url": "01"
}  
```
2. Проверить код состояния ответа.

***Фактический результат:*** Код состояния ответа - 200 OK.

***Ожидаемый результат:*** Код состояния ответа - 400 Bad Request.

## Users

### Баг №8. Неправильный код состояния ответа при отправке запроса POST​/api​/v1​/Users.

***Автор:*** oolongeo (Вера).

***Окружение:*** Yandex Версия 23.7.5.704, (64- bit).

***Серьезность:*** S3 Major (значительный).

***Приоритет:*** P2 Medium (средний).

***Предшествующие условия:***
- Открыт сайт https://fakerestapi.azurewebsites.net/index.html.
- Открыта секция Users.
- Нажата строка Нажата строка POST​/api​/v1​/Users.
- Нажата кнопка Try it out.

***Шаги:***  
1.Отправить POST запрос <https://fakerestapi.azurewebsites.net/api/v1/Users>  с телом запроса:  
```
{  
 "id": 0,  
 "userName": "Ivan",  
 "password": "12345"  
}  
```
2. Проверить код состояния ответа. 

***Фактический результат:*** Код состояния ответа - 200 OK.

***Ожидаемый результат:*** Код состояния ответа - 201 Created.

### Баг №9. Неправильный код состояния ответа при отправке запроса DELETE​/api​/v1​/Users​/{id}.

***Автор:*** oolongeo (Вера).

***Окружение:*** Yandex Версия 23.7.5.704, (64- bit).

***Серьезность:*** S3 Major (значительный).

***Приоритет:*** P2 Medium (средний).

***Предшествующие условия:***
- Открыт сайт https://fakerestapi.azurewebsites.net/index.html.
- Открыта секция Users.
- Нажата строка Нажата строка DELETE​/api​/v1​/Users​/{id}.
- Нажата кнопка Try it out.

***Шаги:***  
1. Отправить POST запрос <https://fakerestapi.azurewebsites.net/api/v1/Users/5> с номером id=5.
2. Проверить код состояния ответа.

***Фактический результат:*** Код состояния ответа - 200 OK.

***Ожидаемый результат:*** Код состояния ответа - 204 No Content.