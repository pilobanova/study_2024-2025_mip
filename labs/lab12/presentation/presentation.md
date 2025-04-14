---
## Front matter
lang: ru-RU
title: "Презентация по лабораторной работе №12"
subtitle: "Дисциплина: Имитационное моделирование"
author:
  - Лобанова П.И.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 14 апреля 2025

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

Выполнить пример моделирования простого протокола передачи данных.

# Задание

Рассмотрим ненадёжную сеть передачи данных, состоящую из источника, получателя.
Перед отправкой очередной порции данных источник должен получить от получателя подтверждение о доставке предыдущей порции данных.
Считаем, что пакет состоит из номера пакета и строковых данных. Передавать будем сообщение «Modelling and Analysis by Means of Coloured Petry Nets», разбитое по 8 символов.

# Выполнение

![*Начальный граф*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab12/report/image/1.png){#fig:001 width=60%}

## 

![*Декларации*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab12/report/image/2.png){#fig:002 width=70%}

## 

![*Добавление промежуточных состояний*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab12/report/image/3.png){#fig:003 width=70%}

## 

![*Декларации*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab12/report/image/4.png){#fig:004 width=70%}

## 

![*Модель простого протокола передачи данных*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab12/report/image/5.png){#fig:005 width=70%}

## 

![*Отчёт о пространстве состояний*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab12/report/image/6.png){#fig:006 width=70%}

##

![*Граф пространства состояний*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab12/report/image/9.png){#fig:009 width=70%}


# Вывод

Я выполнила пример моделирования простого протокола передачи данных.

