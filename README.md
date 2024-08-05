<p align="center">
    <img src="https://github.com/avanslov/square_calculator_library/actions/workflows/main.yml/badge.svg?event=push">
    <a href="https://pypi.org/project/square-calculator-library/">
        <img src="https://img.shields.io/badge/Pypi-Square_calculator_library-black?&logo=Pypi">
    </a>

</p>

# EN

# Python library for calculating the area of geometric shapes

**The library allows you to calculate the area of geometric shapes:**
- Without specifying the type of the calculated figure
    - triangles on three sides;
    - circles by radius;
- Indicating the type of the calculated shape
    - rectangle;
    - Elipsa;
    - trapezoids.

It also allows you to determine the type of calculated shape, even when the shape type is not defined in compile time

## Stack

![Python](https://img.shields.io/badge/-Python-black?style=for-the-badge&logo=python)
![Unittest](https://img.shields.io/badge/-Unittest-black?style=for-the-badge&logo=unittest)

## Quick start
**Installation**

The library must be imported into the installed and activated virtual environment of the project.
```
pip install square-calculator-library
```
**Import**
```
from square_calculator.calculator import Square
```

**Application**
```
sq = Square(a=3, b=4, c=5)
print(sq.calculate())
>> 6.0
print(sq.figure_type)
>> 'rectangular triangle'
```

## How to use

The library helps you calculate the area of a geometric shape.
By default, it calculates the area of a triangle on three sides or a circle by radius.

**At the moment, the library allows you to calculate the area of the following geometric shapes:**
| Shape type | Necessary arguments | Instance Attributes | Example |
| -- | -- | -- | -- |
| Circle | radius | None | ```sq =Square(a=3)```<br>```>> sq.calculate()``` |
| Triangle | a, b, c (lengths of three sides) | None | ```sq = Square(a=3, b=4, c=6)```<br>```>> sq.calculate()``` |
| Right triangle | a, b, c (lengths of three sides) | None | ```sq = Square(a=3, b=4, c=5)```<br>```>> sq.calculate()``` |
| Square | a, b | figure_type | ```sq = Square(a=3, b=4)```<br>```>> sq.figure_type = constants[2] #rectangle```<br>```>> sq.calculate()``` |
| Ellipse | a, b | figure_type | ```sq = Square(a=3, b=4)```<br>```>> sq.figure_type = constants[1] #ellipse```<br>```>> sq.calculate()``` |
| Trapezoid | a, b, h (base lengths and heights) | figure_type, trapezoid_h | ```sq = Square(a=3, b=4)```<br>```>> sq.figure_type = constants[4] #trapezoid```<br>```>> sq.trapezoid_h = 5```<br>```>> sq.calculate()``` |

For the library to work correctly, when creating a class object, named arguments must be passed, the names can be arbitrary.

When creating an object of the Square class, you can pass an unlimited number of parameters.
This allows you to expand and refine the library by adding algorithms for calculating any geometric shapes and the ability to calculate the same geometric shapes in different ways.

> [!IMPORTANT]
> When creating an instance of the Square class, only named parameters must be passed
> **Wrong:**
> ```
> sq = Square(3, 4, 5)
> ```
>
> **That's right:**
> ```
> sq = Square(a=3, b=4, c=5)
> ```

Additionally calculates the area of an ellipse, rectangle, or trapezoid, respectively, if you redefine the instance attribute to the shape type:
- 'ellipse';
- 'rectangle';
- 'trapezoid'.

> [!TIP]
> The shape type can be set using the FIGURE_TYPES tuple from the constants file.

The library allows you to determine the type of the calculated shape after its calculation, even if the shape type was not set initially. The methods of the class will determine the type of the calculated shape themselves.

**You can get the type through the figure_type attribute, for example, like this:**

```
sq = Square(a=3, b=4, c=5)

print(sq.figure_type)

>> 'rectangular triangle'
```

## Tests

**The following tests have been written using the Unittest library:**

- Checking that the expected error is returned when transmitting non-positive values.

- Checking that the calculations correspond to the expected values when transmitting acceptable values.

- Checking that when transmitting acceptable values, the shape type corresponds to the expected one.

- Checking that an error is returned when trying to calculate the area of any geometric shapes except a triangle and a circle without assigning attributes to the instance of the figure_type and trapezoid_h parameters.

**How to run the tests**

1. Go to the tests directory `cd tests`;
2. Run the command `python3 tests.py `.

## Author

**Alexander Buchelnikov**

[![Personal-Website](https://img.shields.io/badge/-Personal_website-black?style=for-the-badge&logo=)](https://buchelnikov.ddns.net/)
[![Telegram](https://img.shields.io/badge/-Telegram-black?style=for-the-badge&logo=Telegram)](https://t.me/aleksandr_buchelnikov)
[![LinkedIn](https://img.shields.io/badge/-LinkedIn-black?style=for-the-badge&logo=LinkedIn)](https://www.linkedin.com/in/aleksandr-buchelnikov/)
[![E-mail](https://img.shields.io/badge/-E_mail-black?style=for-the-badge&logo=Gmail)](mailto:al.buchelnikov@gmail.com)


# RU
# Библиотека для Python для расчета площади геометрических фигур

**Библиотека позволяет рассчитывать площадь геометрических фигур:**
- Без указания типа рассчитываемой фигуры
    - треугольника по трем сторонам;
    - окружности по радиусу;
- C указанием типа рассчитываемой фигуры
    - прямоугольника;
    - элипса;
    - трапеции.

А также позволяет определить тип рассчитаной фигуры, даже когда тип фигуры не определен в compile time

## Стек

![Python](https://img.shields.io/badge/-Python-black?style=for-the-badge&logo=python)
![Unittest](https://img.shields.io/badge/-Unittest-black?style=for-the-badge&logo=unittest)

## Быстрый старт
**Установка**

В установленное и активированное виртуальное окружение проекта необходимо импортировать библиотеку.
```
pip install square-calculator-library
```
**Импорт**
```
from square_calculator.calculator import Square
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

**На данный момент билиотека позволяет рассчитать площадь следующих геометрических фигур:**
| Тип фигуры | Необходимые аргументы | Атрибуты экземпляра | Пример |
| -- | -- | -- | -- |
| Окружность | radius | None | ```sq = Square(a=3)```<br>```>> sq.calculate()``` |
| Треугольник | a, b, c (длины трёх сторон) | None | ```sq = Square(a=3, b=4, c=6)```<br>```>> sq.calculate()``` |
| Прямоугольный треугольник | a, b, c (длины трёх сторон) | None | ```sq = Square(a=3, b=4, c=5)```<br>```>> sq.calculate()``` |
| Квадрат | a, b | figure_type | ```sq = Square(a=3, b=4)```<br>```>> sq.figure_type = constants[2] #rectangle```<br>```>> sq.calculate()``` |
| Эллипс | a, b | figure_type | ```sq = Square(a=3, b=4)```<br>```>> sq.figure_type = constants[1] #ellipse```<br>```>> sq.calculate()``` |
| Трапеция | a, b, h (длины оснований и высоты) | figure_type, trapezoid_h | ```sq = Square(a=3, b=4)```<br>```>> sq.figure_type = constants[4] #trapezoid```<br>```>> sq.trapezoid_h = 5```<br>```>> sq.calculate()``` |

Для корректной работы библиотеки при создании объекта класса необходимо передавать именованые аргументы, имена могут быть произвольными.

При создании объекта класса Square можно передавать неограниченное число параметров.
Это позволяет расширять и дорабатывать библиотеку, добавляя в неё алгоритмы рассчетов любых геометрических фигур и возможности рассчитывать одни и те же геометрические фигуры различными способами.

> [!IMPORTANT]
> При создании экземпляра класса Square необходимо передавать только именованные параметры
> **Неправильно:**
> ```
> sq = Square(3, 4, 5)
> ```
>
> **Правильно:**
> ```
> sq = Square(a=3, b=4, c=5)
> ```

Дополнительно рассчитывает площадь соответственно элипса, прямоугольника или трапеции если переопределить атрибут экземпляра на тип фигуры:
- 'ellipse';
- 'rectangle';
- 'trapezoid'.

> [!TIP]
> Тип фигур можно задавать, используя кортеж FIGURE_TYPES из файла constants.

Библиотека позволет определить тип рассчитаной фигуры после её вычисления, даже, если тип фигуры не был задан изначально. Методы класса сами определят тип рассчитаной фигуры.

**Получить тип можно через атрибут figure_type, например, так:**

```
sq = Square(a=3, b=4, c=5)

print(sq.figure_type)

>> 'rectangular triangle'
```

## Тесты

**С использованием библиотеки Unittest написанны следующие тесты:**

- Проверка, что при передаче не положительных значений возвращается ожидаемая ошибка.

- Проверка, что при передаче допустимых значений расчёты соответствуют ожидаемым.

- Проверка, что при передаче допустимых значений тип фигуры соответствует ожидаемой.

- Проверка, что при попытке рассчитать площадь любых геометрических фигур кроме треугольника и окружности без назначений атрибутам экземпляра параметров figure_type и trapezoid_h возвращается ошибка.

**Как запустить тесты**

1. Перейдите в директорию tests `cd tests`;
2. Выполните команду `python3 tests.py`.

## Автор

**Александр Бучельников**

[![Personal-Website](https://img.shields.io/badge/-Personal_website-black?style=for-the-badge&logo=)](https://buchelnikov.ddns.net/)
[![Telegram](https://img.shields.io/badge/-Telegram-black?style=for-the-badge&logo=Telegram)](https://t.me/aleksandr_buchelnikov)
[![LinkedIn](https://img.shields.io/badge/-LinkedIn-black?style=for-the-badge&logo=LinkedIn)](https://www.linkedin.com/in/aleksandr-buchelnikov/)
[![E-mail](https://img.shields.io/badge/-E_mail-black?style=for-the-badge&logo=Gmail)](mailto:al.buchelnikov@gmail.com)