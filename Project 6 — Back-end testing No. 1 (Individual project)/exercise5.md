# Успешные коды

## Activities

### **№1.**

**Запрос / Request.** GET ​/api​/v1​/Activities

**HTTP-метод.** GET

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Activities

**Заголовки запроса.** "accept: text/plain; v=1.0"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть. / Response body**
```
[
  {
    "id": 1,
    "title": "Activity 1",
    "dueDate": "2023-09-22T16:25:29.6093799+00:00",
    "completed": false
  },
  {
    "id": 2,
    "title": "Activity 2",
    "dueDate": "2023-09-22T17:25:29.609382+00:00",
    "completed": true
  },
]
```


### **№2.**

**Запрос / Request.** POST ​/api​/v1​/Activities

**HTTP-метод.** POST

**Полный URL запроса / Request URL..** https://fakerestapi.azurewebsites.net/api/v1/Activities


**Заголовки запроса.** "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"

**Тело запроса (при наличии) / Request body.**
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-09-22T15:42:24.980Z",
  "completed": true
}
```

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-09-22T15:42:24.98Z",
  "completed": true
}
```

### **№3.**

**Запрос / Request.** GET ​/api​/v1​/Activities​/{id}

**HTTP-метод.** GET

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Activities/1

**Заголовки запроса.** "accept: text/plain; v=1.0"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "id": 1,
  "title": "Activity 1",
  "dueDate": "2023-09-22T20:02:44.6411685+00:00",
  "completed": false
}
```

### **№4.**

**Запрос / Request.** PUT /api​/v1​/Activities​/{id}

**HTTP-метод.** PUT

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Activities/1 

**Заголовки запроса.** "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"

**Тело запроса (при наличии) / Request body.** 
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-09-22T19:06:50.673Z",
  "completed": true
}
```

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-09-22T19:06:50.673Z",
  "completed": true
}
```

### **№5.**

**Запрос / Request.** DELETE ​/api​/v1​/Activities​/{id}

**HTTP-метод.** DELETE 

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Activities/1

**Заголовки запроса.** "accept: */*"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.** Отсутствует.

## Authors

### **№6.**

**Запрос / Request.** GET ​/api​/v1​/Authors

**HTTP-метод.** GET

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Authors

**Заголовки запроса.** "accept: text/plain; v=1.0"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
[
  {
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
  },
  {
    "id": 2,
    "idBook": 1,
    "firstName": "First Name 2",
    "lastName": "Last Name 2"
  }
]
```

### **№7.**

**Запрос / Request.** POST ​/api​/v1​/Authors

**HTTP-метод.** POST

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Authors

**Заголовки запроса.** "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"

**Тело запроса (при наличии) / Request body.**
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.** Отсутствует.


### **№8.**

**Запрос / Request.** GET /api​/v1​/Authors​/authors​/books​/{idBook}

**HTTP-метод.** GET

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/1

**Заголовки запроса.** "accept: text/plain; v=1.0"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
[
  {
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
  },
  {
    "id": 2,
    "idBook": 1,
    "firstName": "First Name 2",
    "lastName": "Last Name 2"
  }
]
```

### **№9.**

**Запрос / Request.** GET /api​/v1​/Authors​/{id}

**HTTP-метод.** GET

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Authors/1

**Заголовки запроса.** "accept: text/plain; v=1.0"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "id": 1,
  "idBook": 1,
  "firstName": "First Name 1",
  "lastName": "Last Name 1"
}
```

### **№10.**

**Запрос / Request.** PUT ​/api​/v1​/Authors​/{id}

**HTTP-метод.** PUT

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Authors/1

**Заголовки запроса.** "Content-Type: application/json; v=1.0"

**Тело запроса (при наличии) / Request body.**
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

### **№11.**

**Запрос / Request.** DELETE /api​/v1​/Authors​/{id}

**HTTP-метод.** DELETE 

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Authors/1

**Заголовки запроса.** "accept: */*" 

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.** Отсутствует.

## Books

### **№12.** 

**Запрос / Request.** GET ​/api​/v1​/Books

**HTTP-метод.** GET

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Books

**Заголовки запроса.** "accept: text/plain; v=1.0" 

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
[
  {
    "id": 1,
    "title": "Book 1",
    "description": "Sed aliquam magna ipsum eum autem. Aliquyam sit dolore. Labore tation et dolore aliquam dolore tempor aliquyam duis ea ex qui at sed ea clita. Dignissim dignissim dolor kasd clita erat magna hendrerit consectetuer amet amet. Amet est sadipscing at facilisi aliquyam feugiat amet dolor in ipsum no elitr amet accusam lorem accusam. Erat sadipscing voluptua tempor dolor ea et blandit ea tempor et duis veniam suscipit sanctus. Dolores nonumy lobortis justo aliquyam vero takimata. Et accumsan sadipscing nulla no dolor zzril et ipsum lorem sed sed amet kasd dolor lorem. Lobortis erat stet et dolores quis veniam clita et et elit ipsum zzril amet. Exerci at takimata eum no justo sit exerci dolor et diam gubergren. Et amet dolores rebum rebum et. Et laoreet ipsum dolore. Magna consequat kasd velit eirmod euismod et sed at et ipsum. Ut sed takimata consequat ex erat lorem dolore est eu dolor dolore clita sadipscing rebum est labore. Amet dolor gubergren accumsan wisi et at stet autem tempor vel lorem soluta diam nonumy. Et eirmod gubergren ea tempor duis dolor nonumy amet nulla eu diam qui in diam justo et.\n",
    "pageCount": 100,
    "excerpt": "Elitr lorem consequat vel sanctus eirmod voluptua lorem tempor elitr sadipscing justo luptatum aliquam. Gubergren et dolore consetetur dolore takimata quis sed vulputate. Justo est dolores et. Eos vel stet et lorem eos no feugait dolores praesent lobortis ipsum sed justo justo. Dolor dolor nulla et takimata magna sea et consequat kasd est accusam. Ad kasd sea et justo eirmod voluptua sit. Rebum takimata ipsum veniam eum accusam accusam magna consetetur dolore dolore. Sed lorem dolor eu. Voluptua tempor accumsan vero justo elit tempor sea est nihil duo. Doming no nibh lorem et no sit at stet sit eleifend sea voluptua duo. Amet tempor et erat at eirmod sed duo sed ea sit tempor congue. Lorem takimata eos dolores invidunt iusto ea ad cum sit consetetur.\nVel duo voluptua et kasd eos et erat dolore et aliquyam ut et. Sed eirmod dolore qui diam nonumy sea stet rebum ipsum lorem nam voluptua consetetur dolore ipsum. Nisl no ex eos vero at sit amet et. Nonumy diam dolores diam tation elitr illum labore ea. Elitr ipsum ipsum magna amet diam tempor takimata magna dolor. At consetetur sit justo et dolores nihil sanctus eu consequat clita dolores rebum nostrud consectetuer elitr ipsum. Aliquyam ullamcorper lorem nulla nibh stet ut clita et minim ut voluptua suscipit et dolor sit dolore amet. No consequat dolor hendrerit rebum sit volutpat augue aliquyam assum. Et no lobortis ut ipsum et. No magna lobortis elit sit est sit. Duo sed magna sed eirmod est dolores autem. Dolores labore justo amet consetetur autem mazim accusam ea. Ipsum sed sanctus sit at labore sed luptatum ipsum. Sadipscing tincidunt praesent labore ea sit clita erat consetetur accusam sea elitr lorem et veniam amet. Est sadipscing sit ut justo ipsum facilisi. Et dolor takimata.\nEa dolore ipsum erat aliquam sit tempor ipsum. Qui dolore facilisi vulputate ea no vero diam ut rebum lobortis lorem laoreet nonumy feugiat. Eirmod illum dignissim praesent at ipsum et tempor sanctus clita commodo aliquyam. Ut voluptua dolore elitr tempor sed no. Accusam dolores euismod ipsum consetetur clita dolores lorem takimata erat eos ut. Sadipscing kasd aliquyam consequat magna vero amet nonumy nulla dolores invidunt tempor lorem. Eum et feugait et rebum accusam placerat aliquip. Kasd aliquyam lorem consequat ipsum commodo duo lorem ea voluptua. Sed ipsum quis ut vero aliquyam esse est. Gubergren magna stet enim ipsum. Dolores dignissim aliquyam amet sadipscing consectetuer eos ipsum ea elitr. Praesent sit no at ut esse lorem. Consectetuer clita et sanctus sed gubergren diam at vulputate feugait takimata voluptua ea. Dolores nonumy laoreet delenit molestie no duo duis hendrerit praesent. Ipsum dolore lorem clita sed diam. Cum esse duo sea diam labore stet et. Nibh facilisis nonumy vulputate duo et. Sed dolore kasd nibh accusam dolore ea accusam accumsan sanctus eirmod ex duo kasd consetetur invidunt diam. Ea invidunt rebum tempor ex.\nErat duis et et feugait lorem tempor sadipscing elitr augue consetetur sanctus ut. Ut hendrerit tation tempor eleifend ipsum elitr nulla et sanctus aliquyam accusam erat suscipit invidunt. Placerat qui at wisi wisi duis magna nulla iriure. Est dolore elitr takimata sea minim dolor sed accusam feugiat stet lorem.\nDiam elitr sit option at sit dolore rebum aliquyam et amet cum et molestie nulla dolores dolores. Eirmod lorem et. Dolore clita sit dolor nihil lobortis nobis in dolor. Dolor consetetur soluta illum nostrud diam dolores cum consectetuer vero sed elitr ut vero. Enim dolor tempor dolore consetetur et praesent sea ipsum eirmod elitr sed no justo. Duis kasd eum sed dolor sit facer stet justo facilisi takimata nisl.\n",
    "publishDate": "2023-09-21T19:50:56.2585214+00:00"
  }
]
```

### **№13.**

**Запрос / Request.** POST ​/api​/v1​/Books

**HTTP-метод.** POST

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Books

**Заголовки запроса.** "Content-Type: application/json; v=1.0"

**Тело запроса (при наличии) / Request body.**
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-09-22T19:52:41.613Z"
}
```

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-09-22T19:52:41.613Z"
}
```

### **№14.**

**Запрос / Request.** GET ​/api​/v1​/Books​/{id}

**HTTP-метод.** GET

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Books/1

**Заголовки запроса.** "accept: text/plain; v=1.0"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "id": 1,
  "title": "Book 1",
  "description": "Dolor nonumy vero dolor invidunt erat lorem luptatum elit elitr justo amet vero lorem dolor. Nisl diam volutpat esse dolores justo takimata at sit. Et ipsum et possim mazim sit ut voluptua et. Justo stet takimata et diam ut ipsum velit stet et gubergren sit cum sit lorem veniam elitr consequat iusto. Vulputate lobortis dolores dolores et nulla hendrerit clita elitr et sit ipsum sed velit dolor illum. Tation et eirmod dolor vero praesent iusto justo sed ut at. No ut sanctus et elitr duo tempor at voluptua wisi dignissim eirmod erat eu elit praesent. Elitr eu dolores illum invidunt velit invidunt elitr praesent voluptua sed ipsum sanctus. Ipsum eu dolor magna ut est diam magna. Diam no vero takimata clita erat blandit ut clita erat accusam eu clita diam ea dolores amet diam. Takimata sit duo labore sadipscing dolor ad sed at labore dolor labore ex. Eum clita at dolore. Nulla et clita duo clita et esse takimata ea dolore et vel adipiscing. Sea ea ipsum amet tempor duo euismod stet amet consetetur eirmod duo sed sit sit vel elitr dolor sanctus. Sanctus in sed clita dolor sit aliquyam vel sit et est sed. Molestie vel voluptua clita labore lorem aliquyam invidunt commodo erat consetetur clita lorem vero erat. Sit ipsum at takimata ea ut sed duis liber eirmod erat voluptua augue accumsan at stet tempor et vero. Justo ut sanctus labore feugiat lobortis feugiat tation gubergren id. Et invidunt elitr ut ipsum diam gubergren lorem et accusam dolor dolor elit sadipscing ipsum magna.\n",
  "pageCount": 100,
  "excerpt": "Duo ipsum at nonumy ea ea blandit zzril labore. Illum sed sed. Dolor diam iusto. Et erat et nulla amet magna at consequat gubergren lorem. Augue sed ullamcorper dolor rebum sea at zzril ipsum duo eum voluptua dolor sit consetetur. Dolore est rebum dolor odio lorem labore nulla aliquyam. Aliquip erat laoreet est sanctus. Molestie diam sit vel sed. Labore ipsum augue amet et diam et justo. Nostrud et est takimata tempor dolore placerat et sea ea accusam vero. Justo ipsum illum sed esse veniam justo autem diam sea no sit lobortis ut elitr ea.\nDolor magna tempor at ut accusam nobis sit duo magna et rebum wisi molestie consequat elitr. Hendrerit vero voluptua exerci tempor invidunt illum at sanctus tempor ullamcorper dolor takimata diam vero aliquam stet delenit. Dolor wisi sit assum est kasd elitr commodo dolore consetetur diam sed stet ipsum dignissim suscipit sanctus et dolor. Vulputate feugiat vel aliquyam invidunt accusam et nostrud amet sadipscing commodo. Diam duis eirmod sed consetetur blandit vero. Dolore ut voluptua sed duis. Nulla ipsum dolores ex kasd dolore consetetur consetetur nulla erat laoreet diam sit voluptua eros amet exerci clita. Dolor dolores velit eirmod sit ea eleifend cum accusam dolore vel nisl kasd amet. Amet at stet est ea autem sanctus est consequat est et adipiscing tempor eum. Sadipscing et lorem et qui stet et minim velit dolor hendrerit consetetur dolor clita. In consequat dolor amet dolor rebum amet takimata dolores dolore labore vel vulputate sea diam kasd. Ipsum magna ipsum. Et vel in eos amet ipsum. Et volutpat et invidunt cum dolor veniam invidunt eirmod eos eirmod ut eos et. Sea feugait takimata amet dolores diam diam zzril suscipit. Dolor ut duis diam. Soluta illum in dolore molestie accusam. Est tempor sed vero eirmod facilisis dolores ut assum kasd vero qui vero justo takimata eirmod amet qui. Duo sit amet stet et sanctus sed invidunt nam.\nWisi consectetuer takimata lorem eirmod vulputate nonumy et. Dolore iriure dolore justo amet duo sed sea dolor at lorem veniam. Tincidunt commodo amet tempor lorem diam nonumy consetetur stet et duis gubergren at invidunt. Dolores aliquam sadipscing adipiscing. Ad stet eos stet aliquyam sed eos vero gubergren. Nonumy labore et nonumy ipsum nulla. Blandit stet exerci accusam dolor. Ipsum elitr at et ipsum voluptua lorem justo elitr nonumy nihil labore duo accusam consetetur possim sed dolores vero.\nSit dolore et sit ipsum voluptua et facilisis accusam eirmod blandit stet amet aliquyam et et amet possim dolore. Te sed in invidunt accusam duis nisl amet labore ad placerat sed facilisi at tempor lorem. Rebum volutpat aliquam dolore justo sed rebum nulla nonumy erat kasd eros eros sea et. Option diam takimata sea magna exerci eos ex feugiat nulla at lorem elitr aliquyam tempor aliquam eu no et. Sit sanctus dolor nonumy vero diam invidunt dolore nonumy delenit nibh labore sed magna. Commodo kasd ipsum duis at sed exerci amet et est feugiat et autem aliquam kasd labore nihil odio. Tempor diam justo possim at voluptua clita duo diam nonumy takimata gubergren rebum diam duo. Dolor clita consetetur lorem accusam lorem consetetur justo dolore dolore invidunt est sed takimata illum magna.\nDolore ipsum magna lorem kasd facilisi nonumy vero tempor at ut tempor eirmod eirmod. Ullamcorper sit sed erat sit justo et erat sit erat accusam magna et elitr. Elitr sit dolore sea. Diam aliquyam lorem gubergren takimata ullamcorper et elitr ut labore diam sadipscing quis. Diam lorem in velit diam sit consetetur.\n",
  "publishDate": "2023-09-21T19:55:06.1380754+00:00"
}

```

### **№15.**

**Запрос / Request.** PUT ​/api​/v1​/Books​/{id}

**HTTP-метод.** PUT

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Books/1

**Заголовки запроса.**  "Content-Type: application/json; v=1.0"

**Тело запроса (при наличии) / Request body.**
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-09-22T19:57:06.501Z"
}
```

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-09-22T19:57:06.501Z"
}
```

### **№16.**

**Запрос / Request.** DELETE /api​/v1​/Books​/{id}

**HTTP-метод.** DELETE 

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Books/1

**Заголовки запроса.** "accept: */*"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.** Отсутствует.

## CoverPhotos

### **№17.**

**Запрос / Request.** GET ​/api​/v1​/CoverPhotos

**HTTP-метод.** GET

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

**Заголовки запроса.** "accept: text/plain; v=1.0"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
[
  {
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
  },
  {
    "id": 2,
    "idBook": 2,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 2&w=250&h=350"
  },
  {
    "id": 3,
    "idBook": 3,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 3&w=250&h=350"
  }
]
```

### **№18.**

**Запрос / Request.** POST /api​/v1​/CoverPhotos

**HTTP-метод.** POST

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

**Заголовки запроса.** "Content-Type: application/json; v=1.0"

**Тело запроса (при наличии) / Request body.**
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```

### **№19.**

**Запрос / Request.** GET ​/api​/v1​/CoverPhotos​/books​/covers​/{idBook}

**HTTP-метод.** GET 

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/1

**Заголовки запроса.** "accept: text/plain; v=1.0"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
[
  {
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
  }
]
```

### **№20.**

**Запрос / Request.** GET ​/api​/v1​/CoverPhotos​/{id}

**HTTP-метод.** GET

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1

**Заголовки запроса.**  "accept: text/plain; v=1.0"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "id": 1,
  "idBook": 1,
  "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```

### **№21.** 

**Запрос / Request.** PUT /api​/v1​/CoverPhotos​/{id}

**HTTP-метод.** PUT

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1 

**Заголовки запроса.**  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0" 

**Тело запроса (при наличии) / Request body.**
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
### **№22.**

**Запрос / Request.** DELETE /api​/v1​/CoverPhotos​/{id}

**HTTP-метод.**  DELETE

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1

**Заголовки запроса.** "accept: */*" 

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.** Отсутствует.

## Users

### **№23.**

**Запрос / Request.** GET ​/api​/v1​/Users

**HTTP-метод.** GET

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Users

**Заголовки запроса.** "accept: text/plain; v=1.0"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
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
  }
]
```

### **№24.**

**Запрос / Request.** POST ​/api​/v1​/Users

**HTTP-метод.** POST 

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Users

**Заголовки запроса.** "accept: */*" -H  "Content-Type: application/json; v=1.0"

**Тело запроса (при наличии) / Request body.**
```
{
  "id": 1,
  "userName": "string",
  "password": "string"
}
```

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "id": 1,
  "userName": "string",
  "password": "string"
}
```


### **№25.**

**Запрос / Request.** GET /api​/v1​/Users​/{id}

**HTTP-метод.** GET 

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Users/1

**Заголовки запроса.** "accept: */*" 

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "id": 1,
  "userName": "User 1",
  "password": "Password1"
}
```


### **№26.**

**Запрос / Request.** PUT ​/api​/v1​/Users​/{id}

**HTTP-метод.** PUT 

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Users/12

**Заголовки запроса.** "accept: */*" -H  "Content-Type: application/json; v=1.0"

**Тело запроса (при наличии) / Request body.**
```
{
  "id": 12,
  "userName": "string",
  "password": "string"
}
```

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "id": 12,
  "userName": "string",
  "password": "string"
}
```

### **№27.**

**Запрос / Request.** DELETE ​/api​/v1​/Users​/{id}

**HTTP-метод.** DELETE

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Users/20

**Заголовки запроса.** "accept: */*"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 200 Success

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.** Отсутствует.

# Провальные коды

## Activities

### **№28.**

**Запрос / Request.** GET ​/api​/v1​/Activities​/{id}

**HTTP-метод.** GET

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Activities/100

**Заголовки запроса.** "accept: text/plain; v=1.0"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 404 Error: Not Found

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-3bd3715a95e28248982c7c938a92cd5b-c22fc9f6c8ea184f-00"
}
```

### **№29.**

**Запрос / Request.** PUT ​/api​/v1​/Activities​/{id}

**HTTP-метод.** PUT

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Activities/8785323123457878946 

**Заголовки запроса.** "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"

**Тело запроса (при наличии) / Request body.**
```
{
  "id": 8785323123457878946,
  "title": "string",
  "dueDate": "2023-09-22T20:42:37.834Z",
  "completed": true
}
```

**Статус-код ответа.** 400 Error: Bad Request

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-4728b1d410715f4b99febfaae11b730a-3beec9096052b740-00",
  "errors": {
    "id": [
      "The value '8785323123457878946' is not valid."
    ],
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 25."
    ]
  }
}
```

### **№30.**

**Запрос / Request.** DELETE /api​/v1​/Activities​/{id}

**HTTP-метод.** DELETE

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Activities/5000365200

**Заголовки запроса.** "accept: */*"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 400 Error: Bad Request

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-6c7590a847eab84e95a6bd6cd15f4668-b1b2e1fb5c132c4a-00",
  "errors": {
    "id": [
      "The value '5000365200' is not valid."
    ]
  }
}
```

## Authors

### **№31.**

**Запрос / Request.** GET ​/api​/v1​/Authors​/authors​/books​/{idBook}

**HTTP-метод.** GET 

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/789663314533

**Заголовки запроса.** "accept: text/plain; v=1.0"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 400 Error: Bad Request

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-b26e40e9c8ba40478ae53b38820ae5cb-1a09326d951c0f49-00",
  "errors": {
    "idBook": [
      "The value '789663314533' is not valid."
    ]
  }
}
```

### **№32.**

**Запрос / Request.** GET /api​/v1​/Authors​/{id}

**HTTP-метод.** GET 

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Authors/87841313212

**Заголовки запроса.** "accept: text/plain; v=1.0"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 400 Error: Bad Request

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-fab2ea321cb5994982fd2aa27ad857fe-276bd260b92dcc45-00",
  "errors": {
    "id": [
      "The value '87841313212' is not valid."
    ]
  }
}
```

### **№33.**

**Запрос / Request.** PUT ​/api​/v1​/Authors​/{id}

**HTTP-метод.** PUT

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Authors/87841313212

**Заголовки запроса.** "Content-Type: application/json; v=1.0" -

**Тело запроса (при наличии) / Request body.**
```
{
  "id": 87841313212,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

**Статус-код ответа.** 400 Error: Bad Request

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-6a566100cebb15488ba2aadf38b7f858-ce5c38d8e693cd4a-00",
  "errors": {
    "id": [
      "The value '87841313212' is not valid."
    ],
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 17."
    ]
  }
}
```

### **№34.**

**Запрос / Request.** DELETE /api​/v1​/Authors​/{id}

**HTTP-метод.** DELETE

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Authors/87841313212

**Заголовки запроса.** "accept: */*"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 400 Error: Bad Request

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-a4da78a0e1bc3c4e8695626bb957841e-59c925461cf20240-00",
  "errors": {
    "id": [
      "The value '87841313212' is not valid."
    ]
  }
}
```
## Books

### **№35.**

**Запрос / Request.** GET /api​/v1​/Books​/{id}

**HTTP-метод.** GET

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Books/87841313212

**Заголовки запроса.**  "accept: text/plain; v=1.0"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 400 Error: Bad Request

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-415ded3c73f7f1488fc1cf3c3e3fd37c-5ae1d2b98712f34d-00",
  "errors": {
    "id": [
      "The value '87841313212' is not valid."
    ]
  }
}
```

### **№36.**

**Запрос / Request.** PUT ​/api​/v1​/Books​/{id}

**HTTP-метод.** PUT 

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Books/87841313212

**Заголовки запроса.** "accept: */*" -H  "Content-Type: application/json; v=1.0"

**Тело запроса (при наличии) / Request body.**
```
{
  "id": 87841313212,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-09-22T19:57:06.501Z"
}
```

**Статус-код ответа.** 400 Error: Bad Request

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-a21c3203af2712469f8df2a4370eb624-37e803cb1879a545-00",
  "errors": {
    "id": [
      "The value '87841313212' is not valid."
    ],
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 17."
    ]
  }
}
```

### **№37.**

**Запрос / Request.** DELETE /api​/v1​/Books​/{id}

**HTTP-метод.** DELETE

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Books/87841313212


**Заголовки запроса.** "accept: */*"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 400 Error: Bad Request

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-85b141946e60244b8215929db6d29733-85239956b4e7624d-00",
  "errors": {
    "id": [
      "The value '87841313212' is not valid."
    ]
  }
}
```

## CoverPhotos

### **№38.**

**Запрос / Request.** GET /api​/v1​/CoverPhotos​/books​/covers​/{idBook}

**HTTP-метод.** GET

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Books/87841313212


**Заголовки запроса.** "accept: text/plain; v=1.0"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 400 Error: Bad Request

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-6c2eefe92b36d140bc1bfaacdc8833ca-3d1d64dcb7c09243-00",
  "errors": {
    "idBook": [
      "The value '87841313212' is not valid."
    ]
  }
}
```

### **№39.**

**Запрос / Request.** GET /api​/v1​/CoverPhotos​/{id}

**HTTP-метод.** GET

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Books/87841313212


**Заголовки запроса.** "accept: text/plain; v=1.0"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 400 Error: Bad Request

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-c06b54bbbe593c4995c9c69dc5adc173-6d08974a958fce4f-00",
  "errors": {
    "id": [
      "The value '87841313212' is not valid."
    ]
  }
}
```

### **№40.**

**Запрос / Request.** PUT /api/v1/CoverPhotos/{id}

**HTTP-метод.** PUT

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Books/87841313212


**Заголовки запроса.** "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"

**Тело запроса (при наличии) / Request body.**
```
{
  "id": 87841313212,
  "idBook": 0,
  "url": "string"
}
```

**Статус-код ответа.** 400 Error: Bad Request

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-5785de9777b51d4c81e3dc962946f7a3-f4966d87fedefe47-00",
  "errors": {
    "id": [
      "The value '87841313212' is not valid."
    ],
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 17."
    ]
  }
}
```

### **№41.**

**Запрос / Request.** DELETE ​/api​/v1​/CoverPhotos​/{id}

**HTTP-метод.** DELETE 

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Books/87841313212


**Заголовки запроса.** "accept: */*"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 400 Error: Bad Request

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-358d8d4664614744a225b93e01e27538-b5d20e29e002e84f-00",
  "errors": {
    "id": [
      "The value '87841313212' is not valid."
    ]
  }
}
```
## Users

### **№42.**

**Запрос / Request.** GET /api​/v1​/Users​/{id}

**HTTP-метод.** GET 

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Books/87841313212


**Заголовки запроса.** "accept: */*"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 400 Error: Bad Request

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-480693e47c518942ae020d16eda148eb-ad879d3f9b9efa49-00",
  "errors": {
    "id": [
      "The value '87841313212' is not valid."
    ]
  }
}
```

### **№43.**

**Запрос / Request.** PUT /api​/v1​/Users​/{id}

**HTTP-метод.** PUT

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Books/87841313212


**Заголовки запроса.** "accept: */*" -H  "Content-Type: application/json; v=1.0"

**Тело запроса (при наличии) / Request body.**
```
{
  "id": 87841313212,
  "userName": "string",
  "password": "string"
}
```

**Статус-код ответа.** 400 Error: Bad Request

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-29b116cfa9f9234c8adafc296d04bf61-331462285f22e24e-00",
  "errors": {
    "id": [
      "The value '87841313212' is not valid."
    ],
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 17."
    ]
  }
}
```

### **№44.**

**Запрос / Request.** DELETE /api​/v1​/Users​/{id}

**HTTP-метод.** DELETE 

**Полный URL запроса / Request URL.** https://fakerestapi.azurewebsites.net/api/v1/Books/87841313212


**Заголовки запроса.** "accept: */*"

**Тело запроса (при наличии) / Request body.** Отсутствует.

**Статус-код ответа.** 400 Error: Bad Request

**Тело ответа (при наличии). Если тело большое, то только его часть / Response body.**
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-fae84cff5684d046a63ac05d9e784136-51b0c2d10bc9634f-00",
  "errors": {
    "id": [
      "The value '87841313212' is not valid."
    ]
  }
}
```