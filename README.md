# CommentBook
Микросервис по хранению и созданию комментариев к курсам ВШЭ
<br/>
# Описание проекта

## Задачи
Проект предназначен для упрощения поиска информации о курсах ВШЭ для студентов и абитурьентов. Данный микросервис предоставляет сайт на котором каждый студент может найти свой предмет/направление/факультет и оставить к нему публичный отзыв

## Архитектура
Так как ВШЭ - ВУЗ с огромным колличеством студентов, на данное приложение может происходить большая нагрузка, поэтому было принято решение использовать микросервисный подход. Таким образом, за счет маштабируемости, будет достигнута большая отказаустойчивость и лёгкость в тестировании отдельных компонентов.
Микросервис не будет содержать в большого колличества компонентов, поэтому была выбрана многослойная архитектура, которую можно представить схемой


## Технологии
 * [Web-Приложение ASP.NET Core](https://docs.microsoft.com/ru-ru/visualstudio/get-started/csharp/tutorial-aspnet-core?view=vs-2022)
 * [Web-Api ASP.NET Core](https://docs.microsoft.com/ru-ru/aspnet/web-api/)
 * [docker-compose](https://docs.docker.com/compose/)
 * [PostgresSQL](https://www.postgresql.org/)

## Краткое описание работы
   Данный проект это композиция докеров WEB-API, postgreSQl, pgAdmin, где API и pgAdmin взаимодействуют с БД посредством портов внутри отедельной docker-network 

## Функционал
 * Сохранение в базе данных факультетов, направлений и курсов с сохранением зависимостей между ними с помощью внешних ключей
 * Воозможность переноса всего контейнера без потери целостности данных
 * Добавление и удаление коментариев к курсам, факультетам или направлениям
 * Возврат любых данных из БД
 * Взаимодействие с БД с использованием pgadmin
