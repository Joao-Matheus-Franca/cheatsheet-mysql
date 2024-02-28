# 🐬 Cheat Sheet para MySQL 🐬

# Create:
### Criar bancos de dados:

``` 
  CREATE DATABASE nome_do_banco_de_dados;
```

### Inserir valores em tabelas:

``` 
  INSERT INTO banco_de_dados.tabela (coluna01, coluna02...)
  VALUES (valor_coluna01, valor_coluna02...);
```

# Read:
### Mostrar bancos de dados:

``` 
  SHOW DATABASES;
```

### Selecionar banco de dados:

``` 
  USE nome_do_banco_de_dados;
```

### Mostrar tabelas do banco de dados selecionado:

``` 
  SHOW TABLES;
```

### Mostrar estrutura de uma tabela:

``` 
  DESCRIBE nome_da_tabela;
```

### Exibir valores em formato de tabela:

``` 
  SELECT valor AS nome_da_coluna;
```

### Exibir colunas de tabelas selecionadas:

``` 
  SELECT nome_da_coluna FROM nome_do_banco_de_dados.nome_da_tabela;
```

### Exibir valores únicos de uma ou mais colunas:

``` 
  SELECT DISTINCT nome_da_coluna FROM nome_do_banco_de_dados.nome_da_tabela;
```

### Limitar número de linhas retornadas por uma consulta:

``` 
  SELECT nome_da_coluna FROM nome_do_banco_de_dados.nome_da_tabela LIMIT valor;
```

### Pular linhas indesejadas ao limitar uma consulta:

``` 
  SELECT coluna FROM banco_de_dados.tabela LIMIT valor OFFSET valor;
```

### Ordenar consultas de maneira crescente:

``` 
  SELECT coluna FROM banco_de_dados.tabela ORDER BY coluna ASC;
```

### Ordenar consultas de maneira decrescente:

``` 
  SELECT coluna FROM banco_de_dados.tabela ORDER BY coluna DESC;
```

### Filtrar usando operadores:

``` 
  SELECT coluna FROM banco_de_dados.tabela WHERE operação_lógica;
```

# Update:
### Atualizar dados em uma tabela (Safe Update: off):

``` 
  UPDATE banco_de_dados.tabela
  SET coluna = novo_valor
  WHERE operação_lógica;
  ⚠️ Atualiza todas as linhas que satisfaçam a lógica estabelecida ⚠️
```

### Atualizar dados em uma tabela (Safe Update: on):

``` 
  UPDATE banco_de_dados.tabela
  SET coluna = novo_valor
  WHERE operação_lógica usando coluna da PRIMARY KEY;
```

# Delete:
### Excluir dados em uma tabela (safe update: off):

``` 
  DELETE banco_de_dados.tabela
  WHERE operação_lógica;
  ⚠️ Atualiza todas as linhas que satisfaçam a lógica estabelecida ⚠️
```

### Excluir dados em uma tabela (safe update: on):

``` 
  DELETE banco_de_dados.tabela
  WHERE operação_lógica (usando coluna da PRIMARY KEY);
```

### Excluir todos os dados de uma tabela:

```
  TRUNCATE banco_de_dados.tabela;
```

# Functions: 
### Exibir em uma nova coluna a concatenação de outras colunas:

``` 
  SELECT CONCAT(coluna01, " ", coluna02) AS nova_coluna FROM banco_de_dados.tabela;
```

### Contar valores não nulos em colunas selecionadas:

``` 
  SELECT COUNT(nome_da_coluna) FROM nome_do_banco_de_dados.nome_da_tabela;
```

### Funções para trabalhar com datas:
|Função|Retorno|
|-|-|
|DATE()|Data no formato: YYYY-MM-DD|
|YEAR()|Ano|
|MONTH()|Mês|
|DAY()|Dia|
|HOUR()|Hora|
|MINUTE()|Minuto|
|SECOND()|Segundo|

# Others:
### Principais restrições(constraints):
- NOT NULL
- UNIQUE
- PRIMARY KEY
- FOREIGN KEY
- DEFAULT

### Principais operadores:
|Operador|Significado|
|--------|-----------|
|=|Igual|
|<>|Diferente|
|>|Maior que|
|<|Menor que|
|>=|Maior ou igual que|
|<=|Menor ou igual que|
|AND|E|
|OR|Ou|
|IS|Igualdade com booleanos|
|LIKE|Igualdade com palavras|
|NOT|Negação|
|IN|Dentre um grupo de valores|
|BETWEEN|Dentre intervalo de valores|

### Principais curingas:
|Curinga|Uso|
|-|-|
|*|Retornar todas as colunas de uma tabela|
|%|Representar nenhum, um ou múltiplos caracteres|
|_|Representar apenas um carácter|

### Comando para desabilitar o safe update:

``` 
  SET SET SQL_SAFE_UPDATES = 0;
```

### Comando para habilitar o safe update:

``` 
  SET SET SQL_SAFE_UPDATES = 1;
```
