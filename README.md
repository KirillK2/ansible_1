# ansible_1

Результат выполнения сценария доступна страница по адресу http://ip_host/ с текстом "DevOps Course 2021"

Условия для запуска playbook на агенте: ОС ubuntu, Open SSH сервер, пакет: python-apt.

Пункты выполняемые в playbook:
1. установка последней версии nginx используя пакетный менеджер apt.
2. запуск и активация сервиса nginx
3. копирование конфигов для активации нового сайта на 80 порту.
4. создание папки tutorial для статичского отображения 
5. копирование конфигов для изменения порта для сайта по умолчанию.
6. копирование нового сайта index.html.

Подробнее о подключении и работе на агенте:
1. подключение к агенту производится с помощью служебной учетной записи ansible_servce и наличием публичного ключа.
2. в inventory описана группа хостов app.

Запуск:
sudo ansible-playbook -i inventory playbook_ii_nginx.yml
