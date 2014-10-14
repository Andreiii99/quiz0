Викторина - бот для ВКонтакте (vk.com)
=======================

Пример работы
------------
[vk.com/quiz0]http://vk.com/quiz0

Описание
------------
Бот постит вопросы в группу и ожидает ответа пользователей

Требования
------------

1. php 5.3+
2. mysql 5.1+
3. Standalone-приложение ВК(создаётся бесплатно в ВК)

Установка
------------

1. Установить Composer: [getcomposer.org](https://getcomposer.org/)
2. Установить зависимости: #`php composer.phar update`
3. Настроить бота
    * импортировать в mysql `db-sheme.sql`
    * импортировать базу вопросов в таблицу `question` (готовую можно найти в гугле)
    * переименовать local.php.example в local.php и настроить
    * получить access_token для зарегистрированного ранее standalone-приложения
    * указать id-группы и access_token в файле `module/Application/src/Application/Vk/Service.php`
4. Запустить бота: #`php public/index.php start`

Известные проблемы
----------

1. Бот не может постить более 200 постов в день в группу - это лимит ВК
2. Время от времени ВК не даёт редактировать посты и отвечать в сообщениях без капчи. 
Обычно это длится час-два, на это время бот лишён возможности выводить правильные ответы и/или давать подсказки.
