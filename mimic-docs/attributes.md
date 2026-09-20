

A tabela `attributes` organiza os atributos usados no sistema.

## Estrutura

| Nome da Coluna         | Tipo    | Constraints                  | Descrição                                                                                  |
| ---------------------- | ------- | ---------------------------- | ------------------------------------------------------------------------------------------ |
| id_attribute           | uuid    | PK, FK -> [[entities]]       | Identificador único do registro desta tabela.                                              |
| id_value_rule          | uuid    | FK -> [[rules]]              | Rule que monta o valor final do atributo.                                                  |
| name                   | varchar | -                            | Nome do atributo.                                                                          |
| value_type             | uuid    | FK -> [[value_types]]        | Estrutura de dados usada.                                                                  |
| expected_value_number  | number  | Nullable                     | Preenchimento do valor esperado para número. Valor esperado é usado para analise de dados. |
| expected_value_string  | varchar | Nullable                     | Preenchimento do valor esperado para string. Valor esperado é usado para analise de dados. |
| expected_value_boolean | boolean | Nullable                     | Preenchimento do valor esperado para bool. Valor esperado é usado para analise de dados.   |
| expected_value_entity  | varchar | Nullable                     | Preenchimento do valor esperado para entity. Valor esperado é usado para analise de dados. |
| default_value_number   | number  | Nullable                     | Preenchimento do valor padrão para number.                                                 |
| default_value_string   | varchar | Nullable                     | Preenchimento do valor padrão para string.                                                 |
| default_value_boolean  | boolean | Nullable                     | Preenchimento do valor padrão para bool.                                                   |
| default_value_entity   | uuid    | FK -> [[entities]], Nullable | Preenchimento do valor padrão para entity.                                                 |
| is_composable          | boolean | Default True                 | Se é composto por sub atributos em [[attribute_items]].                                    |
| is_constant            | boolen  | Default False                | Se o valor é constante.                                                                    |
| min_size_value         | integer | Nullable                     | Valor mínimo, aplicavél para valor de number ou tamanho de string.                         |
| max_size_value         | integer | Nullable                     | Valor máximo, aplicavél para valor de number ou tamanho de string.                         |
