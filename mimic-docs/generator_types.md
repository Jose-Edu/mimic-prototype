

A tabela `generator_types` registra os tipos de [[generators]] que existem no sistema. Geradores são os bônus de atributos e skills que uma ficha receberá, os tipos de geradores são as categorias desses bônus. Exemplo: Raça, Classe e etc.

## Estrutura

| Nome da Coluna     | Tipo    | Constraints            | Descrição                                                                             |
| ------------------ | ------- | ---------------------- | ------------------------------------------------------------------------------------- |
| id_generator_type  | uuid    | PK, FK -> [[entities]] | Identificador único do registro desta tabela.                                         |
| name               | varchar | -                      | Nome do tipo de gerador.                                                              |
| id_validation_rule | uuid    | FK -> [[rules]]        | Regra de validação do tipo de gerador que todos os geradores desse tipo devem seguir. |
| id_compose_rule    | uuid    | FK -> [[rules]]        | Regra de aplicação dos bônus e skills para os geradores desse tipo.                   |
