# Домашнее задание к занятию 2 «Кластеризация и балансировка нагрузки» Шарапат Виктор

### Задание 1
- Запустите два simple python сервера на своей виртуальной машине на разных портах
- Установите и настройте HAProxy, воспользуйтесь материалами к лекции по [ссылке](2/)
- Настройте балансировку Round-robin на 4 уровне.
- На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy.
### Решение 1:
![alt text](https://github.com/sharvik22/2md/blob/main/images/1-1.png)
![alt text](https://github.com/sharvik22/2md/blob/main/images/1-2.png)
![alt text](https://github.com/sharvik22/2md/blob/main/images/1-3.png)
![alt text](https://github.com/sharvik22/2md/blob/main/images/1-4.png)
![alt text](https://github.com/sharvik22/2md/blob/main/images/1-5.png)

[ссылка на конфигурационный файл haproxy] (https://github.com/sharvik22/2md/blob/main/haproxy-1.cfg)
---
### Задание 2
- Запустите три simple python сервера на своей виртуальной машине на разных портах
- Настройте балансировку Weighted Round Robin на 7 уровне, чтобы первый сервер имел вес 2, второй - 3, а третий - 4
- HAproxy должен балансировать только тот http-трафик, который адресован домену example.local
- На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy c использованием домена example.local и без него.
### Решение 2:
![alt text](https://github.com/sharvik22/2md/blob/main/images/2-1.png)
![alt text](https://github.com/sharvik22/2md/blob/main/images/2-2.png)
![alt text](https://github.com/sharvik22/2md/blob/main/images/2-3.png)

[ссылка на конфигурационный файл haproxy] ([haproxy-2.cfg](https://github.com/sharvik22/2md/blob/main/haproxy-2.cfg))

---

## Задания со звёздочкой*
Эти задания дополнительные. Их можно не выполнять. На зачёт это не повлияет. Вы можете их выполнить, если хотите глубже разобраться в материале.

---

### Задание 3*
- Настройте связку HAProxy + Nginx как было показано на лекции.
- Настройте Nginx так, чтобы файлы .jpg выдавались самим Nginx (предварительно разместите несколько тестовых картинок в директории /var/www/), а остальные запросы переадресовывались на HAProxy, который в свою очередь переадресовывал их на два Simple Python server.
- На проверку направьте конфигурационные файлы nginx, HAProxy, скриншоты с запросами jpg картинок и других файлов на Simple Python Server, демонстрирующие корректную настройку.

---

### Задание 4*
- Запустите 4 simple python сервера на разных портах.
- Первые два сервера будут выдавать страницу index.html вашего сайта example1.local (в файле index.html напишите example1.local)
- Вторые два сервера будут выдавать страницу index.html вашего сайта example2.local (в файле index.html напишите example2.local)
- Настройте два бэкенда HAProxy
- Настройте фронтенд HAProxy так, чтобы в зависимости от запрашиваемого сайта example1.local или example2.local запросы перенаправлялись на разные бэкенды HAProxy
- На проверку направьте конфигурационный файл HAProxy, скриншоты, демонстрирующие запросы к разным фронтендам и ответам от разных бэкендов.
