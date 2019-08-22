# Listas


```python
# Declarando um lista
listadomercado = []
```


```python
type(listadomercado)
```




    list




```python
# Criando uma lista
listadomercado = ["ovos, farinha, leite, maças"]
```


```python
# Imprimindo a lista
print(listadomercado)
```

    ['ovos, farinha, leite, maças']
    


```python
# Criando outra lista
listadomercado2 = ["ovos", "farinha", "leite", "maças"]
```


```python
# Imprimindo a lista
print(listadomercado2)
```

    ['ovos', 'farinha', 'leite', 'maças']
    


```python
# Criando lista
lista3 = [12, 100, "Universidade"]
```


```python
# Imprimindo
print(lista3)
```

    [12, 100, 'Universidade']
    


```python
lista3 = [12, 100, "Universidade"]
```


```python
# Atribuindo cada valor da lista a uma variável.
item1 = lista3[0]
item2 = lista3[1]
item3 = lista3[2]
```


```python
# Imprimindo as variáveis
print(item1, item2, item3)
```

    12 100 Universidade
    

## Atualizando um item da lista


```python
# Imprimindo um item da lista
listadomercado2[2]
```




    'leite'




```python
# Atualizando um item da lista
listadomercado2[2] = "chocolate"
```


```python
# Imprimindo lista alterada
listadomercado2
```




    ['ovos', 'farinha', 'chocolate', 'maças']



## Deletando um item da lista


```python
# Out of index. Não é possível deletar um item que não existe na lista
del listadomercado2[4]   
```


    ---------------------------------------------------------------------------

    IndexError                                Traceback (most recent call last)

    <ipython-input-115-84d96cb799fe> in <module>
          1 # Out of index. Não é possível deletar um item que não existe na lista
    ----> 2 del listadomercado2[4]
    

    IndexError: list assignment index out of range



```python
# Deletando um item específico da lista
del listadomercado2[3]
```


```python
# Imprimindo o item com a lista alterada
listadomercado2
```




    ['ovos', 'farinha', 'chocolate']



## Listas de listas (Listas aninhadas)
Listas de listas são matrizes em Python


```python
# Criando uma lista de listas
listas = [[1,2,3], [10,15,14], [10.1,8.7,2.3]]
```


```python
# Imprimindo a lista
listas
```




    [[1, 2, 3], [10, 15, 14], [10.1, 8.7, 2.3]]




```python
# Atribuindo um item da lista a uma variável
a = listas[0]
```


```python
a
```




    [1, 2, 3]




```python
b = a[0]
```


```python
b
```




    1




```python
list1 = listas[1]
```


```python
list1
```




    [10, 15, 14]




```python
valor_1_0 = list1[0]
```


```python
valor_1_0
```




    10




```python
valor_1_2 = list1[2]
```


```python
valor_1_2
```




    14




```python
list2 = listas[2]
```


```python
list2
```




    [10.1, 8.7, 2.3]




```python
valor_2_0 = list2[0]
```


```python
valor_2_0
```




    10.1



### Operações com listas


```python
# Criando uma lista aninhada (lista de listas)
listas = [[1,2,3], [10,15,14], [10.1,8.7,2.3]]
```


```python
listas
```




    [[1, 2, 3], [10, 15, 14], [10.1, 8.7, 2.3]]




```python
# Atribuindo à variável a, o primeiro valor da primeira lista
a = listas[0][0]
```


```python
a
```




    1




```python
b = listas[1][2]
```


```python
b
```




    14




```python
c = listas[0][2] + 10
```


```python
c
```




    13




```python
d = 10
```


```python
d
```




    10




```python
e = d * listas[2][0]
```


```python
e
```




    101.0



### Concatenando listas


```python
lista_s1 = [34, 32, 56]
```


```python
lista_s1
```




    [34, 32, 56]




```python
lista_s2 = [21, 90, 51]
```


```python
lista_s2
```




    [21, 90, 51]




```python
# Concatenando listas
lista_total = lista_s1 + lista_s2
```


```python
lista_total
```




    [34, 32, 56, 21, 90, 51]



## Operador in


```python
# Criando uma lista
lista_teste_op = [100, 2, -5, 3.4]
```


```python
# Verificando se o valor 10 pertence a lista
print(10 in lista_teste_op)
```

    False
    


```python
# Verificando se o valor 100 pertence a lista
print(100 in lista_teste_op)
```

    True
    

## Funções Built-in


```python
# Função len() retorna o comprimento da lista
len(lista_teste_op)
```




    4




```python
# Função max() retorna o valor máximo da lista
max(lista_teste_op)
```




    100




```python
# Função min() retorna o valor mínimo da lista
min(lista_teste_op)
```




    -5




```python
# Criando uma lista
listadomercado2 = ["ovos", "farinha", "leite", "maças"]
```


```python
# imprimindo a listadomercado2
print(listadomercado2)
```

    ['ovos', 'farinha', 'leite', 'maças']
    


```python
# Adicionando um item à lista
listadomercado2.append("carne")
```


```python
listadomercado2
```




    ['ovos', 'farinha', 'leite', 'maças', 'carne']




```python
listadomercado2.append("carne")
```


```python
listadomercado2
```




    ['ovos', 'farinha', 'leite', 'maças', 'carne', 'carne']




```python
# Retorna a frequência de determinado elemento da lista 
listadomercado2.count("carne")
```




    2




```python
# Criando uma lista vazia
a = []
```


```python
print(a)
```

    []
    


```python
type(a)
```




    list




```python
a.append(10)
```


```python
a
```




    [10]




```python
a.append(50)
```


```python
a
```




    [10, 50]




```python
old_list = [1,2,5,10]
```


```python
new_list = []
```


```python
# não há elementos em new_lista
new_list
```




    []




```python
# Copiando os itens de uma lista para outra
for item in old_list:
    new_list.append(item)
```


```python
new_list
```




    [1, 2, 5, 10]




```python
c = [20,30]
```


```python
c.append(60)
```


```python
c.append(70)
```


```python
c
```




    [20, 30, 60, 70]




```python
c.count(20)
```




    1



# Lista nome de cidades


```python
# lista de cidades
cidades = ['Recife', 'Manaus', 'Salvador']
```


```python
# add elementos a lista 
cidades.extend(['Fortaleza', 'Palmas'])
```


```python
print(cidades)
```

    ['Recife', 'Manaus', 'Salvador', 'Fortaleza', 'Palmas']
    


```python
# add mais elementos a lista
cidades.append('Maceió')
```


```python
# imprime lista com novo elemento
print(cidades)
```

    ['Recife', 'Manaus', 'Salvador', 'Fortaleza', 'Palmas', 'Maceió']
    


```python
cidades.index('Salvador')
```




    2



Lembre-se: em Python o índice começa por 0!


```python
# Procurando um elemento que não está na lista: ERRO!
cidades.index('Rio de Janeiro')
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-188-6c94f4f55ba6> in <module>
          1 # Procurando um elemento que não está na lista: ERRO!
    ----> 2 cidades.index('Rio de Janeiro')
    

    ValueError: 'Rio de Janeiro' is not in list



```python
# Como em python o index começa em 0, temos que a posição de Manaus será 1. 
cidades.index('Manaus')
```




    1




```python
cidades
```




    ['Recife', 'Manaus', 'Salvador', 'Fortaleza', 'Palmas', 'Maceió']




```python
# Inserindo números na lista de cidades
cidades.insert(2, 110)
```


```python
cidades
```




    ['Recife', 'Manaus', 110, 'Salvador', 'Fortaleza', 'Palmas', 'Maceió']




```python
# Remove um item da lista
cidades.remove(110)
```


```python
cidades
```




    ['Recife', 'Manaus', 'Salvador', 'Fortaleza', 'Palmas', 'Maceió']




```python
# Reverte a lista
cidades.reverse()
```


```python
# Imprime a lista
cidades
```




    ['Maceió', 'Palmas', 'Fortaleza', 'Salvador', 'Manaus', 'Recife']




```python
x = [3, 4, 2, 1]
```


```python
x
```




    [3, 4, 2, 1]




```python
# Ordena a lista
x.sort()
```


```python
x
```




    [1, 2, 3, 4]


