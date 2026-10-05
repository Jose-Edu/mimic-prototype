

A tabela `mimic_user_role` registra a relação entre os usuários e acessos, definindo quais acessos cada usuário terá.

## Estrutura

| Nome da Coluna | Tipo | Constraints         | Descrição                         |
| -------------- | ---- | ------------------- | --------------------------------- |
| id_user        | uuid | PK, FK -> [[mimic_users]] | Referência ao usuário.            |
| id_access      | uuid | PK, FK -> [[mimic_roles]] | Referência ao acesso relacionado. |

