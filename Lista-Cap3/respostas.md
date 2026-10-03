# Exercicio 01

a. O while testa a condição antes de executar o bloco, então o bloco pode ser executado zero vezes (se a condição já começar falsa). O do-while executa o bloco primeiro e só testa a condição no final, então o bloco é executado pelo menos uma vez.

b.
- **for**: quando o número de repetições é conhecido, com contador que tem início, fim e incremento definidos (ex: imprimir os números de 1 a 100).
- **while**: quando o número de repetições não é conhecido e depende de uma condição (ex: ler valores até o usuário digitar um valor de parada).
- **do-while**: quando o bloco precisa ser executado pelo menos uma vez antes do teste (ex: menus e validação de entrada de dados).

c. Não é erro de compilação, é erro de lógica. O ponto e vírgula vira o corpo do laço (uma instrução vazia). Se condicao for verdadeira, como nada dentro do laço altera condicao, o programa fica preso em um laço infinito testando a condição sem fazer nada. O bloco que vem logo depois, que parecia ser o corpo do laço, nunca é executado.

# Exercicio 02

Código da questão:

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int i;
    for (i = 1; i < 10; i++) {
        int soma = 0;
        soma += i * i;
    }
    printf("Soma final = %d\n", soma);
    system("PAUSE");
    return 0;
}
```

a. A variável soma foi declarada dentro do bloco do for, então ela só existe dentro desse bloco. No printf, que está fora do bloco, o identificador soma não está declarado, e o compilador acusa o erro `'soma' undeclared`.

b. Porque a declaração `int soma = 0;` está dentro do bloco, a cada iteração a variável é criada de novo e zerada. Assim, soma teria apenas o valor `i * i` da iteração atual, e não o acumulado das iterações anteriores.

c. Código corrigido:

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int i;
    int soma = 0;
    for (i = 1; i < 10; i++) {
        soma += i * i;
    }
    printf("Soma final = %d\n", soma);
    system("PAUSE");
    return 0;
}
```

Saída: `Soma final = 285`.

- **Visibilidade (escopo)**: é a região do código onde um identificador pode ser usado.
- **Escopo de bloco**: uma variável declarada dentro de um bloco `{ }` só é visível dentro desse bloco (e dos blocos internos a ele).
- **Tempo de vida**: é o período em que a variável existe na memória. Uma variável de bloco é criada quando a execução entra no bloco e destruída quando sai dele. Por isso, no código original, soma era recriada e zerada a cada iteração.
