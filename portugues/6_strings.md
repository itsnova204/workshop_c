# Strings

## Definir strings

Strings em C são, na verdade, arrays de caracteres. Embora usar ponteiros em C seja um tópico avançado, explicado completamente mais tarde, usaremos ponteiros para um array de caracteres para definir strings simples, da seguinte forma:

```c
char * name = "John Smith";
```

Este método cria uma string que só podemos usar para leitura. Se desejarmos definir uma string que possa ser manipulada, precisaremos de a definir como um array local de caracteres:

```c
char name[] = "John Smith";
```

Esta notação é diferente porque aloca uma variável de array para que a possamos manipular. A notação de parêntesis retos vazios `[]` diz ao compilador para calcular automaticamente o tamanho do array. Isto é, na verdade, o mesmo que alocá-lo explicitamente, adicionando um ao comprimento da string:

```c
char name[] = "John Smith";
/* é o mesmo que */
char name[11] = "John Smith";
```

A razão pela qual precisamos de adicionar um, embora a string `John Smith` tenha exatamente 10 caracteres de comprimento, é para a terminação da string: um carácter especial (igual a 0) que indica o fim da string. O fim da string é marcado porque o programa não sabe o comprimento da string - apenas o compilador o sabe de acordo com o código.

## Formatação de strings com printf

Podemos usar o comando `printf` para formatar uma string juntamente com outras strings, da seguinte maneira:

```c
char * name = "John Smith";
int age = 27;

/* imprime 'John Smith is 27 years old.' */
printf("%s tem %d anos.\n", name, age); // Adjusted phrasing for pt-PT naturalness
```

Note que, ao imprimir strings, temos de adicionar um carácter de nova linha (`\n`) para que a nossa próxima instrução `printf` imprima numa nova linha.

## Comprimento da String

A função `strlen` devolve o comprimento da string que tem de ser passada como argumento:

```c
char * name = "Nikhil";
printf("%d\n",strlen(name));
```

## Comparação de strings

A função `strncmp` compara duas strings, devolvendo o número 0 se forem iguais, ou um número diferente se forem diferentes. Os argumentos são as duas strings a serem comparadas e o comprimento máximo de comparação. Existe também uma versão insegura desta função chamada `strcmp`, mas não é recomendado usá-la. Por exemplo:

```c
char * name = "John";

if (strncmp(name, "John", 4) == 0) {
    printf("Olá, John!\n");
} else {
    printf("Você não é o John. Vá-se embora.\n"); // Adapted phrasing for pt-PT
}
```

## Concatenação de Strings

A função `strncat` anexa os primeiros n caracteres da string `src` à string de destino, onde n é min(n, comprimento(src)). Os argumentos passados são a string de destino, a string de origem e n - o número máximo de caracteres a serem anexados. Por Exemplo:

```c
char dest[20]="Hello";
char src[20]="World";
strncat(dest,src,3);
printf("%s\n",dest);
strncat(dest,src,20);
printf("%s\n",dest);
```

## Exercício

Defina a string `first_name` com o valor `John` usando a notação de ponteiro, e defina a string `last_name` com o valor `Doe` usando a notação de array local.

```c
#include <stdio.h>
#include <string.h>
int main() {
  /* defina first_name */
  /* defina last_name */
  char name[100];

  last_name[0] = 'B';
  sprintf(name, "%s %s", first_name, last_name);
  if (strncmp(name, "John Boe", 100) == 0) {
      printf("Feito!\n"); // Translated "Done!"
  }
  name[0]='\0';
  strncat(name,first_name,4);
  strncat(name,last_name,20);
  printf("%s\n",name);
  return 0;
}
```