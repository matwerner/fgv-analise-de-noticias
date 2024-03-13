# Analisando notícias
Aula de exercícios para o curso de Introdução à Computação da FGV.

Usando as ferramentas aprendidas nas ultimas semanas, nosso objetivo é analisar uma base de documentos.

[Aula de Terminal](https://github.com/fccoelho/introcomp/blob/main/conte%C3%BAdo/Usando%20%20o%20Terminal/shell_Linux.md)
[Aula de Bash](https://github.com/fccoelho/introcomp/blob/main/conte%C3%BAdo/Introdu%C3%A7%C3%A3o%20%C3%A0%20programa%C3%A7%C3%A3o/Bash_shell.md)
[Aula de Grep](https://github.com/fccoelho/introcomp/blob/main/conte%C3%BAdo/Introdu%C3%A7%C3%A3o%20%C3%A0%20programa%C3%A7%C3%A3o/GREP.md).

## Exercícios
Na pasta *dados* estão presentes diversas notícias do portal Globo na forma de vários arquivos de texto, distribuídos por categoria.

1. Quantas notícias temos ao todo?
   - Dica 1: Experimente concatenar todos os arquivos em um para facilitar a contagem.
   - Dica 2: Utilize o comando `tree`
2. Quantas palavras ao todo existem na notícia de economia `0.txt`?
3. E quantas palavras distintas?
   - Dica 1: Para facilitar comece colocando cada palavra em uma linha separada:
   ```bash
   $ echo -e "gato sapato" | sed 's/ /\n/g'
   ```
   No código acima, a expressão regular `s/ /\n/g` substitui todos os espaços por quebras de linha (`\n`).
   - Dica 2: Utilize o comando `uniq`.
4. Agora, liste as palavras distintas que aparecem nele em ordem crescente de frequência, precedidas do número de ocorrências de cada uma.
   - Dica: Utilize os comandos `uniq` e `sort`
   
O resultado deve ser algo como:
```
4 farmácia
4 Farinha
4 familiares
4 família

...
```
5. Repita as questões 2, 3 e 4 considerando todas as notícias.
6. Qual a quantidade média de palavras por notícia?
   - Dica: É possível obter esse valor utilizando resultados já obtidos anteriormente
7. Repita as questões 1, 5 e 6 separando por categoria.
   - Dica: Considere que já existe uma lista predefina `categories=(economia esportes famosos politica tecnologia)`

*Obs 1*: Criar um arquivo diferente para cada solução.
*Obs 2*: Quando em dúvida sobre o funcionamento de um comando, execute `man <comando>` (e.g: `man tree`)
*Obs 3*: Base de dados original foi obtida do [kaggle](https://www.kaggle.com/datasets/diogocaliman/notcias-publicadas-no-brasil/data)