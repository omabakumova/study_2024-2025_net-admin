---
## Front matter
lang: ru-RU
title: Лабораторная работа № 14. Статическая маршрутизация в Интернете. Настройка
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

Настроить взаимодействие через сеть провайдера посредством статической
маршрутизации локальной сети организации с сетью основного здания, расположенного в 42-м квартале в Москве, и сетью филиала, расположенного
в г. Сочи.

# Задание

1. Настроить связь между территориями.

2. Настроить оборудование, расположенное в квартале 42 в Москве.

3. Настроить оборудование, расположенное в филиале в г. Сочи.

4. Настроить статическую маршрутизацию между территориями.

# Задание

5. Настроить статическую маршрутизацию на территории квартала 42 в г.
Москве.

6. Настроить NAT на маршрутизаторе msk-donskaya-gw-1.

7. При выполнении работы необходимо учитывать соглашение об именовании.


# Выполнение лабораторной работы

## Выполнение лабораторной работы

![42 квартал,Москва](image/1.png){#fig:001 width=50%}

## Выполнение лабораторной работы

![Ошибочный модуль](image/2.png){#fig:002 width=50%}

## Выполнение лабораторной работы

![Правильный модуль](image/3.png){#fig:003 width=50%}

## Настройка линка между площадками

![Информация о provider-omabakumova-sw-1](image/4.png){#fig:004 width=30%}

## Настройка линка между площадками

![Настройка интерфейсов коммутатора provider-omabakumova-sw-1](image/5.png){#fig:005 width=40%}

## Настройка линка между площадками

![Успешна настройка provider-omabakumova-sw-1](image/6.png){#fig:006 width=50%}

## Настройка линка между площадками

![Настройка интерфейсов маршрутизатора msk-donskaya-omabakumova-gw-1](image/7.png){#fig:007 width=50%}

## Настройка линка между площадками

![Предварительные результаты настройки msk-donskaya-omabakumova-gw-1](image/8.png){#fig:008 width=50%}

## Настройка линка между площадками

![Настройка интерфейсов маршрутизатора msk-q42-omabakumova-gw-1](image/9.png){#fig:009 width=50%}

## Настройка линка между площадками

![Пинг успешно проходит с msk-q42-omabakumova-gw-1](image/10.png){#fig:010 width=50%}

## Настройка линка между площадками

![Настройка интерфейсов коммутатора sch-sochi-omabakumova-sw-1](image/11.png){#fig:011 width=50%}

## Настройка линка между площадками

![Предварительные результаты настройки sch-sochi-omabakumova-sw-1](image/12.png){#fig:012 width=40%}

## Настройка линка между площадками

```

sch-sochi-omabakumova-gw-1> enable
sch-sochi-omabakumova-gw-1# configure terminal
sch-sochi-omabakumova-gw-1(config)# interface f0/0
sch-sochi-omabakumova-gw-1(config-if)#no shutdown
sch-sochi-omabakumova-gw-1(config-if)#exit
sch-sochi-omabakumova-gw-1(config)# interface f0 /0.6
sch-sochi-omabakumova-gw-1(config-subif)# encapsulation dot1Q 6
sch-sochi-omabakumova-gw-1(config-subif)#ip address 10.128.255.6 255.255.255.252
sch-sochi-omabakumova-gw-1(config-subif)# description donskaya
sch-sochi-omabakumova-gw-1(config-subif)#exit
sch-sochi-omabakumova-gw-1(config)#exit

```

## Настройка линка между площадками

![Предварительные результаты настройки sch-sochi-omabakumova-gw-1](image/13.png){#fig:013 width=50%}

## Настройка линка между площадками

![Пинг успешно проходит с sch-sochi-omabakumova-gw-1](image/14.png){#fig:014 width=50%}

## Настройка площадки 42-го квартала

![Настройка интерфейсов маршрутизатора msk-q42-omabakumova-gw-1 для настройки площадки 42 квартала](image/15.png){#fig:015 width=30%}

## Настройка площадки 42-го квартала

![Настройка интерфейсов коммутатора msk-q42-omabakumova-sw-1](image/16.png){#fig:016 width=50%}

## Настройка площадки 42-го квартала

![Задание шлюза у pc-q42-omabakumova-1](image/17.png){#fig:017 width=50%}

## Настройка площадки 42-го квартала

![Задание статического адреса у pc-q42-omabakumova-1](image/18.png){#fig:018 width=50%}

## Настройка площадки 42-го квартала

![Пингование в пределах 42 квартала](image/19.png){#fig:019 width=30%}

## Настройка площадки 42-го квартала

![Попытка пустить пинг за пределы области](image/20.png){#fig:020 width=50%}

## Настройка площадки 42-го квартала

![Настройка интерфейсов маршрутизирующего коммутатора msk-hostel-omabaumova-gw-1](image/21.png){#fig:021 width=30%}

## Настройка площадки 42-го квартала

![проверка проведенной настройки маршрутизирующего коммутатора msk-hostel-omabaumova-gw-1](image/22.png){#fig:022 width=50%}

## Настройка площадки 42-го квартала

![Пинг успешно проходит к msk-hostel-omabaumova-gw-1](image/23.png){#fig:023 width=50%}

## Настройка площадки 42-го квартала

![Настройка интерфейсов коммутатора msk-hostel-omabakumova-sw-1](image/24.png){#fig:024 width=50%}

## Настройка площадки 42-го квартала

![Задание шлюза у pc-hostel-omabakumova-1](image/25.png){#fig:025 width=50%}

## Настройка площадки 42-го квартала

![Задание статического адреса у pc-hostel-omabakumova-1](image/26.png){#fig:026 width=50%}

## Настройка площадки 42-го квартала

![Попытка пингования с pc-hostel-omabakumova-1](image/27.png){#fig:027 width=50%}

## Настройка площадки в Сочи

![Настройка интерфейсов маршрутизатора sch-sochi-omabakumova-gw-1](image/28.png){#fig:028 width=50%}

## Настройка площадки в Сочи

![Настройка интерфейсов коммутатора sch-sochi-omabakumova-sw-1](image/29.png){#fig:029 width=50%}

## Настройка площадки в Сочи

![Задание шлюза у pc-omabakumova-sochi-1](image/30.png){#fig:030 width=50%}

## Настройка площадки в Сочи

![Задание статического адреса у pc-omabakumova-sochi-1](image/31.png){#fig:031 width=50%}

## Настройка маршрутизации между площадками

![Настройка маршрутизатора msk-donskaya-omabakumova-gw-1](image/32.png){#fig:032 width=50%}

## Настройка маршрутизации между площадками

![Пинг оконечного устройства 42 квартала](image/33.png){#fig:033 width=50%}

## Настройка маршрутизации между площадками

![Пингование различных устройств](image/34.png){#fig:034 width=20%}

## Настройка маршрутизации между площадками

![Настройка маршрутизатора msk-q42-omabakumova-gw-1](image/35.png){#fig:035 width=50%}

## Настройка маршрутизации между площадками

![Повторная попытка пинования](image/36.png){#fig:036 width=50%}

## Настройка маршрутизации между площадками

![Пингование устройств 42 квартала](image/37.png){#fig:037 width=40%}

## Настройка маршрутизации между площадками

![Настройка маршрутизатора sch-sochi-omabakumova-gw-1](image/38.png){#fig:038 width=50%}

## Настройка маршрутизации на 42 квартале

![Настройка маршрутизации msk-q42-omabakumova-gw-1](image/39.png){#fig:039 width=50%}

## Настройка маршрутизации на 42 квартале

![Настройка маршрутизации msk-hostel-omabakumova-gw-1](image/40.png){#fig:040 width=50%}

## Настройка маршрутизации на 42 квартале

![Успешное пингование устройств](image/41.png){#fig:041 width=20%}

## Настройка NAT

![Настройка NAT на маршрутизаторе msk-donskaya-omabakumova-gw-1](image/42.png){#fig:042 width=50%}

## Настройка NAT

![Результаты предварительной настройки NAT на маршрутизаторе msk-donskaya-omabakumova-gw-1](image/43.png){#fig:043 width=50%}

## Настройка NAT

![Пингование www.yandex.ru](image/44.png){#fig:044 width=40%}

## Настройка NAT

![Пингование www.rudn.ru](image/45.png){#fig:045 width=40%}


# Выводы

В процессе выполнения лабораторной работы я настроила взаимодействие через сеть провайдера посредством статической
маршрутизации локальной сети организации с сетью основного здания, расположенного в 42-м квартале в Москве, и сетью филиала, расположенного
в г. Сочи.

