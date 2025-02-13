---
## Front matter
lang: ru-RU
title: "Презентация по лабораторной работе №1"
subtitle: "Дисциплина: Имитационное моделирование"
author:
  - Лобанова П.И.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 11 февраля 2025

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
---

# Информация

## Докладчик


  * Лобанова Полина Иннокентьевна
  * Учащаяся на направлении "Фундаментальная информатика и информационные технологии"
  * Студентка группы НФИбд-02-22
  * [polla-2004@mail.ru](polla-2004@mail.ru)
  

# Цель работы

Приобретение навыков моделирования сетей передачи данных с помощью средства имитационного моделирования NS-2, а также анализ полученных результатов моделирования.

# Задание 

Создать шаблон сценария для NS-2.

# Выполнение

##

В своём рабочем каталоге создала директорию mip, к которой будут выполняться лабораторные работы. Внутри mip создала директорию lab-ns, а в ней файл shablon.tcl.

![*Создание каталогов и файла*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab1/report/лаб1/1.png){#fig:001 width=70%}

##

Сначала создала объект типа Simulator. Затем создала переменную nf и указала, что требуется открыть на запись nam-файл для регистрации выходных результатов моделирования. Далее создала переменную f и открыла на запись файл трассировки для регистрации всех событий модели. После этого добавила процедуру finish, которая закрывает файлы трассировки и запускает nam. Наконец, с помощью команды at указала планировщику событий, что процедуру finish следует запустить через 5 с после начала моделирования, после чего
запустить симулятор ns.

![*Заполнение шаблона*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab1/report/лаб1/2.png){#fig:002 width=30%}

##

Сохранив изменения в отредактированном файле shablon.tcl и закрыв его, запустила симулятор.

![*Аниматора nam*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab1/report/лаб1/4.png){#fig:004 width=40%}

# Задание

Требуется смоделировать сеть передачи данных, состоящую из двух узлов, соединённых дуплексной линией связи с полосой пропускания 2 Мб/с и задержкой 10 мс, очередью с обслуживанием типа DropTail. От одного узла к другому по протоколу UDP осуществляется передача пакетов, размером 500 байт, с постоянной скоростью 200 пакетов в секунду.

# Выполнение

##

Скопировала содержимое созданного шаблона в новый файл.

![*Копирование шаблона*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab1/report/лаб1/5.png){#fig:005 width=70%}

##

Добавила описание топологии сети. Создала агенты для генерации и приёма трафика. Далее создала Null-агент, который работает как приёмник трафика, и прикрепила его к узлу n1. Соединила агенты между собой. Для запуска и остановки приложения CBR добавляются at-события в планировщик событий. 

![*Заполнение файла*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab1/report/лаб1/6.png){#fig:006 width=40%}

##

Сохранила изменения в отредактированном файле и запустила симулятор. 

![*Аниматора nam*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab1/report/лаб1/8.png){#fig:008 width=40%}

# Задание 

Описание моделируемой сети:
– сеть состоит из 4 узлов (n0, n1, n2, n3);

– между узлами n0 и n2, n1 и n2 установлено дуплексное соединение с пропускной
способностью 2 Мбит/с и задержкой 10 мс;

– между узлами n2 и n3 установлено дуплексное соединение с пропускной способностью 1,7 Мбит/с и задержкой 20 мс;

– каждый узел использует очередь с дисциплиной DropTail для накопления пакетов,
максимальный размер которой составляет 10;

– TCP-источник на узле n0 подключается к TCP-приёмнику на узле n3

– TCP-приёмник генерирует и отправляет ACK пакеты отправителю и откидывает
полученные пакеты;

##

– UDP-агент, который подсоединён к узлу n1, подключён к null-агенту на узле n3
(null-агент просто откидывает пакеты);

– генераторы трафика ftp и cbr прикреплены к TCP и UDP агентам соответственно;

– генератор cbr генерирует пакеты размером 1 Кбайт со скоростью 1 Мбит/с;

– работа cbr начинается в 0,1 секунду и прекращается в 4,5 секунды, а ftp начинает
работать в 1,0 секунду и прекращает в 4,0 секунды.

# Выполнение 

##

Скопировала содержимое созданного шаблона в новый файл.

![*Копирование шаблона*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab1/report/лаб1/9.png){#fig:009 width=70%}

##

Создала 4 узла и 3 дуплексных соединения с указанием направления. Создала агент UDP с прикреплённым к нему источником CBR и агент TCP с прикреплённым к нему приложением FTP. Создала агенты-получатели. Соединила агенты udp0 и tcp1 и их получателей. Задала описание цвета каждого потока. Добавила отслеживание событий в очереди, наложение ограничения на размер очереди и at-события. 

![*Заполнение файла*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab1/report/лаб1/10.png){#fig:010 width=30%}

##

Сохранив изменения в отредактированном файле и запустив симулятор, получила анимированный результат моделирования.

![*Аниматора nam*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab1/report/лаб1/12.png){#fig:012 width=40%}

# Задание 

Требуется построить модель передачи данных по сети с кольцевой топологией и динамической маршрутизацией пакетов:
– сеть состоит из 7 узлов, соединённых в кольцо;

– данные передаются от узла n(0) к узлу n(3) по кратчайшему пути;

– с 1 по 2 секунду модельного времени происходит разрыв соединения между узлами n(1) и n(2);

– при разрыве соединения маршрут передачи данных должен измениться на резервный.

# Выполнение 

##

Скопировала содержимое созданного шаблона в новый файл.

![*Копирование шаблона*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab1/report/лаб1/13.png){#fig:013 width=70%}

##

Описала топологию моделируемой сети. Далее соединила узлы так, чтобы создать круговую топологию. Задала передачу данных от узла n(0) к узлу n(3). Добавила команду разрыва соединения между узлами n(1) и n(2) на время в одну секунду, а также время начала и окончания передачи данных. Добавила в начало скрипта после команды создания объекта Simulator: $ns rtproto DV.

![*Заполнение файла*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab1/report/лаб1/14.png){#fig:014 width=30%}

##

Сохранив изменения в отредактированном файле и запустив симулятор, получила анимированный результат моделирования.

![*Передача данных по кратчайшему пути*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab1/report/лаб1/15.png){#fig:015 width=40%}

##

![*Прерывание соезинения*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab1/report/лаб1/16.png){#fig:016 width=50%}

##

![*Передача данных по резервному маршруту*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab1/report/лаб1/17.png){#fig:017 width=50%}

# Задание 

Внесите следующие изменения в реализацию примера с кольцевой
топологией сети:

– передача данных должна осуществляться от узла n(0) до узла n(5) по кратчайшему пути в течение 5 секунд модельного времени;

– передача данных должна идти по протоколу TCP (тип Newreno), на принимающей стороне используется TCPSink-объект типа DelAck; поверх TCP работает протокол FTP с 0,5 до 4,5 секунд модельного времени;

– с 1 по 2 секунду модельного времени происходит разрыв соединения между узлами n(0) и n(1);

– при разрыве соединения маршрут передачи данных должен измениться на резервный, после восстановления соединения пакеты снова должны пойти по кратчайшему пути.

# Выполнение 

##

Скопировала содержимое созданного шаблона в новый файл.

![*Копирование шаблона*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab1/report/лаб1/18.png){#fig:018 width=70%}

##

Создала 5 узлов и соединила их так, чтобы создать круговую топологию. Создала еще один узел(n(5)) и соединила его с узлом n(1). Задала передачу данных от узла n(0) к узлу n(5). Создала агент TCP (тип Newreno) с прикреплённым к нему приложением FTP. Создала агент-получатель (TCPSink-объект типа DelAck). Соединила агент tcp1 и его получателя. Добавила команду разрыва соединения между узлами n(0) и n(1) на время в одну секунду, а также время начала и окончания передачи данных. Добавила в начало скрипта после команды создания объекта Simulator: $ns rtproto DV. 

![*Заполнение файла*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab1/report/лаб1/19.png){#fig:019 width=25%}

##

Сохранив изменения в отредактированном файле и запустив симулятор, получила анимированный результат моделирования.

![*Передача данных по кратчайшему пути*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab1/report/лаб1/22.png){#fig:022 width=50%}

##

![*Прерывание соезинения*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab1/report/лаб1/23.png){#fig:023 width=50%}

##

![*Передача данных по резервному маршруту*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab1/report/лаб1/24.png){#fig:024 width=50%}

# Вывод 

Я приобрела навыки моделирования сетей передачи данных с помощью средства имитационного моделирования NS-2, а также анализ полученных результатов моделирования. 

