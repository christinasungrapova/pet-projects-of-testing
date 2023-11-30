# Local Storage

|№|Key|Value|Description|Source|
|----------|----------|----------|----------|----------|
|1|CartSortVariants|[{"title":"По добавлению","active":true},{"title":"По алфавиту","active":false},{"title":"Сначала дешёвые","active":false},{"title":"Сначала дорогие","active":false}]|Сохраняет фильтрацию товаров|https://belgorod.online.lenta.com/|
|2|searchHistory|["фасоль красная","кекс"]|Сохраняет введенные данные в строке поиска|https://belgorod.online.lenta.com/|  
|3|_gp_crtrgt_isFirstVisit|10/18/2023|Сохраняет дату посещения сайта|https://belgorod.online.lenta.com/|
|4|HDE_VISITOR_DATA[sbermarket.ru]|"id":"8dbce849-2706-4aaa-a9a0-218a5a5c0370","name":"","email":""}|Сохраняет данные пользователя|https://sbermarket.ru/|
|5|retailRocketEvents|[{"ts":1697729845317,"ev":"addToBasket","dt":{"id":640908}},{"ts":1697729849328,"ev":"addToBasket","dt":{"id":31812}},{"ts":1697729866192,"ev":"addToBasket","dt":{"id":75597}},{"ts":1697729867599,"ev":"addToBasket","dt":{"id":278741}},{"ts":1697729869125,"ev":"addToBasket","dt":{"id":258763}},{"ts":1697729870557,"ev":"addToBasket","dt":{"id":1484036}},{"ts":1697729872863,"ev":"addToBasket","dt":{"id":355991}},{"ts":1697729874272,"ev":"addToBasket","dt":{"id":25911}},{"ts":1697729977872,"ev":"groupView","dt":{"ids":[26397911]}},{"ts":1697730012616,"ev":"groupView","dt":{"ids":[26541913]}}]|Показывает каталог товаров|https://sbermarket.ru/|

# Session Storage
|№|Key|Value|Description|Source|
|----------|----------|----------|----------|----------|
|1|location|https://sbermarket.ru/retailer_selection/all|Показывает все магазины|https://sbermarket.ru/|
|2|AlreadySentABTests|["ab_starting_x_web_non_product_pages_header","acq_change_actions_on_map","ads_banner_main_web","search_multiretail_redesign_web","web_growth_multi_search_suggester_placeholder","new_web_merge_api","sberloyalty_cart_registration_web","ads_shelf_cart_web","delivery_conditions_web_bar","web_growth_suggester_placeholder","amound_on_cart","mega_menu_banner_on_show_js","b2b_new_header_step_1","show_special_offers_instead_of_promoted_categories","ads_banner_retailer_main_shelf_web","new_super_banner_on_show_js","ads_banner_retailer_main_carousel_web","show_surge_delivery_price_checkout_web","changing_order_details_web","changing_order_comment","changing_order_phone_web"]|Показывает отправленные тесты|https://sbermarket.ru/|
|3|DownloadMobileApp|"1"|Показывает возможность скачать мобильную версию|https://sbermarket.ru/|
|4|AF_BANNERS_SESSION_ID|1697618298621|Показывает id сеанса|https://belgorod.online.lenta.com/|
|5|GoodsListSorting|"category-popular"|Сохраняет сортировку списка товаров|https://belgorod.online.lenta.com/|

Результат выполнения команд для добавления и получения объекта в "Local Storage"

![Alt text](localStorage_console.png)

Состояние "Local Storage" после добавления объекта

![Alt text](localStorage_application.png)

Результат выполнения команд для добавления и получения объекта в "Session Storage"

![Alt text](sessionStorage_console.png)

Состояние "Session Storage" после добавления объекта

![Alt text](sessionStorage_application.png)
