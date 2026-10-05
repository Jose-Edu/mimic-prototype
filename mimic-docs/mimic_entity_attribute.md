

A tabela `mimic_entity_attribute` define quais atributos uma entidade possui.

## Estrutura

| Nome da Coluna | Tipo | Constraints                | Descrição                                           |
| -------------- | ---- | -------------------------- | --------------------------------------------------- |
| id             | uuid | PK                         | Identificador único do registro desta tabela.       |
| id_entity      | uuid | FK -> [[mimic_entities]]   | Referência à entidade que representa este registro. |
| id_attribute   | uuid | FK -> [[mimic_attributes]] | Referência ao atributo relacionado.                 |
