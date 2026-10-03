
A tabela `test_types` registra os tipos de [[tests]] que existem no sistema. Usado para padronizar e categorizá-los como em: Testes de combate, testes narrativos ou testes de pericias, por exemplo.

## Estrutura

| Nome da Coluna  | Tipo    | Constraints               | Descrição                                               |
| --------------- | ------- | ------------------------- | ------------------------------------------------------- |
| id_test_type    | uuid    | PK, FK -> [[entities]]    | Identificador único do registro desta tabela.           |
| name            | varchar | -                         | Nome do tipo de teste.                                  |
| id_default_rule | uuid    | FK -> [[rules]], nullable | Referência à regra padrão aplicada a testes desse tipo. |

