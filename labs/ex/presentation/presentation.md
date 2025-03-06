---
## Front matter
lang: ru-RU
title: "Презентация по упражнению"
subtitle: "Дисциплина: Имитационное моделирование"
author:
  - Лобанова П.И.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 6 марта 2025

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

Выполнить построение фигуры Лиссажу с разными параметрами.

# Задание 

Постройте с помощью xcos фигуры Лиссажу со следующими параметрами:

1) A = B = 1, a = 2, b = 2, б = 0; π/4; π/2; 3π/4; π;

2) A = B = 1, a = 2, b = 4, б = 0; π/4; π/2; 3π/4; π;

3) A = B = 1, a = 2, b = 6, б = 0; π/4; π/2; 3π/4; π;

4) A = B = 1, a = 2, b = 3, б = 0; π/4; π/2; 3π/4; π.

![](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/пр.png){#fig:001 width=50%}

# Выполнение 

Создала модель в xcos, используя блоки CLOCK_c, GENSIN_f, TEXT_f, CSOPXY.

![*Схема модели*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/1.png){#fig:001 width=50%}

## 

Задала параметры: A = B = 1, a = 2, b = 2, б = π/2, а также параметры регистрирующего устройства.

![*Изменения параметров*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/2.png){#fig:002 width=70%}

## 

![*Изменения параметров*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/4.png){#fig:004 width=70%}

## 

![*График с параметрами A = B = 1, a = 2, b = 2, б = π/2*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/5.png){#fig:005 width=70%}

## 

![*График с параметрами A = B = 1, a = 2, b = 2, б = 0*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/7.png){#fig:006 width=70%}

## 

![*График с параметрами A = B = 1, a = 2, b = 2, б = π/4*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/9.png){#fig:007 width=70%}

## 

![*График с параметрами A = B = 1, a = 2, b = 2, б = 3π/4*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/11.png){#fig:008 width=70%}

## 

![*График с параметрами A = B = 1, a = 2, b = 2, б = π*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/13.png){#fig:009 width=70%}

## 

![*График с параметрами A = B = 1, a = 2, b = 4, б = 0*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/15.png){#fig:010 width=70%}

## 

![*График с параметрами A = B = 1, a = 2, b = 4, б = π/4*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/17.png){#fig:011 width=70%}

## 

![*График с параметрами A = B = 1, a = 2, b = 4, б = π/2*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/19.png){#fig:012 width=70%}

## 

![*График с параметрами A = B = 1, a = 2, b = 4, б = 3π/4*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/21.png){#fig:013 width=70%}

## 

![*График с параметрами A = B = 1, a = 2, b = 4, б = π*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/23.png){#fig:014 width=70%}

## 

![*График с параметрами A = B = 1, a = 2, b = 6, б = 0*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/25.png){#fig:015 width=70%}

## 

![*График с параметрами A = B = 1, a = 2, b = 6, б = π/4*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/27.png){#fig:016 width=70%}

## 

![*График с параметрами A = B = 1, a = 2, b = 6, б = π/2*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/29.png){#fig:017 width=70%}

## 

![*График с параметрами A = B = 1, a = 2, b = 6, б = 3π/4*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/31.png){#fig:018 width=70%}

## 

![*График с параметрами A = B = 1, a = 2, b = 6, б = π*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/33.png){#fig:019 width=70%}

## 

![*График с параметрами A = B = 1, a = 2, b = 3, б = 0*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/35.png){#fig:020 width=70%}

## 

![*График с параметрами A = B = 1, a = 2, b = 3, б = π/4*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/37.png){#fig:021 width=70%}

## 

![*График с параметрами A = B = 1, a = 2, b = 3, б = π/2*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/39.png){#fig:022 width=70%}

## 

![*График с параметрами A = B = 1, a = 2, b = 3, б = 3π/4*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/41.png){#fig:023 width=70%}

## 

![*График с параметрами A = B = 1, a = 2, b = 3, б = π*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/43.png){#fig:024 width=70%}

# Вывод 

Я выполнила построение фигуры Лиссажу с разными параметрами.


