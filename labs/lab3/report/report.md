---
## Front matter
title: "Отчет по лабораторной работе №3"
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

Провести моделирование СМО.

# Выполнение лабораторной работы

1. Скопировала файл с шаблоном и дополнила его.

![*Создание файлов*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab3/report/image/1.png){#fig:001 width=70%}

![*Заполнение файла с проектом*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab3/report/image/2.png){#fig:002 width=70%}

![*Заполнение файла с проектом*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab3/report/image/3.png){#fig:003 width=70%}

2. В каталоге с проектом создала отдельный файл graph_plot и заполнила его.

![*Заполнение файла для графика*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab3/report/image/4.png){#fig:004 width=70%}

3. Сделала файл исполняемым. После компиляции файла с проектом, запустила скрипт в созданном файле graph_plot, который создал файл qm.pdf с результатами моделирования.

![*Запуск файлов*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab3/report/image/5.png){#fig:005 width=70%}

![*График поведения длины очереди*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab3/report/image/6.png){#fig:006 width=70%}


# Выводы

Я провела моделирование СМО.


