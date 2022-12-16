University: [ITMO University](https://itmo.ru/ru/) <br>
Faculty: [FICT](https://fict.itmo.ru) <br>
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies) <br>
Year: 2022/2023 <br>
Group:  K4110c <br>
Author: Usacheva Daria Dmitrievna <br>
Lab: Lab2 <br>
Date of create: 12.12.2022 <br>
Date of finished: 14.12.2022 <br><br>

<h1>Лабораторная работа №2 "Развертывание веб сервиса в Minikube, доступ к веб интерфейсу сервиса. Мониторинг сервиса."</h1><br><br>

<h3>Deployment</h3><br><br>
Создадим новый namespace lab2 <br><br>

![lab1_1](imgs/2022-12-15_02-36-18.png)<br><br> 
 
Далее создадим манифест для развертывания приложения<br><br>

![lab1_1](imgs/2022-12-15_02-42-53.png)<br><br>

![lab1_1](imgs/2022-12-15_02-44-44.png)<br><br>

Далее видно, что deployment создал новый объект, который, в свою очередь, создал необходимое количество реплик приложений.<br><br>

![lab1_1](imgs/2022-12-15_02-46-14.png)<br><br>

<h3>Создание сервиса</h3><br><br>
Манифест svc.yaml для предоставления доступа к подам деплоймента:<br><br>

![lab1_1](imgs/2022-12-15_02-55-47.png)<br><br>
 
Создание сервиса:<br><br>

![lab1_1](imgs/2022-12-15_03-01-41.png)<br><br>
 
IP-адреса совпадают подов деплоймента совпадают адресами подов, на которые сервис будет проксировать трафик.<br><br>

![lab1_1](imgs/2022-12-15_03-07-12.png)<br><br>
 
<h3>Тестирование</h3><br><br>
Получаем доступ к сервису.
Переходим на http://localhost:3000 и проверяем:<br><br>

![lab1_1](imgs/2022-12-15_03-46-08.png)<br><br>


Логи контейнеров:<br><br>

![lab1_1](imgs/2022-12-15_03-31-22.png)<br><br>
![lab1_1](imgs/2022-12-15_03-32-16.png)<br><br>
 
 


