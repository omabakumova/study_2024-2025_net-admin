---
## Front matter
lang: ru-RU
title: Лабораторная работа № 5. Конфигурирование VLAN
author:
  - Абакумова О. М.
institute:
  - Российский университет дружбы народов, Москва, Россия


## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
mainfont: Open Sans Light
---

# Информация

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Абакумова Олеся Максимовна
  * Студентка
  * Российский университет дружбы народов
  * 1132220832@pfur.ru
  * <https://github.com/omabakumova>

:::
::: {.column width="30%"}

![](./image/abakumova.png)

:::
::::::::::::::

# Цель работы

Получить основные навыки по настройке VLAN на коммутаторах сети.

# Задание

1. На коммутаторах сети настроить Trunk-порты на соответствующих интер-
фейсах, связывающих коммутаторы между
собой.
2. Коммутатор msk-donskaya-sw-1 настроить как VTP-сервер и прописать на
нём номера и названия VLAN.
3. Коммутаторы msk-donskaya-sw-2 — msk-donskaya-sw-4,msk-pavlovskaya-sw-1 настроить как VTP-клиенты, на интерфейсах указать
принадлежность к соответствующему VLAN.

# Задание

4. На серверах прописать IP-адреса.
5. На оконечных устройствах указать соответствующий адрес шлюза и прописать статические IP-адреса из диапазона соответствующей сети, следуя
регламенту выделения ip-адресов.
6. Проверить доступность устройств, принадлежащих одному VLAN, и недоступность устройств, принадлежащих разным VLAN.
7. При выполнении работы необходимо учитывать соглашение об именовании.

# Выполнение лабораторной работы

## Настройка Trunk-портов

![Настройка Trunk-порта для msk-donskaya-omabakumova-sw-1](image/1.png){#fig:001 width=40%}

## Настройка Trunk-портов

![Настройка Trunk-порта для msk-donskaya-omabakumova-sw-2](image/2.png){#fig:002 width=40%}

## Настройка Trunk-портов

![Настройка Trunk-порта для msk-donskaya-omabakumova-sw-3](image/3.png){#fig:003 width=40%}

## Настройка Trunk-портов

![Настройка Trunk-порта для msk-donskaya-omabakumova-sw-4](image/4.png){#fig:004 width=40%}

## Настройка Trunk-портов

![Настройка Trunk-порта(дополнительно) для msk-donskaya-omabakumova-sw-1](image/5.png){#fig:005 width=40%}

## Настройка Trunk-портов

![Настройка Trunk-порта для msk-pavlovskaya-omabakumova-sw-1](image/6.png){#fig:006 width=40%}

## Настройка VTP

![Настройка VLAN для msk-donskaya-omabakumova-sw-1](image/7.png){#fig:007 width=40%}

## Настройка VTP

![Вывод команды show vlan](image/8.png){#fig:008 width=40%}

## Настройка VTP

![Настройка msk-donskaya-omabakumova-sw-1, как VTP-сервера](image/9.png){#fig:009 width=40%}

## Настройка VTP

![Настройка msk-donskaya-omabakumova-sw-2, как VTP-клиента](image/10.png){#fig:010 width=40%}

## Настройка VTP

![Настройка msk-donskaya-omabakumova-sw-3, как VTP-клиента](image/11.png){#fig:011 width=40%}

## Настройка VTP

![Настройка msk-donskaya-omabakumova-sw-4, как VTP-клиента](image/12.png){#fig:012 width=40%}

## Настройка VTP

![Вывод команды show vtp](image/13.png){#fig:013 width=40%}

## Настройка VTP

![Вывод команды show vlan на msk-donskaya-omabakumova-sw-4](image/14.png){#fig:014 width=40%}

## Настройка VTP

![Настройка msk-pavlovskaya-omabakumova-sw-1, как VTP-клиента](image/15.png){#fig:015 width=40%}

## Настройка конфигурации портов

![Настройка конфигурации диапазона портов для msk-donskaya-omabakumova-sw-4](image/16.png){#fig:016 width=40%}

## Настройка конфигурации портов

![Настройка конфигурации диапазона портов для msk-donskaya-omabakumova-sw-2](image/17.png){#fig:017 width=40%}

## Настройка конфигурации портов

![Настройка конфигурации диапазона портов для msk-donskaya-omabakumova-sw-3](image/18.png){#fig:018 width=40%}

## Настройка конфигурации портов

![Настройка конфигурации диапазона портов для msk-pavlovskaya-omabakumova-sw-1](image/19.png){#fig:019 width=40%}

## Настройка шлюзов и IP-адреса у оконечных устройств

![Настройка шлюза для оконечного устройства](image/20.png){#fig:020 width=40%}

## Настройка шлюзов и IP-адреса у оконечных устройств

![Настройка IP-адреса для оконечного устройства](image/21.png){#fig:021 width=40%}

## Пингование адресов

![Вывод команды ipconfig](image/22.png){#fig:022 width=40%}

## Пингование адресов

![Пингование IP-адресов](image/23.png){#fig:023 width=40%}

## Режим симуляции

![Пакеты успешно проходят](image/24.png){#fig:024 width=40%}

## Режим симуляции

![Информация PDU](image/25.png){#fig:025 width=40%}

## Режим симуляции

![Пакеты не проходят](image/26.png){#fig:026 width=40%}


# Выводы

Во время выполнения данной лабораторной работы я приобрела основные навыки по настройке VLAN на коммутаторах сети.



