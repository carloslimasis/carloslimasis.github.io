---
title: Hoisting
updated: 2016-01-10
---

## Hoisting

O termo **Hoisting** vem do verbo **hoist** que traduzido significa **içar**. Em **Javascript** as funções e as variáveis são **hoisted**, ou seja, isto significa a grosso modo que elas são **içadas ao topo**. 

O **Hoisting** é um comportamento do **Javascript** responsável por mover declarações para o topo de um escopo.

Para um melhor entendimento vamos mostrar alguns exemplos:

```
	//Exemplo 1
	//Escopo Global

	foo = 2
	var foo;
```

```
	//Exemplo 2
	//Escopo Global

	exemplo();

	function exemplo() {
		console.log('Exemplo de Hoisting');
	}
```

No primeiro exemplo, temos a variável foo que foi declarada **DEPOIS** de sua atribuição.
No segundo exemplo, temos a função exemplo() que foi declarada **DEPOIS** de sua chamada.

Estes dois exemplos funcionam!!!

Tá, mas como isso é possível???
Por causa do **Hoisting**.

Mas como??? 

Recapitulando, o **Hoisting** faz com que as declarações de variáveis e funções sejam **içadas ao topo**.
Desta forma, os exemplos acima poderiam ser implicitamente entendidos como:


```
	//Exemplo 1
	//Escopo Global

	var foo;
	foo = 2;
```

```
	//Exemplo 2
	//Escopo Global

	function exemplo() {
		console.log('Exemplo de Hoisting');
	}

	exemplo();
```


Este comportamento também acontece em escopo de função. Segue o exemplo abaixo:

```
	hoistingFunction();

	function hoistingFunction() {
		foo;
		var foo = 'Variavel hoisting dentro do escopo da função';
		console.log(foo);
	}
```


Bom pessoal, neste artigo falei sobre o comportamento do **Hoisting** presente no **Javascript** esperem que tenha ajudado vocês de alguma forma. Fiquem ligados nos próximos artigos. Valeu!
