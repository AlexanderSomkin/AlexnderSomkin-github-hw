# Домашнее задание к занятию 10.5 «Балансировка нагрузки. HAProxy/Nginx» - Александр Сомкин.

---

### Задание 1

Что такое балансировка нагрузки и зачем она нужна? 

Балансировка нагрузки — это процесс распределения нагрузки на пул серверов.
Распределение происходит на L4 или
L7 уровнях модели OSI.

---

### Задание 2

Чем отличаются алгоритмы балансировки Round Robin и Weighted Round Robin? В каких случаях каждый из них лучше применять? 

Round Robin: Запросы распределяются по пулу
сервером последовательно.
Если в пуле все сервера
одинаковой мощности, то этот
алгоритм скорее всего подойдет
идеально.

Weighted Round Robin: Тот же round robin, но имеет
дополнительное свойство — вес
сервера. С его помощью мы можем
указать балансировщику, сколько
трафика отправлять на тот или иной
сервер. Так сервера помощнее
будут иметь больший вес
и, соответственно, обрабатывать
больше запросов, чем другие
сервера.

---

### Задание 3

Установите и запустите Haproxy.

*Приведите скриншот systemctl status haproxy, где будет видно, что Haproxy запущен.*

![alt text](https://github.com/AlexanderSomkin/srlb-homework/blob/srlb-14/Haproxy.jpg)

---

### Задание 4

Установите и запустите Nginx.

*Приведите скриншот systemctl status nginx, где будет видно, что Nginx запущен.*

![alt text](https://github.com/AlexanderSomkin/srlb-homework/blob/srlb-14/nginx1.jpg)

---

### Задание 5

Настройте Nginx на виртуальной машине таким образом, чтобы при запросе:

`curl http://localhost:8088/ping`

он возвращал в ответе строчку: 

"nginx is configured correctly".

![alt text](https://github.com/AlexanderSomkin/srlb-homework/blob/srlb-14/nginx2.jpg)

[nginx.conf](https://github.com/AlexanderSomkin/AlexnderSomkin-github-hw/blob/main/nginx.conf)
