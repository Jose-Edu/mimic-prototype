

A tabela `systems` registra os sistemas existentes na base de dados.

## Estrutura

| Nome da Coluna  | Tipo                  | Constraints                 | Descrição                                                       |
| --------------- | --------------------- | --------------------------- | --------------------------------------------------------------- |
| id_system       | uuid                  | PK                          | Identificador único do registro desta tabela.                   |
| mimic_version   | varchar               | -                           | Versão do Mimic no padrão 1.0.0.                                |
| name            | varchar               | -                           | Nome do sistema.                                                |
| system_version  | varchar               | -                           | Versão do sistema, no padrão 1.0.0.                             |
| id_author_user  | uuid                  | FK -> [[users]]             | Usuário que é autor do sistema.                                 |
| system_hash     | varchar               | -                           | Hash da geração do sistema.                                     |
| created_at      | timestamp             | -                           | Horário de criação do sistema.                                  |
| updated_at      | timestamp             | -                           | Horário da última atualização no sistema.                       |
| type            | enum("root", "delta") | -                           | Tipo de sistema, se é um sistema ou um [[Mimic Deltas\|Delta]]. |
| id_delta_origin | uuid                  | nullable, FK -> [[systems]] | Sistema base do delta, caso seja um.                            |

