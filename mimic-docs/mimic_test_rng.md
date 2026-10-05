

A tabela `mimic_test_rng` registra as entradas de quais rngs são aplicados em quais testes.

## Estrutura

| Nome da Coluna | Tipo | Constraints              | Descrição                                    |
| -------------- | ---- | ------------------------ | -------------------------------------------- |
| id_test        | uuid | PK, FK -> [[mimic_tests]]      | Referência ao teste.                         |
| id_rng         | uuid | PK, FK -> [[mimic_rngs]] | Referência ao gerador aleatório relacionado. |
