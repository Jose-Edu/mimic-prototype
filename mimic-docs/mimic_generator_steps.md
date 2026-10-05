

A tabela `mimic_generator_steps` registra os passos dos [[mimic_generators]]. Passos de um gerador são usados para medir a geração da ficha quanto a progresso pós criação. Exemplo: Subir de nível, avançar numa perícia e etc.

## Estrutura

| Nome da Coluna         | Tipo    | Constraints                    | Descrição                                                                    |
| ---------------------- | ------- | ------------------------------ | ---------------------------------------------------------------------------- |
| id                     | uuid    | PK, FK -> [[mimic_entities]]   | Identificador único do registro desta tabela.                                |
| id_generator           | uuid    | FK -> [[mimic_generators]]           | Referência ao gerador pai.                                                   |
| id_generator_type_step | uuid    | FK -> [[mimic_generator_type_steps]] | Tipo de passo de gerador aplicado.                                           |
| name                   | varchar | -                              | Nome do generator step.                                                      |
| id_validation_rule     | uuid    | FK -> [[mimic_rules]], Nullable      | Regra de validação própria, se null, aplica o padrão do generator_type_step. |
