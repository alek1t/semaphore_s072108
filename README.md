semaphore_s072108
=========

Роль для установки и настройки Semaphore на ОС Alma Linux 8, включая дополнительные компоненты:
- БД PostgreSQL
- Реверс-прокси NGINX

Requirements
------------

Предустановленные компоненты не требуются

Role Variables
--------------

Переменные описаны в файле defaults/main.yml

Dependencies
------------

Зависимости от других ролей из Ansible-Galaxy нет.

Example Playbook
----------------

    - hosts: servers
      roles:
         - semaphore_s072108

License
-------

Free (No license)

Author Information
------------------

s072108
