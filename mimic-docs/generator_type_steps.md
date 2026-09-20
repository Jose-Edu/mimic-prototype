
A tabela `generator_type_steps` registra o tipo de passo de um tipo de gerador. Passos de um gerador são usados para medir a geração da ficha quanto a progresso pós criação. Exemplo: Subir de nível, avançar numa perícia e etc. Servem como categorização dos passos.

## Estrutura

| Nome da Coluna         | Tipo    | Constraints               | Descrição                                     |
| ---------------------- | ------- | ------------------------- | --------------------------------------------- |
| id_generator_type_step | uuid    | PK, FK -> [[entities]]    | Identificador único do registro desta tabela. |
| id_generator_type      | uuid    | FK -> [[generator_types]] | Tipo de gerador pai.                          |
| id_validation_rule     | uuid    | FK -> [[rules]]           | Regra de validação desse gerador.             |
| name                   | varchar | -                         | Nome do tipo de gerador.                      |

