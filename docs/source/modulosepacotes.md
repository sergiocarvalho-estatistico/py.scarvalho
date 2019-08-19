# Pacotes e Módulos

### Site Pypi Python
* [Pypi](https://pypi.org)
* Neste site encontramos todos os pacotes disponibilizados em python.

### Importando o pacote Math

* **Math** é um pacote matemático que possui uma série de funções matemáticas prontas.


```python
# Importando o math
import math
```

* Verificando todos os métodos disponíveis no pacote math.


```python
print(dir(math))
```

* Usando um dos métodos do módulo math


```python
# extraindo a raiz quadrada
math.sqrt(25)
```

* Importando apenas um dos métodos do módulo math


```python
from math import sqrt
```


```python
# Usando o método
sqrt(9)
```

* Imprimindo todos os métodos do módulo math


```python
print(dir(math))
```

##### A função help pode nos ajudar com eventuais dúvidas sobre os método utilizados.  


```python
# Help do método sqrt do módulo math
help(sqrt)
```


```python
help(pow)
```


```python
pow(2,3)
```

### Importando o pacote Random

* O pacote **random** serve pra gerar valores randomicos ou aleatórios.


```python
import random
```


```python
random.choice(['Maça', 'Banana', 'Laranja'])
```


```python
random.sample(['Maça', 'Banana', 'Laranja'],2)
```


```python
random.sample(range(100), 10)
```

### Importando o pacote Statistics 

* O pacote **statistics** é utilizado para realizar cálculos estatísticos


```python
import statistics
```


```python
dados = [2.75, 1.75, 1.25, 0.25, 0.5, 1.25, 3.5]
```


```python
statistics.mean(dados)
```


```python
statistics.median(dados)
```

### Importando o pacote OS 

* O pacote **os** nos permite realizar operações no sistema operacional


```python
import os
```

* A função getcwd() nos é retornado a endereço do diretório no qual estou trabalhando.     


```python
os.getcwd()
```

* Um print de todos os módulos, funções e atributos disponíveis no pacote OS.


```python
print(dir(os))
```

### Importando o pacote sys

* O pacote **sys** também nos permite interagir com o sistema operacional.


```python
import sys
```

* podemos gravar a palavra teste na saída do **s.o**, basta fazer.   


```python
sys.stdout.write('Teste')
```

* para saber a versão do meu sitema operacional fazemos:   


```python
sys.version
```

* Para saber quais os módulos, funções e atributos do meus sistema operacional, utilizamos;   


```python
print(dir(sys))
```

* Para saber quais os módulos, funções e atributos do meus sistema operacional, utilizamos;   

### Importando o pacote *urllib*

* O módulo request do pacote urllib é usado para trazer url's para dentro do nosso ambiente Python.


```python
import urllib.request
```

* Variável resposta armazena o objeto de conexão à url passada como parâmetro.


```python
resposta = urllib.request.urlopen('http://python.org')
```

* Objeto resposta


```python
print(resposta)
```

* Chamando o método read() do objeto resposta e armazenando o código html na variável html


```python
html = resposta.read()
```


```python
# Imprimindo html
print(html)
```


