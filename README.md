# testtask01_catalog_books
Тестовое задание по PHP. Каталог книг.

Инструкция по запуску:
1) Папку с проектом поместить в htdocs (в xampp)
2) Запустить xampp
3) Запустить Apache и MySQL в xampp
4) В адресной строке прописать путь к проекту (начиная от папки htdocs (её не учитывать))

В начале работы с сайтом:
1) Перед работой с сайтом нужно создать пустую базу данных с названием catalog_books (с кодировкой urf8_general_ci)
2) Убедиться что конфигурация для подключения к б/д правильная (по-умолчанию username: root, password:) 
Изменить конфигурацию можно в классе-файле /Database/DbConfig.php
3) Затем на главной странице перейти во вкладку Миграции б/д и обновить базу данных
4) После чего все таблицы, и данные будут загружены в б/д catalog_books

Как реализованы миграции?
По пути /Database/migrations/sqlFiles/ находятся все файлы миграций. Каждый файл - новая версия. Каждый файл пронумерован, и включено 
краткое описание обновления.
При добавлении новой версии, и обновлении миграций на сайте - в б/д будет выполнен скрипт mysql из файла.
В б/д есть таблица versions в которой находится список загруженных обновлений (версий б/д) с датой-время обновления. Что позволит 
не загружать обновления повторно (если уже они загружены) 
