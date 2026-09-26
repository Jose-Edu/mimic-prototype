

A tabela `rngs` organiza os geradores de aletoriedade do sistema, mais comumente usada para registrar os dados que o sistema usa.

Os valores usados pelo Mimic ficam no final_values, mas a tabela também registra o método por trás da escolha dos valores possíveis. Os valores são gerados a partir de um sequência que pode ter valores filtrados ou pulados. Também é possível deixar os campos null e definir os final_values arbitrariamente, tendo mais liberdade, mas perdendo informação do sistema.
## Estrutura

| Nome da Coluna | Tipo                                     | Constraints               | Descrição                                                                        |
| -------------- | ---------------------------------------- | ------------------------- | -------------------------------------------------------------------------------- |
| id_rng         | uuid                                     | PK, FK -> [[entities]]    | Identificador único do registro desta tabela.                                    |
| name           | varchar                                  | -                         | Nome do gerador.                                                                 |
| id_filter_rule | uuid                                     | nullable, FK -> [[rules]] | Regra booleana que filtra quais valores da sequência entrarão nos valores final. |
| expected_value | integer                                  | nullable                  | Valor médio esperado, usado para analise de dados.                               |
| num_start      | integer                                  | nullable                  | Valor inicial da sequência.                                                      |
| num_end        | integer                                  | nullable                  | Valor final da sequência.                                                        |
| num_step       | integer                                  | nullable                  | Passo usado pela sequência.                                                      |
| final_values   | integer[]                                | array                     | Valores possíveis de serem retornados.                                           |
| type           | enum("other", "dice", "deck", "spinner") | -                         | Qual a origem de aletoriedade é usada na vida real.                              |

