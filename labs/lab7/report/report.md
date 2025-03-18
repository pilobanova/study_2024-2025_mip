---
## Front matter
title: "Отчет по лабораторной работе №7"
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

Реализовать в xcos модель системы массового обслуживания типа M|M|1|∞.

# Выполнение лабораторной работы

1. Зафиксировала начальные данные: lambda = 0, 3, mu = 0, 35, z0 = 6.

![*Начальные данные*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab7/report/image/1.png){#fig:001 width=70%}

2. Используя блоки RAND_m, LOGBLK_f, GAINBLK_f, EVTVARDLY, CLKSOMV_f, CLKINV_f, CLKOUTN_f, реализовала суперблок, моделирующий поступление заявок.

![*Суперблок, моделирующий поступление заявок*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab7/report/image/2.png){#fig:002 width=70%}

3. Используя блоки RAND_m, EVTVARDLY, CLKSOMV_f, scifunc_block_m, IFTHEL_f, IN_f, CONST_m, SUMMATION, CLKINV_f, CLKOUTN_f, реализовала суперблок, моделирующий процесс обработки заявок.

![*Суперблок, моделирующий обработку заявок*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab7/report/image/4.png){#fig:003 width=70%}

4. Используя блоки Select_m, CONST_m, SUMMATION, EVRGEN_f, DOLLAR_f, CSCOPE, CEVENTSCOPE, реализовала модель системы массового обслуживания.

![*Модель M|M|1|∞ в xcos*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab7/report/image/5.png){#fig:004 width=70%}

5. Указала конечное время (30), параметры блоков регистрирующих устройств и запустила моделирование.

![*График поступления (черный) и обработки (зеленый) заявок*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab7/report/image/6.png){#fig:005 width=70%}

![*Динамика размера очереди*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab7/report/image/7.png){#fig:006 width=70%}


# Выводы

Я реализовала в xcos модель системы массового обслуживания типа M|M|1|∞.

# Список литературы{.unnumbered}

::: {#refs}
:::
