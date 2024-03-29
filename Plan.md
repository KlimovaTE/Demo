#Планирование автоматизации тестирования комплексного сервиса, взаимодействующего с СУБД и API Банка

### Перечень сценариев для автоматизации:

##### 1. Сценарии перехода на страницу профессии “Тестировщик ПО” с главной страницы  
1.1
- открыть страницу https://netology.ru
- в меню “Каталог ресурсов” выбрать раздел “Программирование” 
- выбрать профессию “Тестировщик ПО”

1.2   
- открыть страницу https://netology.ru
- в меню “Каталог ресурсов” навести мышку на раздел “Программирование”, но не нажимать
- выбрать профессию “Тестировщик ПО”

1.3
- открыть страницу https://netology.ru
- меню “Каталог ресурсов” выбрать раздел “Полный каталог”
- выбрать профессию “Тестировщик ПО”

1.4
- открыть страницу https://netology.ru
- в разделе “Направления обучения” выбрать окно “Программирование”
- выбрать профессию “Тестировщик ПО”

1.5
- открыть страницу https://netology.ru
- в разделе “Выберите вектор развития” нажать на ссылку “Выбрать курс”
- выбрать профессию “Тестировщик ПО”

##### 2. Сценарии перехода к заполнении формы для записи на странице профессии
2.1
- открыта страница профессии https://netology.ru/programs/qa
- в центре страницы нажать на кнопку “Записаться”

2.2
- открыта страница профессии https://netology.ru/programs/qa
- пролистать до конца страницы до формы записи

2.3
- открыта страница профессии https://netology.ru/programs/qa
- пролистать вниз
- вверху в выпадающем окне нажать на кнопку “Записаться”


##### 3. Сценарии заполнении формы

3.1 Позитивный сценарий   
- заполнение всех полей валидными данными
1. В поле "Имя" ввести строку, состоящее из букв кириллицы или латиницы, где длина строки > 1 буквы. Строка может содержать дефис (например "Иван")
1. В поле для ввода телефона ввести строку, состоящую от 9 до 14 цифр. Строка может содержать символы "+", "(", ")", "-" (например 55555555555)
1. Нажать кнопку "Записаться"
- ожидаемый результат: форма отправлена. На экране появилась надпись "Запись произведена. Наш консультант свяжется с Вами в ближайшее время"

3.2 Негативные сценарии

3.2.1 Поле "Имя" и поле для ввода телефона не заполнены
1. Поле "Имя" оставить незаполненным
1. Поле для ввода телефона оставить незаполненным
1. Нажать кнопку "Записаться"
- ожидаемый результат: форма не отправлена. Поля подсвечиваются красным. Под полами появились надписи "Обязательное поле"

3.2.2 Поле "Имя" не заполнено
1. Поле "Имя" оставить незаполненным
1. В поле для ввода телефона ввести строку, содержащую от 9 до 14 цифр. Строка может содержать символы "+", "(", ")", "-" (например 55555555555)
1. Нажать кнопку "Записаться"
- ожидаемый результат: форма не отправлена. Поле "Имя" подсвечивается красным. Под полем появилась надпись "Обязательное поле"

3.2.3 Поле для ввода телефона не заполнено
1. В поле "Имя" ввести строку, состоящее из букв кириллицы или латиницы, где длина строки > 1 буквы. Строка может содержать дефис (например "Иван")
1. Поле для ввода телефона оставить незаполненным
1. Нажать кнопку "Записаться"
- ожидаемый результат: форма не отправлена. Поле для ввода телефона подсвечивается красным. Под полем появилась надпись "Обязательное поле"

3.2.4 В поле "Имя" введён 1 символ
1. В поле "Имя" ввести строку, состоящую из одной буквы кириллицы или латиницы (например "ф")
1. В поле для ввода телефона ввести строку, содержащую от 9 до 14 цифр. Строка может содержать символы "+", "(", ")", "-" (например 55555555555)
1. Нажать кнопку "Записаться"
- ожидаемый результат: форма не отправлена. Поле "Имя" подсвечивается красным. Под полем появилась надпись "Должно быть не короче 2 символов"

3.2.5 В поле "Имя" введёна строка, содержащая цифры
1. В поле "Имя" ввести строку, содержащую цифры (например "а11")
1. В поле для ввода телефона ввести строку, содержащую от 9 до 14 цифр. Строка может содержать символы "+", "(", ")", "-" (например 55555555555)
1. Нажать кнопку "Записаться"
- ожидаемый результат: форма не отправлена. Поле "Имя" подсвечивается красным. Под полем появилась надпись "Должно состоять из букв"

3.2.6 В поле "Имя" введёна строка, содержащая спецсимволы
1. В поле "Имя" ввести строку, содержащую спецсимволы (например "ааа№")
1. В поле для ввода телефона ввести строку, содержащую от 9 до 14 цифр. Строка может содержать символы "+", "(", ")", "-" (например 55555555555)
1. Нажать кнопку "Записаться"
- ожидаемый результат: форма не отправлена. Поле "Имя" подсвечивается красным. Под полем появилась надпись "Должно состоять из букв"

3.2.7 В поле для ввода телефона введёно меньше 9 цифр
1. В поле "Имя" ввести строку, состоящее из букв кириллицы или латиницы, где длина строки > 1 буквы. Строка может содержать дефис (например "Иван")
1. В поле для ввода телефона ввести строку, содержащую меньше, чем 9 цифр. Строка может содержать символы "+", "(", ")", "-" (например +55555555)
1. Нажать кнопку "Записаться"
- ожидаемый результат: форма не отправлена. Поле для ввода телефона подсвечивается красным. Под полем появилась надпись "Номер в формате +9 (999) 999-99-99"

3.2.8 В поле для ввода телефона введёно больше 14 цифр
1. В поле "Имя" ввести строку, состоящее из букв кириллицы или латиницы, где длина строки > 1 буквы. Строка может содержать дефис (например "Иван")
1. В поле для ввода телефона ввести строку, содержащую больше, чем 14 цифр. Строка может содержать символы "+", "(", ")", "-" (например +555111222333444)
1. Нажать кнопку "Записаться"
- ожидаемый результат: форма не отправлена. Поле для ввода телефона подсвечивается красным. Под полем появилась надпись "Номер в формате +9 (999) 999-99-99"

3.2.9 В поле для ввода телефона введёна строка, содержащая буквы
1. В поле "Имя" ввести строку, состоящее из букв кириллицы или латиницы, где длина строки > 1 буквы. Строка может содержать дефис (например "Иван")
1. В поле для ввода телефона ввести строку, содержащую буквы. Строка может содержать символы "+", "(", ")", "-" (например +555111222333ввв)
1. Нажать кнопку "Записаться"
- ожидаемый результат: форма не отправлена. Поле для ввода телефона подсвечивается красным. Под полем появилась надпись "Номер в формате +9 (999) 999-99-99"

3.2.10 В поле для ввода телефона введёна строка, содержащая спецсимволы
1. В поле "Имя" ввести строку, состоящее из букв кириллицы или латиницы, где длина строки > 1 буквы. Строка может содержать дефис (например "Иван")
1. В поле для ввода телефона ввести строку, содержащую спецсимволы, кроме "+", "(", ")", "-" (например +555111222333%)
1. Нажать кнопку "Записаться"
- ожидаемый результат: форма не отправлена. Поле для ввода телефона подсвечивается красным. Под полем появилась надпись "Номер в формате +9 (999) 999-99-99"

### Перечень используемых инструментов:

- Java - язык написания автотестов;
- IntelliJ IDEA - программа, в которой пишем автотесты;
- Gradle - система автоматической сборки внутри IntelliJ IDEA;
- JUnit 5 - библиотека для тестирования;
- Faker - генерация пользовательских данных (имени и телефона);
- Selenide -для работы с HTML-страницами и CSS-элементами;
- MySQL Connector - для работы с БД на MySQL;
- Allure - для создания отчетов о прохождении тестов;

### Перечень необходимых разрешений, данных и доступов:
- Разрешение на тестирование страниц сайта с помощью автоматизированного ПО;
- Разрешение на доступ к базе данных заявок;
### Перечень и описание возможных рисков при автоматизации:
- Возможна смена кода страницы либо css-селекторов, придется править код;
- Долгое открытие страницы сайта, либо вкладки;
- Недоступность сайта или страницы;
- Неоправданная стоимость автоматизации;
- Невозможность оценки положительных сценариев тестирования в связи с отсутствием доступа к реальной БД;
### Перечень необходимых специалистов для автоматизации:
- Специалист по автоматизированному тестированию со знанием инструментов, указанных в п. “Перечень используемых инструментов”;
### Интервальная оценка с учётом рисков (в часах):
- Необходимое время на тестирование составляет 16 часов, с учетом рисков - 24 часа.
