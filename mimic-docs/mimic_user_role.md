

A tabela `mimic_user_role` registra a relação entre os usuários e os cargos do mimic, sendo a forma padrão de dar [[mimic_access]] a usuários que serão definidos em [[mimic_user_access]]

## Estrutura

| Nome da Coluna | Tipo | Constraints         | Descrição                          |
| -------------- | ---- | ------------------- | ---------------------------------- |
| id_user        | uuid | PK, FK -> [[mimic_users]] | Referência ao usuário relacionado. |
| id_role        | uuid | PK, FK -> [[mimic_roles]] | Referência ao cargo vinculado.     |
