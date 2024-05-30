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
## Первое задание

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

## Второе задание

Вывести ФИО и дату рождения, самого младшего и самого старшего студента

DataBase: EX2/Студенты.xlsx

```sh
students = [
    {"last_name": "Иванов", "first_name": "Иван", "birth_date": "2000-01-01"},
    {"last_name": "Петрова", "first_name": "Мария", "birth_date": "2001-02-02"},
    {"last_name": "Сидоров", "first_name": "Николай", "birth_date": "2002-03-03"},
    {"last_name": "Кузнецова", "first_name": "Ольга", "birth_date": "1998-04-04"},
    {"last_name": "Попова", "first_name": "Светлана", "birth_date": "2003-05-05"},
]

     

import datetime

def get_age(birth_date_str):
  birth_date = datetime.datetime.strptime(birth_date_str, "%Y-%m-%d").date()
  today = datetime.date.today()
  return today.year - birth_date.year

# Сортировка по дате рождения
sorted_students = sorted(students, key=lambda student: student["birth_date"])

# Самый младший студент
youngest_student = sorted_students[0]
youngest_age = get_age(youngest_student["birth_date"])
print(f"Самый младший студент: {youngest_student['last_name']} {youngest_student['first_name']}, возраст: {youngest_age}")

# Самый старший студент
oldest_student = sorted_students[-1]
oldest_age = get_age(oldest_student["birth_date"])
print(f"Самый старший студент: {oldest_student['last_name']} {oldest_student['first_name']}, возраст: {oldest_age}")
``` 
