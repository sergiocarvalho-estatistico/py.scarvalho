## Reduce()

* Reduce é uma função que recebe 2 argumentos:

    * Uma função
    * Uma sequência
    
    
* reduce(Função,Sequência)

    * A função map aplica o parâmetro função em toda a sequência e retorna uma lista com o(s) resultado(s). 
    
    
* Ao contrário da função **map** que apica a função a cada elemento da sequência e retorna uma outra sequência de elementos, a função **reduce** aplica a função, que foi passada como parâmetro, aos elementos da sequência até que reste apenas um elemento.      

![exemplo-reduce](arquivos/reduce.jpg) 

Os conceitos que estão envolvidos na função **map** e **reduce** são os pilares fundamentais do processamento de big date que estão presentes em frameworks como hadoop e spark. 


### Importando a função reduce()

* Observe que para importar a função reduce() nós utilizamos o módulo functools


```python
from functools import reduce
```

* Criando uma lista


```python
lista = [47,11,42,13]
```

* Imprimindo a lista


```python
print(lista)
```

    [47, 11, 42, 13]
    

* Definindo a função a ser passada no **reduce()**


```python
def soma(a,b):
    x = a + b
    return x
```

* Usando reduce() com uma função e uma lista. 
* A função vai retornar a soma dos valores da lista.


```python
reduce(soma, lista)
```




    113



### Função Image

* Importamos a função Image de IPython.display
* Então basta colocar o caminho da imagem.


```python
from IPython.display import Image
Image('arquivos/reduce.png')
```




![png](output_13_0.png)



### Utilizando a função lambda

* Criando uma lista


```python
lst = [47, 11, 42, 65]
```

* Usando a função reduce() com lambda


```python
reduce(lambda x,y: x+y, lst)
```




    165



* Podemos atribuir a expressão lambda a uma variável


```python
max_find2 = lambda a,b: a if (a > b) else b
```


```python
type(max_find2)
```




    function



* Reduzindo a lista até o valor máximo, através da função criada com a expressão lambda


```python
reduce(max_find2, lst)
```




    65



### Conclusão

* A função reduce() permite transformar uma lista de elementos em um único elemento podendo este ser a soma, média, max, min e etc.
