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
  SELECT CONCAT(coluna01, " ", coluna02) AS nova_coluna FROM banco_de_dados.tabela;
```

<h3>Exibir valores únicos de uma ou mais colunas:</h3>

``` 
  SELECT DISTINCT nome_da_coluna FROM nome_do_banco_de_dados.nome_da_tabela;
```

<h3>Contar valores não nulos em colunas selecionadas:</h3>

``` 
  SELECT COUNT(nome_da_coluna) FROM nome_do_banco_de_dados.nome_da_tabela;
```

<h3>Limitar número de linhas retornadas por uma consulta:</h3>

``` 
  SELECT nome_da_coluna FROM nome_do_banco_de_dados.nome_da_tabela LIMIT valor;
```

<h3>Pular linhas indesejadas ao limitar uma consulta:</h3>

``` 
  SELECT coluna FROM banco_de_dados.tabela LIMIT valor OFFSET valor;
```

<h3>Ordenar consultas de maneira crescente:</h3>

``` 
  SELECT coluna FROM banco_de_dados.tabela ORDER BY coluna ASC;
```

<h3>Ordenar consultas de maneira decrescente:</h3>

``` 
  SELECT coluna FROM banco_de_dados.tabela ORDER BY coluna DESC;
```

<details open>
  <summary>
    <h3>Principais operadores:</h3>
  </summary>
  
  <table>
    <tr>
      <th>Operador</th>
      <th>Significado</th>
    </tr>
    <tr>
      <td>=</td>
      <td>Igual</td>
    </tr>
    <tr>
      <td><></td>
      <td>Diferente</td>
    </tr>
    <tr>
      <td>></td>
      <td>Maior que</td>
    </tr>
    <tr>
      <td><</td>
      <td>Menor que</td>
    </tr>
    <tr>
      <td>>=</td>
      <td>Maior ou igual que</td>
    </tr>
    <tr>
      <td><=</td>
      <td>Menor ou igual que</td>
    </tr>
    <tr>
      <td>AND</td>
      <td>E</td>
    </tr> 
    <tr>
      <td>OR</td>
      <td>Ou</td>
    </tr>
    <tr>
      <td>IS</td>
      <td>Igualdade com booleanos</td>
    </tr>
    <tr>
      <td>LIKE</td>
      <td>Igualdade com palavras</td>
    </tr>
    <tr>
      <td>NOT</td>
      <td>Negação</td>
    </tr> 
    <tr>
      <td>IN</td>
      <td>Dentre um grupo de valores</td>
    </tr>
    <tr>
      <td>BETWEEN</td>
      <td>Dentre intervalo de valores</td>
    </tr>
  </table>
</details>

<h3>Filtrar usando operadores:</h3>

``` 
  SELECT coluna FROM banco_de_dados.tabela WHERE operação_lógica;
```

<details open>
  <summary>
    <h3>Principais 'curingas':</h3>
  </summary>
  
  <table>
    <tr>
      <th>Curinga</th>
      <th>Uso</th>
    </tr>
    <tr>
      <td>*</td>
      <td>Retornar todas as colunas de uma tabela</td>
    </tr>
    <tr>
      <td>%</td>
      <td>Representar nenhum, um ou múltiplos caracteres</td>
    </tr>
    <tr>
      <td>_</td>
      <td>Representar apenas um carácter</td>
    </tr>
  </table>
</details>

<details open>
  <summary>
    <h3>Trabalhando com datas:</h3>
  </summary>
  
  <table>
    <tr>
      <th>Função</th>
      <th>Retorno</th>
    </tr>
    <tr>
      <td>DATE()</td>
      <td>Data no formato: YYYY-MM-DD</td>
    </tr>
    <tr>
      <td>YEAR()</td>
      <td>Ano</td>
    </tr>
    <tr>
      <td>MONTH()</td>
      <td>Mês</td>
    </tr>
    <tr>
      <td>DAY()</td>
      <td>Dia</td>
    </tr>
    <tr>
      <td>HOUR()</td>
      <td>Hora</td>
    </tr>
    <tr>
      <td>MINUTE()</td>
      <td>Minuto</td>
    </tr>
    <tr>
      <td>SECOND()</td>
      <td>Segundo</td>
    </tr>
  </table>
</details>

<h3>Inserir valores em tabelas:</h3>

``` 
  INSERT INTO banco_de_dados.tabela (coluna01, coluna02...)
  VALUES (valor_coluna01, valor_coluna02...);
```

<h3>Atualizar dados em uma tabela (safe update: off):</h3>

``` 
  UPDATE banco_de_dados.tabela
  SET coluna = novo_valor
  WHERE operação_lógica;
  ⚠️ Atualiza todas as linhas que satisfaçam a lógica estabelecida ⚠️
```

<h3>Atualizar dados em uma tabela (safe update: on):</h3>

``` 
  UPDATE banco_de_dados.tabela
  SET coluna = novo_valor
  WHERE operação_lógica (usando coluna da PRIMARY KEY);
```

<h3>Comando para desabilitar o safe update</h3>

``` 
  SET SET SQL_SAFE_UPDATES = 0;
```

<h3>Comando para habilitar o safe update</h3>

``` 
  SET SET SQL_SAFE_UPDATES = 1;
```
