### Тестовое задание Александров

#### <u>Задание 1</u>
<p>При приравнивании <code>a</code> к <code>b</code> и присвоению им значение <code>1</code> Python создал один адрес памяти. 
Значение переменной <code>b</code> фактически мы не изменяли, а создали другой объект с тем же именем и присвоили ему другое значение, поэтому адрес памяти изменился. Результат <code>a == b</code> — <b>False</b>.</p>
<p>При создании переменных <code>c</code> и <code>d</code> мы создаем один список, который имеет один адрес в памяти. Таким образом, после модификации одного из имени, значения второго также поменяется. Результат <code>c == d</code> — <b>True</b>

Так как <code>False</code> не равен <code>True</code>, <b>то результатом всего скрипта будет <code>False</code></b>.</p>

#### <u>Задание 2</u>

```python
import random 

def insert_random_numbers(count: int, initial: list = None) -> list:
    """Func inserts new random numbers to list"""
    if initial is None:
        initial = []
    for _ in range(count):
        random_number = random.randint(0, 100)
        initial.append(random_number)
    return initial
```
Я бы попросил исправить указанный список на <code>None</code>.

В аргументах функции в исходном коде <code>initial</code> присвоили пустой список. Данный список при каждом запуске функции будет пополняться, так как мы работаем с одним и тем же объектом. 

#### <u>Задание 3</u>

```python
def sort_rules(elem: str) -> (int, str):
    """Rules how to sort"""
    return -int(elem[2:]), elem[0]


def to_sort(arr: list) -> list:
    """Function to sort"""
    arr.sort(key=sort_rules)
    return arr
```