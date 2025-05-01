# Funções

As funções em C são simples, mas devido à forma como C funciona, o poder das funções é um pouco limitado.

*   As funções recebem um número fixo ou variável de argumentos.
*   As funções só podem devolver um valor, ou não devolver nenhum valor.

Em C, os argumentos são copiados por valor para as funções, o que significa que não podemos alterar os argumentos para afetar o seu valor fora da função. Para fazer isso, teriamos de usar apontadores.

As funções são definidas usando a seguinte sintaxe:

```c
int foo(int bar) {
    /* faz algo */
    return bar * 2;
}

int main() {
  foo(1);
}
```

A função `foo` que definimos recebe um argumento, que é `bar`. A função recebe um inteiro, multiplica-o por dois e devolve o resultado.

Para executar a função `foo` com 1 como argumento `bar`, usamos a seguinte sintaxe:

```c
foo(1);
```

Em C, as funções devem ser primeiro definidas antes de serem usadas no código. Podem ser declaradas primeiro e depois implementadas mais tarde usando um ficheiro de cabeçalho ou no início do ficheiro C, ou podem ser implementadas na ordem em que são usadas (menos preferível).

A forma correta de usar funções é a seguinte:

```c
/* declaração da função */
int foo(int bar);

int main() {
    /* chamar foo a partir de main */
    printf("O valor de foo é %d", foo(1));
}

int foo(int bar) {
    return bar + 1;
}
```

Também podemos criar funções que não devolvem um valor usando a palavra-chave `void`:

```c
void moo() {
    /* faz algo e não devolve um valor */
}

int main() {
    moo();
}
```

## Exercício

Escreva uma função chamada `print_big` que recebe um argumento (um inteiro) e imprime a linha `x is big` (onde x é o argumento) se o argumento dado à função for um número maior que 10.

*   **Importante**: Não se esqueça de adicionar um carácter de nova linha `\n` no final da string do printf.

```c
#include <stdio.h>

/* declaração da função */
void print_big(int number);

int main() {
  int array[] = { 1, 11, 2, 22, 3, 33 };
  int i;
  for (i = 0; i < 6; i++) {
    print_big(array[i]);
  }
  return 0;
}

/* escreva a sua função aqui */
```