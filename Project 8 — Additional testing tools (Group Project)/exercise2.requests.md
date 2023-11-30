## Какой запрос(-ы) отправляется на сервер для получения списка типов товаров в шторке "Каталог"?

POST https://megamarket.ru/api/mobile/v1/catalogService/catalog/menu

POST https://megamarket.ru/api/mobile/v1/catalogService/breadcrumbs/get

## Какой запрос(-ы) отправляется на сервер при использовании поиска товаров в каталоге?
POST https://megamarket.ru/api/mobile/v3/catalogService/catalog/searchSuggest

POST https://megamarket.ru/api/mobile/v1/catalogService/catalog/search

POST https://megamarket.ru/api/mobile/v1/catalogService/filters/search

## Какой запрос(-ы) отправляется на сервер при поиске региона или города в модалке выбора вашего региона?

POST https://megamarket.ru/api/mobile/v1/regionService/region/search

POST https://megamarket.ru/api/mobile/v1/addressSuggestService/address/suggest

