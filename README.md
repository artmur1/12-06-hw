# Домашнее задание к занятию "`Репликация и масштабирование. Часть 1`" - `Мурчин Артем`

### Задание 1

На лекции рассматривались режимы репликации master-slave, master-master, опишите их различия.

*Ответить в свободной форме.*

### Решение 1

В Master-Master репликация настроена как в обычной Master-Slave, но только в обе стороны. Каждый сервер является мастером и слейвом одновременно. Конфигурация master-master добавляет избыточность и повышает эффективность при обращении к данным.

### Задание 2

Выполните конфигурацию master-slave репликации, примером можно пользоваться из лекции.

*Приложите скриншоты конфигурации, выполнения работы: состояния и режимы работы серверов.*

### Решение 2

![alt text](https://github.com/artmur1/12-06-hw/blob/main/hw-12-06-zad2-1.png)

Поднял контейнеры mysql master и slave в docker.

![alt text](https://github.com/artmur1/12-06-hw/blob/main/hw-12-06-zad2-2.png)

Статус mysql-master. Создал пользователя и задал права. И снова статус mysql master.

![alt text](https://github.com/artmur1/12-06-hw/blob/main/hw-12-06-zad2-3.png)

Прописал на mysql-slave данные для подключения slave к мастер: хост, пользователь, пароль, файл и пос. Статус mysql-slave.

![alt text](https://github.com/artmur1/12-06-hw/blob/main/hw-12-06-zad2-4.png)

Статус mysql-slave (продолжение).

![alt text](https://github.com/artmur1/12-06-hw/blob/main/hw-12-06-zad2-5.png)

На mysql-master создал БД с таблицей.

![alt text](https://github.com/artmur1/12-06-hw/blob/main/hw-12-06-zad2-6.png)

На mysql-slave как вновь созданная БД с таблицей на master была реплицирована на slave.

## Дополнительные задания (со звёздочкой*)
Эти задания дополнительные, то есть не обязательные к выполнению, и никак не повлияют на получение вами зачёта по этому домашнему заданию. Вы можете их выполнить, если хотите глубже шире разобраться в материале.

---

### Задание 3* 

Выполните конфигурацию master-master репликации. Произведите проверку.

*Приложите скриншоты конфигурации, выполнения работы: состояния и режимы работы серверов.*
