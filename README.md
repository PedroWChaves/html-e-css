# Capacitação HTML e CSS

De maneira geral, uma página na web é composta por três elementos: HTML, CSS e JavaScript. Cada um possui uma funcionalidade específica e exclusiva:

- HTML: responsável por definir a estrutura da página, ou seja, quais elementos ela possui;
- CSS: responsável por definir os estilos dessa página, ou seja, como ela se aparenta;
- JavaScript: responsável por adicionar a lógica à página, ou seja, dar a sua funcionalidade.

Vale notar que dos três elementos citados, apenas o JavaScript é uma linguagem de programação propriamente dita e, portanto, terá uma capacitação dedicada somente para ele.

# HTML

## Introdução

Como dito anteriormente, HTML **não** se trata de uma linguagem de programação propriamente dita, mas sim de uma Linguagem de Marcação de HiperTexto (**HyperText Markup Language**). Isso significa que ele é responsável por descrever a estrutura de elementos e conteúdos de uma página, como títulos, parágrafos, imagens, links, etc. O HTML desempenha um papel fundamental, sendo a base para a criação de páginas da web, pois permite aos desenvolvedores estruturar e organizar o conteúdo de forma significativa, além de facilitar a acessibilidade e indexação pelos mecanismos de busca.

## Estrutura Básica

A definição de elementos básicos de uma página através do HTML é feita através de **tags** e são escritas entre os símbolos **<** e **>**. As tags geralmente possuem uma abertura e um fechamento correspondente, com o conteúdo entre elas. A sintaxe básica é a seguinte:

```html
<tag>Conteúdo da tag</tag>
```

O exemplo a seguir define uma página que contém uma imagem seguida de um texto - constituído por um título e dois parágrafos:

```html
<body>
  <img src="images/logo.png" alt="Logo Ex Machina" height="200"/>

  <div>
    <h1>Título do texto</h1>
    <p>
      Parágrafo 1 do texto <br />
      Parágrafo 2 do texto
    </p>
  </div>
</body>
```
Resultado:
<img src=”./images/exemplo1.jpeg”>
Nesse exemplo:

- **\<body\>**: Engloba todo o conteúdo apresentado;
- **\<img\>**: define uma imagem e é um exemplo de tag que possui atributos;
- **\<div\>**: representa a seção da página definida pelo texto e é um exemplo de tag que contém outras tags;
- **\<br\>**: representa uma quebra de linha no texto e é um exemplo de tag sem fechamento.

Todo documento HTML possui a seguinte estrutura básica de tags:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Título da Página</title>
  </head>
  <body>
    Conteúdo da Página
  </body>
</html>
```

Onde:

- **\<!DOCTYPE html\>**: Define o tipo de documento como HTML5.
- **\<html\>**: É o elemento raiz da página, que engloba todo o HTML gerado.
- **\<head\>**: Contém informações sobre a página, como título, meta informações (descrição da página para indexação, ícone, entre outros), scripts e estilização (CSS).
- **\<body\>**: Contém o conteúdo visível da página, como textos, imagens, links, etc.

## Algumas tags importantes

### Cabeçalho

São utilizados para definir títulos e subtitulos em uma página. Eles vão de \<h1\> (mais importante) até \<h6\> (menos importante):

```html
<h1>Título Mais Importante</h1>
<h2>Subtítulo</h2>
<h3>Outro Subtítulo</h3>
...
<h6>Título Menos Importante</h6>
```

**OBS: o HTML por padrão deixa o texto da tag \<h1\> maior e diminui até \<h6\>, no entanto não é essa a função dessas tags, a estilização é feita posteriormente através do CSS. A função dessas tags é definir a importência dos tÍtulos inseridos.**

### Parágrafos

- **\<p\>**: Define parágrafos de texto.
- **\<br\>**: Define uma quebra de linha, sem criar um novo parágrafo:

```html
<p>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus sagittis
  posuere felis aliquam accumsan. Mauris molestie bibendum urna, a dapibus justo
  egestas non. Interdum et malesuada fames ac ante ipsum primis in faucibus.
  Integer nec porta neque, in tincidunt dolor. Proin blandit semper nisl.
</p>

<p>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit.<br />
  Vivamus sagittis posuere felis aliquam accumsan.
</p>

<p></p>
```

### Formatação de texto

- **\<strong\>**: Define o texto como negrito.
- **\<em\>**: Define o texto como itálico.
- **\<u\>**: Define o texto como sublinhado.

```html
<p>
  <strong>Texto em negrito</strong>, <em>texto em itálico</em> e
  <u>texto sublinhado</u>.
</p>
```

### Listas

- **\<ol\>**: Define uma lista ordenada, onde cada item é precedido por um número.
- **\<ul\>**: Define uma lista não ordenada, onde cada item é precedido por um marcador.
- **\<li\>**: Define um item dentro de uma lista.

```html
<ol>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ol>

<ul>
  <li>Item A</li>
  <li>Item B</li>
  <li>Item C</li>
</ul>
```

### Inserção de links e imagens

- **\<a\>**: Cria um link para outra página ou recurso. O atributo href define o destino do link.
- **\<img\>**: Insere uma imagem na página. O atributo src especifica o caminho da imagem e o atributo alt fornece um texto alternativo para acessibilidade.

```html
<a href="https://www.exemplo.com">Link para o site Exemplo</a>

<img src="imagem.jpg" alt="Descrição da imagem" />
```
