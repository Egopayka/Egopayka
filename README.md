
![Приветствие](https://media.giphy.com/media/l41lTn7ryHYxbvsmA/giphy.gif)

## О программисте

Я программист с двухлетним опытом работы в сфере разработки. Полюбил программирование еще со школьных лет, и с тех пор стараюсь постоянно совершенствоваться и изучать новые технологии.

## Что делаю

Я увлекаюсь разработкой системных приложений. Мое основное направление - Python. Часто работаю с базами данных.

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


# Задание 1
matrix = [[random.randint(1, 100) for _ in range(3)] for _ in range(3)]
for row in matrix:
    print(row)
max_column = max(row[2] for row in matrix)
max_row = max(matrix[1])
print("Максимальное значение третьего столбца:", max_column)
print("Максимальное значение второй строки:", max_row)


# Задание 2
m = int(input("Введите количество строк массива m: "))
n = int(input("Введите количество столбцов массива n: "))
matrix = [[random.randint(-100, 100) for _ in range(n)] for _ in range(m)]
new_matrix = [[1 if element > 0 else 0 for element in row] for row in matrix]
print("Исходный массив:")
for row in matrix:
    print(row)
print("Новый массив:")
for row in new_matrix:
    print(row)
   
    
# Задание 3
def is_magic_square(matrix):
    sum_row = sum(matrix[0])
    for row in matrix:
        if sum(row) != sum_row:
            return False
    for j in range(len(matrix)):
        if sum(matrix[i][j] for i in range(len(matrix))) != sum_row:
            return False
    if sum(matrix[i][i] for i in range(len(matrix))) != sum_row:
        return False
    if sum(matrix[i][len(matrix) - 1 - i] for i in range(len(matrix))) != sum_row:
        return False
    return True


n = int(input("Введите порядок матрицы n: "))
matrix = [[random.randint(1, 9) for _ in range(n)] for _ in range(n)]
print("Сгенерированная матрица:")
for row in matrix:
    print(row)
if is_magic_square(matrix):
    print("Матрица является магическим квадратом.")
else:
    print("Матрица не является магическим квадратом.")


# Задание 4
def create_random_matrix(n):
    matrix = [[random.randint(1, 100) for _ in range(n)] for _ in range(n)]
    return matrix


def is_symmetric(matrix):
    n = len(matrix)
    for i in range(n):
        for j in range(i + 1, n):
            if matrix[i][j] != matrix[j][i]:
                return False
    return True


n = int(input("Введите порядок матрицы: "))
matrix = create_random_matrix(n)
print("Сгенерированная матрица:")
for row in matrix:
    print(row)
if is_symmetric(matrix):
    print("Матрица симметрична относительно главной диагонали.")
else:
    print("Матрица не симметрична относительно главной диагонали.")


# Задание 5
def create_random_matrix_2(rows, cols):
    matrix = [[random.randint(1, 100) for _ in range(cols)] for _ in range(rows)]
    return matrix


def find_max_min_sum_rows(matrix):
    max_sum = float('-inf')
    min_sum = float('inf')
    max_sum_row = None
    min_sum_row = None
    for i, row in enumerate(matrix):
        row_sum = sum(row)
        if row_sum > max_sum:
            max_sum = row_sum
            max_sum_row = i
        if row_sum < min_sum:
            min_sum = row_sum
            min_sum_row = i
    return max_sum_row, min_sum_row


rows = int(input("Введите количество строк: "))
cols = int(input("Введите количество столбцов: "))
matrix = create_random_matrix_2(rows, cols)
print("Сгенерированная матрица:")
for row in matrix:
    print(row)
max_sum_row, min_sum_row = find_max_min_sum_rows(matrix)
print(f"Строка с наибольшей суммой элементов (сумма = {sum(matrix[max_sum_row])}): {matrix[max_sum_row]}")
print(f"Строка с наименьшей суммой элементов (сумма = {sum(matrix[min_sum_row])}): {matrix[min_sum_row]}")


# Задание 6
def create_random_matrix_3(rows, cols):
    return [[random.randint(1, 100) for _ in range(cols)] for _ in range(rows)]


def transform_matrix(matrix):
    return [[0 if x == min(row) and min(row) % 2 == 0 else 1 if x == min(row) and min(row) % 2 != 0 else x for x in row] for row in matrix]
n = int(input("Введите количество строк: "))
m = int(input("Введите количество столбцов: "))
matrix = create_random_matrix_3(n, m)
print("Исходная матрица:")
for row in matrix:
    print(row)
transformed_matrix = transform_matrix(matrix)
print("Преобразованная матрица:")
for row in transformed_matrix:
    print(row)
    
