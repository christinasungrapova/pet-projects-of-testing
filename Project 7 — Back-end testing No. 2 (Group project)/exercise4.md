## Activities  

**1. GET.Получение списка активностей**    
- URL запроса: {{base_url}}/api/v1/Activities    
- Ожидаемый результат: HTTP Status: 200 Success, Список активностей получен  
- Заголовки запроса:   
User-Agent: PostmanRuntime/7.33.0  
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 08c2a871-1af9-4695-a036-6af4d9bbd4b3  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:  Нет  
- Заголовки ответа:   
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Sat07 Oct 2023 10:21:16 GMT   
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:    
```json   
 [  
  {  
        "id": 1,
        "title": "Activity 1",
        "dueDate": "2023-10-07T11:21:17.7533357+00:00",
        "completed": false 
  },  
  {  
        "id": 2,
        "title": "Activity 2",
        "dueDate": "2023-10-07T11:21:17.7533357+00:00",
        "completed": true  
  },
  {  
        "id": 3,
        "title": "Activity 3",
        "dueDate": "2023-10-07T11:21:17.7533357+00:00",
        "completed": false  
  },  
  {  
        "id": 4,
        "title": "Activity 4",
        "dueDate": "2023-10-07T11:21:17.7533357+00:00",
        "completed": true  
  },    
  ......  
```    
  **2. POST.Создание новой активности**    
- URL запроса: {{base_url}}/api/v1/Activities  
- Ожидаемый результат: HTTP Status: 201 Created, Новая активность добавлена  
- Заголовки запроса:   
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: * /*   
Cache-Control: no-cache  
Postman-Token: 34414ca9-f874-4240-a612-fb7cee507230  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:    
```json    
{
 "id": 0,
 "title": "string",
 "dueDate": "2023-10-07T10:35:40.575Z",
 "completed": true
}   
```    
- Заголовки ответа:   
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Sat07 Oct 2023 10:41:11 GMT   
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:  
```json    
{
    "id": 0,
    "title": "string",
    "dueDate": "2023-10-07T10:35:40.575Z",
    "completed": true
}    
```    
  **3. GET.Получение активности по id**    
- URL запроса: {{base_url}}/api/v1/Activities/{{id}}  
- Ожидаемый результат: HTTP Status: 200 Success, Получена информация об активности под номером 1  
- Заголовки запроса:   
User-Agent: PostmanRuntime/7.33.0  
Accept: * /*   
Cache-Control: no-cache  
Postman-Token: 300f8276-da0d-4a97-a2a0-ab39b697bd22  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса: Нет    
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Sat07 Oct 2023 11:19:34 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:  
```json      
{
    "id": 1,
    "title": "Activity 1",
    "dueDate": "2023-10-07T12:19:34.7317459+00:00",
    "completed": false
}   
```    
  **4. PUT.Редактирование по id активности**    
- URL запроса: {{base_url}}/api/v1/Activities/{{id}}  
- Ожидаемый результат: HTTP Status: 200 Success, Значение параметра "completed": true у активности №1 изменено  
- Заголовки запроса:   
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 62104f86-0e2c-4ff2-944e-53e5867e6333  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:    
```json    
{
  "id": 1,
  "title": "string",
  "dueDate": "2023-10-07T11:48:00.388Z",
  "completed": true
}   
```    
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Sat07 Oct 2023 11:57:46 GMT 
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:  
```json      
{
    "id": 1,
    "title": "string",
    "dueDate": "2023-10-07T11:48:00.388Z",
    "completed": true
}  
```    
  **5. DELETE.Удаление по id активности**    
- URL запроса: {{base_url}}/api/v1/Activities/{{activity_id}}  
- Ожидаемый результат: HTTP Status: 204, Активность под номером 5 - удалена  
- Заголовки запроса:   
User-Agent: PostmanRuntime/7.33.0  
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 2997a920-a87a-42a7-82cd-4ff568dc8872  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса: Нет    
- Заголовки ответа:   
Content-Length: 0  
Date: Sat07 Oct 2023 12:09:23 GMT  
Server: Kestrel  
api-supported-versions: 1.0  
- Тело ответа: Нет  

**6. GET. Получение активности по неверному id**    
- URL запроса: {{base_url}}/api/v1/Activities/{{activity_id_invalid}}  
- Ожидаемый результат: HTTP Status: 404 Error: Not Found, Информация об активности под номером 0 не найдена  
- Заголовки запроса:   
User-Agent: PostmanRuntime/7.33.0  
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 54053a32-6dac-4b8d-b019-7549b8894b87  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса: Нет    
- Заголовки ответа:   
Content-Type: application/problem+json; charset=utf-8; v=1.0  
Date: Sat07 Oct 2023 11:19:34 GMT   
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:      
```json   
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-78ea973023325740bf94f6f92e2ec745-fac688941ec68846-00"
}  
```  
 **7. POST. Создание новой активности с неверным телом запроса**    
- URL запроса: {{base_url}}/api/v1/Activities  
- Ожидаемый результат: HTTP Status: 400 Error: Bad Request, Новая активность не создана так как недопустимая скобка в теле запроса  
- Заголовки запроса:   
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 71cba6d0-da40-41cd-94c4-34bd015aca45  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:    
```json    
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-10-07T11:14:06.629Z",]
  "completed": true
}
```    
- Заголовки ответа:   
Content-Type: application/problem+json; charset=utf-8  
Date: Sat07 Oct 2023 12:16:48 GMT   
Server: Kestrel  
Transfer-Encoding: chunked  
- Тело ответа:    
```json    
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-1b17c982db919e41bf8ee4763af949cb-e1f5522fd6e6344b-00",
    "errors": {
        "$": [
            "']' is an invalid start of a property name. Expected a '\"'. Path: $ | LineNumber: 6 | BytePositionInLine: 39."
        ]
    }
}    
```  
 **8. POST. Создание новой активности с пустыми строками в теле запроса**    
- URL запроса: {{base_url}}/api/v1/Activities  
- Ожидаемый результат: HTTP Status: 400 Error: Bad Request, Новая активность не создана так как пустое значение у параметра "completed":  
- Заголовки запроса:   
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 43afb6c3-1647-44cc-8d41-1891b16759c7  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:    
```json    
{
 "id": 0,
 "title": "string",
 "dueDate": "2023-10-07T11:14:06.629Z",
 "completed":
} 
```    
- Заголовки ответа:   
Content-Type: application/problem+json; charset=utf-8  
Date: Sat07 Oct 2023 12:27:58 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
- Тело ответа:    
```json   
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-f3160ab2fc1d0a46b398445cac601dae-f7e7711d799d4049-00",
    "errors": {
        "$.completed": [
            "'}' is an invalid start of a value. Path: $.completed | LineNumber: 10 | BytePositionInLine: 0."
        ]
    }
}    
```  
 **9. POST. Создание новой активности с неверными значениями в теле запроса**    
- URL запроса: {{base_url}}/api/v1/Activities  
- Ожидаемый результат: HTTP Status: 400 Error: Bad Request, Новая активность не создана так как параметр "title" должен быть типом "string", а не 0  
- Заголовки запроса:   
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0 
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: cd81b0d1-ba60-48f3-b872-c1f985c5831d  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:    
```json    
{
 "id": 0,
 "title": 0,
 "dueDate": "2023-10-07T12:31:11.486Z",
 "completed": true
}
```    
- Заголовки ответа:   
Content-Type: application/problem+json; charset=utf-8  
Date: Sat07 Oct 2023 12:33:04 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
- Тело ответа:    
```json    
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-aeb21da1469a764087b3414e1ad1ab5f-47cf85efef593143-00",
    "errors": {
        "$.title": [
            "The JSON value could not be converted to System.String. Path: $.title | LineNumber: 4 | BytePositionInLine: 11."
        ]
    }
}
```  
**10. PUT.Редактирование по id активности с неверными значениями в теле запроса**    
- URL запроса: {{base_url}}/api/v1/Activities/{{id}}  
- Ожидаемый результат: HTTP Status: 400 Error: Bad Request, Редактирование активности под №1 не выполнено так как значение "completed":'true' неверно  
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: b1737526-b5bd-4fa8-8038-97b1c0358dad  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:    
```json    
{
 "id": 1,
 "title": "string",
 "dueDate": "2023-10-07T12:48:54.709Z",
 "completed": 'true'
}
 ```    
- Заголовки ответа:   
Content-Type: application/problem+json; charset=utf-8  
Date: Sat07 Oct 2023 12:49:47 GMT 
Server: Kestrel  
Transfer-Encoding: chunked  
- Тело ответа:    
```json    
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-445e50bc3032324f8e3e5be8b2293447-07672c23fa5af14b-00",
    "errors": {
        "$.completed": [
            "''' is an invalid start of a value. Path: $.completed | LineNumber: 8 | BytePositionInLine: 14."
        ]
    }
}  
```  
**11. PUT. Редактирование по id активности с пустыми строками в теле запроса**    
- URL запроса: {{base_url}}/api/v1/Activities/{{id}}  
- Ожидаемый результат: HTTP Status: 400 Error: Bad Request, Редактирование активности под №1 не выполнено так как значение параметра id не должно быть пустым  
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 1cce345a-6ff4-427b-ad45-e3c2e1f0cdc8  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:    
```json    
{
 "id": ,
 "title": "string",
 "dueDate": "2023-10-07T12:59:11.776Z",
 "completed": true
}
 ```    
- Заголовки ответа:   
Content-Type: application/problem+json; charset=utf-8  
Date: Sat07 Oct 2023 13:02:10 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
- Тело ответа:    
```json    
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-c80f113ab2a5e944ae714c51002ea67e-daa2d8189cf4c640-00",
    "errors": {
        "$.id": [
            "',' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 7."
        ]
    }
}  
```  
**12. PUT.Редактирование по id активности с неверным телом запроса**    
- URL запроса: {{base_url}}/api/v1/Activities/{{id}}  
- Ожидаемый результат: HTTP Status: 400 Error: Bad Request, Редактирование активности под №1 не выполнено так как лишняя скобка в теле запроса  
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.32.3  
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 6a3810fe-b797-4653-82f5-0d4dcbbaac2e  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:    
```json    
{
 "id": 1,
 "title": "string",
 "dueDate": "2023-10-07T12:59:11.776Z", ]
 "completed": true
}
 ```    
- Заголовки ответа:   
Content-Type: application/problem+json; charset=utf-8  
Date: Sat07 Oct 2023 13:02:10 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
- Тело ответа:    
```json    
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-605c6ebf1bf1fc44b5aace41bb18c952-f03f4918f5817a4f-00",
    "errors": {
        "$": [
            "']' is an invalid start of a property name. Expected a '\"'. Path: $ | LineNumber: 6 | BytePositionInLine: 40."
        ]
    }
} 
```   

#  Authors

**1. GET.Получение списка авторов**    
- URL запроса: {{base_url}}/api/v1/Authors  
- Ожидаемый результат: HTTP Status: 200 Success, Список авторов получен  
- Заголовки запроса:   
User-Agent: PostmanRuntime/7.33.0  
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 08c2a871-1af9-4695-a036-6af4d9bbd4b3  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:  Нет  
- Заголовки ответа:   
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Sat07 Oct 2023 13:20:10 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:    
```json    
 [
    {
        "id": 1,
        "idBook": 1,
        "firstName": "First Name 1",
        "lastName": "Last Name 1"
    },...
   ]  ......  
```    
**2. POST.Создание нового автора**    
- URL запроса: {{base_url}}/api/v1/Authors  
- Ожидаемый результат: HTTP Status: 201 Created, Новый автор добавлен  
- Заголовки запроса:   
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 34414ca9-f874-4240-a612-fb7cee507230  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:    
```json    
{
 "id": 0,
 "idBook": 0,
 "firstName": "Лев",
 "lastName": "Толстой"
}  
```    
- Заголовки ответа:   
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Sat07 Oct 2023 13:28:32 GMT   
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:  
```json    
{
    "id": 0,
    "idBook": 0,
    "firstName": "Лев",
    "lastName": "Толстой"
}    
```    
**3. GET.Получение списка авторов по idBook**    
- URL запроса: {{base_url}}/api/v1/Authors/authors/books/{{idBook}}  
- Ожидаемый результат: HTTP Status: 200 Success, Получен список авторов под номером книги 5  
- Заголовки запроса:   
User-Agent: PostmanRuntime/7.33.0  
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 300f8276-da0d-4a97-a2a0-ab39b697bd22  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса: Нет    
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Sat07 Oct 2023 13:35:16 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:  
```json      
[
  {
    "id": 11,
    "idBook": 5,
    "firstName": "First Name 11",
    "lastName": "Last Name 11"
  },
  {
    "id": 12,
    "idBook": 5,
    "firstName": "First Name 12",
    "lastName": "Last Name 12"
  },
  {
    "id": 13,
    "idBook": 5,
    "firstName": "First Name 13",
    "lastName": "Last Name 13"
  }
  ]
```    
**4. GET.Получение информации об авторе по id**    
- URL запроса: {{base_url}}/api/v1/Authors/{{id}}  
- Ожидаемый результат: HTTP Status: 200 Success, Получена информация об авторе  под номером  1  
- Заголовки запроса:   
User-Agent: PostmanRuntime/7.33.0  
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 300f8276-da0d-4a97-a2a0-ab39b697bd22  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса: Нет    
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Sat07 Oct 2023 13:44:17 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:  
```json      
{
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
}  
```    
**5. PUT.Редактирование информации об авторе по id и корректным телом запроса**    
- URL запроса: {{base_url}}/api/v1/Authors/{{id}}  
- Ожидаемый результат: HTTP Status: 200 Success, Изменения отображаются в теле запроса  
- Заголовки запроса:   
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0 
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 62104f86-0e2c-4ff2-944e-53e5867e6333  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:    
```json    
{
  "id": 1,
  "idBook": 0,
  "firstName": "Александр",
  "lastName": "Пушкин"
}  
```    
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Sat07 Oct 2023 13:48:27 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:  
```json      
{
    "id": 1,
    "idBook": 0,
    "firstName": "Александр",
    "lastName": "Пушкин"
}
```     
  **6. DELETE.Удаление автора по id**    
- URL запроса: {{base_url}}/api/v1/Authors/{{id}}  
- Ожидаемый результат: HTTP Status: 204, Активность под номером 1 - удалена, тело ответа отсутствует  
- Заголовки запроса:   
User-Agent: PostmanRuntime/7.33.0 
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 2997a920-a87a-42a7-82cd-4ff568dc8872  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса: Нет    
- Заголовки ответа:   
Content-Length: 0  
Date: Sat07 Oct 2023 13:48:27 GMT  
Server: Kestrel  
api-supported-versions: 1.0  
- Тело ответа: Нет     
    
**7. GET.​Получение списка авторов с невалидным idBook**    
- URL запроса: {{base_url}}/api/v1/Authors/authors/books/{{idBook_invalid}}  
- Ожидаемый результат: HTTP Status: 400  Bad Request, недопустимое значение  
- Заголовки запроса:   
User-Agent: PostmanRuntime/7.33.0  
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 54053a32-6dac-4b8d-b019-7549b8894b87  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса: Нет    
- Заголовки ответа:   
Content-Type: application/problem+json; charset=utf-8; v=1.0  
Date: Sat07 Oct 2023 13:48:27 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:    
```json    
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-e9cfc37c1b97944783f51365b278c033-7dfd6a939955fb46-00",
    "errors": {
        "idBook": [
            "The value '55555555555555555 ' is not valid."
        ]
    }
}
```  
**8. POST​.Создание автора с некорректным JSON в теле запроса**    
- URL запроса: {{base_url}}/api/v1/Authors  
- Ожидаемый результат: HTTP Status: 400 Error: Bad Request, Сообщение об ошибке в JSON  
- Заголовки запроса:   
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 43afb6c3-1647-44cc-8d41-1891b16759c7  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:    
```json    
{
 "id" 0
 "idBook": 0,
 "firstName": "Лев",
 "lastName": "Толстой"
}
```    
- Заголовки ответа:   
Content-Type: application/problem+json; charset=utf-8  
Date: Sat07 Oct 2023 14:08:37 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
- Тело ответа:    
```json    
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-fc2fdd009dd5c44284b471ec7d0d4bc2-c4842b8f8e20cd4e-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 2 | BytePositionInLine: 1."
        ]
    }
}  
```  
**9. POST​.Создание автора без тела запроса**    
- URL запроса: {{base_url}}/api/v1/Authors  
- Ожидаемый результат: HTTP Status: 400 Bad Request,  требуется обязательное тело запроса  
- Заголовки запроса:   
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 43afb6c3-1647-44cc-8d41-1891b16759c7  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:  нет  
- Заголовки ответа:   
Content-Type: application/problem+json; charset=utf-8  
Date: Sat07 Oct 2023 14:08:37 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
- Тело ответа:    
```json    
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 400,
    "traceId": "00-6c99d67dca9fa74b88afdbebba979984-fececa239ebbb54f-00"
}
```  
**10. POST​.Создание автора с некорректным типом значений в теле запроса**    
- URL запроса: {{base_url}}/api/v1/Authors  
- Ожидаемый результат: HTTP Status: 400 Error: Bad Request, ошибка в типе значения, требуется string  
- Заголовки запроса:   
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 43afb6c3-1647-44cc-8d41-1891b16759c7  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:    
```json    
{
 "id": 0,
 "idBook": 0,
 "firstName": 0,
 "lastName": "string"
}
```    
- Заголовки ответа:   
Content-Type: application/problem+json; charset=utf-8  
Date: Sat07 Oct 2023 14:12:42 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
- Тело ответа:    
```json    
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-d8665f3eeab52641a6a2e90d260b3294-2aa9a498e59f6141-00",
    "errors": {
        "$.firstName": [
            "The JSON value could not be converted to System.String. Path: $.firstName | LineNumber: 3 | BytePositionInLine: 15."
        ]
    }
}
```  
**11. GET.​Получение информации об авторе с невалидным обязательным id**    
- URL запроса: {{base_url}}/api/v1/Authors/{{id_invalid}}  
- Ожидаемый результат: HTTP Status: 400  Bad Request, недопустимое значение  
- Заголовки запроса:   
User-Agent: PostmanRuntime/7.33.0  
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 54053a32-6dac-4b8d-b019-7549b8894b87  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса: Нет    
- Заголовки ответа:   
Content-Type: application/problem+json; charset=utf-8; v=1.0  
Date: Sat07 Oct 2023 14:12:42 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:    
```json    
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-32bc23a59a8e604a90e3e2b3e6dff490-77dbc0eb601ef94c-00",
    "errors": {
        "id": [
            "The value '111111111111' is not valid."
        ]
    }
}
```  
**12. PUT.Редактирование информации об авторе с невалидным обязательным id и корректным телом запроса**    
- URL запроса: {{base_url}}/api/v1/Authors/{{id_invalid}}  
- Ожидаемый результат: HTTP Status: 400  Bad Request, недопустимое значение id  
- Заголовки запроса:   
User-Agent: PostmanRuntime/7.33.0  
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 54053a32-6dac-4b8d-b019-7549b8894b87  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:   
```json   
{
 "id": 0,
 "idBook": 0,
 "firstName": "string",
 "lastName": "string"
}
 ```   
- Заголовки ответа:   
Content-Type: application/problem+json; charset=utf-8; v=1.0  
Date: Sat07 Oct 2023 14:22:01 GMT   
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:    
```json    
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-e8f1279d23820f45827f4c05f4ed9f99-47be7ed8d5b6cb45-00",
    "errors": {
        "id": [
            "The value '111111111111' is not valid."
        ]
    }
}
```  
**13. PUT.Редактирование информации об авторе с валидным обязательным id и без тела запроса**    
- URL запроса: {{base_url}}/api/v1/Authors/{{id}}  
- Ожидаемый результат: HTTP Status: 400 Bad Request,  требуется обязательно тело запроса  
- Заголовки запроса:   
User-Agent: PostmanRuntime/7.33.0  
Accept: * / *  
Cache-Control: no-cache  
Postman-Token: 54053a32-6dac-4b8d-b019-7549b8894b87  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса: нет  
- Заголовки ответа:   
Content-Type: application/problem+json; charset=utf-8; v=1.0  
Date: Sat07 Oct 2023 14:22:01 GMT   
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:    
```json    
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 400,
    "traceId": "00-d67f5343e99e0240839eca0771d8d819-47e3d16757588142-00"
}
```  

## Books

### GET​/api​/v1​/Books

**URL:** {{url_books}}

**Ожидаемый результат:** 200 OK.

**Заголовки запроса:**
``` 
accept: text/plain; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 294b4e9f-53fe-4795-a120-c6496e93fb91
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**
``` 

```     
**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Fri, 06 Oct 2023 11:51:45 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
**Тело ответа:**
```
[
    {
        "id": 1,
        "title": "Book 1",
        "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
        "pageCount": 100,
        "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
        "publishDate": "2023-10-05T11:51:46.0840718+00:00"
    }
]
```

### GET​/api​/v1​/Books - id корректное число

**URL:** {{url_books}}/{{id_correct_number}}

**Ожидаемый результат:** 200 OK.

**Заголовки запроса:** 
```
accept: text/plain; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: a89b9a21-4b5d-4d98-ac2c-4aefccfee61c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**
``` 

``` 
**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Fri, 06 Oct 2023 11:56:02 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
**Тело ответа:**
```
{
    "id": 1,
    "title": "Book 1",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 100,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-10-05T11:56:03.2488455+00:00"
}
```

### POST/api/v1/Books/{id} - id корректное число

**URL:** {{url_books}}

**Ожидаемый результат:** 200 OK.

**Заголовки запроса:** 
```
accept: */*
Content-Type: application/json; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: b562dedd-8ab6-4019-ba7c-e392ce18b48c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**
```
{
  "id": 1,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-10-06T11:15:04.762Z"
}
``` 
**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Fri, 06 Oct 2023 12:01:24 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
**Тело ответа:**
```
{
    "id": 1,
    "title": "string",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-10-06T11:15:04.762Z"
}
```

### PUT/api/v1/Books/{id} - id корректное число

**URL:** {{url_books}}/{{id_correct_number}}

**Ожидаемый результат:** 200 OK.

**Заголовки запроса:** 
```
accept: */*
Content-Type: application/json; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: a8c77f46-a565-41a7-bc7a-74daa4333fe5
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**
```
{
  "id": 1,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-10-06T11:20:37.998Z"
}
```    
**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Fri, 06 Oct 2023 12:08:10 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
**Тело ответа:**
```
{
  "id": 1,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-10-06T11:20:37.998Z"
}
```

### DELETE/api/v1/Books/{id} - id корректное число

**URL:** {{url_books}}/{{id_correct_number}}

**Ожидаемый результат:** 200 OK.

**Заголовки запроса:** 
```
accept: */*
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 5e34bfbd-9fe1-4af3-a72a-fd10ffc2ea80
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**
```

``` 
**Заголовки ответа:**
```
Content-Length: 0
Date: Fri, 06 Oct 2023 12:12:06 GMT
Server: Kestrel
api-supported-versions: 1.0
```
**Тело ответа:**
```

```

### GET/api/v1/Books/{id} - id некорректное число

**URL:** {{url_books}}/{{id_nocorrect_number}}

**Ожидаемый результат:** 400 Bad Request.

**Заголовки запроса:** 
```
accept: text/plain; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 6400f1b8-6643-43e0-b119-1b3e6d037cb2
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**
```

``` 
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 06 Oct 2023 12:15:36 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-34b4eb01385bfc40bab72dda50af1710-b8e73706d21a2b42-00",
    "errors": {
        "id": [
            "The value '20,5' is not valid."
        ]
    }
}
```

### GET/api/v1/Books/{id} - id буквы

**URL:** {{url_books}}/{{id_letter}}

**Ожидаемый результат:** 400 Bad Request.

**Заголовки запроса:** 
```
accept: text/plain; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 36b0e19a-ecc8-403c-b65d-5d75a6b90eae
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**
```

``` 
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 06 Oct 2023 12:17:14 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-ca92e2e2d9649b4e831400ffc78ec32a-9d7008e2da05804c-00",
    "errors": {
        "id": [
            "The value 'fsdsf' is not valid."
        ]
    }
}
```

### POST/api/v1/Books - id некорректное число

**URL:** {{url_books}}

**Ожидаемый результат:** 400 Bad Request.

**Заголовки запроса:** 
```
accept: */*
Content-Type: application/json; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: f34211bd-17f9-4444-b8a2-887c0cdf4b3e
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**
```
{
  "id": 20,5,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-10-06T11:15:04.762Z"
}
``` 
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 06 Oct 2023 12:18:37 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-82b155ff2cbab542bd43793679e1b30b-48c1476176c11c45-00",
    "errors": {
        "$": [
            "'5' is an invalid start of a property name. Expected a '\"'. Path: $ | LineNumber: 1 | BytePositionInLine: 11."
        ]
    }
}
```

### POST/api/v1/Books - id буквы

**URL:** {{url_books}}

**Ожидаемый результат:** 400 Bad Request.

**Заголовки запроса:** 
```
accept: */*
Content-Type: application/json; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: d4d9d22c-f667-4a19-9a98-cc09d31ff589
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**
```
{
  "id": fsdsf,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-10-06T11:15:04.762Z"
}
``` 
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 06 Oct 2023 12:20:43 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-9030ed904655fa479eec574c56349355-3180f2df40ff0144-00",
    "errors": {
        "$.id": [
            "'fsdsf,\r\n  \"title\": \"string\",\r\n  \"description\": \"string\",\r\n  \"pageCount\": 0,\r\n  \"excerpt\": \"string\",\r\n  \"publishDate\": \"2023-10-06T11:15:04.762Z\"\r\n}' is an invalid JSON literal. Expected the literal 'false'. Path: $.id | LineNumber: 1 | BytePositionInLine: 9."
        ]
    }
}
```

### POST/api/v1/Books - id null

**URL:** {{url_books}}

**Ожидаемый результат:** 400 Bad Request.

**Заголовки запроса:** 
```
accept: */*
Content-Type: application/json; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 93c2589c-d457-480f-967c-872b82dfed1c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**
```
{
  "id": ,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-10-06T11:15:04.762Z"
}
``` 
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 06 Oct 2023 12:22:33 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-7f19debe7363e94cb9a9e7ba4e26ed64-8aadb1b8e3b31f4e-00",
    "errors": {
        "$.id": [
            "',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."
        ]
    }
}
```


### POST/api/v1/Books - пустой JSON

**URL:** {{url_books}}

**Ожидаемый результат:** 400 Bad Request.

**Заголовки запроса:** 
```
accept: */*
Content-Type: application/json; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: c6872f6d-3102-44a1-84bf-5cabd04223dc
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**
```

``` 
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 06 Oct 2023 12:24:16 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-bf3427f6eea19b45b95c4b850b6ab79d-c98c33399981f643-00",
    "errors": {
        "": [
            "A non-empty request body is required."
        ]
    }
}
```

### POST/api/v1/Books - некорректный JSON

**URL:** {{url_books}}

**Ожидаемый результат:** 400 Bad Request.

**Заголовки запроса:** 
```
accept: */*
Content-Type: application/json; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 8ed4f54e-84e5-457e-bc13-4391aef81b0a
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**
```
{]
  id: 1,
  "title": "string",
  "description": "string",
  "pageCount": 0]
  "excerpt": "string",]
  "publishDate": "2023-10-06T11:15:04.762Z"]↵↵
``` 
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 06 Oct 2023 12:25:56 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-5402c6a1d9a61440a63368fff3f427db-6ecd195cd8231d4e-00",
    "errors": {
        "$": [
            "']' is an invalid start of a property name. Expected a '\"'. Path: $ | LineNumber: 0 | BytePositionInLine: 1."
        ]
    }
}
```

### PUT/api/v1/Books/{id} - id некорректное число

**URL:** {{url_books}}/{{id_nocorrect_number}}

**Ожидаемый результат:** 400 Bad Request.

**Заголовки запроса:** 
```
accept: */*
Content-Type: application/json; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 1b76b274-d930-4ab3-b70d-2a1f4eb2c5ec
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**
```
{
  "id": 20,5,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-10-06T11:20:37.998Z"
}
``` 
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 06 Oct 2023 12:27:16 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-ef285f0287fe3d4089eda76430ac01c3-c898a345e63f1342-00",
    "errors": {
        "$": [
            "'5' is an invalid start of a property name. Expected a '\"'. Path: $ | LineNumber: 1 | BytePositionInLine: 11."
        ],
        "id": [
            "The value '20,5' is not valid."
        ]
    }
}
```

### PUT/api/v1/Books/{id} - id буквы

**URL:** {{url_books}}/{{id_letter}}

**Ожидаемый результат:** 400 Bad Request.

**Заголовки запроса:** 
```
accept: */*
Content-Type: application/json; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 82463843-b268-4517-9a8c-bdc2993f3fbe
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**
```
{
  "id": fsdsf,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-10-06T11:20:37.998Z"
}
``` 
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 06 Oct 2023 12:30:32 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-2c3c19adbf7f7e428be0db0c6bb42d79-831e0f26fb7ee447-00",
    "errors": {
        "id": [
            "The value 'fsdsf' is not valid."
        ],
        "$.id": [
            "'fsdsf,\r\n  \"title\": \"string\",\r\n  \"description\": \"string\",\r\n  \"pageCount\": 0,\r\n  \"excerpt\": \"string\",\r\n  \"publishDate\": \"2023-10-06T11:20:37.998Z\"\r\n}' is an invalid JSON literal. Expected the literal 'false'. Path: $.id | LineNumber: 1 | BytePositionInLine: 9."
        ]
    }
}
```

### PUT/api/v1/Books/{id} - id null

**URL:** {{url_books}}/{{id_null}}

**Ожидаемый результат:** 405 Method Not Allowed.

**Заголовки запроса:** 
```
accept: */*
Content-Type: application/json; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 7be0e4e4-cf71-4c59-b845-3797a6cee750
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**
```
{
  "id": ,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-10-06T11:20:37.998Z"
}
``` 
**Заголовки ответа:**
```
Content-Length: 0
Date: Fri, 06 Oct 2023 12:32:36 GMT
Server: Kestrel
Allow: GET, POST
```
**Тело ответа:**
```
JSONError: No data, empty input at 1:1
```

### PUT/api/v1/Books/{id} - пустой JSON

**URL:** {{url_books}}/{{id_correct_number}}

**Ожидаемый результат:** 400 Bad Request.

**Заголовки запроса:** 
```
accept: */*
Content-Type: application/json; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 2c91113d-f1f3-41e0-990a-9d3bd5d5c9fb
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**
```

``` 
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 06 Oct 2023 12:35:24 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-b30184ad0a53654fab4d90a2c759d10c-b7f9e0db58cced4a-00",
    "errors": {
        "": [
            "A non-empty request body is required."
        ]
    }
}
```

### PUT/api/v1/Books/{id} - некорректный JSON

**URL:** {{url_books}}/{{id_correct_number}}

**Ожидаемый результат:** 400 Bad Request.

**Заголовки запроса:** 
```
accept: */*
Content-Type: application/json; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 956b8b80-8178-4d55-baeb-78e91289358f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**
```
{]
  id: 1,
  "title": "string",
  "description": "string",
  "pageCount": 0]
  "excerpt": "string",]
  "publishDate": "2023-10-06T11:15:04.762Z"]↵↵
``` 
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 06 Oct 2023 12:36:53 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-cd1fa78f33aec94faed29a343ac11682-e6f1d2bf7d2c2642-00",
    "errors": {
        "$": [
            "']' is an invalid start of a property name. Expected a '\"'. Path: $ | LineNumber: 0 | BytePositionInLine: 1."
        ]
    }
}
```

### DELETE/api/v1/Books/{id} - id некорректное число

**URL:** {{url_books}}/{{id_nocorrect_number}}

**Ожидаемый результат:** 400 Bad Request.

**Заголовки запроса:** 
```
accept: */*
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 46333016-5f9f-4698-b5ee-3ca287bafb90
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**
```

``` 
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 06 Oct 2023 12:39:30 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-bb3b35473eb3bd43bc88b21a32b79463-a5906cdf8e7bd64a-00",
    "errors": {
        "id": [
            "The value '20,5' is not valid."
        ]
    }
}
```

### DELETE/api/v1/Books/{id} - id буквы

**URL:** {{url_books}}/{{id_letter}}

**Ожидаемый результат:** 400 Bad Request.

**Заголовки запроса:** 
```
accept: */*
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 8b1b663b-a123-4844-9834-ed6bab62649a
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**
```

``` 
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 06 Oct 2023 12:40:58 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-3b5323227d15e54a9ac0040de521aa88-54bed065b4d32f45-00",
    "errors": {
        "id": [
            "The value 'fsdsf' is not valid."
        ]
    }
}
```

### DELETE/api/v1/Books/{id} - id null

**URL:** {{url_books}}/{{id_null}}

**Ожидаемый результат:** 405 Method Not Allowed.

**Заголовки запроса:** 
```
accept: */*
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 713a3b26-e300-4a90-8508-fc58149cef2e
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**
```

``` 
**Заголовки ответа:**
```
Content-Length: 0
Date: Fri, 06 Oct 2023 12:42:11 GMT
Server: Kestrel
Allow: GET, POST
```
**Тело ответа:**
```
JSONError: No data, empty input at 1:1
```

## CoverPhotos    

### GET​/api​/v1​/CoverPhotos
**URL:** {{URL_CoverPhotos}}  
**Ожидаемый результат:** 200 OK.  
**Заголовки запроса:**
``` 
accept: text/plain; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 4efc1175-d374-4aa8-a632-8ef736315daa
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**  отсутсвует     
**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 07 Oct 2023 17:20:08 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
**Тело ответа:**
```
[
 {
        "id": 200,
        "idBook": 200,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 200&w=250&h=350"
    }
]
```  
### GET​/api​/v1​/CoverPhotos - id book корректное число
**URL:** {{URL_CoverPhotos}}/{{idBook_correct}}  
**Ожидаемый результат:** 200 OK.  
**Заголовки запроса:**
``` 
accept: text/plain; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 2f5de714-3f04-4633-bdab-f5ce0bae7a04
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:** отсутсвует    
**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 07 Oct 2023 17:33:56 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
**Тело ответа:**
```
{
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```
### GET​/api​/v1​/CoverPhotos - id корректное число
**URL:** {{URL_CoverPhotos}}/{{id_correct}}  
**Ожидаемый результат:** 200 OK.  
**Заголовки запроса:**
``` 
accept: text/plain; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 858bc348-d37e-44ec-9cbe-70fcd493162a
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**  отсутсвует 
**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 07 Oct 2023 17:40:16 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
**Тело ответа:**
```
{
    "id": 10,
    "idBook": 10,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 10&w=250&h=350"
}
```  
### GET​/api​/v1​/CoverPhotos - id book некорректное число
**URL:** {{URL_CoverPhotos}}/{{id_necorrekt}}  
**Ожидаемый результат:** 400 Bad Request.  
**Заголовки запроса:**
``` 
accept: text/plain; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 4a9be4a0-9572-4389-b328-16920e68d058
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:** отсутсвует      
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 07 Oct 2023 17:51:42 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-e3bedf9824159b40812322c3dd794be7-95d7a27bc6a80c4b-00",
    "errors": {
        "id": [
            "The value '10.5' is not valid."
        ]
    }
}
```  
### GET/api​/v1​/CoverPhotos - id некорректное число 
**URL:** {{URL_CoverPhotos}}/{{id_necorrekt}}    
**Ожидаемый результат:** 400 Bad Request.     
**Заголовки запроса:**
``` 
accept: text/plain; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 9c6c9f9b-1a01-4467-9bd4-ea192176e4d2
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
**Тело запроса:**  отсутсвует   
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 07 Oct 2023 18:00:49 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-ebd372b2ba51704aa56eee1a9a32556f-9fbba2781962b94c-00",
    "errors": {
        "id": [
            "The value '10.5' is not valid."
        ]
    }
}
```  
### POST/api/v1/CoverPhotos некорректное число
**URL:**  {{URL_CoverPhotos}}  
**Ожидаемый результат:** 400 Bad Request    
**Заголовки запроса:**  
``` 
accept: text/plain; v=1.0
Content-Type: application/json; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 5a153c77-596b-4860-a8d5-94c468e2340e
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```  
**Тело запроса:**  
``` 
{
    "id":{{id_necorrekt}},
    "idBook":1,
    "url":"string"
}
```       
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 07 Oct 2023 18:12:32 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-3e1de39a6b6dda43948b3303a21b6602-4348e2716dcd9f48-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 10."
        ]
    }
}
```  

### POST/api/v1/CoverPhotos корректное число
**URL:**  {{URL_CoverPhotos}}  
**Ожидаемый результат:** 200 OK.    
**Заголовки запроса:**  
``` 
accept: text/plain; v=1.0
Content-Type: application/json; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 0ded9c2f-414f-4685-8e4c-c8fdb8d91688
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```  
**Тело запроса:**  
``` 
{
"id":{{id_correct}},
"idBook":1,
"url":"string"
}
```       
**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 07 Oct 2023 18:16:55 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
**Тело ответа:**
```
{
    "id": 10,
    "idBook": 1,
    "url": "string"
}
```  
### POST/api/v1/CoverPhotos пустое тело
**URL:** {{URL_CoverPhotos}}   
**Ожидаемый результат:** 400 Bad Request  
**Заголовки запроса:**    
``` 
accept: text/plain; v=1.0
Content-Type: application/json; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 9fee1ae0-6e39-4136-abeb-ec73c51c2491
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```  
**Тело запроса:**  отсутсвует     
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 07 Oct 2023 18:24:55 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-ca40a35054aec64281d375d4d660ab34-98c1e97a4698be41-00",
    "errors": {
        "$": [
            "The input does not contain any JSON tokens. Expected the input to start with a valid JSON token, when isFinalBlock is true. Path: $ | LineNumber: 1 | BytePositionInLine: 0."
        ]
    }
}
```  
 
 ### POST/api/v1/CoverPhotos некорректное тело
**URL:** {{URL_CoverPhotos}}   
**Ожидаемый результат:** 400 Bad Request    
**Заголовки запроса:**  
``` 
accept: text/plain; v=1.0
Content-Type: application/json; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: f8cb56f6-70ca-494c-b56c-423f27fe010a
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```  
**Тело запроса:**  
``` 
{
    "id":{{id_correkt}},
    "idBook":1,
    "url":"{{mistake}}"
}
```       
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 07 Oct 2023 18:37:22 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-ef3a755a0c301348a32b9d8d2a990924-3d0a4e56f647c04f-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 10."
        ]
    }
}
```  
 
 ### PUT/api/v1/CoverPhotos корректное число
**URL:** {{URL_CoverPhotos}}/{{id_correct}}   
**Ожидаемый результат:** 200 OK.  
**Заголовки запроса:**  
``` 
accept: text/plain; v=1.0
Content-Type: application/json; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: fb3befd0-2f12-4caf-9e18-c84481ed4935
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```  
**Тело запроса:**  
``` 
{
    "id":{{id_correct}},
    "idBook":0,
    "url":"string"
}
```       
**Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 07 Oct 2023 18:41:29 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
**Тело ответа:**
```
{
    "id": 10,
    "idBook": 0,
    "url": "string"
}
```  
 ### PUT/api/v1/CoverPhotos некорректное число
**URL:**  {{URL_CoverPhotos}}/{{id_necorrect}}  
**Ожидаемый результат:** 400 Bad Request   
**Заголовки запроса:**  
``` 
accept: text/plain; v=1.0
Content-Type: application/json; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 3e12cf28-2f76-4f26-ab92-69c440655585
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```  
**Тело запроса:**  
``` 
{
    "id":{{id_necorrect}},
    "idBook":0,
    "url":"string"
}
```       
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 07 Oct 2023 18:47:03 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-073e7e12caaf584a8fefb0cfd90f6e5e-37ad4a821f93744f-00",
    "errors": {
        "id": [
            "The value '{{id_necorrect}}' is not valid."
        ],
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 10."
        ]
    }
}
```  

### PUT/api/v1/CoverPhotos/ пустое тело
**URL:**  {{URL_CoverPhotos}}/{{id_correct}}  
**Ожидаемый результат:** 400 Bad Request  
**Заголовки запроса:**  
``` 
accept: text/plain; v=1.0
Content-Type: application/json; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 152ddb4c-3bcf-4e35-8737-dc9d618a6839
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```  
**Тело запроса:**  отсутсвует     
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 07 Oct 2023 18:50:28 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-9bad49fd600f3c4e93f57e42b81d5da1-81458337196cf340-00",
    "errors": {
        "": [
            "A non-empty request body is required."
        ]
    }
}
```  

### PUT/api/v1/CoverPhotos некорректное тело
**URL:**  {{URL_CoverPhotos}}/{{id_correct}}  
**Ожидаемый результат:** 400 Bad Request  
**Заголовки запроса:**    
``` 
accept: text/plain; v=1.0
Content-Type: application/json; v=1.0
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: 80168522-54fe-4db0-998f-41b9afefe0d8
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```  
**Тело запроса:**  
``` 
{
    "id":{{id_correct}},
    "idBook":0,
    "url":{{mistake}}
}
```       
**Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 07 Oct 2023 18:55:19 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-86a6998ceb616a428036f1d5527e41fe-e1a02308ded13d44-00",
    "errors": {
        "$.url": [
            "'v' is an invalid end of a number. Expected a delimiter. Path: $.url | LineNumber: 3 | BytePositionInLine: 13."
        ]
    }
}
```  
### DELETE/api/v1/CoverPhotos удаление
**URL:**  {{URL_CoverPhotos}}/{{id_correct}}  
**Ожидаемый результат:** 200 OK  
**Заголовки запроса:**  
``` 
accept: */*
User-Agent: PostmanRuntime/7.33.0
Cache-Control: no-cache
Postman-Token: d3f8d9e5-f2f0-451a-ae80-6817094f4a75
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```  
**Тело запроса:** отсутсвует       
**Заголовки ответа:**
```
Content-Length: 0
Date: Sat, 07 Oct 2023 19:03:32 GMT
Server: Kestrel
api-supported-versions: 1.0
```
**Тело ответа:** отсутсвует


## Users 

### 1.GET. Получение списка пользователей

**URL запроса:** {{base_url}}/api/v1/Users

**Ожидаемый результат:**

 HTTP Status, 200 Success, 
Список пользователей получен https://postman-rest-api-learner.glitch.me//api/v1/Users/books/covers/15

**Заголовки запроса:**

Пользовательский агент: PostmanRuntime/7.33.0
Принять: */*
Cache-Control: без кэша
Токен почтальона:  4bc34658-3fac-404d-9c3d-558a467d7b72 
Ведущий: postman-rest-api-learner.glitch.me
Accept-Encoding: gzip, deflate, br
Подключение: keep-alive

**Тело запроса:**  Нет

**Заголовки ответа:**

Дата: Вт, 03 Окт 2023 16:39:09 GMT
Content-Type: text/html; charset=utf-8
Содержание-Длина: 167
Подключение: keep-alive
x-powered-by: Экспресс
Content-security-policy: default-src 'none'
x-content-type-options: nosniff

**Тело ответа:**

```json    
[  
   {
       "id": 1,
       "userName": "User 1",
       "password": "Password1"
   },
   {
       "id": 2,
       "userName": "User 2",
       "password": "Password2"
   },
   {
       "id": 3,
       "userName": "User 3",
       "password": "Password3"
   },
   {
       "id": 4,
       "userName": "User 4",
       "password": "Password4"
   }
    
 ......  
``    
### 2. POST Создание пользователя

**URL запроса:** {{base_url}}/api/v1/Users

**Ожидаемый результат:**

 HTTP Status, 201 Created, новый 
ользователь  добавлен  https://postman-rest-api-learner.glitch.me//api/v1/Users/books/covers/15

**Заголовки запроса:**

Пользовательский агент: PostmanRuntime/7.33.0
Принять: */*
Cache-Control: без кэша
Токен почтальона: 4187e7e7-6147-49be-811d-eb04f9204413
Ведущий: postman-rest-api-learner.glitch.me
Accept-Encoding: gzip, deflate, br
Подключение: keep-alive

**Тело запроса:**

``json    
  { 
 "id": 0,
  "userName": "Bob",
  "password": "Bob123" 
}
``` 
**Заголовки ответа:**
   
 Дата: Вт, 03 Окт 2023 16:58:09 GMT
Content-Type: text/html; charset=utf-8
Содержание-Длина: 168
Подключение: keep-alive
x-powered-by: Экспресс
Content-security-policy: default-src 'none'
x-content-type-options: nosniff

**Тело ответа:**

```json  
{
    "id": 0,
    "userName": "Bob",
    "password": "Bob123"
}


### 3. GET.Получение информации об пользователе по корректному id

**URL запроса:** {{base_url}}/api/v1/Users/{{id}}

**Ожидаемый результат:**

 HTTP Status: 200 Success, 
Получена информация о пользователе https://postman-rest-api-learner.glitch.me//api/v1/Users/1%20%20

**Заголовки запроса:**

User-Agent: PostmanRuntime/7.32.3  
Accept: * / *  
Postman-Token: f343feae-991d-41ac-810e-813299bbf10b  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive

**Тело запроса:** Нет

**Заголовки ответа:**

Content-Type: application/json; charset=utf-8; v=1.0 
 Дата: Вт, 03 Окт 2023 17:20:25 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0 

**Тело ответа:**

```json  
{
    "id": 1,
    "userName": "User 1",
    "password": "Password1"
}


### 4. PUT Редактирование информации об пользователе по корректному id

**URL запроса:** {{base_url}}/api/v1/Users/{{id}}

**Ожидаемый результат:**

 HTTP Status: 200 OK  https://postman-rest-api-learner.glitch.me//api/v1/Users/1%20%20

**Заголовки запроса:**

Пользовательский агент: PostmanRuntime/7.33.0
Принять: */*
Cache-Control: без кэша
Токен почтальона: 79fc3e6e-cd1e-4bd5-b5e8-e873561d9bd9
Ведущий: postman-rest-api-learner.glitch.me
Accept-Encoding: gzip, deflate, br
Подключение: keep-alive 
- Тело запроса:    
```json  
{
  "id": 1,
  "userName": "Иван",
  "password": "Иванов"
 }
```
**Заголовки ответа:**

Дата: Вт, 03 Окт 2023 17:20:55 GMT 
Content-Type: text/html; charset=utf-8
Содержание-Длина: 159
Подключение: keep-alive
x-powered-by: Экспресс
Content-security-policy: default-src 'none'
x-content-type-options: nosniff

**Тело ответа:**

```json   
{
    "id": 1,
    "userName": "Иван",
    "password": "Иванов"
}


### 5. DELETE Удаление пользователя по id

**URL запроса:**{{base_url}}/api/v1/Users/{{id}}

**Ожидаемый результат:**

 HTTP Status: 204, Пользователь 
под номером 5 - удален  https://postman-rest-api-learner.glitch.me//api/v1/Users/1%20%20

**Заголовки запроса:**

 Пользовательский агент: PostmanRuntime/7.33.0
Принять: */*
Cache-Control: без кэша
Токен почтальона: 79fc3e6e-cd1e-4bd5-b5e8-e873561d9bd9
Ведущий: postman-rest-api-learner.glitch.me
Accept-Encoding: gzip, deflate, br
Подключение: keep-alive

**Тело запроса:** Нет

**Заголовки ответа:**

Дата: Вт, 03 Окт 2023 17:20:55 GMT 
Content-Type: text/html; charset=utf-8
Содержание-Длина: 159
Подключение: keep-alive
x-powered-by: Экспресс
Content-security-policy: default-src 'none'
x-content-type-options: nosniff

Тело ответа: Нет


### 6. GET ​Получение информации об пользователе с невалидным обязательным id

**URL запроса:** {{users_id_invalid}}/api/v1/Users/

**Ожидаемый результат:**

HTTP Status, 400 Bad Request,
Информация об пользователе  под номером 4444444444 не
верная  https://postman-rest-api-learner.glitch.me//api/v1/Users/%7B%7Busers_id_invalid%7D%7D%20%20%20

**Заголовки запроса:**

Cache-Control: без кэша
Токен почтальона: 00ff61ea-f447-450a-ae6b-49b546597d02
Ведущий: postman-rest-api-learner.glitch.me
Accept-Encoding: gzip, deflate, br
Подключение: keep-alive
Transfer-Encoding: chunked

**Тело запроса:** Нет

**Заголовки ответа:**

Дата: Вт, 03 Окт 2023 18:47:45 GMT 
Content-Type: text/html; charset=utf-8
Содержание-Длина: 189
Подключение: keep-alive
x-powered-by: Экспресс
Content-security-policy: default-src 'none'
x-content-type-options: nosniff

**Тело ответа:**

```json  
 {
    "type": "https://tools.ietf.org/html/
rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": 
"00-6b88a88ca596d54f9708246ee3d0cb99-6d4e63912abe75
49-00",
    "errors": {
        "id": [
            "The value '4444444444' is not valid."
        ]
    }
}


### 7. POST​ Создание информации об пользователе без тела запроса

**URL запроса:** {{base_url}}/api/v1/Users

**Ожидаемый результат:**

HTTP Status, 415 Unsupported 
Media Type   Информация о пользователе не создана так 
как отсутсвует тело запроса  https://postman-rest-api-learner.glitch.me//api/v1/Users/%7B%7Busers_id_invalid%7D%7D%20%20%20

**Заголовки запроса:**

Пользовательский агент: PostmanRuntime/7.33.0
Принять: */*
Cache-Control: без кэша
Токен почтальона: 00ff61ea-f447-450a-ae6b-49b546597d02
Ведущий: postman-rest-api-learner.glitch.me
Accept-Encoding: gzip, deflate, br
Подключение: keep-alive

**Тело запроса:** нет 

**Заголовки ответа:**

Дата: Вт, 03 Окт 2023 18:47:45 GMT 
Content-Type: text/html; charset=utf-8
Содержание-Длина: 189
Подключение: keep-alive
x-powered-by: Экспресс
Content-security-policy: default-src 'none'
x-content-type-options: nosniff

**Тело ответа:**

```json 
   {
    "type": "https://tools.ietf.org/html/
rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": 
"00-4b1a5c0cb0baf54991b43a4f184c28ff-7242b673f1f552
43-00"
}


### 8. POST​ Создание информации об пользователе c неверным телом  запроса

**URL запроса:** {{base_url}}/api/v1/Users

**Ожидаемый результат:**

HTTP Status, 400 Error: Bad 
Request, Пользователь не создан не допустимые скобки в 
теле запроса  https://postman-rest-api-learner.glitch.me//api/v1/Users/%7B%7Busers_id_invalid%7D%7D%20%20%20

**Заголовки запроса:**

Пользовательский агент: PostmanRuntime/7.33.0
Принять: */*
Cache-Control: без кэша
Токен почтальона: 00ff61ea-f447-450a-ae6b-49b546597d02
Ведущий: postman-rest-api-learner.glitch.me
Accept-Encoding: gzip, deflate, br
Подключение: keep-alive

**Тело запроса:**

```json  
[
 "id": 0,
 "userName": "string",
 "password": "string"
]
```    
**Заголовки ответа:**

Дата: Вт, 03 Окт 2023 18:47:45 GMT 
Content-Type: text/html; charset=utf-8
Содержание-Длина: 189
Подключение: keep-alive
x-powered-by: Экспресс
Content-security-policy: default-src 'none'
x-content-type-options: nosniff

**Тело ответа:**

```json   
{
    "type": "https://tools.ietf.org/html/
rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": 
"00-cafd048ab98b9e4dba45a28d22b17ac8-2c184fc2c97ab2
41-00",
    "errors": {
        "$": [
            "The JSON value could not be converted to 
FakeRestAPI.Models.User. Path: $ | 
LineNumber: 0 | BytePositionInLine: 1."
        ]
    }
}


### 9. PUT Редактирование информации об пользователе с невалидным обязательным id и корректным телом запроса

**URL запроса:** {{base_url}}/api/v1/Users/{{users_id_invalid}}

**Ожидаемый результат:**

HTTP Status, 400 Bad Request, 
неверный номер пользователя, информация не откорректирована https://postman-rest-api-learner.glitch.me//api/v1/Users%7B%7Busers_id_invalid%7D%7D%20%20%20

**Заголовки запроса:**

Пользовательский агент: PostmanRuntime/7.33.0
Принять: */*
Cache-Control: без кэша
Токен почтальона: 00ff61ea-f447-450a-ae6b-49b546597d02
Ведущий: postman-rest-api-learner.glitch.me
Accept-Encoding: gzip, deflate, br
Подключение: keep-alive  
 - Тело запроса:    
```json   
{
 "id": 0,
 "userName": "string",
 "password": "string"
 }

**Заголовки ответа:**

Дата: Вт, 03 Окт 2023 18:47:45 GMT 
Content-Type: text/html; charset=utf-8
Содержание-Длина: 189
Подключение: keep-alive
x-powered-by: Экспресс
Content-security-policy: default-src 'none'
x-content-type-options: nosniff

**Тело ответа:**

```json   
{
    "type": "https://tools.ietf.org/html/
rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": 
"00-ae7002a667fb80459c20286509a6b577-7d8ee12dfde659
4f-00",
    "errors": {
        "id": [
            "The value '4444444444' is not valid."
        ]
    }
}


### 10. PUT.Редактирование информации об пользователе с валидным обязательным id и без тела запроса

**URL запроса:** {{base_url}}/api/v1/Users/{{users_id}}

Ожидаемый результат:** HTTP Status: 415 Unsupported 
Media Type . Редактирование пользователя не выполнено 
так как тело запроса не должно быть пустым  https://postman-rest-api-learner.glitch.me//api/v1/Users/%7B%7Busers_id_invalid%7D%7D%20%20%20

**Заголовки запроса:**

Пользовательский агент: PostmanRuntime/7.33.0
Принять: */*
Cache-Control: без кэша
Токен почтальона: 00ff61ea-f447-450a-ae6b-49b546597d02
Ведущий: postman-rest-api-learner.glitch.me
Accept-Encoding: gzip, deflate, br
Подключение: keep-alive

**Тело запроса:**нет 

**Заголовки ответа:

Дата: Вт, 03 Окт 2023 18:47:45 GMT 
Content-Type: text/html; charset=utf-8
Содержание-Длина: 189
Подключение: keep-alive
x-powered-by: Экспресс
Content-security-policy: default-src 'none'
x-content-type-options: nosniff

**Тело ответа:**

```json  
{
{
    "type": "https://tools.ietf.org/html/
rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": 
"00-b4be2395bf3d3a4db5d8dd66e0f57cd8-670c46ef22b9a6
44-00"
}


### 11. PUT Редактирование информации об пользователе по id с неверными значениями в теле запроса

**URL запроса:** {{base_url}}/api/v1/Users/{{users_id}}

**Ожидаемый результат:** HTTP Status, 400 Error: Bad 
Request, Редактирование пользователя не выполнено в id 
не может быть значения «null» 

**Заголовки запроса:**

Content-Type: application/json 
User-Agent: PostmanRuntime/7.32.3  
Accept: * / *  
Postman-Token: 7219d920-f2ea-4d94-a921-ca74c857d1ae  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 70

**Тело запроса:**

```json   
 {
 "id": null,
 "userName": "Ivan",
 "password": "12345"
 }
- Заголовки ответа:  
Content-Type: application/problem+json; charset=utf-8  
Date: Fri, 15 Sep 2023 14:36:32 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
- Тело ответа:    
```json   
{
    "type": "https://tools.ietf.org/html/
rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": 
"00-d589e3d02597164380a8ac05ae4f5da8-95a961ac6de369
49-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to 
System.Int32. Path: $.id | LineNumber: 2 | 
BytePositionInLine: 11."
        ]
    }
} 