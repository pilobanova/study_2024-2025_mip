---
## Front matter
title: "Отчет по лабораторной работе №8"
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

Реализовать модель TCP/AQM в xcos и с использованием языка Modelica в среде OpenModelica.

# Задание

1. Построить схему модели в xcos.

2. Построить график динамики изменения размера TCP окна W(t) и размера очереди Q(t) и фазовый портрет (W, Q). 

3. Реализовать модель с использованием языка Modelica в среде OpenModelica. Для реализации задержки используйте оператор delay(). Постройте график динамики изменения размера TCP окна W(t) и размера очереди Q(t)
и фазовый портрет (W, Q).

# Выполнение лабораторной работы

1. Задала начальные значения параметров.

![*Установка начальных значений*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab8/report/image/1.png){#fig:001 width=70%}

2. Построила схему модели в xcos.

![*Схема xcos, моделирующая систему*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab8/report/image/2.png){#fig:002 width=70%}

![*Динамика изменения размера TCP окна W(t) и размера очереди Q(t)*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab8/report/image/3.png){#fig:003 width=70%}

![*Фазовый портрет (W, Q)*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab8/report/image/4.png){#fig:004 width=70%}

3. Заменила значение параметра С на 0.9.

![*Изменение параметра*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab8/report/image/5.png){#fig:005 width=70%}

![*Динамика изменения размера TCP окна W(t) и размера очереди Q(t) при C = 0, 9*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab8/report/image/6.png){#fig:006 width=70%}

![*Фазовый портрет (W, Q) при C = 0, 9*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab8/report/image/7.png){#fig:007 width=70%}

4. Написала программу для реализации модели с использованием языка Modelica.

![*Программа для реализации модели*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab8/report/image/8.png){#fig:008 width=70%}

![*Динамика изменения размера TCP окна W(t) и размера очереди Q(t)*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab8/report/image/9.png){#fig:009 width=70%}

![*Фазовый портрет (W, Q)*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab8/report/image/10.png){#fig:010 width=70%}


# Выводы

Я реализовала модель TCP/AQM в xcos и с использованием языка Modelica в среде OpenModelica.

# Список литературы{.unnumbered}

::: {#refs}
:::
