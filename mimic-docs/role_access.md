A tabela `role_access` registra o relacionamento N:N entre role e access. define quais acessos um cargo dará para o usuário que o possuir.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_access | integer | PK, FK -> [[access]] | Chave estrangeira para a tabela relacionada. |
| id_role | integer | PK, FK -> [[roles]] | Referência ao papel ou função vinculada. |

