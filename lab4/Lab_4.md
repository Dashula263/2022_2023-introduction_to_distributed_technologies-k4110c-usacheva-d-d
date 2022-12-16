University: [ITMO University](https://itmo.ru/ru/) <br>
Faculty: [FICT](https://fict.itmo.ru) <br>
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies) <br>
Year: 2022/2023 <br>
Group:  K4110c <br>
Author: Usacheva Daria Dmitrievna <br>
Lab: Lab4 <br>
Date of create: 12.12.2022 <br>
Date of finished: 14.12.2022 <br><br>

<h1>Лабораторная работа №4 "Сети связи в Minikube, CNI и CoreDNS" </h1><br>

Разворачиваем minikube cluster:

![lab1_1](imgs/2022-12-15_14-35-15.png)<br><br>
 
Проверим ноды:

![lab1_1](imgs/2022-12-15_14-35-31.png)<br><br>
 
И их статус:

![lab1_1](imgs/2022-12-15_14-36-51.png)<br><br>
 
Создадим calico pod:

![lab1_1](imgs/2022-12-15_14-43-56.png)<br><br>
 
Удаляем дефолтный pool:

![lab1_1](imgs/2022-12-15_14-51-26.png)<br><br>
 
Добавим label:

![lab1_1](imgs/2022-12-15_14-52-26.png)<br><br>
 
Манифест Ip-Pool:

![lab1_1](imgs/2022-12-15_14-55-32.png)<br><br>
 
Далее создадим IP-Pool

![lab1_1](imgs/2022-12-15_14-56-33.png)<br><br>
 
Проверяем:

![lab1_1](imgs/2022-12-15_14-57-01.png)<br><br>
 
Создаем configMap:

![lab1_1](imgs/2022-12-15_14-59-51.png)<br><br>

![lab1_1](imgs/2022-12-15_15-00-04.png)<br><br>
 
Создаем ReplicaSet:

![lab1_1](imgs/2022-12-15_15-05-05.png)<br><br>

![lab1_1](imgs/2022-12-15_15-06-21.png)<br><br> 
 
Далее создаем сервис:

![lab1_1](imgs/2022-12-15_15-07-54.png)<br><br>

![lab1_1](imgs/2022-12-15_15-08-32.png)<br><br>

![lab1_1](imgs/2022-12-15_15-10-08.png)<br><br>

![lab1_1](imgs/2022-12-15_15-11-36.png)<br><br>
 
 
Пропингуем поды:

![lab1_1](imgs/2022-12-15_15-42-54.png)<br><br>
