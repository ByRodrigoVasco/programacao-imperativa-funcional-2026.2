# Exercicio 01

a. O while testa a condição antes de executar o bloco, então o bloco pode ser executado zero vezes (se a condição já começar falsa). O do-while executa o bloco primeiro e só testa a condição no final, então o bloco é executado pelo menos uma vez.

b.
- **for**: quando o número de repetições é conhecido, com contador que tem início, fim e incremento definidos (ex: imprimir os números de 1 a 100).
- **while**: quando o número de repetições não é conhecido e depende de uma condição (ex: ler valores até o usuário digitar um valor de parada).
- **do-while**: quando o bloco precisa ser executado pelo menos uma vez antes do teste (ex: menus e validação de entrada de dados).

c. Não é erro de compilação, é erro de lógica. O ponto e vírgula vira o corpo do laço (uma instrução vazia). Se condicao for verdadeira, como nada dentro do laço altera condicao, o programa fica preso em um laço infinito testando a condição sem fazer nada. O bloco que vem logo depois, que parecia ser o corpo do laço, nunca é executado.
