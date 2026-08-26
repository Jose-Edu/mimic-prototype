Regras de controle de fluxo

- if - condição booleana \[boolean, if, else]

{
	"mimic-version": '1.0.0',
	"rule-type": 'math',
	"root": {
		"operation-type": 'math',
		"operation": '+',
		"arguments": [
			1,

			 {
				 "operation-type": 'flux',
				"operation": 'if',
				"arguments": [
						true,
						 3,
						 2
				]
			 }
		]
	}
} > 4

[[Rules de validation]]