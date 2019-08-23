# Zip()

* zip(sequência1,sequência2)
* A função zip() agrega os valores de duas sequências e retorna uma sequência em um objeto tupla.
* zip() pode ser usada quando o número de elementos for diferente em cada sequência. Mas o objeto resultante será uma sequência de tamanho igual ao da menor sequência.


### Exemplo

* Criando duas listas


```python
x = [1,2,3]
y = [4,5,6]
```

* Unindo as listas. Em Python3 retorna um iterator


```python
zip(x, y)
```




    <zip at 0x16c55c08488>



* Perceba que zip retorna tuplas. Neste caso, uma lista de tuplas


```python
list(zip(x,y))
```




    [(1, 4), (2, 5), (3, 6)]



* Atenção quando as sequências tiverem número diferente de elementos


```python
list(zip('ABCD', 'xy'))
```




    [('A', 'x'), ('B', 'y')]



* Criando duas listas


```python
a = [1,2,3]
b = [4,5,6,7,8]
```

* Observe como o resultado da agregação das listas de número de elementos diferentes resulta em uma tupla com número de elementos igual ao da lista de menor elementos. 


```python
list(zip(a,b)) 
```




    [(1, 4), (2, 5), (3, 6)]



### Criando 2 dicionários


```python
d1 = {'a':1,'b':2}
d2 = {'c':4,'d':5}
```

* Zip vai unir as chaves


```python
list(zip(d1,d2))
```




    [('a', 'c'), ('b', 'd')]



* Zip pode unir os valores (itens)


```python
list(zip(d1, d2.values()))
```




    [('a', 4), ('b', 5)]



* Criando uma função para trocar valores entre 2 dicionários


```python
def trocaValores(d1, d2):
    dicTemp = {}
    
    for d1key, d2val in zip(d1,d2.values()):
        dicTemp[d1key] = d2val
    
    return dicTemp
```


```python
trocaValores(d1, d2)
```




    {'a': 4, 'b': 5}


