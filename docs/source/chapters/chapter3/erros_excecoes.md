# Tratamento de Erros e Exceções

* Erro de sintaxe: 
    * não imprime.


```python
print('Olá)
```


      File "<ipython-input-4-60073fc7b8c6>", line 1
        print('Olá)
                   ^
    SyntaxError: EOL while scanning string literal
    


* Criando uma função para divisão de dois números.


```python
def numDiv (num1, num2):
    resultado = num1 / num2
    print(resultado)
```

* Execução perfeita, sem erros.


```python
numDiv(4,2)
```

    2.0
    

* Execução com erros.
* Como não há divisão por zero naturalmente esperamos uma mensagem de erro.


```python
numDiv(4,0)
```


    ---------------------------------------------------------------------------

    ZeroDivisionError                         Traceback (most recent call last)

    <ipython-input-8-ab1f14e17343> in <module>
    ----> 1 numDiv(4,0)
    

    <ipython-input-6-b24eee9b97fe> in numDiv(num1, num2)
          1 def numDiv (num1, num2):
    ----> 2     resultado = num1 / num2
          3     print(resultado)
    

    ZeroDivisionError: division by zero


### Try, Except, Finally

* Erro de sintaxe.


```python
8 + 's'
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-5-4dc08abe771f> in <module>()
    ----> 1 8 + 's'
    

    TypeError: unsupported operand type(s) for +: 'int' and 'str'


* Tratando erro com try e except.


```python
try:
    8 + 's'
except TypeError:
    print("Operação não permitida")
```

    Operação não permitida
    

* Utilizando try, except e else
* Observe que estamos abrindo um arquivo .txt para escrita
* Se não existir nenhum problema de IO, entrada e saída de dados, a função irá funcionar sem problemas.
* No primeiro exemplo a função função sem problemas.


```python
try:
    f = open('arquivos/testandoerros.txt','w')
    f.write('Gravando no arquivo')
except IOError:
   print ("Erro: arquivo não encontrado ou não pode ser salvo.")
else:
   print ("Conteúdo gravado com sucesso!")
   f.close()
```

    Conteúdo gravado com sucesso!
    

#### Utilizando try, except e else
* Já neste exemplo, retiramos a extensão .txt do arquivo de modo que a função open não irá conseguir abri-lo para escrita o que deve acarretar um erro.
* Uma mensagem de erro é retornada. 


```python
try:
    f = open('arquivos/testandoerros','r')
except IOError:
   print ("Erro: arquivo não encontrado ou não pode ser lido.")
else:
   print ("Conteúdo gravado com sucesso!")
   f.close()
```

    Erro: arquivo não encontrado ou não pode ser lido.
    

* Agora com finally.


```python
try:
    f = open('arquivos/testandoerros.txt','w')
    f.write('Gravando no arquivo')
except IOError:
   print ("Erro: arquivo não encontrado ou não pode ser salvo.")
else:
   print ("Conteúdo gravado com sucesso!")
   f.close()
finally:
   print ("Comandos no bloco finally são sempre executados!")
```

    Conteúdo gravado com sucesso!
    Comandos no bloco finally são sempre executados!
    

* Está função requer um número inteiro.


```python
def askint():
        try:
            val = int((input("Digite um número: ")))
        except UnboundLocalError:
            print ("Você não digitou um número!")
        finally:
            print ("Obrigado!")
        print (val) 
```

* Aplicando a função askint().
    * Testando o número 98 
    * Testando o número 15.5
    * Testando apenas com o enter


```python
askint()
```

    Digite um número:  98
    

    Obrigado!
    98
    


```python
askint()
```

    Digite um número:  15.5
    

    Obrigado!
    


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-14-cc291aa76c10> in <module>
    ----> 1 askint()
    

    <ipython-input-11-e1ec99adaa8b> in askint()
          1 def askint():
          2         try:
    ----> 3             val = int((input("Digite um número: ")))
          4         except UnboundLocalError:
          5             print ("Você não digitou um número!")
    

    ValueError: invalid literal for int() with base 10: '15.5'



```python
askint()
```

    Digite um número:  
    

    Obrigado!
    


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-19-cc291aa76c10> in <module>
    ----> 1 askint()
    

    <ipython-input-18-e1ec99adaa8b> in askint()
          1 def askint():
          2         try:
    ----> 3             val = int((input("Digite um número: ")))
          4         except UnboundLocalError:
          5             print ("Você não digitou um número!")
    

    ValueError: invalid literal for int() with base 10: ''


* Observe que o erro ocorre quando não se digita nada ou se digita um número não inteiro.
* Tratando os erros com while


```python
def askint():
    while True:
        try:
            val = int(input("Digite um número: "))
        except:
            print ("Você não digitou um número inteiro!")
            continue
        else:
            print ("Obrigado por digitar um número inteiro!")
            break
        finally:
            print("Fim da execução!")
        print (val) 
```

* Testando a nova solução


```python
askint()
```

    Digite um número:  15.5
    

    Você não digitou um número inteiro!
    Fim da execução!
    

    Digite um número:  30.4
    

    Você não digitou um número inteiro!
    Fim da execução!
    

    Digite um número:  
    

    Você não digitou um número inteiro!
    Fim da execução!
    

    Digite um número:  12
    

    Obrigado por digitar um número inteiro!
    Fim da execução!
    

#### Adição de elemento em uma tupla?  

* Sabemos que adicionar elemento em uma tupla não é possível porque as tuplas são imutáveis.
* Naturalmente esperamos um erro.

#### definindo a tupla 


```python
tuple = (1,2,3,4,5)
```


```python
try:
    tuple.append(6)
    for each in tuple:
        print(each)
except AttributeError as e:
    print('Erro: ', e)
except IOError as e:
    print('Erro de I/O:', e)
```

    Erro:  'tuple' object has no attribute 'append'
    

#### Lista completa de exceções em Python:

* [Exceções em python](https://docs.python.org/3.6/library/exceptions.html)

