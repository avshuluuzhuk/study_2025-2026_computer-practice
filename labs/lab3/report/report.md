---
## Front matter
title: "Управляющие структуры"
subtitle: "Лабораторная работа № 3"
author: "Шулуужук Айраана НПИбд-02-22"

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
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
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

Основная цель работы — освоить применение циклов функций и сторонних для Julia
пакетов для решения задач линейной алгебры и работы с матрицами.

# Выполнение лабораторной работы

## Циклы for, while 

Для различных операций, связанных с перебором индексируемых элементов структур
данных, традиционно используются циклы while и for (рис. [-@fig:001]) (рис. [-@fig:002])

![цикл while](image/1.png){#fig:001 width=70%}

![цикл for](image/2.png){#fig:002 width=70%}

## Условные выражения

Довольно часто при решении задач требуется проверить выполнение тех или иных
условий. Для этого используют условные выражения (рис. [-@fig:003]) 

![условные выражения и тернарный оператор](image/3.png){#fig:003 width=70%}

## Функции

Julia дает нам несколько разных способов написать функцию. Первый требует ключевых
слов function и end (рис. [-@fig:004]) (рис. [-@fig:005])  (рис. [-@fig:006])

![функции](image/4.png){#fig:004 width=70%}

![функции, сопровождаемые восклицательным знаком](image/5.png){#fig:005 width=70%}

![map(), broadcast](image/6.png){#fig:006 width=70%}

## Сторонние библиотеки (пакеты) в Julia

При первом использовании пакета в вашей текущей установке Julia вам необходимо
использовать менеджер пакетов, чтобы явно его добавить (рис. [-@fig:007])

![cторонние библиотеки (пакеты) в Julia](image/7.png){#fig:007 width=70%}

## Выполнение самостоятельной работы

1. Используя циклы while и for:
- выведите на экран целые числа от 1 до 100 и напечатайте их квадраты (рис. [-@fig:008]).

![1 пункт](image/8.png){#fig:008 width=70%}

- создайте словарь squares, который будет содержать целые числа в качестве ключей и квадраты в качестве их пар-значений (рис. [-@fig:009]).

![2 пункт](image/9.png){#fig:009 width=70%}

- создайте массив squares_arr, содержащий квадраты всех чисел от 1 до 100. (рис. [-@fig:010]).

![3 пункт](image/10.png){#fig:010 width=70%}

2. Напишите условный оператор, который печатает число, если число чётное, и строку
«нечётное», если число нечётное. Перепишите код, используя тернарный оператор (рис. [-@fig:011]).

![2 задание](image/11.png){#fig:011 width=70%}

3. Напишите функцию add_one, которая добавляет 1 к своему входу (рис. [-@fig:012]) 

![3 задание](image/12.png){#fig:012 width=70%}

4. Используйте map() или broadcast() для задания матрицы 𝐴, каждый элемент кото-
рой увеличивается на единицу по сравнению с предыдущим (рис. [-@fig:013]).

![4 задание](image/13.png){#fig:013 width=70%}

5. Задайте матрицу A следующего вида, найти куб, заменить 3 столбец на сумму 2 и 3 столбцов (рис. [-@fig:014]) 

![5 задание](image/14.png){#fig:014 width=70%}

6. Создайте матрицу B с элементами 
Вычислите матрицу C = 𝐵𝑇𝐵 (рис. [-@fig:015])

![6 задание](image/15.png){#fig:015 width=70%}

7. Создайте матрицу Z размерности 6 × 6, все элементы которой равны нулю, и матрицу
𝐸, все элементы которой равны 1. Используя цикл while или for и закономерности
расположения элементов, создайте следующие матрицы размерности 6 × 6 (рис. [-@fig:016]) (рис. [-@fig:017])

![7 задание](image/16.png){#fig:016 width=70%}

![7 задание](image/17.png){#fig:017 width=70%}

8. В языке R есть функция outer(). Фактически, это матричное умножение с возмож-
ностью изменить применяемую операцию (например, заменить произведение на
сложение или возведение в степень).

- Напишите свою функцию, аналогичную функции outer() языка R. Функция
должна иметь следующий интерфейс: outer(x,y,operation). Таким образом,
функция вида outer(A,B,*) должна быть эквивалентна произведению матриц
A и B размерностями L × M и M × N соответственно, где элементы резуль-
тирующей матрицы C  (рис. [-@fig:018]) (рис. [-@fig:019])

![8 задание](image/18.png){#fig:018 width=70%}

![8 задание](image/19.png){#fig:019 width=70%}

9. Решите следующую систему линейных уравнений с 5 неизвестными (рис. [-@fig:020])

![9 задание](image/20.png){#fig:020 width=70%}

10. Создайте матрицу M размерности 6 × 10, элементами которой являются целые числа,
выбранные случайным образом с повторениями из совокупности 1, 2, ... , 10 (рис. [-@fig:021])

![10 задание](image/21.png){#fig:021 width=70%}

– Найдите число элементов в каждой строке матрицы M, которые больше числа N
(например, N = 4) (рис. [-@fig:022])

![10 задание](image/22.png){#fig:022 width=70%}

– Определите, в каких строках матрицы M число M (например, M = 7) встречается
ровно 2 раза? (рис. [-@fig:023])

![10 задание](image/23.png){#fig:023 width=70%}

– Определите все пары столбцов матрицы M, сумма элементов которых больше K
(например, K = 75) (рис. [-@fig:024])

![10 задание](image/24.png){#fig:024 width=70%}

11. Вычислите (рис. [-@fig:025])

![11 задание](image/25.png){#fig:025 width=70%}

# Выводы

В результате выполнения лабораторной работы подготовили было освоено применение циклов функций и сторонних для Julia пакетов для решения задач линейной алгебры и работы с матрицами.
