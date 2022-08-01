# Решение задач из Открытого курса машинного обучения от [ods.ai](ods.ai)
![img](https://sun1.dataix-kz-akkol.userapi.com/impg/Ik3pOdR-RLmYWeDE-H5EumwLzRGy9BO0iBgFrQ/6PdpCWAYUFo.jpg?size=1543x385&quality=96&sign=1c97ea39ea83acb4899139c75cf5f85b&type=album)

Все задачи были решены мною правильно и был получен максимальный балл. 

![image](https://user-images.githubusercontent.com/36912961/182090183-7b5c2255-c58a-4221-b28b-6d03e09d397e.png)

*Правда, к большому сожалению, из-за весенних событий в мире курс был приостановлен преподавателем и не был возобновлен до сих пор* :disappointed:

## Задача 1

Написать код, который вычисляет сумму всех чисел, удовлетворяющих следующие условия:

- положительные целые числа от 1 до 1_000_000_002 (один миллиард два) включительно
- которые нацело (без остатка) делятся на 3 (пример: 3, 6, 9, ...)
- и которые не заканчиваются на 4 и 7 (пример заканчивающихся на 4 и 7: 24, 27, 54, 57 ...)

## Задача 2

На вход поступает текстовый файл из 3-х тысяч строк

> Формат файла:
```    "арифметическая операция"    "целое число #1"    "целое число #2" ```

Разделитель - 4 пробела


Нужно подготовить текстовый файл из 1 строки.
Строка содержит набор из 3-х тысяч чисел, разделенных запятой. 
После последнего числа запятая не ставится.
каждое число - результат операции: 
    "результирующее целое число" = "целое число #1" применить "арифметическая операция" "целое число #2"

> *Пример входного файла:*
>```
>+    5    4
>-    -10449    -7623
>**    2    10
>```

>*Пример выходного файла (для примера входного файла выше):*
>```
>9,-2826,1024
>```

Допустимые операции:

- `+` (сложение)
- `-` (вычитание)
- `*` (умножение)
- `//` (целочисленное деление) (для этой операции подаются только положительные числа)- 
- `%` (остаток от деления) (для этой операции подаются только положительные числа)
- `**` (возведение в степень) (для этой операции подаются только положительные числа)
    
**Входные числа - только целые.
Выходные числа - только целые.**


## Задача 3

На вход поступает два текстовый файл из 3-х тысяч строк каждый.

- Первый файл содержит строки текста.   
 
- Второй файл содержит строки из двух целых неотрицательных чисел.

Первое число в строке всегда меньше или равно второму.

Числа всегда меньше длины соответствующей строки первого файла.

Соответствующей - это значит 1-ая строка из 1-го файла соответствует 1-ой строке из 2-го файла, а 123-я строка из 1-го файла соответствует 123-ей строке из 2-го файла.
 
- Подготовить выходной файл, который состоит из подстрок 1-го входного файла.
Подстроки разделены пробелами.
Какие брать подстроки - написано во втором файле.
В конце файла пробела нет.

Например:

    120 строка в 1-ом файле: JBOljrfkrfjgikenfjerkrkvkfKUGlknc
    120 строка во 2-ом файле: 13 27
    
Это значит 120 подстрока в результирующем файле это символы с 13 по 27, включая 13-ый и 27-ой символы.
Не забывайте, что нумерация символов в строке с 0.

Пример требуемой подстроки: `kenfjerkrkvkfKU`

**Пример 1-го входного файла:**

>```QxBpXEeyDWHiuTttWjhFMGTlrCMqpSvrNOQoxUbyiZombbLaYqBHvydPJlvdspwwpgeLNlHMVYrZvPsQkcQgPpierYSahialdXlde
>rNsZEKdYYlKKRrYGNWEXTYXOpQqrdGANRfoyeVvRwLVhZDfzKhFQkuSYODIXFLYafnXbxuwqZKQKjSiFZAtSponvmulcjicIDhNaQ
>TttSFLqbNkHvOeHSKTTGEEGxwtXImLeCmcKjvsIkIIvvlsUSazNuEsdDYlOljweSubVJxHbSJkBpByFiUCFctgrLKhlYgEWWuDYqx
>```


**Пример 2-го входного файла:**
>```30 84
>5 79
>70 70
>```


**Пример выходного файла:**
>```vrNOQoxUbyiZombbLaYqBHvydPJlvdspwwpgeLNlHMVYrZvPsQkcQgP >KdYYlKKRrYGNWEXTYXOpQqrdGANRfoyeVvRwLVhZDfzKhFQkuSYODIXFLYafnXbxuwqZKQKjSiF b```


## Задача 4

На вход поступает строка.

В ней хранится набор химических символов (He, O, H, Mg, Fe, ...). Без пробелов.
Нужно расшифровать химические символы в название химических элементов.
Для удобства, прилагается json файл, который ставит в соответствие химическому символу его химическое название.

**Как прочитать этот файл в словарь python (dict):**
```
periodic_table = json.load(open('periodic_table.json'))
```

**Пример входной строки:**

>`NOTiFICaTiON`

**Пример выходной строки:**

>`АзотКислородТитанФторЙодКальцийТитанКислородАзот`

Обратите внимание, что, например, "Bi" - это "Висмут", а не "БорЙод".
То есть регистр (заглавные или прописные) букв имеет значение.

Входная строка содержится в файле, скачайте его.
Полученную строку вставить в строку ниже.
