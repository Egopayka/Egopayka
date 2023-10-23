
## О программисте

Я программист с двухлетним опытом работы в сфере разработки. Полюбил программирование еще со школьных лет, и с тех пор стараюсь постоянно совершенствоваться и изучать новые технологии.

## Что делаю

Я увлекаюсь разработкой системных приложений. Мое основное направление - Python. Часто работаю с базами данных.
[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&color=12F7E6&center=%D0%9B%D0%9E%D0%96%D0%AC&vCenter=%D0%9B%D0%9E%D0%96%D0%AC&repeat=%D0%B8%D1%81%D1%82%D0%B8%D0%BD%D0%BD%D1%8B%D0%B9&random=%D0%9B%D0%9E%D0%96%D0%AC&width=435&lines=%D0%AF+%D0%BD%D0%B5+%D0%B8%D1%89%D1%83+%D0%B4%D1%80%D0%B0%D0%BA%D0%B8%2C+%D0%BD%D0%BE+%D1%8F+%D0%BD%D0%B5+%D0%B1%D0%BE%D1%8E%D1%81%D1%8C+%D0%B5%D0%B5;%D0%AF+%D0%BD%D0%B5+%D0%BE%D0%B1%D0%B5%D1%89%D0%B0%D0%BB%2C+%D1%87%D1%82%D0%BE+%D0%B1%D1%83%D0%B4%D1%83+%D0%BC%D0%B8%D0%BB%D0%BE%D1%81%D0%B5%D1%80%D0%B4%D0%BD%D1%8B%D0%BC)](https://git.io/typing-svg)
## Что ты найдешь в моих проектах

Мои проекты на GitHub представляют собой различные приложения, библиотеки и инструменты, которые я создал в процессе обучения и для реализации различных идей.

## Контакты

- Если у тебя есть какие-либо вопросы или предложения, не стесняйся связаться со мной:
  - [Email](mailto:grigoriev4.ea@edu.spbstu.ru)

## Открыт для сотрудничества

Я всегда открыт для интересных проектов, совместных идей и сотрудничества. Если у тебя есть какое-либо предложение, буду рад его обсудить.

## Благодарность

Спасибо, что заглянул на мою страницу! Надеюсь, что найдешь здесь что-то интересное и полезное. Если у тебя есть какие-либо замечания или предложения по улучшению моих проектов или макета Readme, буду рад услышать их.



import random


# # Задание 1
# matrix = [[random.randint(1, 100) for _ in range(3)] for _ in range(3)]
# for i in range(3):
#   for j in range(3):
#     print(matrix[i][j], end = ' ')
#   print()
# max_column = max(row[2] for row in matrix)
# max_row = max(matrix[1])
# print("Максимальное значение третьего столбца:", max_column)
# print("Максимальное значение второй строки:", max_row)
# print('-' * 30)


# # Задание 2
# m = int(input("Введите количество строк массива m: "))
# n = int(input("Введите количество столбцов массива n: "))
# matrix = [[random.randint(-100, 100) for _ in range(n)] for _ in range(m)]
# new_matrix = [[1 if element > 0 else 0 for element in row] for row in matrix]
# print("Исходный массив:")
# for i in range(m):
#   for j in range(n):
#     print(matrix[i][j], end = ' ')
#   print()
# print("Новый массив:")
# for i in range(m):
#   for j in range(n):
#     print(new_matrix[i][j], end = ' ')
#   print()
# print('-' * 30)


# # Задание 3
# def is_magic_square(matrix):
#     sum_row = sum(matrix[0])
#     for row in matrix:
#         if sum(row) != sum_row:
#             return False
#     for j in range(len(matrix)):
#         if sum(matrix[i][j] for i in range(len(matrix))) != sum_row:
#             return False
#     if sum(matrix[i][i] for i in range(len(matrix))) != sum_row:
#         return False
#     if sum(matrix[i][len(matrix) - 1 - i] for i in range(len(matrix))) != sum_row:
#         return False
#     return True


# n = int(input("Введите порядок матрицы n: "))
# matrix = [[random.randint(1, 9) for _ in range(n)] for _ in range(n)]
# # matrix = [[1, 1, 1],[1, 1, 1],[1, 1, 1]]
# print("Сгенерированная матрица:")
# for i in range(n):
#   for j in range(n):
#     print(matrix[i][j], end = ' ')
#   print()
# if is_magic_square(matrix):
#     print("Матрица является магическим квадратом.")
# else:
#     print("Матрица не является магическим квадратом.")
# print('-' * 30)


# # Задание 4
# def create_random_matrix(n):
#     matrix = [[random.randint(1, 100) for _ in range(n)] for _ in range(n)]
#     return matrix


# def is_symmetric(matrix):
#     n = len(matrix)
#     for i in range(n):
#         for j in range(i + 1, n):
#             if matrix[i][j] != matrix[j][i]:
#                 return False
#     return True


# n = int(input("Введите порядок матрицы: "))
# matrix = create_random_matrix(n)
# # matrix = [[9,9,9],[9,9,9],[9,9,9]]
# print("Сгенерированная матрица:")
# for i in range(n):
#   for j in range(n):
#     print(matrix[i][j], end = ' ')
#   print()
# if is_symmetric(matrix):
#     print("Матрица симметрична относительно главной диагонали.")
# else:
#     print("Матрица не симметрична относительно главной диагонали.")
# print('-' * 30)


# # Задание 5
# def create_random_matrix_2(rows, cols):
#     matrix = [[random.randint(-100, 100) for _ in range(cols)] for _ in range(rows)]
#     return matrix


# def find_max_min_sum_rows(matrix):
#     max_sum = float('-inf')
#     min_sum = float('inf')
#     max_sum_row = None
#     min_sum_row = None
#     for i, row in enumerate(matrix):
#         row_sum = sum(row)
#         if row_sum > max_sum:
#             max_sum = row_sum
#             max_sum_row = i
#         if row_sum < min_sum:
#             min_sum = row_sum
#             min_sum_row = i
#     return max_sum_row, min_sum_row


# rows = int(input("Введите количество строк: "))
# cols = int(input("Введите количество столбцов: "))
# matrix = create_random_matrix_2(rows, cols)
# print("Сгенерированная матрица:")
# for i in range(rows):
#   for j in range(cols):
#     print(matrix[i][j], end = ' ')
#   print()
# max_sum_row, min_sum_row = find_max_min_sum_rows(matrix)
# print(f"Строка с наибольшей суммой элементов (сумма = {sum(matrix[max_sum_row])}): {matrix[max_sum_row]}")
# print(f"Строка с наименьшей суммой элементов (сумма = {sum(matrix[min_sum_row])}): {matrix[min_sum_row]}")
# print('-' * 30)


# Задание 6
def transform_matr(matr):
    return [[0 if x == min(row) and min(row) % 2 == 0 else 1 if x == min(row) and min(row) % 2 != 0 else x for x in row] for row in matr]
n = int(input("Введите количество строк: "))
m = int(input("Введите количество столбцов: "))
matr = []
number = 2
for i in range(m):
  brra = list()
  for j in range(n):
    brra.append(number)
    number += random.randint(1, 5)
  random.shuffle(brra)
  matr.append(brra)
print("Исходная матрица:")
for i in range(m):
  for j in range(n):
    print(matr[i][j], end = ' ')
  print()
transformed_matr = transform_matr(matr)
print("Преобразованная матрица:")
for i in range(m):
  for j in range(n):
    print(transformed_matr[i][j], end = ' ')
  print()
