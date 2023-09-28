---
## Front matter
title: "Лабораторная работа №3"
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

Освоить базовые навыки работы в Octave: простейшие вычислительные операции, операции с веторами и матрицами, построение простейших графиков, сравнение циклов и операций с векторами.

# Теоретическое введение



# Выполнение лабораторной работы

Для начала включили журналирование сессии, создав документ "diary". Вычислили значение выражения. Задали вектор-строку (ковектор), вектор-столбец (вектор) и матрицу (рис. @fig:001).

![Простейшие операции](image/Pic 1.png){#fig:001 width=90%}

Задали два вектора-столбца. Осуществили сложение заданных векторов, их скалярное и векторное умножение. Нашли норму одного из векторов (рис. @fig:002).

![Операции с векторами](image/Pic 2.png){#fig:002 width=90%}

Ввели два вектора-строки. Вычислили проекцию одного вектора на другой (рис. @fig:003).

![Вычисление проекции одного вектора на другой](image/Pic 3.png){#fig:003 width=90%}

Ввели две матрицы. Вычислили их произведение, а также их произведение с учетом транспонирования одной из матриц. Вычислили выражение, содержащее единичную матрицу. Нашли определитель матрицы, обратную для нее, вычислили собственные значения матрицы и ее ранг (рис. @fig:004 и рис. @fig:005).

![Матричные операции](image/Pic 4.png){#fig:004 width=90%}

![Матричные операции](image/Pic 5.png){#fig:005 width=90%}

Сздали вектор значений $x$. Задали вектор $y = sin(x)$ и построили график. Очистили рабочую область фигуры для дальнейшего улучшения графика. Задали красный цвет для линии и сделали ее потолще. Подогнали диапазон осей и нарисовали сетку. Подписали оси и сделали заголовок графика, а также задали легенду (рис. @fig:006 и рис. @fig:007).

![Построение простейших графиков](image/Pic 6.png){#fig:006 width=90%}

![Построение простейших графиков](image/Pic 7.png){#fig:007 width=90%}

Очистили память и рабочую область фигуры. Задали два вектора и начертили эти точки, используя кружочки как маркеры. Ввели команду для добавления еще одного графика к текущему. Добавили график регрессии. Задали сетку, оси и легенду (рис. @fig:008).

![Два графика на одном чертеже](image/Pic 8.png){#fig:008 width=90%}

Строим график $y = x^2sin(x)$. Очистим память и рабочую область фигуры. Зададим вектор $x$ и построим график, используя поэлементное возведение в степень и поэлементное умножение (в противном случае выдаст ошибку). Сохраним графики в виде файлов (на сохранении файла в формате pdf программа зависает) (рис. @fig:009).

![График $y = x^2sin(x)$](image/Pic 9.png){#fig:009 width=90%}

Сравним эффективность работы с циклами и операций с векторами. Для этого вычислим сумму: $S = \sum_{n}^{100000}$ $\frac{1}{n^2}$.

Очистим память и рабочую область фигуры. Вычислим сумму $S$ с помощью цикла, создав файл loop_for.m (рис. @fig:010).

![Вычисление суммы с помощью цикла](image/Pic 10.png){#fig:010 width=90%}

Вычислим сумму $S$ с помощью операций с векторами, создав файл loop_vec.m (рис. @fig:011).

![Вычисление суммы с помощью операций с векторами](image/Pic 11.png){#fig:011 width=90%}

Запустив оба файла, видим, что время на выполнение второй программы в 100 раз меньше, чем на выполнение первой (рис. @fig:012). Таким образом, в данном случае операции с векторами эффективнее, чем циклы. В конце завершим запись в файл.

![Сравнение двух программ](image/Pic 12.png){#fig:012 width=90%}
 

# Вывод

В ходе выполнения данной лабораторной работы я освоила базовые навыки работы в Octave: простейшие вычислительные операции, операции с веторами и матрицами, построение простейших графиков, сравнение циклов и операций с векторами.

# Список литературы{.unnumbered}


