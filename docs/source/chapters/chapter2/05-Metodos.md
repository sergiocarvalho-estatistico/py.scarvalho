# Métodos


```python
# Criando uma lista
lst = [100, -2, 12, 65, 0]
```


```python
# Usando um método do objeto lista
lst.append(10)
```


```python
# Imprimindo a lista
lst
```




    [100, -2, 12, 65, 0, 10]




```python
# Usando um método do objeto lista
lst.count(10)
```




    1




```python
# A função help() explica como utilizar cada método de um objeto
help(lst.count)
```

    Help on built-in function count:
    
    count(value, /) method of builtins.list instance
        Return number of occurrences of value.
    
    


```python
# A função dir() mostra todos os métodos e atributos de um objeto
dir(lst)
```




    ['__add__',
     '__class__',
     '__contains__',
     '__delattr__',
     '__delitem__',
     '__dir__',
     '__doc__',
     '__eq__',
     '__format__',
     '__ge__',
     '__getattribute__',
     '__getitem__',
     '__gt__',
     '__hash__',
     '__iadd__',
     '__imul__',
     '__init__',
     '__init_subclass__',
     '__iter__',
     '__le__',
     '__len__',
     '__lt__',
     '__mul__',
     '__ne__',
     '__new__',
     '__reduce__',
     '__reduce_ex__',
     '__repr__',
     '__reversed__',
     '__rmul__',
     '__setattr__',
     '__setitem__',
     '__sizeof__',
     '__str__',
     '__subclasshook__',
     'append',
     'clear',
     'copy',
     'count',
     'extend',
     'index',
     'insert',
     'pop',
     'remove',
     'reverse',
     'sort']




```python
a = 'Isso é uma string'
```


```python
# O método de um objeto pode ser chamado dentro de uma função, como print()
print (a.split())
```

    ['Isso', 'é', 'uma', 'string']
    
