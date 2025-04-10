---
## Front matter
title: "Отчет по лабораторной работе №11"
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

Реализовать модель системы массового обслуживания M|M|1.

# Задание

В систему поступает поток заявок двух типов, распределённый по пуассоновскому закону. Заявки поступают в очередь сервера на обработку. Дисциплина очереди - FIFO. Если сервер находится в режиме ожидания (нет заявок на сервере), то заявка поступает на обработку сервером.

# Выполнение лабораторной работы

1. Построила модель с помощью CPNTools. Использовала три отдельных листа: на первом листе описала граф системы, на втором — генератор заявок, на третьем — сервер обработки заявок.

![*Граф сети системы обработки заявок в очереди*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/1.png){#fig:001 width=70%}

![*Граф генератора заявок системы*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/2.png){#fig:002 width=70%}

![*Граф процесса обработки заявок на сервере системы*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/3.png){#fig:003 width=70%}

2. Задала декларации системы, переменные модели и определила функции системы.

![*Задание деклараций*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/4.png){#fig:004 width=70%}

3. Задала параметры модели на графах сети.

![*Параметры элементов основного графа системы обработки заявок в очереди*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/5.png){#fig:005 width=70%}

![*Параметры элементов генератора заявок системы*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/6.png){#fig:006 width=70%}

![*Параметры элементов обработчика заявок системы*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/7.png){#fig:007 width=70%}

4. Для мониторинга параметров очереди системы M|M|1 потребовалась палитра Monitoring. Выбрала Break Point (точка останова) и установила её на переход Start. После этого в разделе меню Monitor появился новый подраздел, который назвала Ostanovka. В этом подразделе внесла изменения в функцию Predicate, которая будет выполняться при запуске монитора.

![*Функция Predicate монитора Ostanovka*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/9.png){#fig:008 width=70%}

5. Далее необходимо было определить конструкцию Queue_Delay.count(). С помощью палитры Monitoring выбрала Data Call и установила на переходе Start. Появившийся в меню монитор назвала Queue Delay.Изменила функция Observer так, чтобы получить значение задержки в очереди.

![*Функция Observer монитора Queue Delay*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/10.png){#fig:009 width=70%}

6. После запуска программы на выполнение в каталоге с кодом программы появился файл Queue_Delay.log, содержащий в первой колонке — значение задержки очереди, во второй — счётчик, в третьей — шаг, в четвёртой — время. С помощью gnuplot построила график значений задержки в очереди, выбрав по оси x время, а по оси y — значения задержки.

![*Запуск системы обработки заявок в очереди*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/11.png){#fig:010 width=70%}

![*График изменения задержки в очереди*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/12.png){#fig:011 width=70%}

7. Посчитала задержку в действительных значениях. Для этого с помощью палитры Monitoring выбрала Data Call и устанавила на переходе Start. Появившийся в меню монитор называла Queue Delay Real. Функцию Observer изменила. После запуска программы на выполнение в каталоге с кодом программы появился файл Queue_Delay_Real.log с содержимым, аналогичным содержимому файла Queue_Delay.log, но значения задержки имеют действительный тип.

![*Функция Observer монитора Queue Delay Real*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/13.png){#fig:012 width=70%}

8. Посчитала, сколько раз задержка превысила заданное значение. С помощью палитры Monitoring выбрала Data Call и установила на переходе Start. Монитор назвала Long Delay Time. Функцию Observer изменила. В декларациях задала глобальную переменную (в форме ссылки на число 200).

![*Функция Observer монитора Long Delay Time*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/14.png){#fig:013 width=70%}

9. С помощью gnuplot построила график, демонстрирующий, в какие периоды времени значения задержки в очереди превышали заданное значение 200.

![*Периоды времени, когда значения задержки в очереди превышали заданное значение*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab11/report/image/15.png){#fig:014 width=70%}

# Выводы

Я реализовала модель системы массового обслуживания M|M|1.

# Список литературы{.unnumbered}

::: {#refs}
:::
