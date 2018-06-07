<!-- vscode-markdown-toc -->
* [Intordução](#Intorduo)
* [_For_ para varrer uma lista](#For_paravarrerumalista)
* [_For_ usando contadores](#For_usandocontadores)
* [Exercícios](#Exerccios)
* [Desafios](#Desafios)
	* [(Continuação dos desafios da aula passada)](#Continuaodosdesafiosdaaulapassada)

<!-- vscode-markdown-toc-config
	numbering=false
	autoSave=true
	/vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc -->
# For
---

##  1. <a name='Intorduo'></a>Intordução

Vimos Aula passada como fazer um laço de repetição que é executado até que uma determinada condição seja falsa. E se os dados estiverem em uma lista? Como fazemos para exectar um bloco de código para cada item dessa lista? 

##  2. <a name='For_paravarrerumalista'></a>_For_ para varrer uma lista
Neste caso podemos usar o comando for, que faz um ciclo do laço de repetição para cada item da lista, armazenando o valor do item em uma variável temporária que pode ser usada dentro do bloco de código:

```shell
dados="A B C D E F"
for letra in $dados; do
    echo "Letra: $letra"
done
```
O comando acima contém uma lista de informações separadas por espaços, com um loop _for_ que vai colocar o valor do item que está sendo lido dentro da variável _letra_, que é usada dentro do bloco, para mostrar a mensagem com cada letra.

##  3. <a name='For_usandocontadores'></a>_For_ usando contadores
Uma prática comum é criar uma variável temporária, que serve para contar quantos ciclos já foram executados dentro de um laço. Podemos usar este valor para acessar _arrays_ e _matrizes_, ou para executar operações com o número.

Quando usamos um _for_ com contadores, a sintaxe é um pouco diferente:
```shell
for (( i=0; i < 5; i++)); do
    echo "contador com valor $i"
done
```
Veja que usamos dois parênteses, ao invés de colchetes como em outros laços. Além disso, perceba que existem três expressões no cabeçalho do laço:

>i=0

O primeiro deles é a declaração inicial, onde criamos e/ou definimos uma variável como contador. Neste Caso ela é igual a zero.

>i < 5

Indica a condição do loop. Ou seja: enquanto o valor de _i_ for menor que _5_, o bloco será executado até o final.

>i++

Indica a alteração do valor após cada ciclo do loop. Toda vez que o interpretador chegar no final do bloco de código, a variável _i_ será incrementada em _1_.

##  4. <a name='Exerccios'></a>Exercícios
1. Faça um programa que leia todos os usuários do _/etc/passwd_ e mostre um a um, usando um laço for
2. Faça um programa que leia e mostre na tela um resumos de todos os últimos logins (use o comando last), usando for
3. Carregue os nomes e diretórios home de todos os usuários, usando for.

##  5. <a name='Desafios'></a>Desafios 
###  5.1. <a name='Continuaodosdesafiosdaaulapassada'></a>(Continuação dos desafios da aula passada)
1. Crie um programa que leia todos os produtos cadastrados e mostre um resumo para cada item, e um resumo do valor total de mercadorias em estoque.
2. Crie um programa de cadastro de usuários, que armazene o nome do usuário, quanto este usuário gastou em sua última compra.
3. Crie um programa para que o usuário possa comprar os produtos, mostrando quanto ele já gastou na compra. No final da compra, gere um cupom de compras para o usuário saber o que ele comprou, e quanto foi gasto.
Faça o cupom da melhor forma possível, cada detalhe é importante.
