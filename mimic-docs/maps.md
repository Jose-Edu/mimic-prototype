

A tabela `maps` representa os mapas usados pelo Mimic. O sistema de cordenadas ABC é uma forma genérica de se refirir aos 2 possíveis formatos de mapeamento:
- XYZ: Segue um plano carteziano comum. A = X, B = Y, C = Z
- QRS: Mapeamento de coordenadas hexagonais. A = Q, B = R, C = S
## Estrutura

| Nome da Coluna | Tipo               | Constraints            | Descrição                                                      |
| -------------- | ------------------ | ---------------------- | -------------------------------------------------------------- |
| id_map         | uuid               | PK, FK -> [[entities]] | Identificador único do registro desta tabela.                  |
| name           | varchar            | -                      | Nome do mapa.                                                  |
| size_a         | integer            | -                      | Tamanho do mapa no eixo A.                                     |
| size_b         | integer            | -                      | Tamanho do mapa no eixo B.                                     |
| size_c         | integer            | -                      | Tamanho do mapa no eixo C.                                     |
| map_system     | enum("xyz", "qrs") | -                      | Sistema de cordenadas usado neste mapa.                        |
| multi_map      | boolean            | -                      | Define se usa as conexões multi mapas definidas em [[map_map]] |

