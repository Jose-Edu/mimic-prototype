

A tabela `entity_attribute` define quais atributos uma entidade possui.

## Estrutura

| Nome da Coluna      | Tipo | Constraints          | Descrição                                           |
| ------------------- | ---- | -------------------- | --------------------------------------------------- |
| id_entity_attribute | uuid | PK                   | Identificador único do registro desta tabela.       |
| id_entity           | uuid | FK -> [[entities]]   | Referência à entidade que representa este registro. |
| id_attribute        | uuid | FK -> [[attributes]] | Referência ao atributo relacionado.                 |
