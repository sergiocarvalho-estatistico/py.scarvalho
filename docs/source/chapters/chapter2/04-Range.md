# Range

## Aplicação 

* Imprimindo números pares entre 50 e 101


```python
for i in range(50, 101, 2):
    print(i)
```

    50
    52
    54
    56
    58
    60
    62
    64
    66
    68
    70
    72
    74
    76
    78
    80
    82
    84
    86
    88
    90
    92
    94
    96
    98
    100
    


```python
for i in range(3, 6):
    print (i)
```

    3
    4
    5
    


```python
for i in range(0, -20, -2):
    print(i)
```

    0
    -2
    -4
    -6
    -8
    -10
    -12
    -14
    -16
    -18
    


```python
lista = ['Morango', 'Banana', 'Abacaxi', 'Uva']
lista_tamanho = len(lista)
for i in range(0, lista_tamanho):
    print(lista[i])
```

    Morango
    Banana
    Abacaxi
    Uva
    


```python
# Tudo em Python é um objeto
type(range(0,3))
```




    range


