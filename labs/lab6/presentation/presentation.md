---
## Front matter
lang: ru-RU
title: "Презентация по лабораторной работе №6"
subtitle: "Дисциплина: Имитационное моделирование"
author:
  - Лобанова П.И.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 10 марта 2025

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

Реализовать модель «хищник–жертва» в xcos,  с помощью блока Modelica в xcos и  в OpenModelica.

![](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/20.png){#fig:001 width=70%}

# Выполнение 

Зафиксировала начальные данные: a = 2, b = 1, c = 0, 3, d = 1.

![*Значения коэффициентов a, b, c, d*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/1.png){#fig:001 width=50%}

## 

Используя блоки CLOCK_c, CSCOPE, TEXT_f, MUX, INTEGRAL_m, GAINBLK_f, SUMMATION, PROD_f и CSCOPXY, создала модель «хищник–жертва» в xcos.

![*Модель «хищник–жертва» в xcos*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/2.png){#fig:002 width=50%}

## 

В параметрах блоков интегрирования задала начальные значения x(0) = 2, y(0) = 1.

![*Начальные значения в блоках интегрирования*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/3.png){#fig:003 width=70%}


## 

![*Конечное время интегрирования*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/5.png){#fig:005 width=70%}

## 

![*Динамика изменения численности хищников и жертв*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/8.png){#fig:008 width=70%}

## 

![*Фазовый портрет модели*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/9.png){#fig:009 width=70%}

## 

![*Модель «хищник–жертва» в xcos с применением блока Modelica*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/11.png){#fig:011 width=70%}

## 

![*Параметры блока Modelica*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/12.png){#fig:012 width=70%}

## 

![*Параметры блока Modelica*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/13.png){#fig:013 width=70%}

## 

![*Динамика изменения численности хищников и жертв*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/14.png){#fig:014 width=70%}

## 

![*Фазовый портрет модели*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/15.png){#fig:015 width=70%}

## 

![*Код для реализации модели*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/16.png){#fig:016 width=70%}

##

![*Динамика изменения численности хищников и жертв*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/18.png){#fig:018 width=70%}

## 

![*Фазовый портрет модели*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/19.png){#fig:019 width=70%}

# Вывод

Я реализовала модель «хищник–жертва» в xcos,  с помощью блока Modelica в xcos и  в OpenModelica.

