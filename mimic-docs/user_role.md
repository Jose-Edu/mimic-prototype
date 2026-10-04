

A tabela `user_role` registra a relação entre os usuários e os cargos do mimic, sendo a forma padrão de dar [[access]] a usuários que serão definidos em [[user_access]]

## Estrutura

| Nome da Coluna | Tipo | Constraints         | Descrição                          |
| -------------- | ---- | ------------------- | ---------------------------------- |
| id_user        | uuid | PK, FK -> [[users]] | Referência ao usuário relacionado. |
| id_role        | uuid | PK, FK -> [[roles]] | Referência ao cargo vinculado.     |
