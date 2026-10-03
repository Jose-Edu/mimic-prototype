A tabela `role_access` registra o relacionamento N:N entre role e access. define quais acessos um cargo dará para o usuário que o possuir.

## Estrutura

| Nome da Coluna | Tipo | Constraints          | Descrição                                    |
| -------------- | ---- | -------------------- | -------------------------------------------- |
| id_access      | uuid | PK, FK -> [[access]] | Chave estrangeira para a tabela relacionada. |
| id_role        | uuid | PK, FK -> [[roles]]  | Referência ao papel ou função vinculada.     |

