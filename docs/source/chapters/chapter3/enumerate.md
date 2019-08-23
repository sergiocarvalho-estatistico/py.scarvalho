# Enumerate()

* A função enumerate permite retornar o indice de cada valor em uma sequência, à medida que você percorre toda a sequência.
* Enumerate retorna uma tupla no formato tupla(indice,valor).

### Vejamos 

* Criando uma lista


```python
seq = ['a','b','c']
```

* Aplicando a função enumerate() à sequência seq. 


```python
enumerate(seq)
```




    <enumerate at 0x1e061d40e10>



* Note que do nosso imput, que é uma lista, nos é retornado um objeto tupla com os indices e os valores da lista de imput.


```python
list(enumerate(seq))
```




    [(0, 'a'), (1, 'b'), (2, 'c')]



* Imprimindo os valores de uma lista com a função enumerate() e seus respectivos índices


```python
for indice, valor in enumerate(seq):
    print(indice, valor)
```

    0 a
    1 b
    2 c
    

* Imprimindo os valores sob uma condição.


```python
for indice, valor in enumerate(seq):
    if indice >= 2:
        break
    else:
        print (valor)
```

    a
    b
    

* Nova lista


```python
lista = ['Marketing', 'Tecnologia', 'Business']
```

* Aplicando a função enumerate() e imprimindo os elementos da tupla.


```python
for i, item in enumerate(lista):
    print(i, item)
```

    0 Marketing
    1 Tecnologia
    2 Business
    

* Retonando os indices e elementos de uma string.


```python
for i, item in enumerate('Isso é uma string'):
    print(i, item)
```

    0 I
    1 s
    2 s
    3 o
    4  
    5 é
    6  
    7 u
    8 m
    9 a
    10  
    11 s
    12 t
    13 r
    14 i
    15 n
    16 g
    


```python
for i, item in enumerate(range(10)):
    print(i, item)
```

    0 0
    1 1
    2 2
    3 3
    4 4
    5 5
    6 6
    7 7
    8 8
    9 9
    
