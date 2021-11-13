---
## Front matter
lang: ru-RU
title: Дискреционное разграничение прав в Linux. Исследование влияния дополнительных атрибутов
author: Гурбангельдиев Мухаммет НФИбд-03-18

institute: RUDN University

date: Информационная безопасность, 13 ноября, 2021, Москва, Россия

## Formatting
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
toc: false
slide_level: 2
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true

---

# Цель лабораторной работы

Изучение механизмов изменения идентификаторов, применения SetUID- и Sticky-битов. Получение практических навыков работы в консоли с дополнительными атрибутами. Рассмотрение работы механизма смены идентификатора процессов пользователей, а также влияние бита Sticky на запись и удаление файлов.

# Процесс выполнения лабораторной работы

## Выполнение работы

1. Создание программы

2. Практическая работа с дополнительными атрибутами. SetUID- и SetGID- биты.

3. Исследование Sticky-бита


## Создание программы

### Результат

![Программа readfile.c](https://github.com/Mukhammet/information-security/blob/master/lab05/picture/12.png?raw=true){ #fig:001 width=70% }


## Практическая работа с дополнительными атрибутами. SetUID- и SetGID- биты.

### Результат

![Смена владельца и изменения прав](https://github.com/Mukhammet/information-security/blob/master/lab05/picture/16.jpg?raw=true){ #fig:002 width=50% }

![Проверка правильности установки новых атрибутов и смены владельца](https://github.com/Mukhammet/information-security/blob/master/lab05/picture/10.jpg?raw=true){ #fig:003 width=50% }


## Исследование Sticky-бита

### Результат

![Установленные права и разрешенные действия для групп](https://github.com/Mukhammet/information-security/blob/master/lab05/picture/19.jpg?raw=true){ #fig:004 width=40% }

![Установленные права и разрешенные действия для групп](https://github.com/Mukhammet/information-security/blob/master/lab05/picture/22.jpg?raw=true){ #fig:005 width=40% }


# Выводы

Изучил механизмы изменения идентификаторов, примененив SetUID- и Sticky-биты. Получил практические навыкы работы в консоли с дополнительными атрибутами. Рассмотрел работы механизмов смены идентификаторов процесса пользователей, а также влияние бита Sticky на запись и удаление файлов.
