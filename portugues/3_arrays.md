# Arrays

Arrays são variáveis especiais que podem conter mais do que um valor sob o mesmo nome de variável, organizados com um índice. Arrays são definidos usando uma sintaxe muito direta:

```c
/* define um array de 10 inteiros o seja, uma lista de 10 numeros*/
int numbers[10];
```

Aceder a um número do array é feito usando a mesma sintaxe. Note que os arrays em C são baseados em zero, o que significa que se definimos um array de tamanho 10, então as células do array de 0 a 9 (inclusive) estão definidas. `numbers[10]` não é um valor real.

```c
int numbers[10];

/* preenche o array */
numbers[0] = 10;
numbers[1] = 20;
numbers[2] = 30;
numbers[3] = 40;
numbers[4] = 50;
numbers[5] = 60;
numbers[6] = 70;

/* imprime o 7º número do array, que tem o índice 6 */
printf("O 7º número no array é %d", numbers[6]);
```

Arrays só podem ter um tipo de variável, porque são implementados como uma sequência de valores na memória do computador. Por causa disso, aceder a uma célula específica do array é muito eficiente.

## Exercício

*   O código abaixo não compila, porque a variável `grades` está em falta.
*   Uma das notas está em falta. Consegue defini-la para que a média das notas seja 85?

```c
#include <stdio.h>

int main() {
  /* TODO: defina a variável grades aqui */
  int average;

  grades[0] = 80;
  /* TODO: defina a nota em falta
     para que a média seja 85. */
  grades[2] = 90;

  average = (grades[0] + grades[1] + grades[2]) / 3;
  printf("A média das 3 notas é: %d", average);

  return 0;
}
```