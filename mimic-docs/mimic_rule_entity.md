A tabela `mimic_rule_entity` organiza o relacionamento N:N entre rules e entity. Usado para mapear entities que são dependencias de rules.
[[Rules externals]]

## Estrutura

| Nome da Coluna | Tipo                      | Constraints                  | Descrição                                                                                  |
| -------------- | ------------------------- | ---------------------------- | ------------------------------------------------------------------------------------------ |
| id             | uuid                      | PK, FK -> [[mimic_rules]]          | Rule do relacionamento.                                                                    |
| id_entity      | uuid                      | PK, FK -> [[mimic_entities]] | Entity do relacionamento.                                                                  |
| resolve_method | enum("manual", "context") | -                            | Método de resolução de dependencias.                                                       |
| value_type     | uuid                      | FK -> [[mimic_value_types]]        | Tipo de valor usado na rule. Sempre vai ser entity no valor, mas vai variar pela estrutura |
| internal_name  | varchar                   | -                            | nome interno da dependencia.                                                               |
