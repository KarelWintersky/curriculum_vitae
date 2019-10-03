## Личная информация
<img align="right" src="https://github.com/ilyachase/curriculum_vitae/blob/master/img/me.jpg?raw=true" alt="ilya.chase"/>

- ФИО: Левин Илья Викторович
- Дата рождения: 06.12.1992
- Семейное положение: холост
- Локация: г. Челябинск
- Контактный телефон: +7 900 026 4321
- Адрес электронной почты: ilya.chase@yandex.ru

## Образование
Высшее: факультет Вычислительной математики и информатики (ВМИ) ЮУрГУ, направление «Фундаментальная информатика и информационные технологии». Очно, бюджет.

## Опыт работы
- *Май 2016 – октябрь 2019.*
- *Компания: «[Hearst Shkulev Digital Regional Network](http://www.hearst-shkulev-media.ru/projects/rn/)».*
- *Должность: PHP-программист, Ведущий PHP-программист, Тимлид.*

## О себе
### Кратко о карьере
Сразу после защиты диплома получил должность PHP-программиста в 74.ru. Хотел именно туда, потому что 74.ru – это хайлоад, сложный продукт, разрабатываемый крутой командой. Уже к концу года получил повышение до Ведущего PHP-программиста. После интеграции 74.ru и NGS.ru, занимался такими проектами, как [НГС.Знакомства](https://love.ngs.ru/), [НГС.Афиша](https://afisha.ngs.ru/), [НГС.Форум](https://forum.ngs.ru/), [НГС.Объявления](https://do.ngs.ru/) и другими. Последний год занимал должность Тимлида.
Занимался все спектром разработки – не только код, но и инфраструктура, архитектура и дизайн приложений, CI\CD, улучшение процесса разработки (внедрял SCRUM), внедрение стандартов разработки. В свободное время [занимаюсь фрилансом](https://www.upwork.com/freelancers/~012c6b4205549a7dc4) на зарубежной бирже.

### О компетенциях
#### Код
В момент устройства в 74.ru, наша команда активно развивала проект, на котором «крутились» все сайты [сети Rugion](https://rugion.ru/stat/): 74.ru, 72.ru, 63.ru и остальные. Помимо новостных ресурсов, на том же коде работали classified-площадки: domchel.ru (сейчас интегрирован с N1), autochel.ru (сейчас интегрирован с auto.ru) и их зеркала на других регионах.

Код представлял собой рукописный фреймворк с более чем 1 300 000 строк (без учёта вендоров). В тот момент для меня это была самая сложная система, над которой я когда-либо работал. В результате, получил скачкообразный рост, познакомился со многими подходами (реализация отказоустойчивости, распределение нагрузки, организация кода в мульти-доменной многосервисной системе) и хайлоадными «фишками» (изменение структуры очень горячих таблиц, работа с «долгими» скриптами (от нескольких дней), умный stale-кэшинг и т.д.).

<p align="center">
  <img src="https://github.com/ilyachase/curriculum_vitae/blob/master/img/stanok_code_stats.jpg?raw=true" alt="Stanok code stats"/>
</p>

Далее были проекты вертикали НГС: Знакомства, Афиша, Форум, Объявления. Они были написаны давно, на внутреннем фреймворке. По сути, все стандартные элементы любого фреймворка, но написанные руками: роутинг, request\response, ORM, CLI-команды.
Для НГС.Афиши писали новое API на фреймворке Slim, описывали Swagger'ом.

Последний год с новой командой, в которой я был Тимлидом, работали над всеми Форумами HSD RN (74.ru, NGS.RU, NN.RU и E1). Из наиболее запомнившегося можно выделить исходный код NN.RU, который в части сложности, запутанности и количества легаси переплюнул всё, с чем приходилось работать до этого. Приняли решение переписывать его постепенно, внедрив рядом микро-фреймворк Slim. Тем самым, бизнес-задачи не стопорились, а код постепенно переносился на новые рельсы. Опыт успешний, сделали несколько довольно крупных задач (например, рездизайн страницы темы на форуме), количество «живого» кода на новых рельсах увеличивалось, а стоимость разработки уменьшалась.

#### Фреймворки
Помимо основной работы, неприрывно пробую новые технологии на фриланс-заказах. Таким образом наработал навык быстрой разработки на yii2. Нравится [gii](https://www.yiiframework.com/doc/guide/2.0/en/start-gii), но не нравится то, что модули этого фреймворка [прибиты](https://github.com/yiisoft/yii2/issues/11328) к нему [гвоздями](https://github.com/yiisoft/di/issues/23), не реализуя PSR-интерфейсы.

С Laravel познакомился при работе над NN.RU – там был набор «микросервисов» (по сути, отдельных небольших проектов) на Laravel, реализующих разный бизнес-функционал (работа с форумом, юзерами, галереями и т.д.). В Laravel нравится [DI](https://laravel.com/docs/5.7/container) и реализация консольных команд через artisan, но сильно не нравятся [Фасады](https://laravel.com/docs/5.8/facades), которые убивают поддержку кода IDE. Приходится использовать специальные [хаки](https://github.com/barryvdh/laravel-ide-helper) (кстати, в yii2 тоже есть такая [проблема](https://github.com/samdark/yii2-cookbook/blob/master/book/ide-autocompletion.md)).

Работая на Slim 3, тут и там сталкиваешься с тем, что нужно внедрить довольно тривиальный функционал: поддержка CLI-команд, авторизация\аутентификация, поддержку кэшей и т.д. Ничего этого нет в Slim «из коробвки» (ведь это микрофреймворк), и в данной ситуации отлично помогает Symfony. Их реализация [консольных команд](https://symfony.com/doc/current/console.html) остаётся моей любимой, а [компонент авторизации](https://symfony.com/doc/current/components/security/authentication.html) действительно framework agnostic и безболезненно интегрируется в Slim (да и любой другой фреймворк). Отдельной похвалы заслуживает [DomCrawler](https://symfony.com/doc/current/components/dom_crawler.html), который избавляет от [боли](https://stackoverflow.com/a/1732454) работы с разметкой через регулярки или XPath (который [не так тривиален](https://stackoverflow.com/a/1604480), как кажется на первый взгляд).

<p align="center">
  <img src="https://github.com/ilyachase/curriculum_vitae/blob/master/img/code_example.png?raw=true" alt="Stanok code stats"/>
</p>

Желание болшьше писать на микрофреймворках обусловлено стремлением к написанию framework agnostic кода. Со временем хочу прийти к написанию приложений не на MVC, который морально устаревает, а на какой-нибудь реализации Clean Architecture, которая по определению не зависит от фреймворков. Пока что прихожу к тому, чтобы более тщательно раскладывать код по модулям, и более детально разбиваю букву «M» из MVC на слои.

Пример моего кода можно увидеть [здесь](https://github.com/ilyachase/rainbow_score_api) – это часть моего домашнего проекта. Он в стадии активной разработки MVP, так что скорость более приоритетна, чем шлифование деталей, но некоторые идеи, озвученные выше, там всё же можно найти.

Помимо этого, имею представление о современном фронте: на [мобильную версию](https://m.love.ngs.ru/?not_redirect_mobile=1) НГС.Знакомств внедряли Webpack + Vue.js. Немного сам умею в Javascript: начинал как и все с jQuery, затем перешёл на ES6 и Vanilla. Проявляю интерес к Golang (есть выполненные фриланс-заказы на нём).

#### Тестирование
Я люблю тестирование и то, как вследствие написания тестов изменияется и расцепляется код. В компании внедрял сначала end-to-end тесты через Selenium, потом перешли на более быстрые функциональные + юнит тесты. Использовал как Codeception, так и обычный PHPUnit.

<p align="center">
  <img src="https://github.com/ilyachase/curriculum_vitae/blob/master/img/tests_output.png?raw=true" alt="Tests output" />
</p>

#### Инфраструктура и сопутствующие технологии
Помимо непосредственно написания кода, во время работы познакомился с подходами в построении архитектуры для highload-приложений. Довольно плотно работал с Nginx, понимаю, как балансировать с помощью HAProxy и proxy_pass. Работал с кластерными решениями баз (Percona, MongoDB cluster, Apache Cassandra) и хранилищ статики (OpenStack Swift). Для отложенных задач использовал RabbitMQ и beanstalkd.

Весь продакшн был у нас в контейнерах, так что с ними тоже знаком. В компании использовалось кастомное решение, а во всей домашней разработке использую Docker.

Понимаю, что такое репликация и шардинг. Приходилось оптимизировать запросы, разбираться в тонкостях индксов MariaDB и том, как она исполняет запросы, которые не влазят в буфер. Бывало, приходилось работать с таблицами размером больше 100 миллионов записей.

Кроме реляционных баз, работал с MongoDB, Redis и Cassandra. Из поисковых индексов работал со Sphinx и Manticore. Есть желание познакомиться с другими – например, с Elasticsearch.

Довольно неплохо понимаю, как работает HTTP: не составит труда рассказать, как работает SSL, что такое CORS или написать простой GET-запрос текстом прямо в telnet.

И вообще, считаю полезным уметь при необходимости из терминала отредактировать файл через vim, что-нибудь grep-нуть, а если надо, то послушать весь трафик по порту через ngrep.

<p align="center">
  <img src="https://github.com/ilyachase/curriculum_vitae/blob/master/img/ngrep.png?raw=true" alt="ngrep" />
</p>

#### Мониторинг
Для команды разработки важно получать сигналы о проблемах на продакшне. Отлов ошибок мы делали в Sentry, а время работы элементов системы измеряли с помощью Pinba – собирали данные и затем складывали в Grafana. Там же агрегировали значения из логов Nginx. Для мониторинга железа и настройки соответствующих триггеров в компании использовался Zabbix.

<p align="center">
  <img src="https://github.com/ilyachase/curriculum_vitae/blob/master/img/grafana.png?raw=true" alt="grafana" />
</p>

### Мотивация
Хочу любить то, что делаю. Вдохновляют продукты, над которыми работают такие же перфекционисты, как и я. Хочу создавать то, что приносит людям пользу и радость: найти проект, в который влюблюсь сам и буду вкладывать в него душу.
