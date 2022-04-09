# Questões de prova

## Questão 1

*IF Sul Rio-Grandense - 2021 Programação JavaScript IF Sul Rio-Grandense Professor*

Considere o seguinte código JavaScript: 

var a = [1,2,3,4,5];

a.slice(0,3);

a.splice(1,1);

a.pop();

Qual o valor da variável a ao término da execução do código?

A - [1,3,4]

B - [1,3,4,5]

C - [1,3]

D - [3,4,5]

### Comentário

O método slice de Array retorna os dados que estão compreendidos nos índices especificados: `slice(inicio, [fim])`. Assim, a.slice(0, 3) retorna [1, 2, 3], mas não altera a variável a. O método splice de Array remove n elementos a partir do índice i, substuindo-os por b: `a.splice(i, n, [b])`. No caso, não foi especificado o terceiro argumento, então a,splice(1, 1) simplesmente remove o segundo elemento (2). Por fim, o método pop de Array remove e retorna o último elemento (5). Desta maneira, a variável `a = [1, 3, 4]` ao fim do programa.   

Gabarito: A

