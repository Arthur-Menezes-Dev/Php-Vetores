# PhP-Vetores
Aula de PhP 16/10/2026 Sobre Vetores 

## Vetor Básico com Numeros
```php
<?php
	
	$clima = []; // DEFINIDO COMO VETOR
	$clima[0] = 25;
	$clima[1] = 30;
	$clima[2] = 28;
	$clima[3] = 23;
	$clima[4] = 10;
	$clima[5] = 15;
	$clima[6] = 26;


	echo "Vetor: " . PHP_EOL;
	echo "posição 0: " . $clima[0] . PHP_EOL;
	echo "posição 1: " . $clima[1] . PHP_EOL;
	echo "posição 2: " . $clima[2] . PHP_EOL;
	echo "posição 3: " . $clima[3] . PHP_EOL;
	echo "posição 4: " . $clima[4] . PHP_EOL;
	echo "posição 5: " . $clima[5] . PHP_EOL;
	echo "posição 6: " . $clima[6] . PHP_EOL;



?>
```

## Vetor Básico com Palavras e Comando For e Foreach
```php
<?php
	
	$Produto = []; // DEFINIDO COMO VETOR
	$Produto[0] = "Arroz";
	$Produto[1] = "Feijão";
	$Produto[2] = "Macarrão";
	$Produto[3] = "Feijão de Corda";
	$Produto[4] = "Batata";
	$Produto[5] = "Salada";
	$Produto[6] = "Picanha";

	echo "Vetor: " . PHP_EOL;

  // For

  for($i=0;$i<7;$i++){
		echo "Posição $i: " . $Produto[$i] . PHP_EOL;
	}

  echo "\n";

  //Foreach

	foreach($Produto as $p){
		echo "Produto: " . $p . PHP_EOL;
	}

  /* Quando usar cada? A escrita do for é mais complexa que a do Foreach porem eu posso trabalhar com posição por posição de cada índice do vetor. O for conhece posição por posição do vetor
     o Foreach é mais simples na escrita e sempre vai mostrar todos os itens do vetor. Porem ele não trabalha/ mostra posição por posição. Ele mostra todos de uma vez só. */

?>
```

## Escrita Simplificada de Vetor
```php
<?php
	
	$Produto = ["Arroz","Feijão","Macarrão","Feijão de Corda","Batata","Salada","Picanha"]; // DEFINIDO COMO VETOR
	
	echo "Vetor: " . PHP_EOL;

	for($i=0;$i<7;$i++){
		echo "Posição $i: " . $Produto[$i] . PHP_EOL;
	}

	echo "\n";

	foreach($Produto as $p){
		echo "Produto: " . $p . PHP_EOL;
	}

?>
```

## Vetor Associativo
```php
<?php
	
	//VETOR ASSOCIATIVO (Chave e Valor)
	$Produto = [
		[
		"Nome"=> "Arroz",
		"Quantidade"=> 30
		],
		[
		"Nome"=> "Feijão",
		"Quantidade"=> 15
		],
		[
		"Nome"=> "Macarrão",
		"Quantidade"=> 10
		]
	];

	foreach($Produto as $p){
	echo "Nome do Produto: " . $p["Nome"] . PHP_EOL;
 	echo "Quantidade do Produto: " . $p["Quantidade"] . PHP_EOL;
	echo "\n";
	}

/* Colocamos um vetor dentro do outro*/
?>
```

## Vetores com objetos


//São 6 arquivos HelloWorld.php e Produtos.php

### Produtos.php
```php
<?php

class Produto{
	//PROPRIEDADES E ATRIBUTOS
	private $nome;
	private $quantidade;

	//CONSTRUTOR
	public function __construct ($nome, $quantidade){
		$this->nome = $nome;
		$this->quantidade = $quantidade;
	}

	//GETTERS 
	public function getNome(){
		return $this->nome;
	}

	public function getQuantidade(){
		return $this->quantidade;
	}
}

?>


```
###HelloWorld.php
```php
<?php

	include "Produto.php";

	$produtos = [	
		new Produto("Arroz", 10),
		new Produto("Feijão", 20),
		new Produto("Macarrão", 1,),
		new Produto("Batata", 30),
	];

	foreach($produtos as $p){
		echo "Nome do Produto: " . $p->getNome() . PHP_EOL;
		echo "Nome do Quantidade: " . $p->getQuantidade() . PHP_EOL;
		echo "\n";
	}

?>
```

