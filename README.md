# YPIIS

# Мой проект

## Описание 
Напишите две функции. Первая функция заполняет массив случайными значениями, вторая функция выводит массив на экран

Вывести ФИО и дату рождения, самого младшего и самого старшего студента

## Установка
Клонируйте репозиторий:
```sh
https://github.com/hipster-x/YPIIS
```
## Первое задание.

Напишите две функции. Первая функция заполняет массив случайными значениями, вторая функция выводит массив на экран

```sh
import random

def generate_random_array(array_length, min_value, max_value):
  """
  Заполняет массив случайными числами в заданном диапазоне.

  Args:
    array_length: Длина массива.
    min_value: Минимальное значение случайного числа.
    max_value: Максимальное значение случайного числа.

  Returns:
    Массив, заполненный случайными числами.
  """

  random_array = [random.randint(min_value, max_value) for _ in range(array_length)]
  return random_array

def print_array(array):
  """
  Выводит массив на экран.

  Args:
    array: Массив, который нужно вывести.
  """

  for element in array:
    print(element)

# Пример использования

array_length = 10
min_value = 0
max_value = 100

random_array = generate_random_array(array_length, min_value, max_value)
print_array(random_array)

```
