# Estrurua de Repeticação

### While


```python
# Usando o loop while para imprimir os valores de 0 a 9
counter = 0
while counter < 10:
    print(counter)
    counter = counter + 1
```

    0
    1
    2
    3
    4
    5
    6
    7
    8
    9
    


```python
# Também é possível usar a claúsula else para encerrar o loop while
x = 0

while x < 10:
    print ('O valor de x nesta iteração é: ', x)
    print (' x ainda é menor que 10, somando 1 a x')
    x += 1
    
else:
    print ('Loop concluído!')
```

    O valor de x nesta iteração é:  0
     x ainda é menor que 10, somando 1 a x
    O valor de x nesta iteração é:  1
     x ainda é menor que 10, somando 1 a x
    O valor de x nesta iteração é:  2
     x ainda é menor que 10, somando 1 a x
    O valor de x nesta iteração é:  3
     x ainda é menor que 10, somando 1 a x
    O valor de x nesta iteração é:  4
     x ainda é menor que 10, somando 1 a x
    O valor de x nesta iteração é:  5
     x ainda é menor que 10, somando 1 a x
    O valor de x nesta iteração é:  6
     x ainda é menor que 10, somando 1 a x
    O valor de x nesta iteração é:  7
     x ainda é menor que 10, somando 1 a x
    O valor de x nesta iteração é:  8
     x ainda é menor que 10, somando 1 a x
    O valor de x nesta iteração é:  9
     x ainda é menor que 10, somando 1 a x
    Loop concluído!
    

### Pass, Break, Continue


```python
counter = 0
while counter < 100:
    if counter == 4:
        break
    else:
        pass
    print(counter)
    counter = counter + 1
```

    0
    1
    2
    3
    


```python
for verificador in "Python":
    if verificador == "h":
        continue
    print(verificador)
```

    P
    y
    t
    o
    n
    

### While e For juntos


```python
for i in range(2,30):
    j = 2
    counter = 0
    while j < i:
        if i % j == 0:
            counter = 1
            j = j + 1
        else:
            j = j + 1
    
    if counter == 0:
        print(str(i) + " é um número primo")
        counter = 0
    else:
        counter = 0
```

    2 é um número primo
    3 é um número primo
    5 é um número primo
    7 é um número primo
    11 é um número primo
    13 é um número primo
    17 é um número primo
    19 é um número primo
    23 é um número primo
    29 é um número primo
    
