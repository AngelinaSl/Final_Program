# Итоговая работа

## Задача:
Написать программу, которая из имеющегося массива строк формирует массив из строк, длина которых меньше либо равна 3 символа. Первоначальный массив можно ввести с клавиатуры, либо задать на старте выполнения алгоритма. При решение не рекомендуется пользоваться коллекциями, лучше обойтись исключительно массивами

## Решение: 

1. Устанавливаем размерность исходного массива через ввод с клавиатуры. Для удобства реализации программы прописываем условие, в котором массив не должен быть больше 5ти. Также прописываем результат ввода некорректных чисел (если введенное число меньше или равно 0, на экран выведится сообщение о неправильных данных). 
2. Заполняем массив через метод **FillStringArray**. 
3. Для дальнейшей наглядности выводим исходный массив через метод **PrintStringArray**.
4. Через метод **FindSizeOfArrayRows** узнаем, сколько ячеек первого массива подходят под условие задачи (длина символов в строке не должна превышать 3). Тем самым мы узнаем, какого размера нужно создать второй массив (переменная **size**). *Прим. Можно также создать второй массив, равный длине первому. Но тогда, если в исходном массиве есть ячейки, не подходящие под условие, то во втором массиве будут пустые ячейки.*
5. Если в исходном массиве нет строк, подходящих под условие, выводим на консоль "[]".
6. Через метод **FillNewStringArray** создаем и заполняем массив:
* Создаем массив длиной **size**;
* Пробегаем *по всей длине* исходного массива, при этом, если длина строки меньше 4, то заполняем ячейку нового массива значением этой строки и прибавляем индекс второго массива;
* Если длина строки не соответствует условию задачи, то переходим на следующее значение первого массива. И так далее, пока не проверим все значения первого массива.
7. Через метод **PrintStringArray** распечатываем получившийся массив.
 

 ***Блок-схема алгоритма: Flowchart.jpg***

 ***Реализация программы: /Program/Program.cs***