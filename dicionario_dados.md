# DICIONÁRIO DE DADOS

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