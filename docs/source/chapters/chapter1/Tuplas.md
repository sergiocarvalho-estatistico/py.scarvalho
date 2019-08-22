# Tuplas

* O que são tuplas
    * Em python, tuplas são estruturas muito semelhante às listas, no entanto, ao contrário de listas, tuplas são imutáveis.
* Imutabilidade
    * As tuplas são imutáveis, o que significa que não podem ser alteradas. 
* Onde e quando Usar  
    * Você usaria tuplas para apresentar dados que não devem ser alterados, como os dias da semana ou a datas de um calendário.

## Criando uma tupla

Observe que ao criar uma tupla usamos os Parênteses (  ) 


```python
# Criando uma tupla
tupla1 = ("Geografia", 23, "Elefantes")
```


```python
# Imprimindo a tupla
tupla1
```




    ('Geografia', 23, 'Elefantes')



## Adição

* Como são imutáveis as tuplas não suportam adição/remoção de elementos.


```python
# Tuplas não suportam append()
tupla1.append("Chocolate")   
```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    <ipython-input-3-cb90e5e5a1a0> in <module>
          1 # Tuplas não suportam append()
    ----> 2 tupla1.append("Chocolate")
    

    AttributeError: 'tuple' object has no attribute 'append'


## Remoção

* Tuplas não suportam delete de um item específico


```python
del tupla1["Gatos"]  
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-9-24facd06bb21> in <module>()
          1 # Tuplas não suportam delete de um item específico
    ----> 2 del tupla1["Gatos"]
    

    TypeError: 'tuple' object does not support item deletion


* Tuplas podem ter um único item


```python
tupla1 = ("Chocolate")
```


```python
tupla1
```




    'Chocolate'




```python
tupla1 = ("Geografia", 23, "Elefantes")
```


```python
tupla1[0]
```




    'Geografia'



* Verificando o tamanho da tupla


```python
len(tupla1)
```




    3



* Slicing, da mesma forma que se faz com listas


```python
tupla1[1:]
```




    (23, 'Elefantes')




```python
tupla1.index('Elefantes')
```




    2



* Tuplas não suportam atribuição de item


```python
tupla1[1] = 21
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-11-59bcc25f7f2b> in <module>
          1 # Tuplas não suportam atribuição de item
    ----> 2 tupla1[1] = 21
    

    TypeError: 'tuple' object does not support item assignment



```python
# Deletando a tupla
del tupla1
```


```python
tupla1
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-13-9c021f243716> in <module>
    ----> 1 tupla1
    

    NameError: name 'tupla1' is not defined



```python
# Criando uma tupla
t2 = ('A', 'B', 'C')
```


```python
t2
```




    ('A', 'B', 'C')




```python
# Tuplas não suportam atribuição de item
t2[0] = 'D'
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-16-f90994f4060e> in <module>
          1 # Tuplas não suportam atribuição de item
    ----> 2 t2[0] = 'D'
    

    TypeError: 'tuple' object does not support item assignment



```python
# Usando a função list() para converter uma tupla para lista
lista_t2 = list(t2)
```


```python
lista_t2
```




    ['A', 'B', 'C']




```python
lista_t2.append('D')
```


```python
# Usando a função tuple() para converter uma lista para tupla
t2 = tuple(lista_t2)
```


```python
t2
```




    ('A', 'B', 'C', 'D')


