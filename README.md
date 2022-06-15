# Desafio para o Programa Blastoff da empresa Toodoo. 
::toodoo-blastoff
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

<HR>

### QUESTÃO 3) Construa utilizando HTML e JavaScript um link que ao ser clicado, abre um alerta do navegador
```
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <title>Questão 3</title>
    <meta charset="UTF-8">
</head>
<body>
    
    <a href="#" onclick="alert('Fique alerta!')">Clique em mim!</a>

    <script>
        function alertar(mensagem){
            alert(mensagem);
        }
    </script>
</body>
</html>
```
  
<hr>
  
### QUESTÃO 4) Descreva em CSS a seguinte regra: todos os itens de uma lista devem estar orientados na vertical.
```
li{
  display: list-item !important;
}
```
A regra acima aplica a alteração para todas as listas. Caso queira-se definir para uma única lista, deve-se utilizar um ID para a lista e então aplicar a regra aos itens dela (#exemplo li).
  
<hr>
  
### QUESTÃO 5) Descreva em CSS a seguinte regra: somente o último item de uma lista não deve ter uma linha na sua base.
  
```
li:not(li:last-child){
  border-width: 0px 0px 2px 0px; 
  border-style: solid;
  border-color: black;
}  
```
  
<hr>
  
### QUESTÃO 6) Um arquivo externo chamado styles.css precisa ser carregado na página HTML. Escreva o código para fazer tal carregamento.
  
```
  <link rel="stylesheet" href="style.css">
```
O carregamento deste arquivo comumente é feito na tag HEAD. No entanto, para que haja uma melhor performance no lado do usuário, deve ser realizado ao fim do carregamento do conteúdo html.
  
<hr>  
  
### QUESTÃO 7) Um dos critérios de um determinado projeto é que todos os links devem ficar sublinhados quando o usuário passar o mouse por cima deles. Escreva o código para garantir essa regra.
```  
  a{
    text-decoration: none;
  }

  a:hover{
    text-decoration: underline;
  }
```
  
<hr> 
  
### QUESTÃO 8) Escreva um comando JavaScript onde o texto Hello World! seja exibido no console do navegador através de uma variável.
```
  <script>
        var mensagem = 'Hello World!';
        console.log(mensagem);
    </script>
```
  
<hr>  
  
### QUESTÃO 9) Usando o mesmo código da questão anterior, substitua o texto que será exibido no console do navegador para Hello Toodoo! O novo valor deve sobrescrever o valor original.
```
  <script>
        var mensagem = 'Hello World!';
        mensagem = 'Hello Toodoo!'
        console.log(mensagem);
    </script>
```
  
<hr>
  
### QUESTÃO 10) Desenvolva via JavaScript a seguinte estrutura de código levando em consideração as seguintes regras:

#### a) Uma variável deve ter o nome de sorvete de chocolate

#### b) Se o seu valor for igual a chocolate, deve ser exibido no alerta do navegador a mensagem: Amo sorvete de chocolate;

#### c) Se o seu valor for outro, deve exibir a mensagem: Prefiro outros sabores.  
```
<script>
    var sorveteDeChocolate;
    if(sorveteDeChocolate == 'chocolate')
      alert('Amo sorvete de chocolate');
    else
      alert('Prefiro outros sabores');    
</script>
```
  
<hr> 
  
### QUESTÃO 11) Na função JavaScript a seguir, responda quais serão os resultados respectivos:

```
function multiplicacao (num1,num2) {
  let resultado = num1 * num2;
  return resultado;
}
multiplica(4, 7);
multiplica(5, 6);
multiplica(3, 3);
```
  Como o nome da função chamada é diferente do nome da função definida, ocorreria um erro ao invocar a função pois ela não foi definida anteriormente.
  Corrigindo o nome da função, as saídas seriam: 28, 30 e 9.

<hr>

### QUESTÃO 11) Em CSS existe uma maneira de sobrescrever um estilo, quando não há outra maneira, além dessa, de se fazer isso. Qual das propriedades a seguir é utilizada para isso?
#### (a) force
#### (b) strong
#### (c) !important
#### (d) nenhuma das alternativas
  
A alternativa correta é a letra 'c !important';
  
<hr>
  
### QUESTÃO 12) Analisando a estrutura CSS a seguir, qual cor prevalecerá no elemento HTML?
```
li.list-item {
color: red;
}
.list-item {
color: blue
}
#list .list-item {
color: green
}
ul li {
color: black;
}
```
#### (a) red
#### (b) blue
#### (c) green
#### (d) black
  
A resposta correta é a letra 'c green', pois é empregada uma regra com o seletor de id '#list'. Dentre os pesos dos seletores, o peso de atributo é o mais alto, abaixo apenas do css definido inline.
  
<hr>
  
### QUESTÃO 13) Levando em consideração a semântica de código, escreva o HTML de uma tabela que possui as seguintes características:
#### a) Deve possuir 3 colunas (Nome, Idade, Gênero);
#### b) Deve possuir 2 linhas (com dados fictícios);
#### c) E uma última linha com todas as suas colunas mescladas.
  
```
  <table>
    <thead>
        <tr>
            <th>Nome</th>
            <th>Idade</th>
            <th>Gênero</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Maria</td>
            <td>20</td>
            <td>Feminino</td>
        </tr>
        <tr>
            <td>João</td>
            <td>30</td>
            <td>Masculino</td>
        </tr>
    </tbody>
    <tfooter>
      <tr>
        <td colspan="3">Célula Mesclada</td>
      </tr>
  	</tfooter>
</table>
```
  
<hr>
  
### QUESTÃO 14) Utilizando grid system, não sendo necessário a responsividade, elabore uma página web que siga o layout da imagem abaixo:
  
![alt text](https://github.com/ThatsJojo/toodoo-blastoff/blob/main/q14.png)
  
 Resposta nos arquivos anexos.
  
<hr>
  
### QUESTÃO 15) Crie uma página web conforme o layout abaixo que seja responsiva para ser utilizada nos diferentes navegadores e dispositivos:
  
![alt text](https://github.com/ThatsJojo/toodoo-blastoff/blob/main/q15.png)

Resposta nos arquivos anexos.
  
  
