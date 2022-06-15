::toodoo-blastoff
# Desafio para o Programa Blastoff da empresa Toodoo. 

<hr>

### QUESTÃO 1) Construa os elementos básicos para formar uma página HTML. Ela não precisa ter nenhum conteúdo

```
  Elementos básicos necessários para formatar uma página HTML:
  <!DOCTYPE html> <!-- Define a versão do HTML utilizada. -->
  <html lang="pt-br"> <!-- Delimita o documento HTML -->
  <head> <!-- Tag que define o cabeçalho do coumento. Nela, são configurados alguns dos comportamentos do documento. -->
      <meta charset="UTF-8"> <!-- Define a codificação dos caracteres no arquivo HTML corrente. -->
      <title>Questão 1</title> <!-- Define o título da página. -->
  </head> <!-- Fim da tag HEAD -->
  <body> <!-- Tag em que deve estar contido todo o corpo/conteúdo da página. -->

  </body> <!-- Fim do conteúdo da página. -->
  </html> <!-- Fim do documento HTML -->
  
```
É válido notar que a formatação acima não é obrigatória. É possível, por exemplo, exibir conteúdo do corpo da página colocando-o fora da tag 'body'. Mas isso não é considerado uma boa prática.

<hr>

### QUESTÃO 2) Em um determinado projeto os cabeçalhos devem estar previamente definidos com fonte Arial, devem estar em negrito e em caixa alta. Como você faria pra esses parâmetros serem implementados neste projeto? 

Eu definiria em um arquivo .css uma classe cabecalho com as características necessárias, conforme exemplo abaixo:

```
.cabecalho{
  font-weight: bold;
  font-family: Arial;
  text-transform: uppercase;
}  
```

E, então, adicionaria essa classe aos elementos que contenham os cabeçalhos, conforme exemplo abaixo:
```
...
<body>
  <div class="cabecalho">
    Cabeçalho 1
  </div>
  <div class="cabecalho">
    Cabeçalho 2
  </div>
</body>
...
```
