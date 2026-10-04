

A tabela `tests` organiza os testes do sistema, testes, a nível de Mimic, são formulas que relacionam valores aleatórios à atributos e outros valores, sendo um critério muito comum em diversos sistemas.
A montagem de sua regra, por padrão, só soma todos os valores, podendo ser sobreescrista por uma regra arbitrária de composição.

## Estrutura

| Nome da Coluna | Tipo    | Constraints               | Descrição                                               |
| -------------- | ------- | ------------------------- | ------------------------------------------------------- |
| id_test        | uuid    | PK, FK -> [[entities]]    | Identificador único do registro desta tabela.           |
| name           | varchar | -                         | Nome do teste.                                          |
| id_rule        | uuid    | FK -> [[rules]], nullable | Referência à regra de montagem personalizada. Opcional. |


