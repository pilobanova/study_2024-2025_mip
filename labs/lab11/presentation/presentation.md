---
## Front matter
lang: ru-RU
title: "Презентация по лабораторной работе №11"
subtitle: "Дисциплина: Имитационное моделирование"
author:
  - Лобанова П.И.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 10 апреля 2025

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
  

# Цель

Реализовать модель системы массового обслуживания M|M|1.

# Задание

В систему поступает поток заявок двух типов, распределённый по пуассоновскому закону. Заявки поступают в очередь сервера на обработку. Дисциплина очереди - FIFO. Если сервер находится в режиме ожидания (нет заявок на сервере), то заявка поступает на обработку сервером.

# Выполнение

![*Граф сети системы обработки заявок в очереди*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/1.png){#fig:001 width=60%}

## 

![*Граф генератора заявок системы*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/2.png){#fig:002 width=70%}

## 

![*Граф процесса обработки заявок на сервере системы*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/3.png){#fig:003 width=70%}

## 

![*Задание деклараций*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/4.png){#fig:004 width=70%}

## 

![*Параметры элементов основного графа системы обработки заявок в очереди*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/5.png){#fig:005 width=70%}

## 

![*Параметры элементов генератора заявок системы*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/6.png){#fig:006 width=70%}

## 

![*Параметры элементов обработчика заявок системы*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/7.png){#fig:007 width=70%}

## 

Для мониторинга параметров очереди системы M|M|1 потребовалась палитра Monitoring. Выбрала Break Point (точка останова) и установила её на переход Start.

![*Функция Predicate монитора Ostanovka*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/9.png){#fig:008 width=70%}

## 

Далее необходимо было определить конструкцию Queue_Delay.count(). С помощью палитры Monitoring выбрала Data Call и установила на переходе Start.

![*Функция Observer монитора Queue Delay*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/10.png){#fig:009 width=70%}

## 

После запуска программы на выполнение в каталоге с кодом программы появился файл Queue_Delay.log, содержащий в первой колонке — значение задержки очереди, во второй — счётчик, в третьей — шаг, в четвёртой — время.

![*График изменения задержки в очереди*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/12.png){#fig:011 width=50%}

## 

Посчитала задержку в действительных значениях.

![*Функция Observer монитора Queue Delay Real*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/13.png){#fig:012 width=70%}

## 

Посчитала, сколько раз задержка превысила заданное значение.

![*Функция Observer монитора Long Delay Time*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/14.png){#fig:013 width=70%}

## 

![*Периоды времени, когда значения задержки в очереди превышали заданное значение*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/15.png){#fig:014 width=70%}

# Вывод

Я реализовала модель системы массового обслуживания M|M|1.


