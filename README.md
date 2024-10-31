# Дипломный проект: реальный кейс компании «Ростелеком Информационные Технологии»
33.1. Итоговый проект по автоматизации тестирования (PJ-04):

Выполнила: Давыдова Александра QAP-170

Ссылка на чек-лист, тест-кейсы и баг репорты:

Чек-лист, тест-кейсы, баг-репорт: https://docs.google.com/spreadsheets/d/1vdwhUa7A_SHy-B3SZBFyVxH1_h2DJ-WETpU9PMdeQGs/edit?gid=1245835669#gid=1245835669

В процессе выполнения проекта использовалось ручное тестирование в проверках юзабилити интерфейса, работы системы и адаптивности сайта на мобильном устройстве. Некоторые тест-кейсы, которые можно автоматизировать, выполнялись вручную т.к. ручная проверка позволила понять логику работы системы, четко не отраженную в брифе от заказчика. Также применялось автоматизированное тестирование с использованием Selenium WebDriver и библиотеки pytest. С помощью него проверялись часть сценариев авторизации и регистрации, которые легко поддаются автоматизации. Кроме того, автоматизированное тестирование позволило сократить время и затраты на повторное выполнение одних и тех же тест-кейсов вручную, а также повысило гибкость проверок, при внесении изменений в систему. Что касается применения техник тест-дизайна были применены следующие техники:

1. Техника классов эквивалентности

Эта техника применялась для определения наборов тестовых входных данных, которые должны привести к одинаковому поведению системы. Например, TC-RT-001, TC-RT-002, TC-RT-003 и TC-RT-004 проверяют авторизацию с различными валидными входными данными, которые должны привести к успешной авторизации.

2. Техника анализа граничных значений

Эта техника применялась для проверки граничных значений входных данных. Например, TC-RT-020, TC-RT-021 и TC-RT-022 проверяют восстановление пароля с некорректными паролями, которые не соответствуют требованиям по длине, наличию заглавных букв и использованию только латинских символов.

Автотесты имеют названия отражающие ожидаемый результат и объект тестирования.

Команда для запуска всех тестов в пакете "tests":

python -m pytest -v --driver Chrome --driver-path C:\chromedriver.exe tests

Команда для запуска отдельного теста, например, в файле test_reg_page_check.py:

python -m pytest -v --driver Chrome --driver-path C:\chromedriver.exe tests\test_reg_page_check.py -k "test_reg_page_check_all_fields_text"

В основной директории проекта файл screenshot_tests_run.png содержит скриншот терминала с результатом выполнения всех автотестов. Из 22 тестов 2 теста падают, т.к. есть сложности с многократной регистрацией в процессе отладки тестов.

Файл .env удален из индекса Git
