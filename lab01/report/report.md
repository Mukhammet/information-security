---
# Front matter
lang: ru-RU
title: "Отчет по лабораторной работе №1"
subtitle: "Установка и конфигурация операционной системы на виртуальную машину"
author: "Гурбангельдиев Мухаммет НФИбд-03-18"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Последовательность выполнения работы

Загрузить в дисплейном классе операционную систему Linux. Осуществить вход в систему.

Запустить терминал. Перейти в каталог /var/tmp:

cd /var/tmp

Создать каталог с именем пользователя (желательно совпадающим с логином студента в дисплейном классе), например, mgurbangeldiev:

Скопировать образ виртуальной машины и переместить в каталог mgurbangeldiev (рис. -@fig:001)

![Каталог mgurbangeldiev с образом виртуальной машины](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(737).png?raw=true){ #fig:001 width=70% }


Запустить виртуальную машину, введя VirtualBox в командной строке (рис. -@fig:002)

![Менеджер VirtualBox](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(738).png?raw=true){ #fig:002 width=70% }


Проверить в свойствах VirtualBox месторасположение каталога для
виртуальных машин. Для этого в VirtualBox выбрать Файл потом Свойства, вкладка Общие. В поле Папка для машин должно стоять /var/tmp/имя_пользователя где имя_пользователя — логин (учётная запись) студента в дисплейном классе. Если указан другой каталог, то изменить его, как указано выше. (рис. -@fig:004)

![Окно «Свойства» VirtualBox](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(739).png?raw=true){ #fig:003 width=70% }


Создать новую виртуальную машину. Для этого в VirtualBox выбрать Машина потом Создать.

Указать имя виртуальной машины — Base, тип операционной системы — Linux, RedHat. (рис. -@fig:004)

![Окно «Имя машины и тип ОС»](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(741).png?raw=true){ #fig:004 width=70% }


Указать размер основной памяти виртуальной машины — 1024 МБ. (рис. -@fig:005)

![Окно «Размер основной памяти»](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(743).png?raw=true){ #fig:005 width=70% }


Задать конфигурацию жёсткого диска — загрузочный, VDI (BirtualBox Disk Image), динамический виртуальный диск.

![Окно «Виртуальный жёсткий диск»](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(744).png?raw=true){ #fig:006 width=70% }

![Окно «Мастер создания нового виртуального диска»](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(745).png?raw=true){ #fig:007 width=70% }

![Окно «Дополнительные атрибуты виртуального диска»](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(746).png?raw=true){ #fig:008 width=70% }


Задать размер диска — 40 ГБ, его расположение — в данном случае /var/tmp/имя_пользователя/Base/Base.vdi (рис. -@fig:09)

![Окно «Расположение и размер виртуального диска»](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(747).png?raw=true){ #fig:09 width=70% }


Далее нам нужно проверить, что папка Base имеет путь к /var/tmp/имя_пользователя/Base/Snapshots. (рис. -@fig:010)

![Окно «Свойства» виртуальной машины Base](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(748).png?raw=true){ #fig:010 width=70% }  

Теперь нам нужно добавить новый привод оптических дисков и выбрать образ, который мы переместили к /var/tmp/mgurbangeldiev (рис. -@fig:011)  

![Окно «Носители» виртуальной машины Base: выбор образа оптического диска](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(750).png?raw=true){ #fig:011 width=70% }

![Окно «Носители» виртуальной машины Base](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(751).png?raw=true){ #fig:012 width=70% }


Запустить виртуальную машину Base, выбрать установку системы на жёсткий диск. Далее устанавливаем русский язык для интерфейса и раскладки клавиатуры (рис. -@fig:013)

![Виртуальная машина Base. Установка русского языка](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(753).png?raw=true){ #fig:013 width=70% }

![Виртуальная машина Base. Установка русского языка для раскладки клавиатуры ](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(754).png?raw=true){ #fig:014 width=70% }


В качестве имени машины указать «имя_пользователя.localdomain».(рис. -@fig:015)

![Задать сетевое имя виртуальной машины](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(755).png?raw=true){ #fig:015 width=70% }


Указать часовой пояс «Москва».(рис. -@fig:016)

![Указать часовой пояс «Москва»](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(756).png?raw=true){ #fig:016 width=70% }


Установить пароль для root (рис. -fig:017)

![Указать часовой пояс «Москва»](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(757).png?raw=true){ #fig:017 width=70% }

Также мы выбрали Сервер с GUI и по умолчанию установили Средства разработки.

![Выбор программ](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(759).png?raw=true){ #fig:018 width=50% }

![Конфигурация жёсткого диска](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(760).png?raw=true){ #fig:019 width=50% }

![Отключение KDUMP](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(761).png?raw=true){ #fig:020 width=50% }

После того как установили переходим к следующим действиям.

Принимаем лицензию.(рис. -@fig:021)

![Информация о лицензии](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(762).png?raw=true){ #fig:021 width=70% }

Далее создаем пользователя. (рис. -@fig:022)

![Настройка виртуальной машины: учётная запись](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(764).png?raw=true){ #fig:022 width=70% }

Подключиться к виртуальной машине с помощью созданной учётной записи. (рис. -@fig:023)

![Подключение к виртуальной машине](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(766).png?raw=true){ #fig:023 width=70% }

Завершил настройки.(рис. -@fig:024)

![Завершение настроек](https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(767).png?raw=true){ #fig:024 width=70% }

Далее для повышения производительности и удобства использования нужно подключить образ диска Дополнений гостевой OC, состоящие из драйверов устройств и системных приложений, которые оптимизируют гостевую операционную систему.(рис. -@fig:025)

![https://github.com/Mukhammet/information-security/blob/master/lab01/picture/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20(768).png?raw=true](https://github.com/zikarimov/os-intro/blob/master/lab01/screen/27.png?raw=true){ #fig:025 width=70% }


# Выводы

Приобрел практические навыки установки операционной системы на виртуальную машину, также научился настраивать минимально необходимое для дальнейшей работы сервисов.
