# Strings

## Criando uma String
Para criar uma string em Python você pode usar aspas simples ou duplas. Por exemplo:


```python
# Uma única palavra
'String'
```




    'String'




```python
# Uma frase
'Criando uma string em Python'
```




    'Criando uma string em Python'




```python
# Podemos usar aspas duplas
"Podemos usar aspas duplas ou simples para strings em Python"
```




    'Podemos usar aspas duplas ou simples para strings em Python'




```python
# Você pode combinar aspas duplas e simples
"Testando strings em 'Python'"
```




    "Testando strings em 'Python'"



## Imprimindo uma String


```python
print ('Testando Strings em Python')
```

    Testando Strings em Python
    


```python
print ('Testando \nStrings em \nPython')
```

    Testando 
    Strings em 
    Python
    


```python
print ('\n')
```

    
    
    

## Indexando Strings


```python
# Atribuindo uma string
s = 'Ciência de dados em python'
```


```python
print(s)
```

    Ciência de dados em python
    


```python
# O 1° elemento de uma string, indice 0
# O 2° pelo indice 1
# O 3° pelo indice 2
#       .
#       .
#       .
# O n° pelo indice n-1
s[0]
```




    'C'




```python
# O segundo elemento de um vetor de caracter é listado pelo indice 0. 
s[1]
```




    'i'




```python
s[2]
```




    'ê'



Podemos retornar os elementos de uma string de diferentes formas, veja o exemplo em que retornamos todos os elementos da string a partir do 2° elemento


```python
# Retorna todos os elementos da string, começando pela posição (lembre-se que Python começa a indexação pela posição 0),
# até o fim da string.
s[1:]
```




    'iência de dados em python'




```python
# A string original permanece inalterada
s[1:7]
```




    'iência'




```python
# Retorna tudo até a posição 3
s[:3]
```




    'Ciê'




```python
s[:]
```




    'Ciência de dados em python'




```python
# Nós também podemos usar a indexação negativa e ler de trás para frente.
s[-1]
```




    'n'




```python
# Retornar tudo, exceto a última letra
s[:-1]
```




    'Ciência de dados em pytho'



Nós também podemos usar a notação de índice e fatiar a string em pedaços específicos (o padrão é 1). Por exemplo, podemos usar dois pontos duas vezes em uma linha e, em seguida, um número que especifica a frequência para retornar elementos. Por exemplo:


```python
s[::1]
```




    'Ciência de dados em python'




```python
s[::2]
```




    'Cêcad ao mpto'




```python
# invertendo a string
s[::-1]
```




    'nohtyp me sodad ed aicnêiC'



## Propriedades de Strings


```python
s
```




    'Ciência de dados em python'




```python
# Não é possível alterear um caracter de uma string.
s[0] = 'c'
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-23-2b287687565c> in <module>
          1 # Não é possível alterear um caracter de uma string.
    ----> 2 s[0] = 'c'
    

    TypeError: 'str' object does not support item assignment



```python
# Concatenando strings
s + ' é muito legal!'
```




    'Ciência de dados em python é muito legal!'




```python
s = s + ' é muito legal!'
```


```python
print(s)
```

    Ciência de dados em python é muito legal!
    


```python
# Podemos usar o símbolo de multiplicação para criar repetição!
letra = 'w'
```


```python
letra * 3
```




    'www'



## Funções Built-in de Strings


```python
s
```




    'Ciência de dados em python é muito legal!'




```python
# Upper Case 
s.upper()
```




    'CIÊNCIA DE DADOS EM PYTHON É MUITO LEGAL!'




```python
# Lower case
s.lower()
```




    'ciência de dados em python é muito legal!'




```python
# Dividir uma string por espaços em branco (padrão)
s.split()
```




    ['Ciência', 'de', 'dados', 'em', 'python', 'é', 'muito', 'legal!']




```python
# Dividir uma string por um elemento específico
s.split('y')
```




    ['Ciência de dados em p', 'thon é muito legal!']



## Funções String


```python
s = 'seja bem vindo ao universo de python'
```


```python
s.capitalize()
```




    'Seja bem vindo ao universo de python'




```python
s.count('a')
```




    2




```python
s.find('p')
```




    30




```python
s.center(5,'z')
```




    'seja bem vindo ao universo de python'




```python
s.isalnum()
```




    False




```python
s.isalpha()
```




    False




```python
s.islower()
```




    True




```python
s.isspace()
```




    False




```python
s.endswith('o')
```




    False




```python
s.partition('!')
```




    ('seja bem vindo ao universo de python', '', '')



## Comparando Strings


```python
print("Python" == "R")
```

    False
    


```python
print("Python" == "Python")
```

    True
    
