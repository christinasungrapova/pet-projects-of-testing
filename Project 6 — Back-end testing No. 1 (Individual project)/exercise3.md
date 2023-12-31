## Коды ответов

### Код ответа: 201. Тело ответа:
```
[
    {
        "name": "Малышева Екатерина Матвеевна",
        "birthday": "1995-06-01",
        "post": "Бухгалтер"
    },
    {
        "name": "Капустин Роман Артёмович",
        "birthday": "1991-01-18",
        "post": "Финансовый аналитик"
    },
    {
        "name": "Касьянов Ярослав Ярославович",
        "birthday": "1989-07-29",
        "post": "Кредитный эксперт"
    },
    {
        "name": "Белова Елизавета Руслановна",
        "birthday": "1997-04-13",
        "post": "Аудитор"
    },
    {
        "name": "Романов Константин Александрович",
        "birthday": "2001-12-14",
        "post": "Кассир"
    },
    ...
]
```
Согласно официальной спецификации HTTP, код 201 используется для указания, что новый ресурс был успешно создан на сервере. В данном случае, где мы запрашиваем список работников банка с использованием GET-метода, код 201 не является верным статус-кодом. Нам следует использовать код 200 для указания успешного выполнения запроса и возврата списка работников.

Таким образом, необходимо заменить код ответа 201 на 200.

**Код 200** - это правильный код ответа. 

### Код ответа: 400. Тело ответа:
```
{
  "message": "Неверные данные для авторизации."
}
```
Исходя из предоставленного ответа сервера, можно сделать вывод, что код 400 указывает на ошибку в запросе клиента, а именно - "Неверные данные для авторизации.".

Однако, в данном конкретном случае, код 400, скорее всего, не является подходящим статус-кодом для ситуации, где клиент запрашивает список работников банка. Код 400 обычно используется для указания на ошибки в запросе, когда данные клиента не соответствуют ожидаемому формату или требованиям.

Вместо этого, для ситуации, когда клиент неавторизован и пытается получить доступ к данному эндпоинту, более подходящим статус-кодом будет 401 Unauthorized. Код 401 обозначает, что клиент должен предоставить правильные учетные данные для авторизации, чтобы получить доступ к этому ресурсу.

Таким образом, если клиент неавторизован, то правильным статус-кодом будет 401 Unauthorized.

**Код 401** - это правильный код ответа. 

### Код ответа: 500. Тело ответа:
```
{
  "message": "Неверно составлен запрос."
}
```
В данном случае, код ответа 500 означает внутреннюю ошибку сервера. Это означает, что сервер не смог обработать запрос, поскольку он содержит неправильные данные или нарушены логика и правила обработки запросов.

Однако, в данном конкретном случае, код ответа 500, в сочетании с сообщением "Неверно составлен запрос", является не совсем подходящим. Здесь следует использовать код ответа 400 - Bad Request. Код 400 обычно используется, когда запрос пользователя неверный или содержит ошибку, которая не может быть исправлена сервером. 

**Код 400** - это правильный код ответа. 