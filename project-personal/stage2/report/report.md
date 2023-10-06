---
## Front matter
title: "Индивидуальный проект. Этап 2."
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

Добавить на сайт данные о себе.

# Задание

- Разместить фотографию владельца сайта,

- Разместить краткое описание владельца сайта (Biography),

- Добавить информацию об интересах (Interests),

- Добавить информацию об образовании (Education),

- Сделать пост по прошедшей неделе,

- Добавить пост на тему "Непрерывная интеграция и непрерывное развертывание (CI/CD)".

# Теоретическое введение

Статический генератор сайта — программа, которая из различных исходных файлов (картинок, шаблонов в разных форматах, текстовых файлов и т.п) генерирует статический HTML-сайт. Один из ярких представителей — __Hugo__. Это один из самых популярных генераторов статических сайтов с открытым исходным кодом, написан на языке Go. 

Основные преимущества Hugo:

- Очень быстрый и гибкий,

- Для него легко настроить хостинг,

- Безопасный,

- Хорошая структура исходников,

- Возможность хранить содержимое в удобном формате (YAML, JSON или TOML),

- Поддержка тем. Есть готовый набор тем, более 200,

- Легко SEO-оптимизировать,

- Быстрый в освоении. Исчерпывающая документация.

Более подробно см. в [@hugo:bash] 


# Выполнение лабораторной работы

Для загрузки фотографии на сайт в каталог work/blog/content/authors/admin было добавлено изображение "avatar.png" (рис. @fig:001).

![Добавление фотографии](image/Pic 1.png){#fig:001 width=110%}

Для добавления информации о себе в файле work/blog/content/authors/admin/_index.md были изменены следующие разделы: Display name, Full name, Role/position/tagline, Organizations, Short bio, Interests, Education, Social/Academic Networking и основной раздел с биографией (рис. @fig:002) и (рис. @fig:003).

![Добавление информации о себе в файл _index.md](image/Pic 2.png){#fig:002 width=110%}

![Добавление информации о себе в файл _index.md](image/Pic 3.png){#fig:003 width=110%}

Чтобы создать посты на сайте необходимо изменить содержимое двух каталогов: work/blog/content/post/getting-started и work/blog/content/post/writing-technical-content. В данные каталоги были добавлены необходимые изображения, а также изменены файлы index.md (рис. @fig:004) - (рис. @fig:009).

![Добавление постов](image/Pic 4.png){#fig:004 width=110%}

![Добавление постов](image/Pic 5.png){#fig:005 width=110%}

![Добавление постов](image/Pic 6.png){#fig:006 width=110%}

![Добавление постов](image/Pic 7.png){#fig:007 width=110%}

![Добавление постов](image/Pic 8.png){#fig:008 width=110%}

![Добавление постов](image/Pic 9.png){#fig:009 width=110%}

Также была изменена цветовая тема сайта в файле work/blog/config/_default/params.yaml в разделе Appearance -> theme\_day (рис. @fig:010).

![Изменение цветовой темы сайта](image/Pic 10.png){#fig:010 width=110%}

После редактирования всех нобходимых каталогов и файлов запустили hugo и отправили файлы на GitHub (рис. @fig:011).

![Запуск hugo и добавление файлов на GitHub](image/Pic 11.png){#fig:011 width=110%}

Таким образом, текущая версия сайта выглядит следующим образом (рис. @fig:012) - (рис. @fig:015).

![Текущая версия сайта](image/Pic 12.png){#fig:012 width=110%}

![Текущая версия сайта](image/Pic 13.png){#fig:013 width=110%}

![Текущая версия сайта](image/Pic 14.png){#fig:014 width=110%}

![Текущая версия сайта](image/Pic 15.png){#fig:015 width=110%}

# Выводы

В ходе выполнения данной лабораторной работы на сайт были добавлены данные о себе и два поста по требуемым темам.

# Список литературы{.unnumbered}

::: {#refs}
:::

