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

# Exercicio 03

Código da questão:

```c
int a = 2, b = 4, c = 5, d = 10;
a += b + c;          // Valor final de a = ?
b *= c = d - 2;      // Valores finais de b e c = ?
d %= a + 3;          // Valor final de d = ?
a += b += c += 5;    // Valores finais de a, b e c = ?
```

Estado inicial: a=2, b=4, c=5, d=10.

1. `a += b + c;` → a = a + (b + c) = 2 + (4 + 5) = 11. **a = 11**.

2. `b *= c = d - 2;` → o operador `=` é avaliado primeiro (associatividade à direita): c = d - 2 = 10 - 2 = 8, então **c = 8**. Em seguida b *= c → b = 4 * 8 = 32, então **b = 32**.

3. `d %= a + 3;` → a + 3 = 11 + 3 = 14. d = d % 14 = 10 % 14 = 10 (o valor não muda pois 10 < 14). **d = 10**.

4. `a += b += c += 5;` → primeiro c += 5 → c = 8 + 5 = 13 (**c = 13**); depois b += c → b = 32 + 13 = 45 (**b = 45**); por fim a += b → a = 11 + 45 = 56 (**a = 56**).

Valores finais: **a = 56, b = 45, c = 13, d = 10**.
