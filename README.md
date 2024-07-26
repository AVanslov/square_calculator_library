<p align="center">
    <img src="https://github.com/avanslov/square_calculator_library/actions/workflows/main.yml/badge.svg?event=push">
    <a href="https://pypi.org/project/square-calculator-library/">
        <img src="https://img.shields.io/badge/Pypi-Square_calculator_library-black?&logo=Pypi">
    </a>

</p>


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