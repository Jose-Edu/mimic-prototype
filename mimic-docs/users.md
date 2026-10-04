

A tabela `users` organiza quais usuários existem no banco de dados e poderão interagir com os sistemas.
O Mimic não controla por si funções como autenticação, portanto, cada app deve criar uma 1:1 com essa tabela para seus próprios dados de usuários.

## Estrutura

| Nome da Coluna | Tipo    | Constraints | Descrição                                     |
| -------------- | ------- | ----------- | --------------------------------------------- |
| id_user        | uuid    | PK          | Identificador único do registro desta tabela. |
| name           | varchar | -           | Nome do usuário.                              |

