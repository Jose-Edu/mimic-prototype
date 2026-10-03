

A tabela `test_rng` registra as entradas de quais rngs são aplicados em quais testes.

## Estrutura

| Nome da Coluna | Tipo | Constraints         | Descrição                                    |
| -------------- | ---- | ------------------- | -------------------------------------------- |
| id_test        | uuid | PK, FK -> [[tests]] | Referência ao teste.                         |
| id_rng         | uuid | PK, FK -> [[rngs]]  | Referência ao gerador aleatório relacionado. |
