

A tabela `generator_step_skill` é usada para mapear o relacionamento N:N entre o [[generator_steps]] e [[skills]]. Relacionamento esse que representa quais skills um generator step aplica na sheet.

## Estrutura

| Nome da Coluna          | Tipo | Constraints               | Descrição                                     |
| ----------------------- | ---- | ------------------------- | --------------------------------------------- |
| id_generator_step_skill | uuid | PK                        | Identificador único do registro desta tabela. |
| id_generator_step       | uuid | FK -> [[generator_steps]] | Chave estrangeira para o generator step.      |
| id_skill                | uuid | FK -> [[skills]]          | Chave estrangeira para a skill.               |

