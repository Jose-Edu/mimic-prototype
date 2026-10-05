

A tabela `mimic_generator_step_skill` é usada para mapear o relacionamento N:N entre o [[mimic_generator_steps]] e [[mimic_skills]]. Relacionamento esse que representa quais skills um generator step aplica na sheet.

## Estrutura

| Nome da Coluna    | Tipo | Constraints               | Descrição                                     |
| ----------------- | ---- | ------------------------- | --------------------------------------------- |
| id                | uuid | PK                        | Identificador único do registro desta tabela. |
| id_generator_step | uuid | FK -> [[mimic_generator_steps]] | Chave estrangeira para o generator step.      |
| id_skill          | uuid | FK -> [[mimic_skills]]          | Chave estrangeira para a skill.               |

