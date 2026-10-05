
A tabela `mimic_skills` registra as habilidades que as fichas poderão ter.
skills são quaisquer ações a nível de [[Rules/Rules|Rules]], como golpes, pericias para testes e etc.

## Estrutura

| Nome da Coluna | Tipo    | Constraints                  | Descrição                                     |
| -------------- | ------- | ---------------------------- | --------------------------------------------- |
| id             | uuid    | PK, FK -> [[mimic_entities]] | Identificador único do registro desta tabela. |
| id_skill_type  | uuid    | FK -> [[mimic_skill_types]]  | Tipo de habilidade                            |
| name           | varchar | -                            | Nome da habilidade                            |
| id_action_rule | uuid    | FK -> [[mimic_rules]]        | Regra de ação da skill.                       |
