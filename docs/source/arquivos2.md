# Manipulação de Arquivos

- Arquivos TXT
- Arquivos CSV 
- Arquivos JSON

## Manipulando Arquivos TXT


```python
# textos 1
texto = "Cientista de Dados é a profissão que mais tem crescido em todo mundo.\n"
```


```python
# texto 1 concatena com texto 2
texto = texto + "Esses profissionais precisam se especializar em Programação, Estatística e Machine Learning.\n"
```


```python
# texto concatena com texto 3
texto += "E claro, em Big Data."
```


```python
print(texto)
```

    Cientista de Dados é a profissão que mais tem crescido em todo mundo.
    Esses profissionais precisam se especializar em Programação, Estatística e Machine Learning.
    E claro, em Big Data.
    

## O Módulo Operating System (OS) 

* O pacote OS serve para manipular o sistema operacional, ele é super útil em várias situações como:
    * Manipular arquivos
    * Manipular diretórios
    * E até o Sistema Operacional utilizando variáveis de ambientes. 



```python
# Importando o módulo 'os' (operate system)
import os
```

#### Criando arquivo


```python
# Criando um arquivo para escrita 'w'
arquivo = open(os.path.join('arquivos/cientista.txt'),'w')
```


```python
# Gravando os dados no arquivo
for palavra in texto.split():
    arquivo.write(palavra+' ')
```


```python
# Fechando o arquivo
arquivo.close()
```

### Lendo o arquivo


```python
# Lendo o arquivo
arquivo = open('arquivos/cientista.txt','r')
conteudo = arquivo.read()
arquivo.close()

print(conteudo)
```

    Cientista de Dados é a profissão que mais tem crescido em todo mundo. Esses profissionais precisam se especializar em Programação, Estatística e Machine Learning. E claro, em Big Data. 
    

### Usando a expressão `with` 

O método close() é executado automaticamente


```python
# Na expressão abaixo lêia-se: Com o arquivo cientista.txt aberto para leitura (r) como arquivo, faça a relituda de seu conteúdo (read)
with open('arquivos/cientista.txt','r') as arquivo:
    conteudo = arquivo.read()
```


```python
print(len(conteudo))
```

    185
    


```python
arquivo.close()
```


```python
print(conteudo)
```

    Cientista de Dados é a profissão que mais tem crescido em todo mundo. Esses profissionais precisam se especializar em Programação, Estatística e Machine Learning. E claro, em Big Data. 
    


```python
with open('arquivos/cientista.txt','w') as arquivo:
    arquivo.write(texto[:21])
    arquivo.write('\n')
    arquivo.write(texto[:33])
```


```python
# Lendo o arquivo
arquivo = open('arquivos/cientista.txt','r')
conteudo = arquivo.read()
arquivo.close()

print (conteudo)
```

    Cientista de Dados é 
    Cientista de Dados é a profissão 
    

### Manipulando Arquivos CSV (comma-separated values )


```python
# Importando o módulo csv
import csv
```


```python
# com o numeros.csv aberto para a escrita como arquivo, escreva:
with open('arquivos/numeros.csv','w') as arquivo:
    writer = csv.writer(arquivo)
    writer.writerow(('primeira','segunda','terceira'))
    writer.writerow((55,93,76)) 
    writer.writerow((62,14,86))
```


```python
# Leitura de arquivos csv
with open('arquivos/numeros.csv','r') as arquivo:
    leitor = csv.reader(arquivo)
    for x in leitor:
        print ('Número de colunas:', len(x))
        print(x)
```

    Número de colunas: 3
    ['primeira', 'segunda', 'terceira']
    Número de colunas: 0
    []
    Número de colunas: 3
    ['55', '93', '76']
    Número de colunas: 0
    []
    Número de colunas: 3
    ['62', '14', '86']
    Número de colunas: 0
    []
    


```python
# Código alternativo para eventuais problemas com linhas em branco no arquivo
with open('arquivos/numeros.csv','r', encoding='utf8', newline = '\r\n') as arquivo:
    leitor = csv.reader(arquivo)
    for x in leitor:
        print ('Número de colunas:', len(x))
        print(x)
```

    Número de colunas: 3
    ['primeira', 'segunda', 'terceira']
    Número de colunas: 3
    ['55', '93', '76']
    Número de colunas: 3
    ['62', '14', '86']
    


```python
# Gerando uma lista com dados do arquivo csv
with open('arquivos/numeros.csv','r') as arquivo:
    leitor = csv.reader(arquivo)
    dados = list(leitor)
    
    
print (dados)
```

    [['primeira', 'segunda', 'terceira'], [], ['55', '93', '76'], [], ['62', '14', '86'], []]
    


```python
# Impriminfo a partir da segunda linha
for linha in dados[1:]:
    print (linha)
```

    []
    ['55', '93', '76']
    []
    ['62', '14', '86']
    []
    

### Manipulando Arquivos JSON (Java Script Object Notation )

* JSON (JavaScript Object Notation) é uma maneira de armazenar informações de forma organizada e de fácil acesso. 
* Ele nos dá uma coleção legível de dados que podem ser acessados de forma muito lógica. 
* Pode ser uma fonte de Big Data.


```python
# Criando um dicionário
dict = {'nome': 'Guido van Rossum',
        'linguagem': 'Python',
        'similar': ['c','Modula-3','lisp'],
        'users': 1000000}
```


```python
for k,v in dict.items():
    print (k,v)
```

    nome Guido van Rossum
    linguagem Python
    similar ['c', 'Modula-3', 'lisp']
    users 1000000
    


```python
# Importando o módulo Json
import json
```


```python
# Convertendo o dicionário para um objeto json
json.dumps(dict)
```




    '{"nome": "Guido van Rossum", "linguagem": "Python", "similar": ["c", "Modula-3", "lisp"], "users": 1000000}'




```python
# Criando um arquivo Json
with open('arquivos/dados.json','w') as arquivo:
    arquivo.write(json.dumps(dict))
```


```python
# Leitura de arquivos Json
with open('arquivos/dados.json','r') as arquivo:
    texto = arquivo.read()
    data = json.loads(texto)
```


```python
print (data)
```

    {'nome': 'Guido van Rossum', 'linguagem': 'Python', 'similar': ['c', 'Modula-3', 'lisp'], 'users': 1000000}
    


```python
print(data['nome'])
```

    Guido van Rossum
    


```python
# Imprimindo um arquivo Json copiado da internet
from urllib.request import urlopen

response = urlopen("http://vimeo.com/api/v2/video/57733101.json").read().decode('utf8')
data = json.loads(response)[0]
```


```python
print ('Título: ', data['title'])
print ('URL: ', data['url'])
print ('Duração: ', data['duration'])
print ('Número de Visualizações: ', data['stats_number_of_plays'])
```

    Título:  The Good Man trailer
    URL:  https://vimeo.com/57733101
    Duração:  143
    Número de Visualizações:  5783
    


```python
# Copiando o conteúdo de um arquivo para outro
import os

arquivo_fonte = 'arquivos/dados.json'
arquivo_destino = 'arquivos/json_data.txt'
```


```python
# Método 1
with open(arquivo_fonte,'r') as infile:
    text = infile.read()
    with open(arquivo_destino,'w') as outfile:
        outfile.write(text)  
```


```python
# Método 2
open(arquivo_destino,'w').write(open(arquivo_fonte,'r').read()) 
```




    107




```python
# Leitura de arquivos Json
with open('arquivos/json_data.txt','r') as arquivo:
    texto = arquivo.read()
    data = json.loads(texto)
```


```python
print(data)
```

    {'nome': 'Guido van Rossum', 'linguagem': 'Python', 'similar': ['c', 'Modula-3', 'lisp'], 'users': 1000000}
    
