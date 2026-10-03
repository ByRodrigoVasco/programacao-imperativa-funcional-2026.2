# Exercicio 01

Alternativa correta: **c**.

Como a linguagem C diferencia letras maiúsculas de minúsculas, 'valor'/'VALOR', 'peso'/'Peso' e 'taxa'/'TAXA' são identificadores totalmente distintos para o compilador.

# Exercicio 02

Código da questão:

```c
#include <stdio.h>
#include <stdlib.h>;

int Main()
{
    int idade = 20;
    printf( A idade do aluno eh: %d anos.. , idade);
    cout << endl;
    system("PAUSE");
    return 0;
}
```

Erros:

1. `int Main()` está com 'M' maiúsculo. O compilador não reconhece como a função principal, e o programa não tem main (erro na ligação: `undefined reference to main`). O correto é `int main()`.
2. A string do printf não está entre aspas duplas. O correto é `printf("A idade do aluno eh: %d anos.\n", idade);`.
3. `cout << endl;` é da linguagem C++, não existe em C. Para quebrar a linha em C usa-se `printf("\n");` (ou o `\n` dentro da própria string do printf).

Além disso, o `#include <stdlib.h>;` não deve ter ponto e vírgula no final, porque diretivas de pré-processador não terminam com `;`.
