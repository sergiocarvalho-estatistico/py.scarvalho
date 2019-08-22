# Estrutura Condicional

## Condicional If


```python
if 5 > 2:
    print("Python funciona!")
```

    Python funciona!
    


```python
if 10 > 9:
    print('10 > 9')
else:
    print('10 < 9')
```

    10 > 9
    


```python
# Statement If...Else
if 5 < 2:
   print("Python funciona!")
else:
   print("Algo está errado!")
```

    Algo está errado!
    


```python
6 > 3
```




    True




```python
3 > 7
```




    False




```python
4 < 8
```




    True




```python
4 >= 4
```




    True




```python
if 5 == 5:
  print("Testando Python!")
```

    Testando Python!
    


```python
if True:
    print('Parece que Python funciona!')
```

    Parece que Python funciona!
    


```python
# Atenção com a sintaxe
if 4 > 3
  print("Se não fizer direito não funciona!")
```


      File "<ipython-input-10-1d6e2ebd33a5>", line 2
        if 4 > 3
                ^
    SyntaxError: invalid syntax
    



```python
# Atenção com a sintaxe
if 4 > 3:
    print("Mas se eu faço direito, tudo funciona!")
```

    Mas se eu faço direito, tudo funciona!
    

## Condicionais Aninhados


```python
idade = 18
if idade > 17:
   print("Você pode dirigir!")
```

    Você pode dirigir!
    


```python
Nome = "Bob"
idade = 21
if idade > 20:
   print('Ok',Nome,',você está autorizado a entrar!')
else:
   print(Nome,", desculpe, mas você não pode entrar!")
```

    Ok Bob ,você está autorizado a entrar!
    


```python
idade = 13
Nome = "Bob"
if idade >= 13 and Nome == "Bob":
    print("Ok Bob, você está autorizado a entrar!")
```

    Ok Bob, você está autorizado a entrar!
    


```python
idade = 12
Nome = "Bob"
if (idade >= 13) or (Nome == "Bob"):
    print("Ok Bob, você está autorizado a entrar!")
```

    Ok Bob, você está autorizado a entrar!
    

## Elif


```python
dia = "Terça"
if dia == "Segunda":
  print("Hoje fará sol!")
else:
  print("Hoje vai chover!")
```

    Hoje vai chover!
    


```python
dia = 'Quarta-feira'
if dia == "Segunda":
  print("Hoje fará sol!")
elif dia == "Terça":
  print("Hoje vai chover!")
else:
  print("Sem previsão do tempo para o dia selecionado")
```

    Sem previsão do tempo para o dia selecionado
    

## Operadores Lógicos


```python
idade = 18
nome = "Bob"
if idade > 17:
   print("Você pode dirigir!")
```

    Você pode dirigir!
    


```python
idade = 18
if idade > 17 and nome == "Bob":
   print("Autorizado!")
```

    Autorizado!
    


```python
# Usando mais de uma condição na cláusula if 
disciplina = input('Digite o nome da disciplina: ')
nota_final = input('Digite a nota final (entre 0 e 100): ')

if disciplina == 'Geografia' and nota_final >= '70':
    print('Você foi aprovado!')
else:
    print('Lamento, acho que você precisa estudar mais!')
```

    Digite o nome da disciplina:  Geografia
    Digite a nota final (entre 0 e 100):  75
    

    Você foi aprovado!
    


```python
# Usando mais de uma condição na cláusula if e introduzindo Placeholders

disciplina = input('Digite o nome da disciplina: ')
nota_final = input('Digite a nota final (entre 0 e 100): ')
semestre = input('Digite o semestre (1 a 4): ')

if disciplina == 'Geografia' and nota_final >= '50' and int(semestre) != 1:
    print('Você foi aprovado em %s com média final %r!' %(disciplina, nota_final))
else:
    print('Lamento, acho que você precisa estudar mais!')
```

    Digite o nome da disciplina:  Geografia
    Digite a nota final (entre 0 e 100):  85
    Digite o semestre (1 a 4):  3
    

    Você foi aprovado em Geografia com média final '85'!
    
