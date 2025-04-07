---
## Front matter
title: "Отчет по лабораторной работе №10"
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

Реализация модели задачи об обедающих мудрецах.

# Задание

Пять мудрецов сидят за круглым столом и могут пребывать в двух состояниях — думать и есть. Между соседями лежит одна палочка для еды. Для приёма пищи необходимы две палочки. Палочки — пересекающийся ресурс. Необходимо синхронизировать процесс еды так, чтобы мудрецы не умерли с голода.

# Выполнение лабораторной работы

1. Нарисовала граф сети.

![*Граф сети задачи об обедающих мудрецах*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab10/report/image/1.png){#fig:001 width=70%}

2. В меню задала новые декларации модели: типы фишек, начальные значения позиций, выражения для дуг.

![*Задание деклараций задачи об обедающих мудрецах*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab10/report/image/2.png){#fig:002 width=70%}

3. Указала типы фишек, начальные значения и выражения для дуг на графе.

![*Модель задачи об обедающих мудрецах*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab10/report/image/3.png){#fig:003 width=70%}

4. Запустила модель.

![*Запуск модели задачи об обедающих мудрецах*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab10/report/image/4.png){#fig:004 width=70%}

5. Вычислила пространство состояний. Сформировала отчёт о пространстве состояний и проанализировала его.

![*Отчет о пространстве состояний*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab10/report/image/5.png){#fig:005 width=70%}

6. Построила граф пространства состояний.

![*Граф пространства состояний*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab10/report/image/6.png){#fig:006 width=70%}

# Выводы

Я реализовала модель задачи об обедающих мудрецах.

# Список литературы{.unnumbered}

::: {#refs}
:::
