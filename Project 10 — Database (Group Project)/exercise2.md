## Веб-хранилища №1 
### Что такое Local Storage и Session Storage? В чём заключается их различие? 

***Local Storage*** является объектом, который позволяет хранить данные без истечения срока действия. Это означает, что данные, которые вы сохраняете в local Storage, останутся там, даже если пользователь закроет браузер или выключит компьютер. Данные, хранящиеся в local Storage, имеют лимит размера (обычно около 5-10 МБ), и они доступны только для того же домена, что и ваш веб-сайт.  

***Session Storage*** — это временное хранилище данных в браузере. Временное — потому что после закрытия вкладки все данные в sessionStorage автоматически удаляются. При этом перезагрузка вкладки не влияет на данные, главное, чтобы не прервалась сессия или не поменялась Wi-Fi-точка.  

***Различие*** Local Storage и Session Storageв том, что данные в sessionStorage удаляются после закрытия вкладки браузера, а в localStorage они не удаляются "никогда";    
Доступность: данные о пользователе в localStorage доступны из любого окна, при условии, что вы осуществляется заход под теми же данными (например, авторизуетесь на сайте), в то время как sessionStorage работает только из того же окна, а изменение вкладки браузера приведет к удалению информации.  

### Основные методы взаимодействия с Local Storage и Session Storage через консоль в браузере  

Объекты хранилища sessionStorage и localStorage предоставляют одинаковые методы и свойства:

**setItem(key, value)** – сохранить пару ключ/значение;  
**getItem(key)** – получить данные по ключу key;  
**removeItem(key)** – удалить данные с ключом key;  
**clear()** – удалить все;  
**key(index)** – получить ключ на заданной позиции;  
**length** – количество элементов в хранилище. 

### Как производить сохранение, получение, удаление данных, очистку хранилища?  
**Сохранение данных:**   
<u> *Local Storage* и Session Storage </u> Для сохранения данных можно использовать метод setItem():  
Пример Local Storage:   
| index.js  |  
|-----|  
| localStorage.setItem("username", "John");  |
----
В приведенном выше примере мы сохраняем значение John с ключом username в localStorage.

Пример Session Storage:  
| index.js  |  
|---------|  
| sessionStorage.setItem("username", "John");|  
-----
В этом примере мы сохраняем значение John с ключом username в sessionStorage.  

**Получение данных:**  
<u> *Local Storage* и Session Storage </u> Для получения данных используется метод getItem():  
Пример Local Storage:   
| index.js  |  
|-----|  
| 1  const username = localStorage.getItem("username");  |
| 2  console.log(username); // Выводит: "John"  |
----
Мы используем метод getItem() и передаем ключ username для получения значения "John".

Пример Session Storage:  
| index.js  |  
|---------|  
| 1 const username = sessionStorage.getItem("username"); |
| 2 console.log(username); // Выводит: "John"|  
-----
Мы используем метод getItem() и передаем ключ username для получения значения John.  

**Удаление данных:**  
<u> *Local Storage* и Session Storage </u> Для удаления данных используется метод removeItem():
Пример Local Storage:   
| index.js  |  
|-----|  
| localStorage.removeItem("username"); |
----
Мы передаем ключ username в метод removeItem() для удаления соответствующего значения из localStorage.

Пример Session Storage:  
| index.js  |  
|---------|  
| sessionStorage.removeItem("username");|
-----
Мы передаем ключ username в метод removeItem() для удаления соответствующего значения из sessionStorage.  

**Очистка хранилища:**  
<u> *Local Storage* и Session Storage </u> Для полной очистки и удаления всех данных из него можно использовать метод clear():
Пример Local Storage:   
| index.js  |  
|-----|  
| localStorage.clear(); |
----
Метод clear() удаляет все данные из localStorage.

Пример Session Storage:  
| index.js  |  
|---------|  
| sessionStorage.clear();|
-----
Метод clear() удаляет все данные из sessionStorage.

### Что такое IndexedDB? Чем этот вид хранилища отличается от описанных выше?  

***IndexedDB*** - это способ постоянного хранения данных внутри клиентского браузера, другими словами это NOSQL хранилище на стороне клиента. Что позволяет создавать веб-приложения с богатыми возможностями обращения к данным независимо от доступности сети, ваши приложения могут работать как онлайн, так и офлайн.  
 Он может хранить значительный объем структурированных данных — даже файлы и большие двоичные объекты. Как и любая база данных, IndexedDB индексирует данные для эффективного выполнения запросов.   
 Использовать IndexedDB сложнее, нужно создать базу данных, таблицы и использовать транзакции. По сравнению с localStorage IndexedDB требуется намного больше кода. В отличие от других форм хранилища браузера, IndexedDB не ограничивается хранением строк. IndexedDB может хранить данные всех стандартных типов JavaScript.   

 ## Как можно просмотреть содержимое всех веб-хранилищ в браузере?  

Для просмотра содержимого веб-хранилища используют DevTools в инструментах разработчика в вкладке Application  
Например в браузере Google Chrome вызвать инструменты разработчика можно несколькими способами:  
  *Из основного меню.* Кликаем по кнопке меню (три точки в правом верхнем углу окна браузера), наводим курсор на выпадающий список "Дополнительные инструменты" и в нём нажимаем пункт "Инструменты разработчика" дальше выбираем -> Application (Приложение) -> вкладка Storage (Хранилище) в нем хранятся данные "Local Storage", "Session Storage" и "IndexedDB" и другие данные. 
 *Горячими клавишами.* Для вызова можно нажать кнопку F12 или комбинацию CTRL+SHIFT+I.     
 *Из контекстного меню.* Нажимаем правой кнопкой мыши на веб-страничке и выбираем пункт "Просмотреть код" 


