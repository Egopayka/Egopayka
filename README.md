
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

def count_words_starting_with_e(text):
    words = text.split()
    count = 0
    for word in words:
        if word.startswith('е') or word.startswith('Е'):
            count += 1
    return count


text = "Ежевика и еда, еловые еще не, Елки, ехидным голосом, ел ужин."
count = count_words_starting_with_e(text)
print(count) 



s = "строка с двоеточиями:"
count_do = s.count("%")
s = s.replace(":", "%")
count_replace = s.count("%")
print(s)
print(count_do - count_replace)



s = "Эта строка содержит.. точки."
count_deleted = s.count(".")
s_without_dot = s.replace(".", "")
print(s_without_dot)
print(count_deleted)



array = [1, -2, -3, 4, -5, 6, 7, -8, -9, 10]
for i in range(len(array) - 1):
    if array[i] < 0 and array[i+1] < 0:
        print(array[i], array[i+1])
        
        
        
def find_min_index(arr):
    min_index = 0
    min_elem = min(arr)
    min_index = arr.index(min_elem)
    return min_index


N = int(input("Введите размер массива: "))
arr = []
for i in range(N):
    arr.append(int(input("Введите элемент массива: ")))
index = find_min_index(arr)
print("Индекс минимального элемента:", index)



arr = [10, 20, 5, 30, 12, 8, 25, 18]
for i in range(len(arr)):
    if arr[i] < 15:
        arr[i] *= 2
print(arr)



string = "ACbcCCHhha"
unique_chars = []
for char in string:
    if char not in unique_chars:
        unique_chars.append(char)
unique_chars.sort(key=lambda x: x.lower())
print(unique_chars)
