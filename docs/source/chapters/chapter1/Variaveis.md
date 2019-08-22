# Variáveis e Operadores 


```python
# Atribuindo o valor 1 à variável var_teste
var_teste = 1
```


```python
# Imprimindo o valor da variável
var_teste
```




    1




```python
# Imprimindo o valor da variável
print(var_teste)
```

    1
    


```python
# Não podemos utilizar uma variável que não foi definida. Veja a mensagem de erro.
my_var
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-4-7f70398ca07b> in <module>
          1 # Não podemos utilizar uma variável que não foi definida. Veja a mensagem de erro.
    ----> 2 my_var
    

    NameError: name 'my_var' is not defined



```python
var_teste = 2
```


```python
var_teste
```




    2




```python
type(var_teste)
```




    int




```python
var_teste = 9.5
```


```python
type(var_teste)
```




    float




```python
x = 1
```


```python
x
```




    1



## Declaração Múltipla


```python
pessoa1, pessoa2, pessoa3 = "Maria", "José", "Tobias"
```


```python
pessoa1
```




    'Maria'




```python
pessoa2
```




    'José'




```python
pessoa3
```




    'Tobias'




```python
fruta1 = fruta2 = fruta3 = "Laranja"
```


```python
fruta1
```




    'Laranja'




```python
fruta2
```




    'Laranja'




```python
# Fique atento!!! Python é case-sensitive. Criamos a variável fruta2, mas não a variável Fruta2.
# Letras maiúsculas e minúsculas tem diferença no nome da variável.
Fruta2
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-19-064185b35816> in <module>
          1 # Fique atento!!! Python é case-sensitive. Criamos a variável fruta2, mas não a variável Fruta2.
          2 # Letras maiúsculas e minúsculas tem diferença no nome da variável.
    ----> 3 Fruta2
    

    NameError: name 'Fruta2' is not defined


## Os nome das variáveis não podem começar com números.


```python
x1 = 50
```


```python
x1
```




    50




```python
# erro: nome de variável iniciando com um número.
1x = 50
```


      File "<ipython-input-22-efc872d8762a>", line 2
        1x = 50
         ^
    SyntaxError: invalid syntax
    


## Lista das palavras reservadas em python.

## False      
## class      
## finally    
## is         
## return
## None       
## continue   
## for        
## lambda     
## try
## True       
## def        
## from       
## nonlocal   
## while
## and        
## del        
## global     
## not        
## with
## as         
## elif       
## if         
## or         
## yield
## assert     
## else       
## import     
## pass
## break      
## except     
## in         
## raise


```python
# Não podemos usar palavras reservadas como nome de variável
break = 1
```


      File "<ipython-input-23-e88ee5721a0c>", line 2
        break = 1
              ^
    SyntaxError: invalid syntax
    


## Atribuição de variáveis


```python
largura = 2
```


```python
altura = 4
```


```python
area = largura * altura
```


```python
area
```




    8




```python
perimetro = 2 * largura + 2 * altura
```


```python
perimetro
```




    12




```python
# A ordem dos operadores é a mesma seguida na Matemática
perimetro = 2 * (largura + 2)  * altura
```


```python
perimetro
```




    32



## Operações com variáveis


```python
idade1 = 25
```


```python
idade2 = 35
```


```python
idade1 + idade2
```




    60




```python
idade2 - idade1
```




    10




```python
idade2 * idade1
```




    875




```python
idade2 / idade1
```




    1.4




```python
idade2 % idade1
```




    10



## Concatenação de Variáveis


```python
nome = "Steve"
```


```python
sobrenome = "Jobs"
```


```python
fullName = nome + " " + sobrenome
```


```python
fullName
```




    'Steve Jobs'


