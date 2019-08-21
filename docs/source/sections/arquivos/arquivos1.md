# Manipulando Arquivos 1

* Caso você tenha problemas com acentos nos arquivos:
* Primeiro, recomendamos a leitura do material sobre Formato Unicode, ao final do capítulo 4.
* Uma forma de resolver esse problema, é abrir o arquivo em um editor de texto como o Sublime Text, clicar em File - Save with Encoding e então salvar com encoding UTF-8.
* Outra opção é incluir o parâmetro encoding='utf8' ao abrir o arquivo para leitura ou escrita.


Obs: Crie um arquivo txt, chamado arquivo1.txt no diretório "arquivos" na pasta onde está seu Jupyter Notebook, digite a frase: Python é uma linguagem poderosa! e salve o arquivo.


```python
# lendo o arquivo
import os 
```


```python
arr = os.listdir('arquivos')
print(arr)
```

    ['arquivo1.txt', 'binary.csv', 'cientista.txt', 'dados.json', 'file.csv', 'json_data.txt', 'numeros.csv', 'reduce.png', 'salarios.csv', 'testandoerros.txt', 'teste.txt']
    

### Lendo Arquivos


```python
# Abrindo o arquivo para leitura
arq1 = open("arquivos/arquivo1.txt","r")
```


```python
# Lendo o arquivo
print(arq1.read())
```

    Escrita do arquivo modificada Acrescentando conteúdo
    


```python
# Contar o número de caracteres
print(arq1.tell())
```

    52
    


```python
# Retornar para o iníco do arquivo
print(arq1.seek(0,0))
```

    0
    


```python
# Ler os primeiros 10 caracteres
print(arq1.read(10))
```

    Escrita do
    

### Gravando Arquivos


```python
# Abrindo arquivo para gravação
arq2 = open("arquivos/arquivo1.txt", "w")
```


```python
# Como abrimos o arquivo apenas para gravação, não podemos usar comandos de leitura.
print(arq2.read())
```


    ---------------------------------------------------------------------------

    UnsupportedOperation                      Traceback (most recent call last)

    <ipython-input-76-c83c8e14ed9b> in <module>
          1 # Como abrimos o arquivo apenas para gravação, não podemos usar comandos de leitura.
    ----> 2 print(arq2.read())
    

    UnsupportedOperation: not readable



```python
# Gravando arquivo
arq2.write("Escrita do arquivo modificada")
```




    29




```python
arq2.close()
```


```python
# Lendo arquivo gravado
arq2 = open("arquivos/arquivo1.txt", "r")
```


```python
print(arq2.read())
```

    Escrita do arquivo modificada
    


```python
# Acrescentando conteúdo
arq2 = open("arquivos/arquivo1.txt", "a")
```


```python
arq2.write(" Acrescentando conteúdo")
```




    23




```python
arq2.close()
```


```python
arq2 = open("arquivos/arquivo1.txt", "r")
```


```python
print(arq2.read())
```

    Escrita do arquivo modificada Acrescentando conteúdo
    


```python
# Retornando ao início do arquivo para leitura
arq2.seek(0,0)
```




    0




```python
print(arq2.read())
```

    Escrita do arquivo modificada Acrescentando conteúdo
    

### Automatizando o processo de gravação


```python
fileName = input("Digite o nome do arquivo: ")
```

    Digite o nome do arquivo:  arquivo1
    


```python
fileName = fileName + ".txt"
```


```python
arq3 = open(fileName, "w")
```


```python
arq3.write("Incluindo novo texto no arquivo criado")
```




    38




```python
arq3.close()
```


```python
arq3 = open(fileName, "r")
```


```python
print(arq3.read())
```

    Incluindo novo texto no arquivo criado
    


```python
arq3.close()
```

### Abrindo um dataset em uma única linha

Faça download do arquivo salarios.csv em nosso repositório no github. Este arquivo foi obtido no site de dados abertos do governo da cidade de Chicago, nos EUA: https://data.cityofchicago.org/


```python
# open file
f = open('arquivos/salarios.csv', 'r')
```


```python
data = f.read()
```


```python
rows = data.split('\n')
```


```python
#print(rows)
```

### Dividindo um dataset em colunas


```python
f = open('arquivos/salarios.csv', 'r')
```


```python
data = f.read()
```


```python
rows = data.split('\n')
```


```python
full_data = []
```


```python
for row in rows:
    split_row = row.split(",")
    full_data.append(split_row)
```


```python
# print(full_data)
```

### Contando as linhas de um arquivo


```python
f = open('arquivos/salarios.csv', 'r')
```


```python
data = f.read()
```


```python
rows = data.split('\n')
```


```python
full_data = []
```


```python
for row in rows:
    split_row = row.split(",")
    full_data.append(split_row)
```


```python
count = 0
for row in full_data:
    count += 1   # Equivalente a: count = count + 1
```


```python
print(count)
```

    32184
    

### Contando o número de colunas de um arquivo


```python
f = open('arquivos/salarios.csv', 'r')
data = f.read()
rows = data.split('\n')
full_data = []
```


```python
for row in rows:
    split_row = row.split(",")
    full_data.append(split_row)
    first_row = full_data[0]
count = 0
```


```python
for column in first_row:
    count = count + 1
    
# Outra solução possível
# for column in full_data[0]:
#     count = count + 1
```


```python
print(count)
```

    4
    

### Gravando arquivo pelo Jupyter Notebook


```python
%%writefile arquivos/teste.txt   
Olá este arquivo foi gerado pelo próprio Jupyter Notebook.
Podemos gerar quantas linhas quisermos e o Jupyter gera o arquivo final.
```

    Overwriting arquivos/teste.txt
    


```python
arq4 = open("arquivos/teste.txt", 'r',encoding='utf8')
```


```python
arq4.read()
```




    'Olá este arquivo foi gerado pelo próprio Jupyter Notebook.\nPodemos gerar quantas linhas quisermos e o Jupyter gera o arquivo final.\n'




```python
# Estamos no final do arquivo e não há mais nada para ler
arq4.read()
```




    ''




```python
# Retornando ao início do arquivo
arq4.seek(0)
```




    0




```python
arq4.seek(0)
arq4.readlines()
```




    ['Olá este arquivo foi gerado pelo próprio Jupyter Notebook.\n',
     'Podemos gerar quantas linhas quisermos e o Jupyter gera o arquivo final.\n']




```python
# Podemos usar um loop for para ler o arquivo
for line in open('arquivos/teste.txt',encoding='utf8'):
    print(line)
```

    Olá este arquivo foi gerado pelo próprio Jupyter Notebook.
    
    Podemos gerar quantas linhas quisermos e o Jupyter gera o arquivo final.
    
    

## Importando um dataset com Pandas


```python
import pandas as pd
```


```python
file_name = "arquivos/binary.csv"
```


```python
df = pd.read_csv(file_name)
```


```python
df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>admit</th>
      <th>gre</th>
      <th>gpa</th>
      <th>rank</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>380</td>
      <td>3.61</td>
      <td>3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>660</td>
      <td>3.67</td>
      <td>3</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>880</td>
      <td>4.00</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>640</td>
      <td>3.19</td>
      <td>4</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>520</td>
      <td>2.93</td>
      <td>4</td>
    </tr>
  </tbody>
</table>
</div>




```python
file2 = "arquivos/salarios.csv"
```


```python
df2 = pd.read_csv(file2)
```


```python
df2.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Position Title</th>
      <th>Department</th>
      <th>Employee Annual Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>AARON,  ELVIA J</td>
      <td>WATER RATE TAKER</td>
      <td>WATER MGMNT</td>
      <td>$88968.00</td>
    </tr>
    <tr>
      <th>1</th>
      <td>AARON,  JEFFERY M</td>
      <td>POLICE OFFICER</td>
      <td>POLICE</td>
      <td>$80778.00</td>
    </tr>
    <tr>
      <th>2</th>
      <td>AARON,  KARINA</td>
      <td>POLICE OFFICER</td>
      <td>POLICE</td>
      <td>$80778.00</td>
    </tr>
    <tr>
      <th>3</th>
      <td>AARON,  KIMBERLEI R</td>
      <td>CHIEF CONTRACT EXPEDITER</td>
      <td>GENERAL SERVICES</td>
      <td>$84780.00</td>
    </tr>
    <tr>
      <th>4</th>
      <td>ABAD JR,  VICENTE M</td>
      <td>CIVIL ENGINEER IV</td>
      <td>WATER MGMNT</td>
      <td>$104736.00</td>
    </tr>
  </tbody>
</table>
</div>

.. include:: arquivos2.md
