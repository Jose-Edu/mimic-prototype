A table `value_types` registra a tipagem de valores que podem ser usadas em atributos e [[Rules/Rules|Rules]]. A tabela serve de padronização de registro dos tipos, sendo usada em multiplos contextos.

[[Value types em Rules]]

## Sobre os tipos de valores:
- Number: Registra número num padrão Double (número de ponto flutuante).
- String: Registra textos.
- Boolean: Registra true/false.
- Entity: Relaciona o id de uma entidade.

## Sobre os tipos de estrutura de dados:
- Value: Registra o valor final, apenas.
- List: Lista encadeada de entrada por ordem.
- Consumable: Estrutura para atributos de barra, sempre recebe dois number, o primeiro, valor atual, e o segundo, valor total.
- Enum: Array imutável de chave de número inteiro e valor qualquer de tipo determinado. Ordenado por order.
- Key-value: Mapa chave-valor de chave string e valor qualquer de tipo determinado. Organizado por order no padrão de: número par: chave, número impar: valor, 

## Estrutura

| Nome da Coluna | Tipo                                                     | Constraints | Descrição                                     |
| -------------- | -------------------------------------------------------- | ----------- | --------------------------------------------- |
| id_value_type  | uuid                                                     | PK.         | Identificador único do registro desta tabela. |
| value_type     | enum("number", "string", "boolean", "entity")            | -           | Tipo de dado.                                 |
| struct_type    | enum("value", "list", "consumable", "enum", "key-value") | -           | Estrutura final do valor.                     |

