# Expressões Lambda

## Definindo uma função

* Em três linhas de código.


```python
def potencia(num):
    result = num**2
    return result
```


```python
potencia(5)
```




    25



* Definindo uma função com 2 linhas de código


```python
def potencia(num):
    return num**2
```


```python
potencia(5)
```




    25



* Definindo uma função - 1 linha de código


```python
def potencia(num): return num**2
```


```python
potencia(5)
```




    25




```python
# Definindo uma expressão lambda
potencia = lambda num: num**2
```


```python
potencia(5)
```




    25




```python
# Lembre: operadores de comparação retornam boolean, true or false
Par = lambda x: x%2==0
```


```python
Par(3)
```




    False




```python
Par(4)
```




    True




```python
first = lambda s: s[0]
```


```python
first('Python')
```




    'P'




```python
reverso = lambda s: s[::-1]
```


```python
reverso('Python')
```




    'nohtyP'




```python
addNum = lambda x,y : x+y
```


```python
addNum(2,3)
```




    5


