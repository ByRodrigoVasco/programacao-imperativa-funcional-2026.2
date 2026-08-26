# Exercicio 09

Código da questão:

```c
printf("%c%c%cPrimeiro programa", '\n', '\t', '\"');
printf("%c", "\"");
```

Na primeira linha, quebra de linha, tab e aspas são constantes de caractere, então o %c imprime cada uma normal, e depois escreve Primeiro programa.

Na segunda linha, a aspa entre aspas duplas é uma string, não uma constante de caractere. Passar uma string pro %c é erro de tipo. O compilador avisa, e o que sai na tela não é a aspa esperada, e sim um valor sem sentido. O certo era usar aspa simples.
