University: [ITMO University](https://itmo.ru/ru/) <br>
Faculty: [FICT](https://fict.itmo.ru) <br>
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies) <br>
Year: 2022/2023 <br>
Group:  K4110c <br>
Author: Usacheva Daria Dmitrievna <br>
Lab: Lab3 <br>
Date of create: 12.12.2022 <br>
Date of finished: 14.12.2022 <br><br>

<h1>Лабораторная работа №3 "Сертификаты и "секреты" в Minikube, безопасное хранение данных."<br></h1>

Создадим новый namespace lab3:<br><br>

 ![lab1_1](imgs/2022-12-15_04-34-03.png)<br><br>
 
Манифест configmap:<br><br>

 ![lab1_1](imgs/2022-12-15_04-34-56.png)<br><br>
 
Манифест для развертывания приложения:<br><br>

 ![lab1_1](imgs/2022-12-15_04-47-59.png)<br><br>
 
Манифест service.yaml для доступа к подам приложения<br><br>

 ![lab1_1](imgs/2022-12-15_04-48-40.png)<br><br>
 
Создадим ConfigMap, ReplicaSet и Service:<br><br>

 ![lab1_1](imgs/2022-12-15_04-45-26.png)<br><br>
 
<h3>Развертывание ingress-controller и создание TLS сертификата</h3>
Nginx Ingress controller:<br><br>

 ![lab1_1](imgs/2022-12-15_04-52-36.png)<br><br>
 
После развертывания в неймспейсе ingress-nginx появился сервис типа LoadBalancer - ingress-nginx-controller<br><br>

 ![lab1_1](imgs/2022-12-15_04-53-42.png)<br><br> 

Перед генерацией TLS-сертификата скачаем mkcert с помощью Chocolatey:<br><br>

 ![lab1_1](imgs/2022-12-15_05-14-18.png)<br><br>
 
Генерация сертификата с помощью утилиты mkcert:<br><br>

 ![lab1_1](imgs/2022-12-15_05-18-29.png)<br><br>
 
Далее с помощью команды *kubectl create secret tls tls-cert --key key.pem --cert cert.pem -n lab3*
Импортируем TLS-сертификат в кластер как Secret.
Создаем Ingress в minikube:<br><br>

 ![lab1_1](imgs/2022-12-15_05-50-11.png)<br><br>
 
 ![lab1_1](imgs/2022-12-15_05-49-08.png)<br><br>
 
 
Чтобы приложение dori3 было доступно по FQDN на хосте, необходимо внести изменения в файл hosts, добавив следующую строку: 127.0.0.1 dori3.usacheva.com<br>
После этого его можно открыть по адресу https:// dori3.usacheva.com/ и увидеть интерфейс, схожий с представленным в лабораторной работе №2
