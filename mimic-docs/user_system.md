

A tabela `user_system` organiza quais usuários estão interagindo (jogando) quais sistemas. Lembrando que cada campanha tem seu próprio sistema, conforme o conceito de [[Mimic Deltas]].

## Estrutura

| Nome da Coluna | Tipo | Constraints           | Descrição                                          |
| -------------- | ---- | --------------------- | -------------------------------------------------- |
| id_user        | uuid | PK, FK -> [[users]]   | Referência ao usuário relacionado.                 |
| id_system      | uuid | PK, FK -> [[systems]] | Referência ao sistema ao qual o registro pertence. |

