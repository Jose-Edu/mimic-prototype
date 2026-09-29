
A tabela `rules` armazena as [[Rules/Rules|Rules]] usadas no sistema, sendo as estruturas lógicas do sistema.

## Estrutura

| Nome da Coluna  | Tipo                                                            | Constraints               | Descrição                                                                              |
| --------------- | --------------------------------------------------------------- | ------------------------- | -------------------------------------------------------------------------------------- |
| id_rule         | uuid                                                            | PK, FK -> [[entities]]    | Identificador único do registro desta tabela.                                          |
| name            | varchar                                                         | -                         | Nome da rule.                                                                          |
| type            | enum("math", "validation", "action", "relationship", "trigger") | -                         | Tipo da rule.                                                                          |
| id_trigger_rule | uuid                                                            | nullable, FK -> [[rules]] | Regra de trigger que chamará essa regra, se null, a regra só será chamada manualmente. |
| rule            | jsonb                                                           | -                         | AST em json com a lógica estruturada.                                                  |

