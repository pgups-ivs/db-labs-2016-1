Лабораторные работы по курсу "Базы данных", часть 1
================================

Работы этого семестра будут использовать в качестве примера БД с сайта http://postgresqltutorial.com/, которая была, в свою очередь, портирована из проекта Sakila для MySQL (http://dev.mysql.com/doc/sakila/en/).

В [канале Telegram](telegram.me/pgups_db) будут публиковаться новости-объявления, позже будет добавлен групповой чат для обсуждения работ. Пока его нет, можно обращаться ко мне в VK.

#Расписание
Занятия в этом семестре будут проходить один раз в две недели, начиная с 19 февраля:

Дата | Тема
---- | ----
19.02.2016 | Вводное занятие. Установка PG, импорт данных, простейшие запросы.
04.03.2016 | Оператор Select
18.03.2016 | Оператор Select
01.04.2016 | Операторы DDL. Разработка своей схемы.
15.04.2016 | Операторы DDL. Разработка своей схемы.
29.04.2016 | Триггеры/Функции/Процедуры
13.05.2016 | Триггеры/Функции/Процедуры
27.05.2016 | защита работ


#Начало работы
Для подготовки к выполнению работ необходимо скачать-установить сервер СУБД, и потом скачать и импортировать образ базы данных с сайта:
http://www.postgresqltutorial.com/postgresql-sample-database/

#Схема базы данных
![Схема данных](http://www.postgresqltutorial.com/wp-content/uploads/2013/05/PostgreSQL-Sample-Database.png)


# Что читать
В первую очередь стоит просмотреть обучающий раздел на сайте Postgresql.org ( [Tutorial](http://www.postgresql.org/docs/9.4/static/tutorial.html) ) и первые уроки на postresqltutorial.com. Также скачать электронные книги с диска F: или из чата.

# Тема 1: Оператор Select
[Полный синтаксис оператора Select](http://www.postgresql.org/docs/9.4/static/sql-select.html)

Изучение оператора разделено на два занятия:

1. Базовая структура оператора select (выборки данных из одной таблицы)
  * Однострочные функции
    *	[агрегатные функции](http://www.postgresql.org/docs/9.4/static/functions-aggregate.html) (COUNT, SUM, AVG, MAX, MIN)
    *	использование [строковых](http://www.postgresql.org/docs/9.4/static/functions-string.html), [числовых](http://www.postgresql.org/docs/9.4/static/functions-math.html) и функций для работы с [датами](http://www.postgresql.org/docs/9.4/static/functions-datetime.html)
    *	функции [преобразования типов данных](http://www.postgresql.org/docs/9.4/static/functions-formatting.html)
    *	условные выражения: [CASE и COALESCE](http://www.postgresql.org/docs/9.4/static/functions-conditional.html)
    *	[операторы сравнения строк](http://www.postgresql.org/docs/9.4/static/functions-matching.html): LIKE, SIMILAR TO и регулярные выражения
  * [Группировка данных](http://www.postgresql.org/docs/9.4/static/queries-table-expressions.html#QUERIES-GROUP)
    * группировка данных с помощью фразы GROUP BY
    * исключение итоговых строк при помощи фразы HAVING
  * Сортировка данных - фраза [ORDER BY](http://www.postgresql.org/docs/9.4/static/queries-order.html)
  * Ограничение размера результата выборки - фразы [LIMIT и OFFSET](http://www.postgresql.org/docs/9.4/static/queries-limit.html)
2. Выборка данных из нескольких таблиц
  * [соединения таблиц](http://www.postgresql.org/docs/9.4/static/queries-table-expressions.html#QUERIES-FROM)
    * декартово произведение - CROSS JOIN
    * внутренее соединение - INNER JOIN
      * эквисоединение - условия ON и USING
      * естественное соединение - условие NATURAL
    * внешние соединения (LEFT [OUTER] JOIN, RIGHT [OUTER] JOIN, FULL [OUTER] JOIN)
    * соединение более двух таблиц
    * соединение таблицы с собой
  * объединение запросов
    * [операторы UNION, INTERSECT, EXCEPT](http://www.postgresql.org/docs/9.4/static/queries-union.html)
  * Подзапросы
    * подзапросы в фразах FROM и HAVING
    * коррелированные подзапросы
    * использование операторов [EXISTS, ANY, SOME, ALL, IN, NOT IN](http://www.postgresql.org/docs/9.4/static/functions-subquery.html)


# Тема 2: Разработка схем данных


# Тема 3: Хранимые процедуры
