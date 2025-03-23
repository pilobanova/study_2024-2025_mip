---
## Front matter
lang: ru-RU
title: "Презентация по лабораторной работе №8"
subtitle: "Дисциплина: Имитационное моделирование"
author:
  - Лобанова П.И.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 23 марта 2025

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

Реализовать модель TCP/AQM в xcos и с использованием языка Modelica в среде OpenModelica.

# Задание 

1. Построить схему модели в xcos.

2. Построить график динамики изменения размера TCP окна W(t) и размера очереди Q(t) и фазовый портрет (W, Q). 

3. Реализовать модель с использованием языка Modelica в среде OpenModelica. Для реализации задержки используйте оператор delay(). Постройте график динамики изменения размера TCP окна W(t) и размера очереди Q(t)
и фазовый портрет (W, Q).

# Выполнение

![*Установка начальных значений*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab8/report/image/1.png){#fig:001 width=70%}

## 

![*Схема xcos, моделирующая систему*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab8/report/image/2.png){#fig:002 width=70%}

## 

![*Динамика изменения размера TCP окна W(t) и размера очереди Q(t)*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab8/report/image/3.png){#fig:003 width=70%}

## 

![*Фазовый портрет (W, Q)*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab8/report/image/4.png){#fig:004 width=70%}

## 

![*Изменение параметра*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab8/report/image/5.png){#fig:005 width=70%}

## 

![*Динамика изменения размера TCP окна W(t) и размера очереди Q(t) при C = 0, 9*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab8/report/image/6.png){#fig:006 width=70%}

## 

![*Фазовый портрет (W, Q) при C = 0, 9*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab8/report/image/7.png){#fig:007 width=70%}

## 

![*Программа для реализации модели*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab8/report/image/8.png){#fig:008 width=70%}

## 

![*Динамика изменения размера TCP окна W(t) и размера очереди Q(t)*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab8/report/image/9.png){#fig:009 width=70%}

## 

![*Фазовый портрет (W, Q)*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab8/report/image/10.png){#fig:010 width=70%}

# Вывод

Я реализовала модель TCP/AQM в xcos и с использованием языка Modelica в среде OpenModelica.
