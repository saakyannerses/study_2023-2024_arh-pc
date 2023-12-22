---
## Front matter
title: "Отчёта по лабораторной работе"
subtitle: "Арифметические операции в NASM."
author: "Саакян Нерсес Варданович"

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

Освоение арифметических инструкций языка ассемблера NASM.

# Задание

 1 Написать программу вычисления выражения 𝑦 = 𝑓(𝑥). Вид функции 𝑓(𝑥)
выбрать из таблицы 6.3 вариантов заданий в соответствии с номером
полученным при выполнении лабораторной работы.
 2 Загрузите файлы на GitHub.


# Выполнение лабораторной работы

Создайте каталог для программам лабораторной работы No 6, перейдите в него и создайте файл lab6-1.asm (рис. @fig:001).

![Создание каталога и файла лаб 6-1.asm](image/1.jpg){#fig:001 width=70%}

Рассмотрим примеры программ вывода символьных и численных значений. Програм-
мы будут выводить значения записанные в регистр eax. (рис. @fig:002).

![Программа 1](image/2.jpg){#fig:002 width=70%}

Создайте исполняемый файл и запустите его. (рис. @fig:003).

![Запуск программы](image/3.jpg){#fig:003 width=70%}

Создайте файл lab6-2.asm в каталоге ~/work/arch-pc/lab06 (рис. @fig:004).

![Создание файла lab6-2.asm](image/4.jpg){#fig:004 width=70%}

Введите в него текст программы из листинга 6.2. (рис. @fig:005).

![Введение текста](image/5.jpg){#fig:005 width=70%}

Создайте исполняемый файл и запустите его. (рис. @fig:006).

![Запуск файла](image/6.jpg){#fig:006 width=70%}

Аналогично предыдущему примеру изменим символы на числа. Замените строки (рис. @fig:007).

![Замена символов на числа](image/7.jpg){#fig:007 width=70%}

Создайте исполняемый файл и запустите его. (рис. @fig:008).

![Запуск файла](image/8.jpg){#fig:008 width=70%}

В результате полчили число 10.

Замените функцию iprintLF на iprint (рис. @fig:009).

![Замена функции](image/9.jpg){#fig:009 width=70%}

Создайте исполняемый файл и запустите его. (рис. @fig:010).

![Запуск файла](image/10.jpg){#fig:010 width=70%}

В качестве примера выполнения арифметических операций в NASM приведем про-
грамму вычисления арифметического выражения 𝑓(𝑥) = (5 ∗ 2 + 3)/3

Создайте файл lab6-3.asm в каталоге ~/work/arch-pc/lab06 (рис. @fig:011).

![Создание файла lab6-3.asm](image/11.jpg){#fig:011 width=70%}

Внимательно изучите текст программы из листинга 6.3 и введите в lab6-3.asm. (рис. @fig:012).

![Введение текста](image/12.jpg){#fig:012 width=70%}

Создайте исполняемый файл и запустите его.  (рис. @fig:013).

![Запуск файла](image/13.jpg){#fig:013 width=70%}

Измените текст программы для вычисления выражения 𝑓(𝑥) = (4 ∗ 6 + 2)/5 (рис. @fig:014).

![Изменение ткста](image/14.jpg){#fig:014 width=70%}

Создайте исполняемый файл и проверьте его работу. (рис. @fig:015).

![Запуск файла](image/15.jpg){#fig:015 width=70%}

В качестве другого примера рассмотрим программу вычисления варианта задания по
номеру студенческого билета, работающую по следующему алгоритму:
• вывести запрос на введение No студенческого билета
• вычислить номер варианта по формуле: (𝑆𝑛 mod 20) + 1, где 𝑆𝑛 – номер студен-
ческого билета (В данном случае 𝑎 mod 𝑏 – это остаток от деления 𝑎 на 𝑏).
• вывести на экран номер варианта.

Создайте файл variant.asm в каталоге ~/work/arch-pc/lab06 (@fig:016).

![Создание файла variant.asm ](image/16.jpg){#fig:016 width=70%}

Внимательно изучите текст программы из листинга 6.4 и введите в файл variant.asm. (рис. @fig:017).

![Введение текста](image/17.jpg){#fig:017 width=70%}

Создайте исполняемый файл и запустите его (рис. @fig:018).

![Запуск файла](image/18.jpg){#fig:018 width=70%}

# Ответы на вопросы

 1 "mov eax, rem" и "call sprint" в секции кода отвечают за вывод сообщения "Ваш вариант:" на экран.
 2 "mov ecx, x" и "mov edx, 80" загружают адрес буфера (x) и длину буфера (80) соответственно в регистры ecx и edx для вызова подпрограммы sread, которая считывает строку из консоли.
 3 "call atoi" вызывает подпрограмму atoi для преобразования ASCII кодов символов в число, результат которого сохраняется в регистре eax.
 4 Код для вычисления варианта начинается с "xor edx, edx" и "mov ebx, 20", после чего происходит деление числа, сохраненного в eax, на 20 с помощью инструкции "div ebx". Результат деления (цифра варианта) записывается в нижнюю часть регистра AX (AL). Затем происходит увеличение цифры варианта на единицу с помощью инструкции "inc edx".
 5 Результат деления (цифра варианта) записывается в нижнюю часть регистра AX (AL).
 6 Инструкция "inc edx" увеличивает цифру варианта на единицу для того, чтобы результат деления не оказывался равным нулю.
 7 "mov eax, edx" загружает цифру варианта из AL (нижней части регистра AX)в регистр eax для вывода результата на экран с помощью подпрограммы iprintLF.

# Выводы

В ходе выполнения работы, я освоил работу с арифметическими операциями на
языке assebly.

# Список литературы{.unnumbered}
GDB: The GNU Project Debugger. — URL: https://www.gnu.org/software/gdb/.
GNU Bash Manual. — 2016. — URL: https://www.gnu.org/software/bash/manual/.
Midnight Commander Development Center. — 2021. — URL: https://midnight-commander.org/.
NASM Assembly Language Tutorials. — 2021. — URL: https://asmtutor.com/.
Newham C. Learning the bash Shell: Unix Shell Programming. — O’Reilly Media, 2005. — 354 с. — (In a Nutshell). — ISBN 0596009658. — URL: http://www.amazon.com/Learning-
bash-Shell-Programming-Nutshell/dp/0596009658.
Robbins A. Bash Pocket Reference. — O’Reilly Media, 2016. — 156 с. — ISBN 978-1491941591.
The NASM documentation. — 2021. — URL: https://www.nasm.us/docs.php.
Zarrelli G. Mastering Bash. — Packt Publishing, 2017. — 502 с. — ISBN 9781784396879.
Колдаев В. Д., Лупин С. А. Архитектура ЭВМ. — М. : Форум, 2018.
Куляс О. Л., Никитин К. А. Курс программирования на ASSEMBLER. — М. : Солон-Пресс,2017.
Новожилов О. П. Архитектура ЭВМ и систем. — М. : Юрайт, 2016.
Расширенный ассемблер: NASM. — 2021. — URL: https://www.opennet.ru/docs/RUS/nasm/.
Робачевский А., Немнюгин С., Стесик О. Операционная система UNIX. — 2-е изд. — БХВ-
Петербург, 2010. — 656 с. — ISBN 978-5-94157-538-1.
Столяров А. Программирование на языке ассемблера NASM для ОС Unix. — 2-е изд. —
М. : МАКС Пресс, 2011. — URL: http://www.stolyarov.info/books/asm_unix.
Таненбаум Э. Архитектура компьютера. — 6-е изд. — СПб. : Питер, 2013. — 874 с. —
(Классика Computer Science).
 Таненбаум Э., Бос Х. Современные операционные системы. — 4-е изд. — СПб. : Питер,2015 — 1120 с. — (Классика Computer Science).
::: {#refs}
:::
