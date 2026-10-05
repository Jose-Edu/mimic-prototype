
A tabela `mimic_test_types` registra os tipos de [[mimic_tests]] que existem no sistema. Usado para padronizar e categorizá-los como em: Testes de combate, testes narrativos ou testes de pericias, por exemplo.

## Estrutura

| Nome da Coluna  | Tipo    | Constraints                     | Descrição                                               |
| --------------- | ------- | ------------------------------- | ------------------------------------------------------- |
| id              | uuid    | PK, FK -> [[mimic_entities]]    | Identificador único do registro desta tabela.           |
| name            | varchar | -                               | Nome do tipo de teste.                                  |
| id_default_rule | uuid    | FK -> [[mimic_rules]], nullable | Referência à regra padrão aplicada a testes desse tipo. |

