---
## Front matter
title: "Отчет по лабораторной работе №16"
subtitle: "Дисциплина: Имитационное моделирование"
author: "Лобанова Полина Иннокентьевна"


## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Реализовать с помощью GPSS-модели две стратегии обслуживания и оценить оптимальные параметры.

# Задание

На пограничном контрольно-пропускном пункте транспорта имеются 2 пункта пропуска. Интервалы времени между поступлением автомобилей имеют экспоненциальное распределение со средним значением µ. Время прохождения автомобилями пограничного контроля имеет равномерное распределение на интервале [a, b]. Предлагается две стратегии обслуживания прибывающих автомобилей:

1) автомобили образуют две очереди и обслуживаются соответствующими пунктами пропуска;

2) автомобили образуют одну общую очередь и обслуживаются освободившимся пунктом пропуска.

Исходные данные: µ = 1, 75 мин, a = 1 мин, b = 7 мин.

– составить модель для второй стратегии обслуживания, когда прибывающие автомобили образуют одну очередь и обслуживаются освободившимся пропускным пунктом;

– свести полученные статистики моделирования в таблицу 16.1.

– по результатам моделирования сделать вывод о наилучшей стратегии обслуживания автомобилей;

– изменив модели, определить оптимальное число пропускных пунктов (от 1 до 4) для каждой стратегии при условии, что:

    – коэффициент загрузки пропускных пунктов принадлежит интервалу [0, 5; 0, 95];

    – среднее число автомобилей, одновременно находящихся на контрольно-пропускном пункте, не должно превышать 3;

    – среднее время ожидания обслуживания не должно превышать 4 мин.


# Выполнение лабораторной работы

1. Построила модель для первой стратегии обслуживания, когда прибывающие автомобили образуют две очереди и обслуживаются соответствующими пропускными пунктами.

![*Модель для первой стратегии с 2 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/1.png){#fig:001 width=70%}

![*Отчет по модели для первой стратегии с 2 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/2.png){#fig:002 width=70%}

2. Построила модель для второй стратегии обслуживания, когда прибывающие автомобили образуют одну очередь и обслуживаются освободившимся пропускным пунктом.

![*Модель для второй стратегии с 2 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/3.png){#fig:003 width=70%}

![*Отчет по модели для второй стратегии с 2 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/4.png){#fig:004 width=70%}

3. Сравнила две стратегии обслуживания, используя следующие критерии:

– коэффициенты загрузки системы;

– максимальные и средние длины очередей;

– средние значения времени ожидания обслуживания.

![*Сравнение стратегий*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/0.png){#fig:000 width=70%}

4. Построила модель для первой стратегии обслуживания при 1 пропускном пункте (она совпадает со второй).

![*Модель для обеих стратегий с 1 пропускным пунктом*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/5.png){#fig:005 width=70%}

![*Отчет по модели для обеих стратегий с 1 пропускным пунктом*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/6.png){#fig:006 width=70%}

5. Построила модель для первой стратегии обслуживания при 3 пропускных пунктах.

![*Модель для первой стратегии с 3 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/7.png){#fig:007 width=70%}

![*Отчет по модели для первой стратегии с 3 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/8.png){#fig:008 width=70%}

6. Построила модель для первой стратегии обслуживания при 4 пропускных пунктах.

![*Модель для первой стратегии с 4 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/9.png){#fig:009 width=70%}

![*Отчет по модели для первой стратегии с 4 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/10.png){#fig:010 width=70%}

7. Построила модель для второй стратегии обслуживания при 3 пропускных пунктах.

![*Модель для второй стратегии с 3 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/11.png){#fig:011 width=70%}

![*Отчет по модели для второй стратегии с 3 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/12.png){#fig:012 width=70%}

8. Построила модель для второй стратегии обслуживания при 4 пропускных пунктах.

![*Модель для второй стратегии с 4 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/13.png){#fig:013 width=70%}

![*Отчет по модели для второй стратегии с 4 пропускными пунктами*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab16/report/image/14.png){#fig:014 width=70%}

# Выводы

Я реализовала с помощью GPSS-модели две стратегии обслуживания и оценить оптимальные параметры.

# Список литературы{.unnumbered}

::: {#refs}
:::
