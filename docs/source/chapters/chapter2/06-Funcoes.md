# Funções em Python

## Definindo uma função


```python
def primeiraFunc():
    print('Hello World')
```


```python
primeiraFunc()
```

    Hello World
    


```python
# Definindo uma função com parâmetro
def primeiraFunc(nome):
    print('Hello %s' %(nome))
```


```python
primeiraFunc('Hélio Cardoso')
```

    Hello Hélio Cardoso
    


```python
def funcLeitura():
    for i in range(0, 5):
        print("Número " + str(i))
```


```python
funcLeitura()
```

    Número 0
    Número 1
    Número 2
    Número 3
    Número 4
    


```python
# Função para somar números
def addNum(firstnum, secondnum):
    print("Primeiro número: " + str(firstnum))
    print("Segundo número: " + str(secondnum))
    print("Soma: ", firstnum + secondnum)
```


```python
# Chamando a função e passando parâmetros
addNum(45, 3)
```

    Primeiro número: 45
    Segundo número: 3
    Soma:  48
    

## Variáveis locais e globais


```python
# Variável Global
var_global = 10  # Esta é uma variável global

def multiply(num1, num2):
    var_global = num1 * num2  # Esta é uma variável local
    print(var_global)
```


```python
multiply(5, 25)
```

    125
    


```python
print(var_global)
```

    10
    


```python
# Variável Local
var_global = 10  # Esta é uma variável global
def multiply(num1, num2):
    var_local = num1 * num2   # Esta é uma variável local
    print(var_local)
```


```python
multiply(5, 25)
```

    125
    


```python
# A variável precisa ser declarada globalmente
print(var_local)
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-13-679175cc3b28> in <module>
          1 # A variável precisa ser declarada globalmente
    ----> 2 print(var_local)
    

    NameError: name 'var_local' is not defined


## Funções Built-in


```python
abs(-56)
```




    56




```python
abs(23)
```




    23




```python
bool(0)
```




    False




```python
bool(1)
```




    True



## Funções str, int, float

* Erro ao executar por causa da conversão


```python
idade = input("Digite sua idade: ")
if idade > 13:
  print("Você pode acessar o Facebook")  
```

    Digite sua idade:  15
    


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-19-f21b3dafa64b> in <module>
          1 # Erro ao executar por causa da conversão
          2 idade = input("Digite sua idade: ")
    ----> 3 if idade > 13:
          4   print("Você pode acessar o Facebook")
    

    TypeError: '>' not supported between instances of 'str' and 'int'


* Usando a função int para converter o valor digitado


```python
idade = int(input("Digite sua idade: "))
if idade > 13:
  print("Você pode acessar o Facebook")  
```

    Digite sua idade:  43
    

    Você pode acessar o Facebook
    


```python
int("26")
```




    26




```python
float("123.345")
```




    123.345




```python
str(14)
```




    '14'




```python
len([23,34,45,46])
```




    4




```python
array = ['a', 'b', 'c']
```


```python
max(array)
```




    'c'




```python
min(array)
```




    'a'




```python
array = ['a', 'b', 'c', 'd', 'A', 'B', 'C', 'D']
```


```python
array
```




    ['a', 'b', 'c', 'd', 'A', 'B', 'C', 'D']




```python
max(array)
```




    'd'




```python
min(array)
```




    'A'




```python
list1 = [23, 23, 34, 45]
```


```python
sum(list1)
```




    125



### Criando funções usando outras funções


```python
import math

def numPrimo(num):
    '''
    Verificando se um número 
    é primo. 
    '''
    if (num % 2) == 0 and num > 2: 
        return "Este número não é primo"
    for i in range(3, int(math.sqrt(num)) + 1, 2):
        if (num % i) == 0:
            return "Este número não é primo"
    return "Este número é primo"
```


```python
numPrimo(1051)
```




    'Este número é primo'



### Fazendo split dos dados


```python
# Fazendo split dos dados
def split_string(text):
    return text.split(" ")
```


```python
texto = "Esta função será bastante útil para separar grandes volumes de dados."
```


```python
# Isso divide a string em uma lista.
print(split_string(texto))
```

    ['Esta', 'função', 'será', 'bastante', 'útil', 'para', 'separar', 'grandes', 'volumes', 'de', 'dados.']
    


```python
# Podemos atribuir o output de uma função, para uma variável
token = split_string(texto)
```


```python
token
```




    ['Esta',
     'função',
     'será',
     'bastante',
     'útil',
     'para',
     'separar',
     'grandes',
     'volumes',
     'de',
     'dados.']




```python
caixa_baixa = "Este Texto Deveria Estar Todo Em LowerCase"
```


```python
def lowercase(text):
    return text.lower()
```


```python
lowercased_string = lowercase(caixa_baixa)
```


```python
lowercased_string
```




    'este texto deveria estar todo em lowercase'




```python
# Funções com número variável de argumentos
def printVarInfo( arg1, *vartuple ):
   # Imprimindo o valor do primeiro argumento
    print ("O parâmetro passado foi: ", arg1)
   
   # Imprimindo o valor do segundo argumento 
    for item in vartuple:
        print ("O parâmetro passado foi: ", item)
    return;
```


```python
# Fazendo chamada à função usando apenas 1 argumento
printVarInfo(10)
```

    O parâmetro passado foi:  10
    


```python
printVarInfo('Chocolate', 'Morango', 'Banana')
```

    O parâmetro passado foi:  Chocolate
    O parâmetro passado foi:  Morango
    O parâmetro passado foi:  Banana
    
