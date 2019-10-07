
# Crie seu perfil no git hub
# Coloque os exercícios realizados na sua área no git

Crie uma rotina que gera entradas aleatoriamente, e mostre o resultado da execução de cada desafio em um arquivo texto.

## Desafio 1

A entrada é uma matriz bidimensional, 

O programa deve girar a matrix uma quantidade de vezes e imprimir a matriz resultante ao final. A rotação deve estar no sentido anti-horário.

A rotação de uma matriz é representada pela figura a seguir. 

início         primeira rotação  Segunda rotação
 1 2 3 4        2  3  4  5       3  4  5  6
12 1 2 5  ->   1  2  3  6 ->     2  3  4  7
11 4 3 6      12  1  4  7         1  2  1  8
10 9 8 7      11 10  9  8       12 11 10  9

## Desafio 2

Para duas cadeias A e B, definimos a semelhança das cadeias como sendo o comprimento do prefixo mais longo comum a ambas as cadeias. Por exemplo, a similaridade das cadeias "abc" e "abd" é 2, enquanto a similaridade das cadeias "aaa" e "aaab" é 3.

Calcule a soma das semelhanças de uma sequência S com cada um dos seus sufixos.

Ex: aabagh
sufixo 1: abagh
sufixo 2: bagh
sufixo 3: agh
sufixo 4: gh
sufixo 5: h


Formato de entrada

A primeira linha contém o número de casos de teste t.
Cada uma das próximas t linhas contém uma string para processar.


A saída é gerada da seguinte forma: Linhas t de saída, cada uma contendo a resposta para o caso de teste correspondente.

## Desafio 3

Greg quer construir uma String S, de comprimento N. Começando com uma string vazia, ele pode executar operações:

Adicione um caractere ao final de S por A dólares.
Copie qualquer substring de S e adicione-o ao final de por B dólares.

Calcule a quantidade mínima de dinheiro que Greg precisa construir.

Formato de entrada

A primeira linha contém o número de casos de teste.

As linhas subseqüentes descrevem um caso de teste em duas linhas:
A primeira linha contém 3 números inteiros separados por espaço, N , A, e B, respectivamente.
A segunda linha contém S (a string que Greg deseja construir).

## Desafio 4


Tieu é dono de uma pizzaria e a administra à sua maneira. Enquanto em um restaurante normal, um cliente é atendido seguindo a regra de primeiro a chegar, primeiro a ser atendido, Tieu simplesmente minimiza o tempo médio de espera de seus clientes. Então, ele decide quem é servido primeiro, independentemente de quanto mais cedo ou mais tarde uma pessoa vier.

Diferentes tipos de pizzas levam diferentes quantidades de tempo para cozinhar. Além disso, quando ele começa a cozinhar uma pizza, ele não pode cozinhar outra pizza até que a primeira pizza esteja completamente cozida. Digamos que temos três clientes que chegam no momento t = 0, t = 1, & t = 2, respectivamente, e o tempo necessário para cozinhar suas pizzas é 3, 9 e 6, respectivamente. Se o Tieu aplicar a regra de primeiro a chegar, primeiro a ser servido, o tempo de espera de três clientes será 3, 11 e 16, respectivamente. O tempo médio de espera neste caso é (3 + 11 + 16) / 3 = 10. Esta não é uma solução otimizada. Depois de atender o primeiro cliente no momento t = 3, Tieu pode optar por atender o terceiro cliente. Nesse caso, o tempo de espera será 3, 7 e 17, respectivamente. Portanto, o tempo médio de espera é (3 + 7 + 17) / 3 = 9.

Ajude Tieu a alcançar o tempo médio médio de espera.

Formato de Entrada

A primeira linha contém um número inteiro N, que é o número de clientes.
Nas próximas N linhas, a i-ésima linha contém dois números separados por espaço Ti e Li. Ti é o momento em que o cliente pede uma pizza, e Li é o tempo necessário para cozinhar essa pizza.

## Desafio 5

Há um número de plantas em um jardim. Cada uma dessas plantas foi tratada com uma certa quantidade de pesticida. Após cada dia, se alguma planta tiver mais pesticida que a esquerda, sendo mais fraca que a esquerda, ela morre.

Você recebe os valores iniciais do pesticida em cada uma das plantas. Imprima o número de dias após o qual nenhuma planta morre, ou seja, o tempo após o qual não há plantas com mais conteúdo de pesticida do que a planta à sua esquerda.

Por exemplo, níveis de pesticidas p = [3,6,2,7,5]. Usando uma matriz 1-d indexada, no dia 1 as plantas 2 e 4 morrem deixando p = [3,2,5]. No dia 2, a planta 3 morre saindo p = [3,2]. Como não existe planta com maior concentração de pesticida do que a esquerda, as plantas param de morrer após o dia 2.

Descrição da função
Implemente uma função que retorna um número inteiro representando o número de dias até que as plantas não morram mais de pesticidas.

Formato de entrada

A primeira linha contém um número inteiro referente ao tamanho da matriz.
A próxima linha contém números inteiros separados por espaço representando a matriz.
