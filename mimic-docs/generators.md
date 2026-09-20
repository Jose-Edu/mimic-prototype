

A tabela `generators` registra os geradores usados para compor as entradas de [[attributes]] e [[skills]] aplicados às [[sheets]]. Exemplos: Instâncias de raças e classes: Elfo, Guerreiro, Humando, Mago e etc.

## Estrutura

| Nome da Coluna     | Tipo    | Constraints                    | Descrição                                                                                                      |
| ------------------ | ------- | ------------------------------ | -------------------------------------------------------------------------------------------------------------- |
| id_generator       | uuid    | PK, FK -> [[entities]]         | Identificador único do registro desta tabela.                                                                  |
| id_generator_type  | uuid    | FK -> [[generator_types]]      | Tipo de gerador aplicado.                                                                                      |
| id_super_generator | uuid    | nullable, FK -> [[generators]] | Referência ao gerador pai. Quando um gerador possui um gerador pai, ele é chamado junto a ele automaticamente. |
| name               | varchar | -                              | Nome do gerador.                                                                                               |
