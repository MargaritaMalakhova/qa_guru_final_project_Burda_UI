# Дипломный проект по автоматизации тестирования (WEB)

## 	Содержание

> ➠ [Web приложение BurdaStyle](#web-приложение-burdastyle)
>
> ➠ [Технологический стек UI](#технологический-стек-ui)
> 
> ➠ [Запуск тестов из терминала](#запуск-тестов-из-терминала)
>
> ➠ [Запуск тестов в Jenkins](#запуск-тестов-в-Jenkins)
>
> ➠ [Отчет о результатах тестирования в Allure Report](#-главная-страница-allure-отчета)
>
> ➠ [Тест-кейсы в Allure Test Ops](#-тест-кейсы-в-allure-test-ops)
>
> ➠ [Уведомления в Telegram с использованием бота](#-уведомления-в-telegram-с-использованием-бота)
> >
> ➠ [Пример запуска теста в Selenoid](#-пример-запуска-теста-в-selenoid)

##  Web приложение BurdaStyle

###  Функциональные тесты для web приложения BurdaStyle

> Разработаны автотесты на <code>UI</code>.

- [x] Авторизация в веб приложении (позитивный тест)
- [x] Авторизация в веб приложении (негативный тест)
- [x] Изменение профиля пользователя
- [x] Добавление товаров в Wish List
- [x] Добавление товаров в корзину
- [x] Оформление и оплата заказа
- [x] Скачивание PDF-файла заказа

## Технологический стек UI

<p align="center">
<img width="6%" title="IntelliJ IDEA" src="readme_interactive_elements/logo/Intelij_IDEA.svg">
<img width="6%" title="Java" src="readme_interactive_elements/logo/Java.svg">
<img width="6%" title="Selenide" src="readme_interactive_elements/logo/Selenide.svg">
<img width="6%" title="Selenoid" src="readme_interactive_elements/logo/Selenoid.svg">
<img width="6%" title="Allure Report" src="readme_interactive_elements/logo/Allure_Report.svg">
<img width="6%" title="Allure Test Ops" src="readme_interactive_elements/logo/Allure_Test_Ops.svg">
<img width="6%" title="Gradle" src="readme_interactive_elements/logo/Gradle.svg">
<img width="6%" title="JUnit5" src="readme_interactive_elements/logo/JUnit5.svg">
<img width="6%" title="GitHub" src="readme_interactive_elements/logo/GitHub.svg">
<img width="6%" title="Jenkins" src="readme_interactive_elements/logo/Jenkins.svg">
<img width="6%" title="Telegram" src="readme_interactive_elements/logo/Telegram.svg">
</p>

### В данном проекте автотесты написаны на <code>Java</code> с использованием <code>Selenide</code> для UI-тестов.
>
> <code>Selenoid</code> выполняет запуск браузеров в контейнерах <code>Docker</code>.
>
> <code>Allure Report</code> формирует отчет о запуске тестов.
>
> Для автоматизированной сборки проекта используется <code>Gradle</code>.
>
> В качестве библиотеки для запуска тестов используется <code>JUnit 5</code>.
>
> <code>Jenkins</code> выполняет запуск тестов.
> 
> После завершения прогона отправляются уведомления с помощью бота в <code>Telegram</code>.

### Запуск тестов из терминала

### Локальный запуск тестов

#### Локальный запуск тестов с использованием параметров из файла test.properties

```
gradle clean test
```

#### Описание параметров для запуска тестов
>
> -DbrowserName <code>название браузера</code>
>
> -DbrowserVersion <code>версия браузера</code>
>
> -DbaseUrl <code>url стенда фронта</code>
>
> -DbrowserSize <code>разрешение браузера</code>
>
> -DpageLoadTimeout <code>таймаут загрузки страницы</code>
>
> -Dtimeout <code>таймаут ожидания загрузки элемента страницы</code>
>
> -DisRemote <code>запуск тестов локально или через remote сервис</code>
>
> -DremoteUrl <code>url remote сервиса</code>

### Удаленный запуск тестов

#### Удалённый запуск через передачу параметров

```
gradle clean test 
-DremoteUrl=
-DbaseUrl=
-DbrowserName=
-DbrowserVersion=
-DbrowserSize=
-DisRemote=
-DpageLoadTimeout=
-Dtimeout=
```

## <img width="4%" title="Jenkins" src="readme_interactive_elements/logo/Jenkins.svg"> Запуск тестов в Jenkins

> Для запуска тестов используется параметризированная сборка.
> Ссылка на Jenkins Job: <code>https://jenkins.autotests.cloud/job/19-marg0shek-final_project_ui/</code>

<p align="center">
<img title="Jenkins" src="readme_interactive_elements/screens/Jenkins.png">
</p>

## <img width="4%" title="Allure_Report" src="readme_interactive_elements/logo/Allure_Report.svg"> Главная страница allure отчета

> Ссылка на Allure report: <code>https://jenkins.autotests.cloud/job/19-marg0shek-final_project_ui/28/allure/</code>

<p align="center">
<img title="Allure_main" src="readme_interactive_elements/screens/AllureReportMainPage.png">
</p>

### <img width="4%" title="Allure_Report" src="readme_interactive_elements/logo/Allure_Report.svg"> Группировка тестов по проверяемому функционалу

<p align="center">
<img title="Allure_suits" src="readme_interactive_elements/screens/AllureReportSuites.png">
</p>

### <img width="4%" title="Allure_testops" src="readme_interactive_elements/logo/Allure_Test_Ops.svg"> Тест-кейсы в Allure Test Ops

> Ссылка на TestOps: <code>https://allure.autotests.cloud/project/3596/test-cases?treeId=0</code>

<p align="center">
<img title="Allure_testops" src="readme_interactive_elements/screens/TestOps.png">
</p>

## <img width="4%" title="Telegram" src="readme_interactive_elements/logo/Telegram.svg"> Уведомления в Telegram с использованием бота

> После завершения сборки специальный бот, созданный в <code>Telegram</code>, автоматически обрабатывает и отправляет сообщение с отчетом о прогоне.
>
> Информация по настройке и использованию бота <code>https://github.com/qa-guru/allure-notifications</code>

<p align="center">
<img title="Telegram_notifications" src="readme_interactive_elements/screens/Telegram.png">
</p>

## <img width="4%" title="Selenoid" src="readme_interactive_elements/logo/Selenoid.svg"> Пример запуска теста в Selenoid

> К каждому тесту в отчете прилагается видео. Одно из таких видео представлено ниже.

<p align="center">
<img title="Selenoid_gif" src="readme_interactive_elements/Selenoid.gif">
</p>
