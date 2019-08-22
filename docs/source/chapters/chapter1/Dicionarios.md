# Dicionários

## Definição

* São estruturas de dados que implementam mapeamentos
* Um mapeamento é uma coleção de associações entre pares de valores
* O primeiro elemento do par é chamado de chave e o outro de conteúdo
* De certa forma, um mapeamento é uma generalização da idéia de acessar dados por índices, exceto que num mapeamento os índices (ou chaves) podem ser de qualquer tipo imutável

* Relembrando o que é uma lista 


```python
# Isso é uma lista
estudantes_lst = ["Mateus", 24, "Fernanda", 22, "Tamires", 26, "Cristiano", 25]   
```


```python
estudantes_lst
```




    ['Mateus', 24, 'Fernanda', 22, 'Tamires', 26, 'Cristiano', 25]



## Construindo um Dicionário


```python
# Isso é um dicionário
estudantes_dict = {"Mateus":24, "Fernanda":22, "Tamires":26, "Cristiano":25}
```


```python
estudantes_dict 
```




    {'Mateus': 24, 'Fernanda': 22, 'Tamires': 26, 'Cristiano': 25}




```python
estudantes_dict["Mateus"]
```




    24




```python
estudantes_dict["Pedro"] = 23
```


```python
estudantes_dict["Pedro"]
```




    23




```python
estudantes_dict
```




    {'Mateus': 24, 'Fernanda': 22, 'Tamires': 26, 'Cristiano': 25, 'Pedro': 23}




```python
estudantes_dict["Tamires"]
```




    26




```python
estudantes_dict.clear()
```


```python
estudantes_dict
```




    {}




```python
del estudantes_dict
```


```python
estudantes_dict
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-13-29b87ec1321c> in <module>
    ----> 1 estudantes_dict
    

    NameError: name 'estudantes_dict' is not defined



```python
estudantes = {"Mateus":24, "Fernanda":22, "Tamires":26, "Cristiano":25}
```


```python
estudantes
```




    {'Mateus': 24, 'Fernanda': 22, 'Tamires': 26, 'Cristiano': 25}




```python
len(estudantes)
```




    4




```python
estudantes.keys()
```




    dict_keys(['Mateus', 'Fernanda', 'Tamires', 'Cristiano'])




```python
estudantes.values()
```




    dict_values([24, 22, 26, 25])




```python
estudantes.items()
```




    dict_items([('Mateus', 24), ('Fernanda', 22), ('Tamires', 26), ('Cristiano', 25)])




```python
estudantes2 = {"Maria":27, "Erika":28, "Milton":26}
```


```python
estudantes2
```




    {'Maria': 27, 'Erika': 28, 'Milton': 26}




```python
estudantes.update(estudantes2)
```


```python
estudantes
```




    {'Mateus': 24,
     'Fernanda': 22,
     'Tamires': 26,
     'Cristiano': 25,
     'Maria': 27,
     'Erika': 28,
     'Milton': 26}




```python
dic1 = {}
```


```python
dic1
```




    {}




```python
dic1["key_one"] = 2
```


```python
print(dic1)
```

    {'key_one': 2}
    


```python
dic1[10] = 5
```


```python
dic1
```




    {'key_one': 2, 10: 5}




```python
dic1[8.2] = "Python"
```


```python
dic1
```




    {'key_one': 2, 10: 5, 8.2: 'Python'}




```python
dic1["teste"] = 5
```


```python
dic1
```




    {'key_one': 2, 10: 5, 8.2: 'Python', 'teste': 5}




```python
dict1 = {}
```


```python
dict1
```




    {}




```python
dict1["teste"] = 10
```


```python
dict1["key"] = "teste"
```


```python
# Atenção, pois chave e valor podem ser iguais, mas representam coisas diferentes.
dict1
```




    {'teste': 10, 'key': 'teste'}




```python
dict2 = {}
```


```python
dict2["key1"] = "Big Data"
```


```python
dict2["key2"] = 10
```


```python
dict2["key3"] = 5.6
```


```python
dict2
```




    {'key1': 'Big Data', 'key2': 10, 'key3': 5.6}




```python
a = dict2["key1"]
```


```python
b = dict2["key2"]
```


```python
c = dict2["key3"]
```


```python
a, b, c
```




    ('Big Data', 10, 5.6)




```python
# Dicionário de listas
dict3 = {'key1':1230,'key2':[22,453,73.4],'key3':['leite','maça','batata']}
```


```python
dict3
```




    {'key1': 1230, 'key2': [22, 453, 73.4], 'key3': ['leite', 'maça', 'batata']}




```python
dict3['key2']
```




    [22, 453, 73.4]




```python
# Acessando um item da lista, dentro do dicionário
dict3['key3'][0].upper()
```




    'LEITE'




```python
# Operações com itens da lista, dentro do dicionário
var1 = dict3['key2'][0] - 2
```


```python
var1
```




    20




```python
# Duas operações no mesmo comando, para atualizar um item dentro da lista
dict3['key2'][0] -= 2
```


```python
dict3
```




    {'key1': 1230, 'key2': [20, 453, 73.4], 'key3': ['leite', 'maça', 'batata']}



### Criando dicionários aninhados


```python
# Criando dicionários aninhados
dict_aninhado = {'key1':{'key2_aninhada':{'key3_aninhada':'Dict aninhado em Python'}}}
```


```python
dict_aninhado
```




    {'key1': {'key2_aninhada': {'key3_aninhada': 'Dict aninhado em Python'}}}




```python
dict_aninhado['key1']['key2_aninhada']['key3_aninhada']
```




    'Dict aninhado em Python'


