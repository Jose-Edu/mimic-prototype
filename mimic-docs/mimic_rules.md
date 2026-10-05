
A tabela `mimic_rules` armazena as [[Rules/Rules|Rules]] usadas no sistema, sendo as estruturas lógicas do sistema.

## Estrutura

| Nome da Coluna  | Tipo                                                            | Constraints                     | Descrição                                                                              |
| --------------- | --------------------------------------------------------------- | ------------------------------- | -------------------------------------------------------------------------------------- |
| id              | uuid                                                            | PK, FK -> [[mimic_entities]]    | Identificador único do registro desta tabela.                                          |
| name            | varchar                                                         | -                               | Nome da rule.                                                                          |
| type            | enum("math", "validation", "action", "relationship", "trigger") | -                               | Tipo da rule.                                                                          |
| id_trigger_rule | uuid                                                            | nullable, FK -> [[mimic_rules]] | Regra de trigger que chamará essa regra, se null, a regra só será chamada manualmente. |
| rule            | jsonb                                                           | -                               | AST em json com a lógica estruturada.                                                  |

