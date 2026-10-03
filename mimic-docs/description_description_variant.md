

A tabela `description_description_variant` armazena a relação N:N entre descrições e as suas variantes. Representa a idea de que uma descrição pode seguir a muitas variantes e uma variante pode ser implementada a muitas descrições.

## Estrutura

| Nome da Coluna         | Tipo    | Constraints                        | Descrição                           |
| ---------------------- | ------- | ---------------------------------- | ----------------------------------- |
| id_description         | uuid    | PK, FK -> [[descriptions]]         | Referencia à descrição.             |
| id_description_variant | uuid    | PK, FK -> [[description_variants]] | Referência à variante implementada. |


