# План автоматизации тестирование возможности записи на обучение профессии "Тестировщик ПО" на сайте netology.ru

## Введение
Цель создания плана - описание процесса автоматизации тестирования перехода к форме записи на обучение и заполнения данной формы;

## Виды тестирования:
* Функциональное тестирование - проверить функциональность на соответствие требованиям;
* Тестирование веб интерфейса(интеграционное) - проверить дефекты в интерфейсе, во взаимодействии между интегрированными компонентами или системами;

## Перечень автоматизируемых сценариев(проверить открытие [сайта](https://netology.ru)):
* Проверить наличие меню "Каталог курсов", "Программирование", "Тестировщик ПО", "НЕО для начинающих", "Изучайте актуальные темы";
* Проверить открытие страницы с профессиями при нажатии на кнопку "Каталог курсов"->"Программирование"->"Тестировщик ПО";
* Проверить открытие страницы с профессиями при нажатии на круг "НЕО для начинающих"->"Лучшие курсы для старта"->"Тестировщик ПО";
* Проверить открытие страницы с профессиями при нажатии на круг "НЕО для начинающих"->"Программирование"->"Тестировщик ПО";
* Проверить наличие кнопки "Записаться" на странице для перехода к пункту заполнения полей;
* Проверить работу кнопки "Записаться" и переход в форму заполнения анкеты;
* Проверить появившейся интерфейс с формой для записи;
* Проверить наличие полей для записи имени, телефона, а также активных кнопок "Записаться" и "Получить консультацию";
* Проверить открытие и соответствие раздела "Нажимая кнопку, принимаю условия политики и пользовательского соглашения";

## Позитивные сценарии:
* Отправить валидную форму:
1. Заполнить поле "Имя" "Андрей";
2. Заполнить поле "Телефон" "+79999999999";
3. Заполнить поле "Почта" "иванов@mail.ru";
4. Нажать кнопку "Получить консультацию";
5. Ожидаемый результат: На странице появляется всплывающее сообщение с текстом "Вы записались на курс";
* Отправить данные авторизованного пользователя:
1. Заполнить поле "Имя" "Иван";
2. Заполнить поле "Телефон" "+791199991799";
3. Нажать кнопку "Записаться";
4. Ожидаемый результат: На странице появляется всплывающее сообщение с текстом "Скоро вам позвонят";
* Отправить форму, заполнив поле "Имя", используя латинские буквы:
1. Заполнить поле "Имя" "Andrey";
2. Заполнить поле "Телефон" "+791199991798"
3. Заполнить поле "Почта" "иванов@mail.ru";
4. Нажать кнопку "Записаться";
5. Ожидаемый результат: На странице появляется всплывающее сообщение с текстом "Вы записались на курс";
* Проверить заполнение формы, используя русские и латинские буквы:
1. Заполнить поле "Имя" "Dmitrii Иванов";
2. Заполнить поле "Телефон" "+791199991798"
3. Заполнить поле "Почта" "иванов@mail.ru";
4. Нажать кнопку "Записаться";
5. Ожидаемый результат: На странице появляется всплывающее сообщение с текстом "Вы записались на курс";

## Негативные сценарии:
* Отправить пустую форму:
1. Нажать кнопку "Записаться";
2. Ожидаемый результат: На странице под полями "Имя", "Телефон", "Почта" появляется всплывающее сообщение с текстом "Обязательное поле";
* Отправить заполненную форму только именем:
1. Заполнить поле "Имя" "Николай";
2. Нажать кнопку "Записаться";
3. Ожидаемый результат: На странице под полем "Телефон" и "Почта" появляется всплывающее сообщение с текстом "Обязательное поле";
* Отправить заполненную форму указав только номер телефона:
1. Заполнить поле "Телефон" "+791199991798";
2. Нажать кнопку "Записаться";
3. Ожидаемый результат: На странице под полем "Имя" и "Почта" появляется всплывающее сообщение с текстом "Обязательное поле";
* Отправить форму не заполняя поле "Почта":
1. Заполнить поле "Имя" "Фафа";
2. Заполнить поле "Телефон" "+791199991798";
3. Нажать кнопку "Записаться";
4. Ожидаемый результат: На странице под полем "Почта" появляется всплывающее сообщение с текстом "Обязательное поле";
* Отправить форму, заполнив поле "Имя" граничными значениями:
1. Заполнить поле "Имя" "А";
2. Заполнить поле "Телефон" "+791199991798";
3. Заполнить поле "Почта" "иванов@mail.ru";
4. Нажать кнопку "Записаться";
5. Ожидаемый результат: На странице под полем "Имя" появляется всплывающее сообщение с текстом "Должно быть не короче 2 символов";
* Отправить форму, заполнив поле "Телефон" граничными значениями:
1. Заполнить поле "Имя" "А";
2. Заполнить поле "Телефон" "+799999999999990";
3. Заполнить поле "Почта" "иванов@mail.ru";
4. Нажать кнопку "Записаться";
5. Ожидаемый результат: На странице под полем "Телефон" появляется всплывающее сообщение с текстом "Номер в формате +9 (999) 999-99-99"; 
* Отправить форму, заполнив поле "Имя", используя символы:
1. Заполнить поле "Имя" "%№";
2. Заполнить поле "Телефон" "+791199991798";
3. Заполнить поле "Почта" "иванов@mail.ru";
4. Нажать кнопку "Записаться";
5. Ожидаемый результат: На странице под полем "Имя" появляется всплывающее сообщение с текстом "Должно состоять из букв";

## Перечень используемых инструментов с обоснованием выбора:
* IntelliJ IDEA - среда разработки ПО;
* Java - язык программирования для автоматизации;
* JUnit 5 - фреймворк для модульного тестирования ПО на языке Java;
* Gradle - система автоматической сборки для упрощения работы с Java;
* Selenide - фреймворк для автоматизированного тестирования веб-приложения;
* Faker - библиотека для генерации случайных данных;
* Allure - популярный инструмент построения отчётов, упрощающий их анализ;

## Перечень необходимых разрешений/данных/доступов:
* Разрешение на тестирование страниц [сайта](https://netology.ru) с помощью автоматизированного ПО;
* Разрешение на доступ к базе данных;

## Перечень и описание возможных рисков при автоматизации:
* Возможность изменения структуры сайта;
* Возможность изменения/удаления обучаемой профессии на сайте;
* Возможность изменения количества обязательных полей в заявке;
* Невозможность написания в форме некоторых букв(например, буквы ё);
* Долгое открытие страницы сайта либо вкладки;
* Недоступность сайта или страницы;

## Перечень необходимых специалистов для автоматизации:
* Инженер по автоматизированному тестированию;

## Необходимое время на тестирование:
* 39 часов с учетом рисков;