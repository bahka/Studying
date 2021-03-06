
# Операции с целыми числами
### Сложение
```
>>> 2 + 5
 7
```

### Вычитание
```
>>> 10 - 5
5
```

### Умножение
```
>>> 6 * 7
42
```

### Длинная арифметика  (большиче числа не приводят к ошибкам переполнения разрядов, как в других языках)

```
>>> 12345678 * 987654328765432318765
12193262318244164938266047670
```

### Деление

```
>>> 40 / 8
5.0
```

```
>>> 30 / 8
3.75
```

### Целоичисленное деление

```
>>> 40 // 8
5
```

```
>>> 30 // 8
3
```

```
>>> 42 // 8
5
```

### Взятие остатка (то, что остаётся в дробной части)
```
>>> 42 % 8
2
```

> Проверка: 5 * 8 + 2 = 42.
> Остаток не может быть отрицательным, всегда меньше основания, в данном случае 8.

```
>>> 3 % 8
3
```

```
>>> 239 % 10
9
```

### Возведение в степень 
```
>>> 5 ** 2 
25
```

```
>>> 3 ** 3
27
```


## Комбинация действий

### Порядок вычисления операций по умолчанию

```
>>> 3 + 5 * 4
23
```

### Скобки меняют порядок вычисления
```
>>> (3 + 5) * 4
32
```

```
>>> 239 // 10
23
```

```
>>> 2 ** 5
32
```

### Унарные операции
```
>>> - (42)
-42
```

```
>>> + (42)
42
```

```
>>> +-+42
-42
```

# Ошибки при вычислении
### Синтаксические ошибки
```
>>> -*42
  File "<ipython-input-16-85d397208f73>", line 1
    -*42
     ^
SyntaxError: invalid syntax
```

```
>>> * 23
  File "<stdin>", line 1
SyntaxError: can't use starred expression here
```

 
### Математические ошибки

```
>>> 5 // 0
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: integer division or modulo by zero
```

## Числа с плавающей точкой
```
>>> 0.5 + 0.3
0.8
```

```
>>> 5 / 2
2.5
```

```
>>> 5 // 2
2
```

```
>>> 1 / 3
0.3333333333333333
```

```
>>> 0.3 + 0.3 + 0.3
0.8999999999999999
```

### Взятие корня
```
>>> 9 ** 0.5
3.0
```

### Экспоненциальная запись числа и её перевод в десятичный вид.
```
>>> 5e-1
0.5
````

```
>>> 1234e2
123400.0
```

# Переменные
```
>>> a = 3  # присваиваем значение переменной, или инициализируем переменную а со значением 3
>>> a
3

>>> a += 4
>>> a
7

>>> 2 * a  # значение а не меняется, получается новое число
14

>>> a 
7
``` 

# Вывод данных на стандартный вывод

##### Для вывода значений в своих программах используйте функцию print(). Обратите внимание на наличие скобок при вызове функции print!
```
>>> a = 7
>>> print(a)
7
>>> print(2 * a)
14
``` 

##### Можно выводить диалоговые сообщения при 'общении' c пользователем. Но не отправляйте в проверочную систему программы, содержащие лишний вывод

```
>>> name = input('Enter your name: ')
Enter your name: Pavel

>>> print('Hello ', name)
Hello  Pavel
```

>  комментарий 'xxx' в input('xxx') также выводится на стандартный вывод, поэтому проверяющая система будет ругаться на него.

```
>>> a = int(input())
12

>>> print(a * 2)
24
```

```
>>> a = int(input())
5

>>> b = int(input())
7

>>> print(a * b)
35
```

# Логические операции
```
>>> a = int(input())
-234

>>> print(a > 0)   # -234 > 0 - Нет, значит False
False 
```

```
>>> a = int(input())
10

>>> print(a >= 10 and a < 100)   # 10 >= 10 and 10 < 100  - Да и Да - Да, значит True
True
```

```
>>> a = int(input())
23

>>> print(10 <= a < 100)   # короткая запись аналогичная 10 <= a and a < 100
True
````

### Множественное присваивание
```
>>> x1, x2, x3 = False, True, False

>>> not x1 or x2 and x3  # не False или True и False - True или True и False - True или False - True.
True
```

## Изменение порядка вычисления логических операций
> Добавляя скобки в выражения, можно изменить порядок вычисления и значение результирующего выражения. Если не уверены в приоритете операций, смело добавляйте скобки, чтобы быть уверенными в том, что выражение вычисляется именно так, как вы хотите
```
>>> ((not x1) or x2) and x3
False 
```

# Условия
```
>>> a = int(input())
5
>>> b = int(input())
10
>>> print(a / b)
0.5
```

```
>>> a = int(input())
5
>>> b = int(input())
0
>>> if b != 0:
...    print(a / b)
... else:
...    print('Деление невозможно')
...

Деление невозможно
```

```
>>> a = int(input())
4
>>> b = int(input())
0
>>> if b != 0:
...     print(a / b)
... else:
...     print('Деление невозможно')
...     b = int(input('Введите ненулевое значение '))
...     print(a / b)
...

Деление невозможно
Введите ненулевое значение 2
2.0
```

```
>>> a = int(input())
5
>>> b = int(input())
0
>>> if b != 0:
...    print(a / b)
... else:
...    print('Деление невозможно')
...    b = int(input('Введите ненулевое значение '))
...    if b == 0:
...        print('Вы не справились!')
...    else:
...        print(a / b)
...
Деление невозможно
Введите ненулевое значение 0
Вы не справились!
```


```
>>> x = int(input())
25
>>> if x % 2 == 0:
...    print('Четное')
... else:
...    print('Нечетное')
...
Нечетное
```

## Наибольшее из двух чисел

```
>>> a = 4
>>> b = 7
>>> if a >= b:
...    print(a)
... else:
...    print(b)
...
7
```

```
>>> a = 4
>>> b = 7
>>> m = a
>>> if b > m:
...    m = b
...
>>> print(m)
7
```

# Строки
```
>>> a = 'string'
>>> b = 'another string'
>>> print(a, b)
string another string
```

```
>>> print(a + b)  # конкатенация строк
stringanother string
```

### Многострочный комментарий* (многострочные строки/ док-стринг)
```
>>> a = '''    
... multiline
... comment 
... '''
>>> print(a)
             # 1ая строка вывода
multiline    # 2ая
comment      # 3ья
             # 4ая. Это потому что у нас на входе было 4 строки - 2 пустые, 2 с текстом.
```

```
>>> a = 'string'
>>> b = 'another string'
>>>  print(a + '\n' + b)  # вывод в двух различных строчках
string
another string
```

```
>>> 'string1'
'string1'
```


```
>>> "string2"
'string2'
```

```
>>> '''multiple lines
... string'''
'multiple lines\nstring'
```

```
>>> """multiple lines
... string with double qoutes"""
'multiple lines\nstring with double qoutes'
```

```
>>> 'abc' + 'def'
'abcdef'
```

```
>>> 'abc' * 3
'abcabcabc'
```


```
>>> len('abcdef')
6
```

```
>>> 'abc' == '''abc'''
True
```

```
>>> 'abc' < 'ac'
True
```

```
>>> 'abc' > 'ab'
True
```

```
>>> print('First line', '\n\n\n', 'Last line')
First line 


 Last line
```

```
>>> # это комментарий
>>> x = 5 # комментарий к действию
>>> '''
... Многострочный комментарий – это просто
... строка
... '''
'\nМногострочный комментарий – это просто\nстрока\n'
```
