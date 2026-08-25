# Banco de Dados Aula03

## MER DER Conceitual

![MER DER Conceitual](./MER_DER_Conceitual.png)

## MER DER Lógico

![MER DER Lógico](./MER_DER_Logico.png)

## Dicionário de Dados

| Tabela | Campo | Tipo | Tamanho | Descrição | Chave |
|---|---|---|---:|---|---|
| AUTORES | id_autor | INT | 11 | Identificador do autor | PK |
| AUTORES | nome | VARCHAR | 100 | Nome do autor | — |
| AUTORES | nacionalidade | VARCHAR | 50 | Nacionalidade do autor | — |
| AUTORES | data_nascimento | DATE | — | Data de nascimento | — |
| LIVRO | id_livro | INT | 11 | Identificador do livro | PK |
| LIVRO | titulo | VARCHAR | 150 | Título do livro | — |
| LIVRO | ISBN | VARCHAR | 20 | Código ISBN | — |
| LIVRO | genero | VARCHAR | 50 | Gênero literário | — |
| LIVRO | ano_publicacao | INT | 4 | Ano de publicação | — |
| LIVRO | id_autor | INT | 11 | Autor do livro | FK |
| CLIENTE | id_cliente | INT | 11 | Identificador do cliente | PK |
| CLIENTE | nome | VARCHAR | 100 | Nome do cliente | — |
| CLIENTE | CPF | VARCHAR | 14 | CPF do cliente | — |
| VENDA | id_venda | INT | 11 | Identificador da venda | PK |
| VENDA | data_venda | DATE | — | Data da venda | — |
| VENDA | valor_total | DECIMAL | 10,2 | Valor total da venda | — |
| VENDA | id_cliente | INT | 11 | Cliente da venda | FK |
| ITEM_VENDA | id | INT | 11 | Identificador do item | PK |
| ITEM_VENDA | id_venda | INT | 11 | Venda relacionada | FK |
| ITEM_VENDA | id_livro | INT | 11 | Livro vendido | FK |
| ITEM_VENDA | quantidade | INT | 11 | Quantidade vendida | — |
| ITEM_VENDA | preco_unitario | DECIMAL | 10,2 | Preço unitário | — |

## Dados de Teste

### AUTORES

| id_autor | nome | nacionalidade | data_nascimento |
|---:|---|---|---|
| 1 | Machado de Assis | Brasileira | 21/06/1839 |
| 2 | Aluísio Azevedo | Brasileira | 14/04/1857 |
| 3 | Jorge Amado | Brasileira | 10/08/1912 |
| 4 | Clarice Lispector | Brasileira | 10/12/1920 |
| 5 | Graciliano Ramos | Brasileira | 27/10/1892 |
| 6 | George Orwell | Britânica | 25/06/1903 |
| 7 | J. R. R. Tolkien | Britânica | 03/01/1892 |

### LIVRO

| id_livro | titulo | ISBN | genero | ano_publicacao | id_autor |
|---:|---|---|---|---:|---:|
| 1 | Dom Casmurro | 9788535902772 | Romance | 1899 | 1 |
| 2 | O Cortiço | 9788573260422 | Romance | 1890 | 2 |
| 3 | Capitães da Areia | 9788535911699 | Ficção | 1937 | 3 |
| 4 | A Hora da Estrela | 9788520929662 | Romance | 1977 | 4 |
| 5 | Vidas Secas | 9788501067342 | Drama | 1938 | 5 |
| 6 | 1984 | 9788535914849 | Distopia | 1949 | 6 |
| 7 | O Hobbit | 9788595084759 | Fantasia | 1937 | 7 |

### CLIENTE

| id_cliente | nome | CPF |
|---:|---|---|
| 1 | Ana Souza | 123.456.789-01 |
| 2 | Bruno Lima | 234.567.890-12 |
| 3 | Carla Mendes | 345.678.901-23 |
| 4 | Daniel Rocha | 456.789.012-34 |
| 5 | Eduarda Alves | 567.890.123-45 |

### VENDA

| id_venda | data_venda | valor_total | id_cliente |
|---:|---|---:|---:|
| 1001 | 10/01/2026 | R$ 189,90 | 1 |
| 1002 | 12/01/2026 | R$ 79,90 | 2 |
| 1003 | 15/01/2026 | R$ 245,50 | 3 |
| 1004 | 02/02/2026 | R$ 129,80 | 1 |
| 1005 | 08/02/2026 | R$ 299,90 | 4 |

### ITEM_VENDA

| id | id_venda | id_livro | quantidade | preco_unitario |
|---:|---:|---:|---:|---:|
| 1 | 1001 | 1 | 1 | R$ 59,90 |
| 2 | 1001 | 2 | 2 | R$ 65,00 |
| 3 | 1002 | 3 | 1 | R$ 79,90 |
| 4 | 1003 | 4 | 1 | R$ 120,00 |
| 5 | 1003 | 5 | 1 | R$ 125,50 |
| 6 | 1004 | 2 | 2 | R$ 64,90 |
| 7 | 1005 | 6 | 1 | R$ 149,90 |
| 8 | 1005 | 7 | 1 | R$ 150,00 |
