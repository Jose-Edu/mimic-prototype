

A tabela `mimic_action_types` registra os tipos de [[mimic_actions]] que existem no sistema. Servindo como categorias como: Pericias, Golpes, Passivas e etc.

## Estrutura

| Nome da Coluna     | Tipo    | Constraints                  | Descrição                                              |
| ------------------ | ------- | ---------------------------- | ------------------------------------------------------ |
| id                 | uuid    | PK, FK -> [[mimic_entities]] | Identificador único do registro desta tabela.          |
| name               | varchar | -                            | Nome do tipo de action.                                 |
| id_validation_rule | uuid    | FK -> [[mimic_rules]]        | Regra de validação estrutural para esse tipo de action. |
