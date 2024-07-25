# Библиотека для Python для расчета площади геометрических фигур

## Стек

![Python](https://img.shields.io/badge/-Python-black?style=for-the-badge&logo=python)
![Unittest](https://img.shields.io/badge/-Unittest-black?style=for-the-badge&logo=unittest)

## Быстрый старт
**Установка**

В установленное и активированное виртуальное окружение проекта необходимо импортировать библиотеку.
```
pip install square_calculator
```
**Импорт**
```
from square_calculator import calculator
```

**Применение**
```
sq = Square(a=3, b=4, c=5)
print(sq.calculate())
>> 6.0
print(sq.figure_type)
>> 'rectangular triangle'
```

## Как использовать

Библиотека помогает рассчитывать площадь геометрической фигуры.
По умолчанию рассчитывает площадь треугольника по трем сторонам или окружности по радиусу.

Для корректной работы библиотеки при создании объекта класса необходимо передавать именованые аргументы, имена могут быть произвольными.

При создании объекта класса Square можно передавать неограниченное число параметров.
Это позволяет расширять и дорабатывать библиотеку, добавляя в неё алгоритмы рассчетов любых геометрических фигур и возможности рассчитывать одни и те же геометрические фигуры различными способами.

**Неправильно:**
```
sq = Square(3, 4, 5)
```

**Правильно:**
```
sq = Square(a=3, b=4, c=5)
```

Если передать в аргументах тип фигуры:
'ellipse', 'rectangle' или 'trapezoid'
рассчитывает площадь соответственно
элипса, прямоугольника или трапеции.

Тип фигур можно задавать,
используя кортеж FIGURE_TYPES из файла constants.

Определить тип рассчитаной фигуры можно через атрибут figure_type, например, так:

```
sq = Square(a=3, b=4, c=5)

print(sq.figure_type)

>> 'rectangular triangle'
```

## Как запустить тесты

### Автор

**Александр Бучельников**

[![Personal-Website](https://img.shields.io/badge/-Personal_website-black?style=for-the-badge&logo=)](https://buchelnikov.ddns.net/)
[![Telegram](https://img.shields.io/badge/-Telegram-black?style=for-the-badge&logo=Telegram)](https://t.me/aleksandr_buchelnikov)
[![LinkedIn](https://img.shields.io/badge/-LinkedIn-black?style=for-the-badge&logo=LinkedIn)](https://www.linkedin.com/in/aleksandr-buchelnikov/)
[![E-mail](https://img.shields.io/badge/-E_mail-black?style=for-the-badge&logo=Gmail)](mailto:al.buchelnikov@gmail.com)