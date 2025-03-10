---
## Front matter
title: "Отчет по лабораторной работе №6"
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

Реализовать модель «хищник–жертва» в xcos,  с помощью блока Modelica в xcos и  в OpenModelica.

# Выполнение лабораторной работы

1. Зафиксировала начальные данные: a = 2, b = 1, c = 0, 3, d = 1.

![*Значения коэффициентов a, b, c, d*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/1.png){#fig:001 width=70%}

2. Используя блоки CLOCK_c, CSCOPE, TEXT_f, MUX, INTEGRAL_m, GAINBLK_f, SUMMATION, PROD_f и CSCOPXY, создала модель «хищник–жертва» в xcos.

![*Модель «хищник–жертва» в xcos*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/2.png){#fig:002 width=70%}

3. В параметрах блоков интегрирования задала начальные значения x(0) = 2, y(0) = 1.

![*Начальные значения в блоках интегрирования*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/3.png){#fig:003 width=70%}

![*Начальные значения в блоках интегрирования*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/4.png){#fig:004 width=70%}

4. Задала конечное время интегрирования, равным времени моделирования: 30. А также параметры блоков регулирующих устройств.

![*Конечное время интегрирования*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/5.png){#fig:005 width=70%}

![*Параметры блока регулирующего устройства CSCOPE*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/6.png){#fig:006 width=70%}

![*Параметры блока регулирующего устройства CSCOPXY*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/7.png){#fig:007 width=70%}

![*Динамика изменения численности хищников и жертв*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/8.png){#fig:008 width=70%}

![*Фазовый портрет модели*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/9.png){#fig:009 width=70%}

5. Как и ранее, задала значения коэффициентов a, b, c, d.

![*Значения коэффициентов a, b, c, d*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/10.png){#fig:010 width=70%}

6. Для реализации модели с помощью языка Modelica использовала следующие блоки xcos: CLOCK_c, CSCOPE, CSCOPXY, TEXT_f, MUX, CONST_m и MBLOCK.

![*Модель «хищник–жертва» в xcos с применением блока Modelica*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/11.png){#fig:011 width=70%}

7. Задала параметры блока Modelica.

![*Параметры блока Modelica*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/12.png){#fig:012 width=70%}

![*Параметры блока Modelica*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/13.png){#fig:013 width=70%}

![*Динамика изменения численности хищников и жертв*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/14.png){#fig:014 width=70%}

![*Фазовый портрет модели*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/15.png){#fig:015 width=70%}

8. Для реализации модели «хищник – жертва» в OpenModelica написала код.

![*Код для реализации модели*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/16.png){#fig:016 width=70%}

9. Задала конечное время.

![*Конечное время интегрирования*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/17.png){#fig:017 width=70%}

![*Динамика изменения численности хищников и жертв*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/18.png){#fig:018 width=70%}

![*Фазовый портрет модели*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab6/report/image/19.png){#fig:019 width=70%}

# Выводы

Я реализовала модель «хищник–жертва» в xcos,  с помощью блока Modelica в xcos и  в OpenModelica.

# Список литературы{.unnumbered}

::: {#refs}
:::
