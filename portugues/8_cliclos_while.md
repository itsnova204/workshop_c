# Ciclos While

Os ciclos `while` são semelhantes aos ciclos `for`, mas têm menos funcionalidade. Um ciclo `while` continua a executar o bloco `while` enquanto a condição no `while` permanecer verdadeira. Por exemplo, o código seguinte será executado exatamente dez vezes:

```c
int n = 0;
while (n < 10) {
    n++;
}
```

Os ciclos `while` também podem executar infinitamente se for dada uma condição que avalia sempre como verdadeira (diferente de zero):

```c
while (1) {
    /* faz algo */
}
```

## Diretivas de ciclo

Existem duas diretivas de ciclo importantes que são usadas em conjunto com todos os tipos de ciclo em C - as diretivas `break` e `continue`.

A diretiva `break` interrompe um ciclo após dez iterações, mesmo que o ciclo `while` nunca termine:

```c
int n = 0;
while (1) {
    n++;
    if (n == 10) {
        break;
    }
}
```

No código seguinte, a diretiva `continue` faz com que o comando `printf` seja ignorado, de modo que apenas números pares são impressos:

```c
int n = 0;
while (n < 10) {
    n++;

    /* verifica se n é ímpar */
    if (n % 2 == 1) {
        /* volta ao início do bloco while */
        continue;
    }

    /* chegamos a este código apenas se n for par */
    printf("O número %d é par.\n", n);
}
```

## Exercício

A variável `array` consiste numa sequência de dez números. Dentro do ciclo `while`, deve escrever duas condições `if`, que alteram o fluxo do ciclo da seguinte maneira (sem alterar o comando `printf`):

*   Se o número atual que está prestes a ser impresso for menor que 5, não o imprima.
*   Se o número atual que está prestes a ser impresso for maior que 10, não o imprima e pare o ciclo.

Note que se não avançar a variável iteradora `i` e usar a diretiva `continue`, ficará preso num ciclo infinito.

```c
#include <stdio.h>

int main() {
    int array[] = {1, 7, 4, 5, 9, 3, 5, 11, 6, 3, 4};
    int i = 0;

    while (i < 10) { // Note: The original text says "sequence of ten numbers" but the array has 11. The loop condition `i < 10` will only process the first 10. The exercise description seems aligned with processing 10 elements.
        /* o seu código fica aqui */

        printf("%d\n", array[i]);
        i++;
    }

    return 0;
}
```