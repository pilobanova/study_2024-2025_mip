---
## Front matter
title: "Oтчет по лабораторной работе №5"
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

Построить модель SIR в xcos и в  OpenModelica.

# Задание 

1. Реализовать модель в xcos.

2. Реализовать модель с помощью блока Modelica в xcos.

3. Реализовать модель SIR в OpenModelica.

4. В дополнение к предположениям, которые были сделаны для модели SIR (5.1), предположим, что учитываются демографические процессы, в частности, что смертность в популяции полностью уравновешивает рождаемость, а все рожденные индивидуумы появляются на свет абсолютно здоровыми.

Требуется:

– реализовать модель SIR с учётом процесса рождения / гибели особей в xcos (в том числе и с использованием блока Modelica), а также в OpenModelica;

– построить графики эпидемического порога при различных значениях параметров модели (в частности изменяя параметр µ);

– сделать анализ полученных графиков в зависимости от выбранных значений параметров модели.


# Выполнение лабораторной работы

1. В меню Моделирование, Задать переменные окружения задала значения переменных B=1 и v=0.3.

![*Установка переменных окружения в xcos*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/1.png){#fig:001 width=70%}

2. Создала модель в xcos с помощью блоков CLOCK_c, CSCOPE, TEXT_f, MUX, INTEGRAL_m, GAINBLK_f, SUMMATION и PROD_f.

![*Модель SIR в xcos*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/2.png){#fig:002 width=70%}

3. В параметрах верхнего и среднего блока интегрирования задала начальные значения s(0) = 0,999 и i(0) = 0,001.

![*Установка начальных значений в блоках интегрирования*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/3.png){#fig:003 width=70%}

![*Установка начальных значений в блоках интегрирования*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/4.png){#fig:004 width=70%}

4. В меню Моделирование, Установка задала конечное время интегрирования, равным времени моделирования (в данном случае 30).

![*Установка конечного времени интегрирования в xcos*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/5.png){#fig:005 width=70%}

![*Эпидемический порог модели SIR при B = 1, v = 0.3*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/6.png){#fig:006 width=70%}

5. Для реализации модели с помощью языка Modelica помимо блоков CLOCK_c, CSCOPE, TEXT_f и MUX использовала блоки CONST_m, MBLOKC. Задала значения переменных B и v.

![*Модель SIR в xcos с применением блока Modelica*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/7.png){#fig:007 width=70%}

6. Установила параметры блока Modelica.

![*Параметры блока Modelica для модели*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/8.png){#fig:008 width=70%}

![*Параметры блока Modelica для модели*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/9.png){#fig:009 width=70%}

![*Результат моделирования*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/10.png){#fig:010 width=70%}

7. Написала код для реализации модели SIR в OpenModelica.

![*Код для реализации модели SIR в OpenModelica*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/11.png){#fig:011 width=70%}

8. Задала конечное время интегрирования, равным времени моделирования (в данном случае 30).

![*Установка конечного времени интегрирования*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/12.png){#fig:012 width=70%}

![*Результат моделирование*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/13.png){#fig:013 width=70%}

9. Создала модель в xcos с помощью блоков CLOCK_c, CSCOPE, TEXT_f, MUX, INTEGRAL_m (3), GAINBLK_f (5), SUMMATION (4) и PROD_f.

![*Модель SIR с учётом процесса рождения / гибели особей в xcos*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/14.png){#fig:014 width=70%}

10. В меню Моделирование, Задать переменные окружения задала значения переменных B=1, v=0.3 и м=0.1.

![*Установка переменных окружения в xcos*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/15.png){#fig:015 width=70%}

![*Эпидемический порог модели SIR при B = 1, v = 0.3 и м=0.1*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/16.png){#fig:016 width=70%}

11. Создала модель с помощью блоков CLOCK_c, CSCOPE, TEXT_f, MUX, CONST_m, MBLOKC. 

![*Модель SIR в xcos с применением блока Modelica*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/17.png){#fig:017 width=70%}

12. Задала значения переменных B, v и м.

![*Установка переменных окружения в xcos*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/18.png){#fig:018 width=70%}

13. Установила параметры блока Modelica.

![*Параметры блока Modelica для модели*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/19.png){#fig:019 width=70%}

![*Параметры блока Modelica для модели*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/20.png){#fig:020 width=70%}

![*Результат моделирования*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/21.png){#fig:021 width=70%}

14. Написала код для реализации модели SIR в OpenModelica.

![*Код для реализации модели SIR в OpenModelica*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/22.png){#fig:022 width=70%}

15. Задала конечное время интегрирования.

![*Установка конечного времени интегрирования*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/23.png){#fig:023 width=70%}

![*Результат моделирования*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/24.png){#fig:024 width=70%}

16. Изменила значения параметра м (=0.5).

![*Изменение параметра м*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/25.png){#fig:025 width=70%}

![*Эпидемический порог модели SIR при B = 1, v = 0.3 и м=0.5*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/26.png){#fig:026 width=70%}

17. Изменила значения параметра B (=7).

![*Изменение параметра B*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/27.png){#fig:027 width=70%}

![*Эпидемический порог модели SIR при B = 7, v = 0.3 и м=0.1*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/28.png){#fig:028 width=70%}

18. Изменила значения параметра v (=1).

![*Изменение параметра v*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/29.png){#fig:029 width=70%}

![*Эпидемический порог модели SIR при B = 1, v = 1 и м=0.1*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/lab5/report/image/30.png){#fig:030 width=70%}

# Выводы

Я построила модель SIR в xcos и в  OpenModelica.

# Список литературы{.unnumbered}

::: {#refs}
:::
