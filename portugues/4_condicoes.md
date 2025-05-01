# Condições

## Tomada de Decisão

Na vida, todos temos de tomar decisões. Para tomar uma decisão, ponderamos as nossas opções, e os nossos programas também o fazem.

Aqui está a forma geral das estruturas de tomada de decisão encontradas em C.

```c
int target = 10;
if (target == 10) {
    printf("O Target é igual a 10");
}
```

## A instrução if

A instrução `if` permite-nos verificar se uma expressão é verdadeira ou falsa, e executar código diferente de acordo com o resultado.

Para avaliar se duas variáveis são iguais, usa-se o operador `==`, tal como no primeiro exemplo.

Operadores de desigualdade também podem ser usados para avaliar expressões, por exemplo:

```c
int foo = 1;
int bar = 2;

if (foo < bar) {
  printf("foo é menor que bar.");
}

if (foo > bar) {
  printf("foo é maior que bar.");
}
```

Podemos usar a palavra-chave `else` para executar código quando a nossa expressão avalia como falsa.

```c
int foo = 1;
int bar = 2;

if (foo < bar) {
  printf("foo é menor que bar.");
} else {
  printf("foo é maior que bar.");
}
```

Por vezes, teremos mais do que dois resultados para escolher. Nestes casos, podemos "encadear" múltiplas instruções `if else`.

```c
int foo = 1;
int bar = 1;

if (foo < bar) {
  printf("foo é menor que bar.");
} else if (foo == bar) {
  printf("foo é igual a bar.");
} else {
  printf("foo é maior que bar.");
}
```

Também pode aninhar instruções `if else`, se quiser.

```c
int peanuts_eaten = 22;
int peanuts_in_jar = 100;
int max_peanut_limit = 50;

if (peanuts_in_jar > 80) {
    if (peanuts_eaten < max_peanut_limit) {
        printf("Pode comer tantos amendoins quantos quiser!\n");
    }
} else {
    if (peanuts_eaten > peanuts_in_jar) {
        printf("Já não pode comer mais amendoins!\n");
    }
    else {
        printf("Está bem, só mais um amendoim.\n");
    }
}
```

Duas ou mais expressões podem ser avaliadas juntas usando operadores lógicos para verificar se ambas as expressões avaliam como verdadeiras em conjunto, ou se pelo menos uma delas avalia como verdadeira. Para verificar se duas expressões avaliam ambas como verdadeiras, use o operador E (`&&`). Para verificar se pelo menos uma das expressões avalia como verdadeira, use o operador OU (`||`).

```c
int foo = 1;
int bar = 2;
int moo = 3;

if (foo < bar && moo > bar) {
  printf("foo é menor que bar E moo é maior que bar.");
}

if (foo < bar || moo > bar) {
  printf("foo é menor que bar OU moo é maior que bar.");
}
```

O operador NÃO (`!`) também pode ser usado da mesma forma:

```c
int target = 9;
if (target != 10) {
  printf("Target não é igual a 10");
}
```

## Exercício

Neste exercício, tem de construir uma instrução `if` dentro da função `guessNumber` que verifica se o número `guess` é igual a 555. Se for esse o caso, a função deve imprimir usando `printf` "Correto. Adivinhaste!". Se `guess` for menor que 555, a função deve imprimir usando `printf` "O teu palpite é muito baixo.". Se `guess` for maior que 555, a função deve imprimir usando `printf` "O teu palpite é muito alto.".

*   **Importante**: Não se esqueça de adicionar um carácter de nova linha `\n` no final da string do printf.

```c
#include <stdio.h>

void guessNumber(int guess) {
    // TODO: escreva o seu código aqui
}

int main() {
    guessNumber(500);
    guessNumber(600);
    guessNumber(555);
}
```