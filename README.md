# Установка и настройка веб-сервера

## Стек

+ Nginx
+ php-fpm
+ MySQL
+ MongoDB
+ Memcached


## Использование
Запустить виртуалку через Vagrant

```
$ vagrant up
```

Запуск плейбука Ansible

```
$ ansible-playbook -i hosts playbook.yml -kK
```

Vagrant боксы: https://vagrantcloud.com/discover/featured