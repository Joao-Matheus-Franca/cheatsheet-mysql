<h1>🐬 Cheat Sheet para MySQL 🐬</h1>

<h3>Mostrar bancos de dados:</h3>

``` 
  SHOW DATABASES;
```

<h3>Selecionar banco de dados:</h3>

``` 
  USE nome_do_banco_de_dados;
```

<h3>Mostrar tabelas do banco de dados selecionado:</h3>

``` 
  SHOW TABLES;
```

<h3>Mostrar estrutura de uma tabela:</h3>

``` 
  DESCRIBE nome_da_tabela;
```

<h3>Criar bancos de dados:</h3>

``` 
  CREATE DATABASE nome_do_banco_de_dados;
```

<details open>
  <summary>
    <h3>Principais restrições(constraints):</h3>
  </summary>
  
  ```
    NOT NULL
  ```
  ```
    UNIQUE
  ```
  ```
    PRIMARY KEY
  ```
  ```
    FOREIGN KEY
  ```
  ```
    DEFAULT
  ```
</details>

<h3>Exibir valores em formato de tabela:</h3>

``` 
  SELECT valor AS nome_da_coluna;
```

<h3>Exibir colunas de tabelas selecionadas:</h3>

``` 
  SELECT nome_da_coluna FROM nome_do_banco_de_dados.nome_da_tabela;
```

<h3>Exibir em uma nova coluna a concatenação de outras colunas:</h3>

``` 
  SELECT CONCAT(coluna_01, " ", coluna_02) AS nova_coluna FROM banco_de_dados.tabela;
```

<h3>Exibir valores únicos de uma ou mais colunas:</h3>

``` 
  SELECT DISTINCT nome_da_coluna FROM nome_do_banco_de_dados.nome_da_tabela;
```
