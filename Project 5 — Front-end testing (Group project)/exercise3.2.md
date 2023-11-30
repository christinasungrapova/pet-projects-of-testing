# Описание XPath    
 https://online.sberbankins.ru/store/property-insurance/    

## Кнопки: 
(1) ***Юридическое лицо*** //*[@id="mat-button-toggle-1-button"]

(2) ***Индивидуальный предприниматель*** //*[@id="mat-button-toggle-2-button"]

(3) ***Гражданин РФ*** //*[@id="mat-button-toggle-38-button"]

(4) ***Иностранный гражданин*** //*[@id="mat-button-toggle-39-button"]

(5) ***Мужской*** //*[@id="mat-button-toggle-40-button"]

(6) ***Женский*** //*[@id="mat-button-toggle-41-button"]

Является законсервированным, под реконструкцией, незавершенным строительством:  
(7) - ***да*** //*[@id="mat-button-toggle-10-button"]  
(8) - ***нет***  //*[@id="mat-button-toggle-11-button"]  

Является некапитальным зданием/сооружением без фундамента, воздухоопорной и/или надувной конструкцией  
(9) - ***да***  //*[@id="mat-button-toggle-12-button"]  
(10) - ***нет**  //*[@id="mat-button-toggle-13-button"]  

На объекте отсутствуют первичные средства пожаротушения (огнетушители / пожарный кран / пожарный водопровод) или их количество и состояние не соответствуют действующим нормам пожарной безопасности РФ  
(11) - ***да***  //*[@id="mat-button-toggle-14-button"] 
(12) - ***нет***  //*[@id="mat-button-toggle-15-button"]  

Имеет не исполненные предписания МЧС и/или Ростехнадзора на начало страхования  
(13) - ***да***  //*[@id="mat-button-toggle-16-button"]
(14) - ***нет***  //*[@id="mat-button-toggle-17-button"]  

Расположено в зоне объявленной чрезвычайной ситуации  
(15) - ***да***  //*[@id="mat-button-toggle-18-button"]  
(16) - ***нет***   //*[@id="mat-button-toggle-19-button"] 

Является рынком (совокупность отдельно стоящих или примыкающих друг к другу строений, расположенных на одной территории); отдельностоящей баней/сауной/бассейном; памятником истории/культуры/архитектуры  
(17) - ***да***  //*[@id="mat-button-toggle-20-button"]  
(18) - ***нет***  //*[@id="mat-button-toggle-21-button"]  

Имеется неузаконенная перепланировка / реконструкция объекта в части капитальной конструкции и инженерных систем  
(19) - ***да***  //*[@id="mat-button-toggle-22-button"] 
(20) - ***нет*** //*[@id="mat-button-toggle-23-button"]  


**Количество кнопок для каждого добавления / удаления объекта и территории может быть не более 50 кнопок, при этом Xpath будет менять на цифру n+1.**

(21) ***Добавить объект***  //button[contains(@class, 'mat-focus-indicator action-delete mat-stroked-button mat-button-base') and contains(span[contains(@class, 'mat-button-wrapper')], 'Добавить объект')]

/html/body/app-root/app-policy-form/div/div/app-policy-contact-form/form/div/div[3]/div/app-insured[14]/div[14]/div[n+1]/button[1]

(22) ***Удалить объект 1*** 

//button[contains(@class, 'mat-focus-indicator action-delete mat-stroked-button mat-button-base ng-star-inserted') and contains(span[contains(@class, 'mat-button-wrapper')], 'Удалить объект 1')] 

***Удалить объект 2*** 
//button[contains(@class, 'mat-focus-indicator action-delete mat-stroked-button mat-button-base ng-star-inserted') and contains(span[contains(@class, 'mat-button-wrapper')], 'Удалить объект 2')] 

/html/body/app-root/app-policy-form/div/div/app-policy-contact-form/form/div/div[3]/div/app-insured[14]/div[14]/div[n+1]/button[2]/span[1]

(23) ***Добавить территорию*** //button[contains(@class, 'mat-focus-indicator action-delete mat-stroked-button mat-button-base') and contains(span[contains(@class, 'mat-button-wrapper')], 'Добавить территорию')]

/html/body/app-root/app-policy-form/div/div/app-policy-contact-form/form/div/div[3]/div/div[n+1]/button[1]/span[1]

(24) ***Удалить территорию 1*** 
//button[contains(@class, 'mat-focus-indicator action-delete mat-stroked-button mat-button-base ng-star-inserted') and contains(span[contains(@class, 'mat-button-wrapper')], Удалить	территорию 1')] 

/html/body/app-root/app-policy-form/div/div/app-policy-contact-form/form/div/div[3]/div/div[n+1]/button[2]/span[1]

(25) ***Рассчитать*** //button[contains(@class, 'mat-focus-indicator mat-flat-button mat-button-base mat-accent') and contains(span[contains(@class, 'mat-button-wrapper')], 'Рассчитать')]

(26) ***Применить (Франшиза/Введите промокод)*** //button[contains(@class, 'mat-focus-indicator stroke-btn mat-stroked-button mat-button-base mat-button-disabled') and contains(span[contains(@class, 'mat-button-wrapper')], 'Применить')]

//buttoncontains(@class, 'mat-focus-indicator') and contains(@class, 'stroke-btn') and contains(@class, 'mat-stroked-button') and contains(@class,'mat-button-base') and contains(@class,'mat-button-disabled') and contains(span[contains(@class, 'mat-button-wrapper'), 'Применить')]

(27) ***Назад*** //button[contains(@class, 'mat-focus-indicator stroke-btn mat-stroked-button mat-button-base') and contains(span[contains(@class, 'mat-button-wrapper')], 'Назад')]

(28) ***Оформить полис*** //button[contains(@class, 'mat-focus-indicator mat-flat-button mat-button-base mat-accent mat-button-disabled') and contains(span[contains(@class, 'mat-button-wrapper')], 'Оформить полис')]

## Поля ввода:
 ### Для Юридического лица:
 (1) ***Поиск по Наименованию/ИНН/ОГРН*** //*[@id="mat-input-21"]

 Если отметить чек-бокс Заполнить вручную, то появляются следующие поля для заполнения:

 (2) ***Страна регистрации***  //*[@id="mat-input-22"] 
 (3) ***Полное наименование***  //*[@id="mat-input-23"]
 (4) ***ИНН***  //*[@id="mat-input-24"]
 (5) ***КПП***  //*[@id="mat-input-25"]  
 (6) ***ОГРН***  //*[@id="mat-input-26"]  
 (7) ***Регион***  //*[@id="mat-input-27"]
 (8) ***Город или Населенный пункт***  //*[@id="mat-input-28"] 
 (9) ***Улица***  //*[@id="mat-input-29"] 
 (10) ***Дом, литер, корпус***  //*[@id="mat-input-30"] 
 (11) ***Офис, помещение***  //*[@id="mat-input-31"]  

 ### Для Индивидуального предпринимателя:  

 (12) ***Поиск по ФИО/ИНН/ОГРНИП***  //*[@id="mat-input-38"]

 Если отметить чек-бокс Заполнить вручную, то появляются следующие поля для заполнения:  

 (13) ***Фамилия***  //*[@id="mat-input-39"]
 (14) ***Имя***  //*[@id="mat-input-40"] 
 (15) ***Отчество***  //*[@id="mat-input-41"]
 (16) ***ИНН***  //*[@id="mat-input-43"]
 (17) ***ОГРНИП*** //*[@id="mat-input-44"]
 (18) ***Регион*** //*[@id="mat-input-45"]
 (19) ***Город или населенный пункт***  //*[@id="mat-input-46"] 
 (20) ***Улица*** //*[@id="mat-input-47"]
 (21) ***Дом, литер, корпус***  //*[@id="mat-input-48"]  
 (22) ***Офис, помещение***  //*[@id="mat-input-49"]

### Адрес имущества:
(24) ***Регион***  //*[@id="mat-input-10"]
(25) ***Город*** //*[@id="mat-input-11"]
(26) ***Улица*** //*[@id="mat-input-12"]
(27) ***Дом***  //*[@id="mat-input-13"]
(28) ***Офис, помещение, кадастровый номер, территориальный ориентир*** //*[@id="mat-input-14"] 

### Вид деятельности
(29) ***Класс опасности*** //*[@id="mat-input-7"]
(30) ***Требование к АПС*** //*[@id="mat-input-8"]

### Информация по территории страхования:  
(31) ***Год постройки здания или последний капремонт***  
//*[@id="mat-input-9"]

### Объект 1:
(32) ***Расшифровка названия объекта*** //*[@id="mat-input-15"]
(33) ***Офис/помещение*** //*[@id="mat-input-16"]
(34) ***Кадастровый номер*** //*[@id="mat-input-17"]  
(35) ***Площадь объекта*** //*[@id="mat-input-18"]  
(36) ***Страховая сумма*** //*[@id="mat-input-19"] 
(37) ***Страховая стоимость*** //*[@id="mat-input-20"]

### Контактная информация:  
(38) ***Телефон***  //*[@id="mat-input-1"]
(39) ***Электронная почта***  //*[@id="mat-input-2"]
(40) ***Дополнительная электронная почта***  //*[@id="mat-input-3"]

(41) ***Франшиза***  //*[@id="mat-input-4"]  
(42) ***Введите промокод***  //*[@id="mat-input-5"]


 ## Чек-боксы:
(1) ***Залог Сбербанка***   //*[@id="mat-checkbox-1"]  

(2) ***Заполнить вручную*** //*[@id="mat-checkbox-2"]/label/span[1] 

(3) ***Отчество отсутствует*** //*[@id="mat-checkbox-17"]/label/span[2]

(4) ***Улица отсутствует (Заполнить вручную)*** //*[@id="mat-checkbox-17"]/label/span[1]

(5) ***Адрес имущества совпадает с адресом регистрации*** //*[@id="mat-checkbox-3"]/label/span[1]  

(6) ***Улица отсутствует (Адрес имущества совпадает с адресом регистрации)*** //*[@id="mat-checkbox-18"]/label/span[1]

(7) ***Внезапные и непредвиденные расходы по расчистке территории от последствий возникновения ущерба*** //*[@id="mat-checkbox-10"]/label/span[1]  

(8) ***Внезапные и непредвиденные расходы по ограждению, укреплению, обшивке материалами, герметизации или поддержке зданий, сооружений или застрахованного имущества для обеспечения их безопасности*** //*[@id="mat-checkbox-11"]/label/span[1]    

(9) ***Расходы на перемещение и защиту***  //*[@id="mat-checkbox-12"]/label/span[1]  

(10) ***Расходы по благоустройству территории*** //*[@id="mat-checkbox-13"]/label/span[1]  

(11) ***Расходы по замене ключей, замков, мастер-ключей и т. д. (в случае их хищения)***  //*[@id="mat-checkbox-14"]/label/span[1]  

(12) ***Покрытие по риску терроризм***  //*[@id="mat-checkbox-5"]/label/span[1]  

(13) ***Покрытие по риску диверсия***  //*[@id="mat-checkbox-6"]/label/span[1]  

(14) ***Покрытие по риску народные волнения***  //*[@id="mat-checkbox-7"]/label/span[1]   

(15) ***Покрытие по риску бой стекол***  //*[@id="mat-checkbox-8"]/label/span[1]  

(16) ***Покрытие по риску не капитальный ремонт***  //*[@id="mat-checkbox-9"]/label/span[1]  

 
## Датапикеры: 
(1) **Дата начала страхования***  //*[@id="mat-input-0"]  
(2) ***Дата заключения*** //*[@id="mat-input-0"]  
(3) ***Дата рождения (Датапикер в сведениях об ИП)***  //div[contains(@class, 'mat-form-field-infix ng-tns-c65-688')]


***Слайдер в блоке выбора срока страхования*** //div[@class="mat-slider-wrapper"]

***Логотип "СБЕР СТРАХОВАНИЕ"*** //div[@class="header_logo"]

***Хедер "Данные страхователя"*** //h4[@class="block-header"]

## Текстовые блоки
(1) ***Укажите дату начала действия полиса и срока страхования***
//p[@class="date-police"]

(2) ***Является законсервированным, под реконструкцией, незавершенным строительством***
//span[@class="stop1"]

(3) ***Является некапитальным зданием/сооружением без фундамента, воздухоопорной и/или надувной конструкцией***
//span[@class="stop2"]

(4) ***На объекте отсутствуют первичные средства пожаротушения (огнетушители / пожарный кран / пожарный водопровод) или их количество и состояние не соответствуют действующим нормам пожарной безопасности РФ***
//span[@class="stop3"]

(5) ***Имеет не исполненные предписания МЧС и/или Ростехнадзора на начало страхования***
//span[@class="stop4"]

(6) ***Расположено в зоне объявленной чрезвычайной ситуации***
//span[@class="stop5"]

(7) ***Является рынком (совокупность отдельно стоящих или примыкающих друг к другу строений, расположенных на одной территории); отдельностоящей баней/сауной/бассейном; памятником истории/культуры/архитектуры*** 
//span[@class="stop6"]

(8) ***Имеется неузаконенная перепланировка / реконструкция объекта в части капитальной конструкции и инженерных систем*** 
//span[@class="stop7"]