

A tabela `mimic_sheet_types` registra os tipos de [[mimic_sheets]] usadas no sistema.

## Estrutura

| Nome da Coluna     | Tipo                                             | Constraints                            | Descrição                                                                |
| ------------------ | ------------------------------------------------ | -------------------------------------- | ------------------------------------------------------------------------ |
| id                 | uuid                                             | PK, FK -> [[mimic_entities]]           | Identificador único do registro desta tabela.                            |
| name               | varchar                                          | -                                      | Nome do tipo de ficha.                                                   |
| id_validation_rule | uuid                                             | FK -> [[mimic_rules]]                  | Regra de validação estrutural.                                           |
| id_compose_rule    | uuid                                             | FK -> [[mimic_rules]]                  | Regra de composição das fichas.                                          |
| category           | enum("other", "player", "npc", "item", "object") | -                                      | Categoria no qual esse tipo de ficha se enquadra.                        |
| id_base_generator  | uuid                                             | FK -> [[mimic_generators]], nullable   | Gerador base aplicado por padrão a todas as fichas desse tipo. Opcional. |
| id_default_group   | uuid                                             | FK -> [[mimic_sheet_groups]], nullable | Grupo aplicado por padrão para as fichas desse tipo. Opcional.           |

