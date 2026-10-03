

A tabela `skill_types` registra os tipos de [[skills]] que existem no sistema. Servindo como categorias como: Pericias, Golpes, Passivas e etc.

## Estrutura

| Nome da Coluna     | Tipo    | Constraints            | Descrição                                              |
| ------------------ | ------- | ---------------------- | ------------------------------------------------------ |
| id_skill_type      | uuid    | PK, FK -> [[entities]] | Identificador único do registro desta tabela.          |
| name               | varchar | -                      | Nome do tipo de skill.                                 |
| id_validation_rule | uuid    | FK -> [[rules]]        | Regra de validação estrutural para esse tipo de skill. |
