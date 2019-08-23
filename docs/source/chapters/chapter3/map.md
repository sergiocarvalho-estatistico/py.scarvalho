# Programação Funcional

* Podemos dizer que a programação funcional é uma programação orientada à expressão e neste sentido, Python fornece várias funções que permitem uma abordagem funcional à programação, oferecendo mais facilidade na criação do seu código.

* Funções orientadas à expressão em Python:
    * map(Função,Sequência)
    * reduce(Função,Sequência)
    * filter(Função,Sequência)
    * lambda
    * list comprehension

## Map

* Map é uma função que recebe 2 argumentos:

    * Uma função
    * Uma sequência
    
    
* map(Função,Sequência)

    * A função map aplica o parâmetro função em toda a sequência e retorna uma lista com o(s) resultado(s). 

### Criando  duas funções

* Função 1 - Recebe uma temperatura como parâmetro e retorna a temperatura em Fahrenheit


```python
def fahrenheit(T):
    return ((float(9)/5)*T + 32)
```

* Função 2 - Recebe uma temperatura como parâmetro e retorna a temperatura em Celsius


```python
def celsius(T):
    return (float(5)/9)*(T-32)
```

* Criando uma sequência com uma lista numérica.


```python
temperaturas = [0, 22.5, 40, 100]
```

* Aplicando a função a cada elemento da lista de temperaturas. 
* Em Python 3, a funçãp map() retornar um iterator


```python
map(fahrenheit, temperaturas)
```




    <map at 0x15e1bbbb3c8>



* Função map() reotrnando a lista de temperaturas convertidas em Fahrenheit


```python
list(map(fahrenheit, temperaturas))
```




    [32.0, 72.5, 104.0, 212.0]



* Usando um loop for para imprimir o resultado da função map()


```python
for temp in map(fahrenheit, temperaturas):
    print(temp)
```

    32.0
    72.5
    104.0
    212.0
    

* Convertendo para Celsius


```python
map(celsius, temperaturas)
```




    <map at 0x15e1bbbbcc0>




```python
list(map(celsius, temperaturas))
```




    [-17.77777777777778, -5.277777777777778, 4.444444444444445, 37.77777777777778]



* Usando a função lambda


```python
map(lambda x: (5.0/9)*(x - 32), temperaturas)
```




    <map at 0x15e1bbc14e0>




```python
list(map(lambda x: (5.0/9)*(x - 32), temperaturas))
```




    [-17.77777777777778, -5.277777777777778, 4.444444444444445, 37.77777777777778]



* Somando os elementos de 2 listas


```python
a = [1,2,3,4]
b = [5,6,7,8]
```


```python
list(map(lambda x,y:x+y, a, b))
```




    [6, 8, 10, 12]



* Somando os elementos de 3 listas


```python
a = [1,2,3,4]
b = [5,6,7,8]
c = [9,10,11,12]
```


```python
list(map(lambda x,y,z:x+y+z, a, b, c))
```




    [15, 18, 21, 24]


