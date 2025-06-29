---
## Front matter
lang: ru-RU
title: "Презентация по лабораторной работе №16"
subtitle: "Дисциплина: Имитационное моделирование"
author:
  - Лобанова П.И.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 15 мая 2025

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

Реализовать с помощью GPSS-модели две стратегии обслуживания и оценить оптимальные параметры.

# Задание

На пограничном контрольно-пропускном пункте транспорта имеются 2 пункта пропуска. Интервалы времени между поступлением автомобилей имеют экспоненциальное распределение со средним значением µ. Время прохождения автомобилями пограничного контроля имеет равномерное распределение на интервале [a, b]. Предлагается две стратегии обслуживания прибывающих автомобилей:

1) автомобили образуют две очереди и обслуживаются соответствующими пунктами пропуска;

2) автомобили образуют одну общую очередь и обслуживаются освободившимся пунктом пропуска.

Исходные данные: µ = 1, 75 мин, a = 1 мин, b = 7 мин.

## 

– составить модель для второй стратегии обслуживания, когда прибывающие автомобили образуют одну очередь и обслуживаются освободившимся пропускным пунктом;

– свести полученные статистики моделирования в таблицу 16.1.

– по результатам моделирования сделать вывод о наилучшей стратегии обслуживания автомобилей;

– изменив модели, определить оптимальное число пропускных пунктов (от 1 до 4) для каждой стратегии при условии, что:

    – коэффициент загрузки пропускных пунктов принадлежит интервалу [0, 5; 0, 95];

    – среднее число автомобилей, одновременно находящихся на контрольно-пропускном пункте, не должно превышать 3;

    – среднее время ожидания обслуживания не должно превышать 4 мин.

# Выполнение

![*Модель для первой стратегии с 2 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/1.png){#fig:001 width=70%}

## 

![*Отчет по модели для первой стратегии с 2 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/2.png){#fig:002 width=70%}

## 

![*Модель для второй стратегии с 2 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/3.png){#fig:003 width=70%}

## 

![*Отчет по модели для второй стратегии с 2 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/4.png){#fig:004 width=70%}

## 

![*Сравнение стратегий*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/0.png){#fig:000 width=70%}

## 

![*Модель для обеих стратегий с 1 пропускным пунктом*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/5.png){#fig:005 width=70%}

## 

![*Отчет по модели для обеих стратегий с 1 пропускным пунктом*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/6.png){#fig:006 width=70%}

## 

![*Модель для первой стратегии с 3 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/7.png){#fig:007 width=70%}

## 

![*Отчет по модели для первой стратегии с 3 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/8.png){#fig:008 width=70%}

## 

![*Модель для первой стратегии с 4 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/9.png){#fig:009 width=70%}

## 

![*Отчет по модели для первой стратегии с 4 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/10.png){#fig:010 width=70%}

## 

![*Модель для второй стратегии с 3 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/11.png){#fig:011 width=70%}

## 

![*Отчет по модели для второй стратегии с 3 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/12.png){#fig:012 width=70%}

## 

![*Модель для второй стратегии с 4 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/13.png){#fig:013 width=70%}

## 

![*Отчет по модели для второй стратегии с 4 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/14.png){#fig:014 width=70%}

# Вывод

Я реализовала с помощью GPSS-модели две стратегии обслуживания и оценить оптимальные параметры.


