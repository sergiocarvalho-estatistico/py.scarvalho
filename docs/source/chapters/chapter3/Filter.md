## Filter()

* Filter() é uma função que recebe 2 argumentos:

    * Uma função
    * Uma sequência
    
* filter(Função,Sequência)

    * A função passada como parâmetro para filter() deve retornar um valor boolean True ou False. 
    
    
* A função será aplicada a todos os valores de uma sequência e os valores serão retornados, apenas se retornarem True para a função. 

### Criando uma função


```python
def verificaPar(num):
    if num % 2 == 0:
        return True
    else:
        return False
```

* Chamando a função e passando um número como parâmetro. 
* Retornará Falso de for ímpar e True se for par.


```python
verificaPar(35)
```




    False



* Definindo uma lista numérica.


```python
lista = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18]
```

* Aplicando a função filter() 


```python
filter(verificaPar, lista)
```




    <filter at 0x22a32e1e390>



* Observe que serão retornados somente os elementos cujo o output da função verificarpar() é true.


```python
list(filter(verificaPar, lista))
```




    [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]



### Utilizando a função anônima lambda


```python
list(filter(lambda x: x%2==0, lista))
```




    [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]



* mais um exemplo utilizando a função lambda


```python
list(filter(lambda num: num > 8, lista))
```




    [9, 10, 11, 12, 13, 14, 15, 16, 17, 18]


