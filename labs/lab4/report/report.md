---
## Front matter
title: "Лабораторная работа №4"
subtitle: "Научное программирование"
author: "Леонтьева Ксения Андреевна | НПМмд-02-23"

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
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Изучить встроенные в Octave алгоритмы, необходимые для решения систем линейных уравнений.

# Теоретическое введение

__Метод Гаусса__

Запишем исходную систему

\begin{equation*}
 \begin{cases}
   a_{1}^{1}x^{1}+...+ a_{n}^{1}x^{n} = b^{1} \\
   a_{1}^{m}x^{1}+...+ a_{n}^{m}x^{n} = b^{m}
 \end{cases}
\end{equation*}

Более подробно см. в [@Octave_1:bash] и [@Octave_2:bash].

# Выполнение лабораторной работы

Для системы линейных уравнений:

$Ax = b \rightarrow
\begin{bmatrix}
1& 2& 3\\
0& -2& -4\\
1& -1& 0
\end{bmatrix}
\begin{bmatrix}
x^1\\
x^2\\
x^3
\end{bmatrix}
=
\begin{bmatrix}
4\\
6\\
0
\end{bmatrix}$

построим расширенную матрицу вида

$B = [A|b]=
\left[
\begin{array}{ccc|c}
1& 2& 3 & 4\\
0& -2& -4 & 6\\
1& -1& 0 & 0 \\
\end{array}
\right]$.

Рассмотрим ее поэлементно, например, выведем элемент, стоящий на пересечении 2й строки и 3го столбца. Также можем извлечь целый вектор строки или вектор столбца, например, выведем первую строку.

Реализуем явно метод Гаусса. Сначала добавим к третьей строке первую строку, умноженную на −1. Далее добавим к третьей строке вторую строку, умноженную на −1.5. Выведем явно решение системы, а затем воспользуемся встроенной командой. Можем поменять формат вывода значений, чтобы отображалось более пяти десятичных знаков. Затем вернем изначальный формат представления (рис. @fig:001) и (рис. @fig:002). 

![Метод Гаусса](image/Pic 1.jpg){#fig:001 width=90%}

![Метод Гаусса](image/Pic 2.jpg){#fig:002 width=90%}

Встроенная операция для решения линейных систем вида $Ax=b$ в Octave называется левым делением и записывается как $A \backslash b$. Это концептуально эквивалентно выражению $A^{-1}b$. Выделим из расширенной матрицы B матрицу A и вектор b. После чего найдем вектор $x$  (рис. @fig:003).

![Левое деление](image/Pic 3.jpg){#fig:003 width=90%}

Пусть дана матрица:

$A = 
\begin{bmatrix}
1& 2& 3\\
0& -2& -4\\
1& -1& 0
\end{bmatrix}$

С помощью Octave распишем её LU-разложение и найдем вектор $x$ (рис. @fig:004).

![LU-разложение](image/Pic 4.jpg){#fig:004 width=90%}

Для этой же матрицы A распишем LUP-разложение (рис. @fig:005).

![LUP-разложение](image/Pic 5.jpg){#fig:005 width=90%}


# Вывод

В ходе выполнения данной лабораторной работы я изучила встроенные в Octave алгоритмы, необходимые для решения систем линейных уравнений.

# Список литературы{.unnumbered}


