---
## Front matter
title: "Отчет по лабораторной работе №4"
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

Выполнение самостоятельного задания.

# Задание

Описание моделируемой сети:

– сеть состоит из N TCP-источников, N TCP-приёмников, двух маршрутизаторов R1 и R2 между источниками и приёмниками (N = 20);

– между TCP-источниками и первым маршрутизатором установлены дуплексные соединения с пропускной способностью 100 Мбит/с и задержкой 20 мс очередью типа DropTail;

– между TCP-приёмниками и вторым маршрутизатором установлены дуплексные соединения с пропускной способностью 100 Мбит/с и задержкой 20 мс очередью типа DropTail;

– между маршрутизаторами установлено симплексное соединение (R1–R2) с пропускной способностью 20 Мбит/с и задержкой 15 мс очередью типа RED, размером буфера 300 пакетов; в обратную сторону — симплексное соединение (R2–R1) с пропускной способностью 15 Мбит/с и задержкой 20 мс очередью типа DropTail;

– данные передаются по протоколу FTP поверх TCPReno;

– параметры алгоритма RED: qmin = 75, qmax = 150, qw = 0, 002, pmax = 0.1;

– максимальный размер TCP-окна 32; размер передаваемого пакета 500 байт; время
моделирования — 20 единиц модельного времени.

1. Для приведённой схемы разработать имитационную модель в пакете NS-2.
2. Построить график изменения размера окна TCP (в Xgraph и в GNUPlot);
3. Построить график изменения длины очереди и средней длины очереди на первом
маршрутизаторе.

# Выполнение лабораторной работы

1. Скопировала шаблон и заполнила файл в соответствии с заданием.

![*Листинг программы*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab4/report/лаб4/1.png){#fig:001 width=70%}

![*Листинг программы*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab4/report/лаб4/2.png){#fig:002 width=70%}

![*Листинг программы*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab4/report/лаб4/3.png){#fig:003 width=70%}

2. Запустила его и получила модель сети в nam, также график изменения размера окна TCP и график изменения длины очереди и средней длины очереди на первом маршрутизаторе в Xgraph.

![*Модель сети*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab4/report/лаб4/4.png){#fig:004 width=70%}

![*График изменения средней длины очереди*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab4/report/лаб4/5.png){#fig:005 width=70%}

![*График изменения длины очереди*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab4/report/лаб4/6.png){#fig:006 width=70%}

![*График изменения размера окна TCP на всех источниках при N=20*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab4/report/лаб4/7.png){#fig:007 width=70%}

![*График изменения размера окна TCP на линке 1-го источника при N=20*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab4/report/лаб4/8.png){#fig:008 width=70%}

3. Создала новый файл и заполнила его для создания графиков в GNUPlot.

![*Листинг программы*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab4/report/лаб4/9.png){#fig:009 width=70%}

![*Листинг программы*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab4/report/лаб4/10.png){#fig:010 width=70%}

![*График изменения размера окна TCP на линке 1-го источника при N=20*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab4/report/лаб4/11.png){#fig:011 width=70%}

![*График изменения размера окна TCP на всех источниках при N=20*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab4/report/лаб4/12.png){#fig:012 width=70%}

![*График изменения длины очереди*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab4/report/лаб4/13.png){#fig:013 width=70%}

![*График изменения средней длины очереди*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab4/report/лаб4/14.png){#fig:014 width=70%}


# Выводы

Я разработала имитационную модель в пакете NS-2, построила график изменения размера окна TCP (в Xgraph и в GNUPlot), а также график изменения длины очереди и средней длины очереди на первом маршрутизаторе.

# Список литературы{.unnumbered}

::: {#refs}
:::
