---
## Front matter
lang: ru-RU
title: "Презентация по лабораторной работе №9"
subtitle: "Дисциплина: Имитационное моделирование"
author:
  - Лобанова П.И.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 31 марта 2025

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

Реализовать модель «Накорми студентов».

# Задание

Рассмотрим пример студентов, обедающих пирогами. Голодный студент становится сытым после того, как съедает пирог.
Таким образом, имеем:

– два типа фишек: «пироги» и «студенты»;

– три позиции: «голодный студент», «пирожки», «сытый студент»;

– один переход: «съесть пирожок».

1. Реализовать модель.

2. Вычислите пространство состояний. Сформируйте отчёт о пространстве состояний и проанализируйте его. Постройте граф пространства состояний.

# Выполнение

![*Граф сети модели «Накорми студентов»*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab9/report/image/1.png){#fig:001 width=70%}

## 

![*Задание деклараций модели «Накорми студентов»*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab9/report/image/2.png){#fig:002 width=70%}

## 

![*Задание типа фишкам и значений переменных*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab9/report/image/3.png){#fig:003 width=70%}

## 

![*Задание начальных значений*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab9/report/image/4.png){#fig:004 width=70%}

## 

![*Запуск модели «Накорми студентов»*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab9/report/image/5.png){#fig:005 width=70%}

## 

![*Отчет о пространстве состояний*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab9/report/image/6.png){#fig:006 width=70%}

## 

![*Граф пространства состояний*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab9/report/image/7.png){#fig:007 width=70%}

# Вывод

Я реализовала модель «Накорми студентов».

