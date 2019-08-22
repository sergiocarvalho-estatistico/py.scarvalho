# Exercícios Propostos

## Exercício 1

* Imprima na tela os números de 1 a 10. Use uma lista para armazenar os números.


```python
numeros = list(range(1, 11))
```


```python
numeros
```




    [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]



## Exercício 2

* Crie uma lista de 5 objetos e imprima na tela


```python
# Criando a lista com 5 objetos
lista_five_objects = ['object1',100,['gato',465,'numeros'],(10,'Eu sei','python'),'object5']
```


```python
# imprimindo a lista
lista_five_objects
```




    ['object1', 100, ['gato', 465, 'numeros'], (10, 'Eu sei', 'python'), 'object5']



## Exercício 3 

* Crie duas strings e concatene as duas em uma terceira string


```python
string1 = 'Sérgio'
```


```python
string2 = ' Carvalho'
```


```python
# concatenando as strings
string1 + string2
```




    'Sérgio Carvalho'



## Exercício 4

*  Crie uma tupla com os seguintes elementos: 1, 2, 2, 3, 4, 4, 4, 5 


```python
tupla1 = (1,2,3,4,4,4,5)
```

### Utilize a função count 


```python
tupla1.count(4)
```




    3



## Exercício 5

* Crie um dicionário vazio e imprima na tela


```python
## Criando um dicionário vazio
dicionario = {}
```


```python
## Imprimindo o dicionário vazio
dicionario
```




    {}



## Exercício 6 

* Crie um dicionário com 3 chaves e 3 valores e imprima na tela


```python
dicionario = {'Nome':'Sérgio','Idade':43,'Profissão':'Estatístico'}
```


```python
print(dicionario)
```

    {'Nome': 'Sérgio', 'Idade': 43, 'Profissão': 'Estatístico'}
    

## Exercício 7

* Adicione mais um elemento ao dicionário criado no exercício anterior e imprima na tela


```python
dicionario['Hoby'] = 'Violonista' 
```


```python
dicionario
```




    {'Nome': 'Sérgio',
     'Idade': 43,
     'Profissão': 'Estatístico',
     'Hoby': 'Violonista'}



## Exercício 8

* Crie um dicionário com 3 chaves e 3 valores. Um dos valores deve ser uma lista de 2 elementos numéricos. 


```python
new_dic = {'Nome': 'Sérgio', "Idade":[43,6],'Profissão':'Estatístico'}
```

* Imprima o dicionário na tela


```python
new_dic
```




    {'Nome': 'Sérgio', 'Idade': [43, 6], 'Profissão': 'Estatístico'}



# Exercício 9

* Crie uma lista de 4 elementos. 
    * O primeiro elemento deve ser uma string, 
    * O segundo uma tupla de 2 elementos, o terceiro um dcionário com 2 chaves e 2 valores e 
    * O quarto elemento um valor do tipo float.


```python
lista = ['Sérgio',(10,20),{'Profissão':'Estatístico','Hobby':'Violonista'},[10.3,18.48,20.1] ]
```


```python
##### Imprima a lista na tela.
lista
```




    ['Sérgio',
     (10, 20),
     {'Profissão': 'Estatístico', 'Hobby': 'Violonista'},
     [10.3, 18.48, 20.1]]



## Exercício 10 

* Considere a string abaixo. Imprima na tela apenas os caracteres da posição 1 a 18.



```python
frase = 'Cientista de Dados é o profissional mais sexy do século XXI'
```


```python
len(frase)
```




    59




```python
frase[0:18]
```




    'Cientista de Dados'


