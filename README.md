# Capacitação HTML e CSS

Como a criação de uma página na web possui uma complexidade grande, é necessário fazer algum tipo de organização para o seu desenvolvimento. Diferentes ferramentas possuem diferentes maneiras de fazê-lo, o React, por exemplo, que veremos ao final das capacitações, separada diferentes "componentes" básicos de uma página para a sua composição. No entanto, usando as ferramentas "vanilla" HTML, CSS e JavaScript, essa organização é feita separando a funcionalidade de cada arquivo
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
  <img src="images/logo.png" alt="Logo Ex Machina" height="200" />

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
<img src=”./images/exemplo1.png”>
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

- Uso de formulários para coletar dados dos usuários
- Elementos de formulário, como campos de entrada de texto (\<input\>), caixas de seleção (\<select\>), botões (\<button\>), etc
- Atributos de validação e controle de formulário
- Estruturação de página

- Uso de elementos semânticos, como \<header\>, \<nav\>, \<main\>, \<section\>, \<article\>, \<aside\>, \<footer\>, etc.
- Criação de menus de navegação.
- Manipulação de links e URLs:

- Uso de URLs absolutas e relativas.
- Links internos e externos.
- Uso de âncoras (\<a\>) para navegação interna.
- Meta informações:

- Inclusão de metatags para otimização de mecanismos de busca (SEO).
- Definição de metatags para a exibição de título, descrição e ícones da página.

- Esses são os conceitos básicos sobre HTML e alguns exemplos de uso das tags mencionadas. HTML oferece uma ampla variedade de tags e recursos para criar conteúdo e estruturar páginas web. É importante explorar e praticar para se familiarizar com as possibilidades que essa linguagem oferece.

### Principais usos para React

# CSS

## Introdução

Assim como HTML, CSS **não** se trata de uma linguagem de programação, mas sim de uma linguagem de estilização, ou uma Foha de Estilos em Cascata (**Cascading Style Sheets**). Isso significa que ele é responsável por definir a aparência e o layout de uma página da web, através de propriedades dos elementos HTML como cor, tamanho, fonte, margens, posicionamento, etc. O CSS é fundamental para o design e a apresentação visual de uma página web, permitindo criar layouts atraentes, coesos e responsivos.

Um aspecto que pode ficar um pouco confuso com a nomenclatura é em relação à "cascata", mas isso simplesmente quer dizer que os estilos aplicados mais abaixo no arquivo terão prioridade para ser aplicados em relação aos de cima, caso seja a mesma propriedade a ser alterada.

A sintaxe básica do CSS consiste em regras que são aplicadas a elementos HTML. Cada regra é composta por um seletor e um bloco de declarações. O seletor especifica quais elementos HTML devem ser estilizados, e as declarações definem as propriedades de estilo que serão aplicadas a esses elementos. O CSS pode ser adicionado a uma página HTML de diferentes maneiras, incluindo o uso de estilos internos no próprio documento HTML, estilos embutidos diretamente nos elementos HTML ou por meio de folhas de estilo externas.

Os seletores CSS são usados para selecionar os elementos HTML aos quais se deseja aplicar estilos. Existem vários tipos de seletores:

Seletores de elementos: selecionam elementos com base em seus nomes de tag. Por exemplo, o seletor "p" seleciona todos os parágrafos na página.

Seletores de classes e IDs: permitem selecionar elementos com base em suas classes ou IDs atribuídos. Os seletores de classes começam com um ponto (.), seguido pelo nome da classe, enquanto os seletores de IDs começam com um hash (#), seguido pelo ID do elemento.

Seletores de atributos: selecionam elementos com base em um atributo específico. Por exemplo, o seletor "[type='text']" seleciona todos os elementos com o atributo "type" igual a "text".

Pseudo-classes: selecionam elementos em um estado específico ou em um contexto específico. Por exemplo, o seletor ":hover" seleciona um elemento quando o cursor do mouse está sobre ele.

O CSS oferece uma ampla variedade de propriedades de estilo para controlar a aparência dos elementos HTML. Alguns exemplos incluem:

Cores e fundos: é possível definir cores para texto e fundo usando valores hexadecimais, nomes de cores ou funções de gradiente. Também é possível usar imagens como fundo.

Tipografia: permite controlar a fonte, tamanho, estilo (negrito, itálico), espaçamento entre linhas e outros aspectos relacionados ao texto.

Margens, preenchimentos e bordas: são usadas para ajustar o espaçamento em torno dos elementos e definir estilos de borda.

Posicionamento: o CSS permite posicionar elementos de forma estática (fluxo normal do documento), relativa (em relação à sua posição normal), absoluta (em relação ao elemento pai) e fixa (em relação à janela do navegador).

Layouts: o CSS oferece recursos como Flexbox e Grid para criar layouts responsivos e controlar o posicionamento dos elementos em relação a seus contêineres.

Animações e transições: é possível criar efeitos de animação e transição suaves em elementos, permitindo que eles mudem gradualmente de uma aparência para outra.

O modelo de caixa é um conceito fundamental no CSS, que descreve como cada elemento é renderizado na página. Ele consiste em propriedades de dimensões (largura, altura), margens, preenchimentos e bordas, que afetam o espaço ocupado pelo elemento e sua aparência visual. O modelo de caixa pode ser ajustado usando a propriedade "box-sizing", que permite controlar se as dimensões incluem ou não as bordas e preenchimentos.

A responsividade no CSS refere-se à capacidade de uma página se adaptar a diferentes dispositivos e tamanhos de tela. As media queries são usadas para aplicar estilos diferentes com base nas características do dispositivo, como largura de tela. As unidades de medida responsivas, como porcentagem e "em", permitem que os elementos sejam dimensionados de acordo com o tamanho do contêiner ou do dispositivo.

O posicionamento e o layout no CSS são usados para controlar a posição e a disposição dos elementos na página. O posicionamento flutuante (float) permite que os elementos sejam deslocados para a esquerda ou direita de seu contêiner, enquanto o posicionamento flexível com flexbox oferece um modelo de layout mais poderoso e responsivo. O CSS Grid permite criar layouts de grade bidimensionais, facilitando a organização dos elementos em linhas e colunas.

A estilização avançada no CSS envolve o uso de pseudo-elementos e pseudo-classes. Os pseudo-elementos são usados para adicionar estilos a partes específicas de um elemento, como o primeiro parágrafo de um texto. As pseudo-classes são usadas para selecionar elementos em estados específicos, como o estado "hover" de um link.

Boas práticas de CSS incluem a organização de estilos em folhas de estilo externas, o uso de comentários e documentação para facilitar a manutenção do código, e a otimização de desempenho e carga de página, minimizando a quantidade de CSS e usando técnicas como a concatenação e minificação dos arquivos CSS.

Introdução ao CSS:

O que é CSS e sua importância no design e na apresentação de páginas web.
Sintaxe básica do CSS e sua relação com o HTML.
Seletores CSS:

Seletores de elementos, classes e IDs.
Seletores de atributos e pseudo-classes.
Aninhamento de seletores.
Propriedades de estilo:

Cores e fundos: definição de cores, uso de gradientes, imagens de fundo, etc.
Tipografia: controle de fontes, tamanhos, estilos, espaçamento entre linhas, etc.
Margens, preenchimentos e bordas: ajuste de espaçamento e estilo.
Posicionamento: posicionamento estático, relativo, absoluto e fixo.
Layouts: uso de flexbox e grid para criar layouts responsivos.
Animações e transições: criação de efeitos de animação e transição de elementos.
Box model:

Compreensão do conceito de modelo de caixa.
Propriedades de dimensões (largura, altura, margens, preenchimentos, bordas).
Ajuste do modelo de caixa usando box-sizing.
Responsividade:

Media queries: aplicação de estilos diferentes com base nas características do dispositivo.
Unidades de medida responsivas: uso de unidades relativas, como porcentagem e em.
Posicionamento e layout:

Posicionamento flutuante (float) e clear.
Posicionamento flexível com flexbox.
Layout de grade com CSS Grid.
Estilização avançada:

Uso de pseudo-elementos e pseudo-classes.

Estilização de formulários e elementos de interface.
Estilização de links e elementos de navegação.
Boas práticas:

Organização de estilos com folhas de estilo externas (<link>).
Comentários e documentação de código CSS.
Otimização de desempenho e carga de página.
