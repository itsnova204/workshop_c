# Variáveis e Tipos

## Tipos de dados

C tem vários tipos de variáveis, mas existem alguns tipos básicos:

*   **Inteiros** - números inteiros que podem ser positivos ou negativos (exemplo: -1, 0, 1, 20 etc...). Definidos usando `int`.
*   **Números de ponto flutuante** - números reais (números com parte fracionária). Definidos usando `float` (exemplo: 1.00001).
*   **Estruturas** - serão explicadas mais tarde, na secção Estruturas.

C usa arrays de caracteres para definir strings (tipicamente texto), e será explicado na secção Strings.

## Definir variáveis

Para números, usaremos normalmente o tipo `int`. Na maioria dos computadores atuais, é um número de 32 bits, o que significa que o número pode variar de -2.147.483.648 a 2.147.483.647.

Para definir as variáveis `foo` e `bar`, precisamos de usar a seguinte sintaxe:

```c
int foo;
int bar = 1;
```

A variável `foo` pode ser usada, mas como não a inicializámos, não sabemos o que contém. A variável `bar` contém o número 1.

Agora, podemos fazer algumas operações matemáticas. Assumindo que `a`, `b`, `c`, `d` e `e` são variáveis, podemos simplesmente usar os operadores de adição, subtração e multiplicação na seguinte notação, e atribuir um novo valor a `a`:

```c
int b = 3, c = 2;
a = b * c;
printf("%d", a); /* imprimirá 3*2 = 6 */
```

## Exercício

No próximo exercício, vamos criar um programa que imprima a soma dos números `a`, `b` e `c`.

```c
#include <stdio.h>

int main() {
  int a = 3;
  float b = 4.5;
  float sum;

  /* O seu código fica aqui */

  printf("A soma de a, b e c é %f.", sum);
  return 0;
}
```