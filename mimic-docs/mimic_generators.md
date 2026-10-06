

A tabela `mimic_generators` registra os geradores usados para compor as entradas de [[mimic_attributes]] e [[mimic_actions]] aplicados às [[mimic_sheets]]. Exemplos: Instâncias de raças e classes: Elfo, Guerreiro, Humando, Mago e etc.

## Estrutura

| Nome da Coluna     | Tipo    | Constraints                          | Descrição                                                                                                      |
| ------------------ | ------- | ------------------------------------ | -------------------------------------------------------------------------------------------------------------- |
| id                 | uuid    | PK, FK -> [[mimic_entities]]         | Identificador único do registro desta tabela.                                                                  |
| id_generator_type  | uuid    | FK -> [[mimic_generator_types]]      | Tipo de gerador aplicado.                                                                                      |
| id_super_generator | uuid    | nullable, FK -> [[mimic_generators]] | Referência ao gerador pai. Quando um gerador possui um gerador pai, ele é chamado junto a ele automaticamente. |
| name               | varchar | -                                    | Nome do gerador.                                                                                               |
