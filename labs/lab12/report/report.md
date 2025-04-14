---
## Front matter
title: "Отчет по лабораторной работе №12"
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

Выполнить пример моделирования простого протокола передачи данных.


# Задание

Рассмотрим ненадёжную сеть передачи данных, состоящую из источника, получателя.
Перед отправкой очередной порции данных источник должен получить от получателя подтверждение о доставке предыдущей порции данных.
Считаем, что пакет состоит из номера пакета и строковых данных. Передавать будем сообщение «Modelling and Analysis by Means of Coloured Petry Nets», разбитое по 8 символов.

# Выполнение лабораторной работы

1. Построила модель с помощью CPNTools. Основные состояния: источник (Send), получатель (Receiver). Действия (переходы): отправить пакет (Send Packet), отправить подтверждение (Send ACK). Промежуточное состояние: следующий посылаемый пакет (NextSend).

![*Начальный граф*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab12/report/image/1.png){#fig:001 width=70%}

2. Задала декларации модели.

![*Декларации*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab12/report/image/2.png){#fig:002 width=70%}

3. Расставила на графе типы, начальные значения и значения дуг. Задала промежуточные состояния (A, B с типом INTxDATA, C, D с типом INTxDATA) для переходов: передать пакет Transmit Packet, передать подтверждение Transmit ACK. Добавила переход получения пакета (Receive Packet) и состояние NextRec, задала вспомогательные состояния SP и SA.

![*Добавление промежуточных состояний*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab12/report/image/3.png){#fig:003 width=70%}

5. Задала декларации.

![*Декларации*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab12/report/image/4.png){#fig:004 width=70%}

![*Модель простого протокола передачи данных*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab12/report/image/5.png){#fig:005 width=70%}

6. Вычислила пространство состояний. Сформировала отчёт о пространстве состояний и проанализировала его. 

![*Отчёт о пространстве состояний*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab12/report/image/6.png){#fig:006 width=70%}

![*Отчёт о пространстве состояний*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab12/report/image/7.png){#fig:007 width=70%}

![*Отчёт о пространстве состояний*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab12/report/image/8.png){#fig:008 width=70%}

7. Построила граф пространства состояний.

![*Граф пространства состояний*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab12/report/image/9.png){#fig:009 width=70%}

# Выводы

Я выполнила пример моделирования простого протокола передачи данных.

# Список литературы{.unnumbered}

::: {#refs}
:::
