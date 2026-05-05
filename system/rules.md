# Rules

## Entrada

- origem:
  - a: Atributo
  - v: Valor manual
  - g: Global
- tipo:
  - int
  - float
  - string
  - bool
  - enum
  - list
- nome-ex: nome externo do valor
- nome-in: nome interno do valor

**EX:**

    "entry": [
    
        {
            "origem": "a" | "v" | "g"...
            "tipo": "int" | "float" ...,
            "nome-ex": "numero de ataques",
            "nome-in": "n_atk"
        }

    ]

## Processamento

- tipos de rule:
  - validation rule (bool)
  - filter rule (bool)
  - trigger rule (bool)
  - action rule
  - compose rule
  - relationship rule

## Saída
