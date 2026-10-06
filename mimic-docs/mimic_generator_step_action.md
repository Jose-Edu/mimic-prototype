

A tabela `mimic_generator_step_action` é usada para mapear o relacionamento N:N entre o [[mimic_generator_steps]] e [[mimic_actions]]. Relacionamento esse que representa quais actions um generator step aplica na sheet.

## Estrutura

| Nome da Coluna    | Tipo | Constraints               | Descrição                                     |
| ----------------- | ---- | ------------------------- | --------------------------------------------- |
| id                | uuid | PK                        | Identificador único do registro desta tabela. |
| id_generator_step | uuid | FK -> [[mimic_generator_steps]] | Chave estrangeira para o generator step.      |
| id_action          | uuid | FK -> [[mimic_actions]]          | Chave estrangeira para a action.               |

