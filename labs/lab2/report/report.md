---
## Front matter
title: "Отчет по лабораторной работе №2"
subtitle: "Дисциплина: Имитационное моделирование"
author: "Лобанова Полина Иннекентьевна"

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

Исследование протокола TCP и алгоритма управления очередью RED.

# Задание

1. Описание моделируемой сети:

– сеть состоит из 6 узлов;

– между всеми узлами установлено дуплексное соединение с различными пропускной способностью и задержкой 10 мс;

– узел r1 использует очередь с дисциплиной RED для накопления пакетов, максимальный размер которой составляет 25;

– TCP-источники на узлах s1 и s2 подключаются к TCP-приёмнику на узле s3;

– генераторы трафика FTP прикреплены к TCP-агентам.

2. 
– Измените в модели на узле s1 тип протокола TCP с Reno на NewReno, затем на Vegas. Сравните и поясните результаты.

– Внесите изменения при отображении окон с графиками (измените цвет фона, цвет траекторий, подписи к осям, подпись траектории в легенде).

# Выполнение лабораторной работы

1. Скопировала шаблон в новый файл и дополнила его.

![*Копирование файла*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab2/report/image/1.png){#fig:001 width=70%}

![*Заполнение файла*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab2/report/image/2.png){#fig:002 width=70%}

![*Заполнение файла*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab2/report/image/3.png){#fig:003 width=70%}

![*График изменения длины очереди и средней длины очереди*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab2/report/image/4.png){#fig:004 width=70%}

![*График изменения TCP-окна*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab2/report/image/5.png){#fig:005 width=70%}

2. Изменила в модели на узле s1 тип протокола TCP с Reno на NewReno.

![*Изменение типа протокола*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab2/report/image/6.png){#fig:006 width=70%}

![*График изменения TCP-окна*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab2/report/image/7.png){#fig:007 width=70%}

![*График изменения длины очереди и средней длины очереди*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab2/report/image/8.png){#fig:008 width=70%}

3. Изменила в модели на узле s1 тип протокола TCP с NewReno на Vegas.

![*Изменение типа протокола*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab2/report/image/9.png){#fig:009 width=70%}

![*График изменения длины очереди и средней длины очереди*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab2/report/image/10.png){#fig:010 width=70%}

4. Внесла изменения при отображении окон с графиками (изменила цвет фона, цвет траекторий, подписи к осям, подпись траектории в легенде).

![*Изменение графика*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab2/report/image/11.png){#fig:011 width=70%}

![*График изменения длины очереди и средней длины очереди*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab2/report/image/12.png){#fig:012 width=70%}


# Выводы

Я исследовала протокол TCP и алгоритм управления очередью RED.

