# ksik4143answer

Конечно, вот решения семи задач на Python:

**Задача 1: Сумма чисел от 1 до n**

```python
n = int(input("Введите число n: "))
sum = 0
for i in range(1, n + 1):
    sum += i
print("Сумма чисел от 1 до", n, "равна", sum)
```

**Задача 2: Поиск простых чисел**

```python
def is_prime(num):
    if num < 2:
        return False
    for i in range(2, num):
        if num % i == 0:
            return False
    return True

start = 1
end = 100
print("Простые числа в диапазоне от", start, "до", end, ":")
for num in range(start, end + 1):
    if is_prime(num):
        print(num)
```

**Задача 3: Проверка палиндрома**

```python
def is_palindrome(s):
    s = s.lower().replace(" ", "")
    return s == s[::-1]

word = input("Введите слово или фразу: ")
if is_palindrome(word):
    print("Это палиндром.")
else:
    print("Это не палиндром.")
```

**Задача 4: Генерация чисел Фибоначчи**

```python
n = int(input("Сколько чисел Фибоначчи сгенерировать: "))
a, b = 0, 1
fibonacci_numbers = [a]
while len(fibonacci_numbers) < n:
    a, b = b, a + b
    fibonacci_numbers.append(a)
print("Первые", n, "чисел Фибоначчи:", fibonacci_numbers)
```

**Задача 5: Поиск наибольшего общего делителя (НОД)**

```python
def gcd(a, b):
    while a!=0 and b!=0:
        if a > b:
            a = a % b
        else:
            b = b % a
    print (a+b)

num1 = int(input("Введите первое число: "))
num2 = int(input("Введите второе число: "))
gcd(num1, num2)
```

**Задача 6: Сортировка списка (метод пузырька)**

```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n - i - 1):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]

numbers = [64, 34, 25, 12, 22, 11, 90]
bubble_sort(numbers)
print("Отсортированный список:", numbers)
```

**Задача 7: Палиндромные простые числа**

```python
def is_prime(num):
    if num < 2:
        return False
    for i in range(2, num):
        if num % i == 0:
            return False
    return True

def is_palindrome(s):
    s = str(s)
    return s == s[::-1]

n = int(input("Сколько палиндромных простых чисел найти: "))
count = 0
number = 2
while count < n:
    if is_prime(number) and is_palindrome(number):
        print(number, end=" ")
        count += 1
    number += 1
```

Надеюсь, что эти решения помогут вам лучше понять и практиковать программирование на Python.
