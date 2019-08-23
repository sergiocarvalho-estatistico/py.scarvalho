## Pacote Datetime

* O pacote Datetime Este pacote permite a manipulação de datas
* Esse módulo permite a manipulação de datas em Python.


```python
# importando o pacote.
import datetime
```

* Que horas são agora?


```python
agora = datetime.datetime.now()
```


```python
agora
```




    datetime.datetime(2019, 8, 20, 10, 30, 33, 656485)



* setando uma data específica.


```python
t = datetime.time(7, 43, 28)
```


```python
print(t)
```

    07:43:28
    

* podemos também retornar as horas, minutos, segundos e até microsegundos.


```python
print('Hora  :', t.hour)
print('Minute:', t.minute)
print('Segundo:', t.second)
print('Microsegundo:', t.microsecond)
```

    Hora  : 7
    Minute: 43
    Segundo: 28
    Microsegundo: 0
    

* Qual será a hora de menor valor?


```python
print(datetime.time.min)
```

    00:00:00
    

* Qual será a hora de maior valor?


```python
datetime.time.max
```

    23:59:59.999999
    

* Que dia é hoje?


```python
hoje = datetime.date.today()
```


```python
print(hoje)
print('ctime:', hoje.ctime())
print('Ano:', hoje.year)
print('Mês :', hoje.month)
print('Dia :', hoje.day)
```

    2019-08-20
    ctime: Tue Aug 20 00:00:00 2019
    Ano: 2019
    Mês : 8
    Dia : 20
    

* Operações com datas.


```python
d1 = datetime.date(2015, 4, 28)
print ('d1:', d1)
```

    d1: 2015-04-28
    


```python
d2 = d1.replace(year=2016)
print('d2:', d2)
```

    d2: 2016-04-28
    


```python
# Diferença em dias entre duas datas
d2-d1
```




    datetime.timedelta(days=366)


