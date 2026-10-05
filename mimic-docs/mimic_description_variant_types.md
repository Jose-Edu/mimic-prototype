

A tabela `mimic_description_variant_types` define os tipos de variantes de descrições usadas no sistema, ex: Idioma, Tamanho de descrição e etc.
## Estrutura

| Nome da Coluna | Tipo    | Constraints       | Descrição                                          |
| -------------- | ------- | ----------------- | -------------------------------------------------- |
| id             | uuid    | PK                | Identificador único do registro desta tabela.      |
| id_system      | uuid    | FK -> [[mimic_systems]] | Referência ao sistema ao qual o registro pertence. |
| name           | varchar | -                 | Nome do tipo.                                      |
