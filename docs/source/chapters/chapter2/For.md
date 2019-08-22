# Estrutura de Repetição

## Loop For

* Criando uma tupla e imprimindo cada um dos valores


```python
tp = (2,3,4)
for i in tp:
    print(i)
```

    2
    3
    4
    

* Criando uma lista e imprimindo cada um dos valores


```python
ListaDoMercado = ["Leite", "Frutas", "Carne"]
for i in ListaDoMercado:
    print(i)
```

    Leite
    Frutas
    Carne
    

* Imprimindo os valores no intervalo entre 0 e 5 (exclusive)


```python
for contador in range(0,5):
    print(contador)
```

    0
    1
    2
    3
    4
    

*  Imprimindo na tela os números pares da lista de números


```python
lista = [1,2,3,4,5,6,7,8,9,10]
for num in lista:
    if num % 2 == 0:
        print (num)
```

    2
    4
    6
    8
    10
    

* Listando os números no intervalo entre 0 e 101, com incremento em 2


```python
for i in range(0,101,2):  
    print(i)
```

    0
    2
    4
    6
    8
    10
    12
    14
    16
    18
    20
    22
    24
    26
    28
    30
    32
    34
    36
    38
    40
    42
    44
    46
    48
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
    

* Strings também são sequências


```python
for caracter in 'Python é uma linguagem de programação divertida!':
    print(caracter)
```

    P
    y
    t
    h
    o
    n
     
    é
     
    u
    m
    a
     
    l
    i
    n
    g
    u
    a
    g
    e
    m
     
    d
    e
     
    p
    r
    o
    g
    r
    a
    m
    a
    ç
    ã
    o
     
    d
    i
    v
    e
    r
    t
    i
    d
    a
    !
    

## Loops Aninhados


```python
for i in range(0,5):
    print(i)
    for a in range(0,5):
        print(a)
```

    0
    0
    1
    2
    3
    4
    1
    0
    1
    2
    3
    4
    2
    0
    1
    2
    3
    4
    3
    0
    1
    2
    3
    4
    4
    0
    1
    2
    3
    4
    

* Operando os valores de uma lista com loop for


```python
listaB = [32,53,85,10,15,17,19]
soma = 0
for i in listaB:
    double_i = i * 2
    soma += double_i

print(soma)
```

    462
    

* Loops em lista de listas


```python
listas = [[1,2,3], [10,15,14], [10.1,8.7,2.3]]
for valor in listas:
    print(valor)
```

    [1, 2, 3]
    [10, 15, 14]
    [10.1, 8.7, 2.3]
    

* Contando os itens de uma lista


```python
lista = [5,6,10,13,17]
count = 0
for item in lista:
    count += 1
    
print(count)
```

    5
    

* Contando o número de colunas


```python
lst = [[1,2,3],[3,4,5],[5,6,7]]
primeira_linha = lst[0]
count = 0
for column in primeira_linha:
    count = count + 1
    
print(count)
```

    3
    

* Pesquisando em listas


```python
listaC = [5, 6, 7, 10, 50]

# Loop através da lista
for item in listaC:
    if item == 5:
        print("Número encontrado na lista!")
```

    Número encontrado na lista!
    

* Listando as chaves de um dicionário


```python
dict = {'k1':'Python','k2':'R','k3':'Scala'}
for item in dict:
    print(item)
```

    k1
    k2
    k3
    

* Imprimindo chave e valor do dicionário. Usando o método items() para retornar os itens de um dicionário


```python
for k,v in dict.items():
    print (k,v)
```

    k1 Python
    k2 R
    k3 Scala
    
