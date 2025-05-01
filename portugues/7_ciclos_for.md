# Ciclos For

Os ciclos `for` em C são diretos. Eles fornecem a capacidade de criar um ciclo - um bloco de código que corre múltiplas vezes. Os ciclos `for` requerem uma variável iteradora, geralmente designada por `i`.

Os ciclos `for` oferecem a seguinte funcionalidade:

*   Inicializar a variável iteradora com um valor inicial
*   Verificar se o iterador atingiu o seu valor final
*   Incrementar o iterador

Por exemplo, se desejarmos iterar sobre um bloco 10 vezes, escrevemos:

```c
int i;
for (i = 0; i < 10; i++) {
    printf("%d\n", i);
}
```

Este bloco imprimirá os números de 0 a 9 (10 números no total).

Os ciclos `for` podem iterar sobre os valores de um array. Por exemplo, se quiséssemos somar todos os valores de um array, usaríamos o iterador `i` como índice do array:

```c
int array[10] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
int sum = 0;
int i;

for (i = 0; i < 10; i++) {
    sum += array[i];
}

/* sum contém agora a[0] + a[1] + ... + a[9] */
printf("A soma do array é %d\n", sum);
```

## Exercício

Calcule o fatorial (multiplicação de todos os itens `array[0]` a `array[9]`, inclusive) da variável `array`.

```c
#include <stdio.h>

int main() {
  int array[] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
  int factorial = 1;
  int i;

  /* calcule o fatorial usando um ciclo for aqui*/

  printf("10! é %d.\n", factorial);
}
```