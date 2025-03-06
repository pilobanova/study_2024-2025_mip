---
## Front matter
title: "Отчет по упражнению"
subtitle: "Дисциплина: Имитационное моделирование"
author: "Лобанова Полина Иннекетьевна"

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

Выполнить построение фигуры Лиссажу с разными параметрами.

# Задание

Постройте с помощью xcos фигуры Лиссажу со следующими параметрами:

1) A = B = 1, a = 2, b = 2, б = 0; π/4; π/2; 3π/4; π;

2) A = B = 1, a = 2, b = 4, б = 0; π/4; π/2; 3π/4; π;

3) A = B = 1, a = 2, b = 6, б = 0; π/4; π/2; 3π/4; π;

4) A = B = 1, a = 2, b = 3, б = 0; π/4; π/2; 3π/4; π.


# Выполнение лабораторной работы

1. Создала модель в xcos, используя блоки CLOCK_c, GENSIN_f, TEXT_f, CSOPXY.

![*Схема модели*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/1.png){#fig:001 width=70%}

2. Задала параметры: A = B = 1, a = 2, b = 2, б = π/2, а также параметры регистрирующего устройства.

![*Изменения параметров*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/2.png){#fig:002 width=70%}

![*Изменения параметров*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/3.png){#fig:003 width=70%}

![*Изменения параметров*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/4.png){#fig:004 width=70%}

![*График с параметрами A = B = 1, a = 2, b = 2, б = π/2*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/5.png){#fig:005 width=70%}

3. Изменила параметра на A = B = 1, a = 2, b = 2, б = 0.

![*График с параметрами A = B = 1, a = 2, b = 2, б = 0*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/7.png){#fig:006 width=70%}

4. Изменила параметры на A = B = 1, a = 2, b = 2, б = π/4. 

![*График с параметрами A = B = 1, a = 2, b = 2, б = π/4*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/9.png){#fig:007 width=70%}

5. Изменила параметры на A = B = 1, a = 2, b = 2, б = 3π/4.

![*График с параметрами A = B = 1, a = 2, b = 2, б = 3π/4*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/11.png){#fig:008 width=70%}

6. Изменила параметры на A = B = 1, a = 2, b = 2, б = π.

![*График с параметрами A = B = 1, a = 2, b = 2, б = π*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/13.png){#fig:009 width=70%}

7. Изменила параметры на A = B = 1, a = 2, b = 4, б = 0.

![*График с параметрами A = B = 1, a = 2, b = 4, б = 0*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/15.png){#fig:010 width=70%}

8. Изменила параметры на A = B = 1, a = 2, b = 4, б = π/4.

![*График с параметрами A = B = 1, a = 2, b = 4, б = π/4*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/17.png){#fig:011 width=70%}

9. Изменила параметры на A = B = 1, a = 2, b = 4, б = π/2.

![*График с параметрами A = B = 1, a = 2, b = 4, б = π/2*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/19.png){#fig:012 width=70%}

10. Изменила параметры на A = B = 1, a = 2, b = 4, б = 3π/4.

![*График с параметрами A = B = 1, a = 2, b = 4, б = 3π/4*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/21.png){#fig:013 width=70%}

11. Изменила параметры на A = B = 1, a = 2, b = 4, б = π.

![*График с параметрами A = B = 1, a = 2, b = 4, б = π*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/23.png){#fig:014 width=70%}

12. Изменила параметры на A = B = 1, a = 2, b = 6, б = 0.

![*График с параметрами A = B = 1, a = 2, b = 6, б = 0*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/25.png){#fig:015 width=70%}

13. Изменила параметры на A = B = 1, a = 2, b = 6, б = π/4.

![*График с параметрами A = B = 1, a = 2, b = 6, б = π/4*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/27.png){#fig:016 width=70%}

14. Изменила параметры на A = B = 1, a = 2, b = 6, б = π/2.

![*График с параметрами A = B = 1, a = 2, b = 6, б = π/2*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/29.png){#fig:017 width=70%}

15. Изменила параметры на A = B = 1, a = 2, b = 6, б = 3π/4.

![*График с параметрами A = B = 1, a = 2, b = 6, б = 3π/4*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/31.png){#fig:018 width=70%}

16. Изменила параметры на A = B = 1, a = 2, b = 6, б = π.

![*График с параметрами A = B = 1, a = 2, b = 6, б = π*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/33.png){#fig:019 width=70%}

17. Изменила параметры на  A = B = 1, a = 2, b = 3, б = 0.

![*График с параметрами A = B = 1, a = 2, b = 3, б = 0*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/35.png){#fig:020 width=70%}

18. Изменила параметры на  A = B = 1, a = 2, b = 3, б = π/4.

![*График с параметрами A = B = 1, a = 2, b = 3, б = π/4*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/37.png){#fig:021 width=70%}

19. Изменила параметры на  A = B = 1, a = 2, b = 3, б = π/2.

![*График с параметрами A = B = 1, a = 2, b = 3, б = π/2*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/39.png){#fig:022 width=70%}

20. Изменила параметры на  A = B = 1, a = 2, b = 3, б = 3π/4.

![*График с параметрами A = B = 1, a = 2, b = 3, б = 3π/4*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/41.png){#fig:023 width=70%}

21. Изменила параметры на  A = B = 1, a = 2, b = 3, б = π.

![*График с параметрами A = B = 1, a = 2, b = 3, б = π*](/home/pilobanova/work/study/2024-2025/Имитационное моделирование/mip/labs/ex/report/image/43.png){#fig:024 width=70%}


# Выводы

Я выполнила построение фигуры Лиссажу с разными параметрами.

# Список литературы{.unnumbered}

::: {#refs}
:::
