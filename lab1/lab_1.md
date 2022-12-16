University: [ITMO University](https://itmo.ru/ru/) <br>
Faculty: [FICT](https://fict.itmo.ru) <br>
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies) <br>
Year: 2022/2023 <br>
Group:  K4110c <br>
Author: Usacheva Daria Dmitrievna <br>
Lab: Lab1 <br>
Date of create: 12.12.2022 <br>
Date of finished: 14.12.2022 <br><br>

<h1>Лабораторная работа №1 "Установка Docker и Minikube, мой первый манифест." <br></h1>

Для начала проверим, поддерживается ли виртуализация<br><br>
 ![lab1](imgs/2022-12-14_20-07-48.png)<br><br>
<h3>Установка minikube</h3><br><br>
Далее устанавливаем Hypervisor. В моем случае VirtualBox.<br><br>
 ![lab1](imgs/2022-12-14_20-07-48.png)<br><br>
Установка Minikube с помощью исполняемого файла установки<br><br>
 ![lab1](imgs/2022-12-14_20-07-48.png)<br><br>
Установка прошла успешно<br><br>
 ![lab1](imgs/2022-12-14_20-07-48.png)<br><br>
Чтобы убедиться в том, что гипервизор и Minikube были установлены корректно, выполним следующую команду, которая запускает локальный кластер Kubernetes:<br><br>
 ![lab1](imgs/2022-12-14_20-07-48.png)<br><br> 
Далее выполняем команду для проверки состояния кластера:<br><br>
 ![lab1](imgs/2022-12-14_20-07-48.png)<br><br>

Манифест:<br><br>
 ![lab1](imgs/2022-12-14_20-07-48.png)<br><br>
Далее устанавливаем kubectl по ссылке:<br><br>
 https://storage.googleapis.com/kubernetes-release/release/v1.26.0/bin/windows/amd64/kubectl.exe <br><br>
 
Создаем локальный minikube кластер:<br><br>
 ![lab1](imgs/2022-12-14_20-07-48.png)<br><br>
Создаем под и сервис для доступа к контейнеру vault (указываем тип сервиса NodePort и порт 8200):<br><br>
 ![lab1](imgs/2022-12-14_20-07-48.png)<br><br>
Переходим по ссылке http://localhost:8200<br><br>
 ![lab1](imgs/2022-12-14_20-07-48.png)<br><br>
Далее входим, используя токен, найденный в логах:<br><br>
minikube kubectl -- logs service/vault<br><br>
![lab1](imgs/2022-12-14_20-07-48.png)<br><br>
 
 

