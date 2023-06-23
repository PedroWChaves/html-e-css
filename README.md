# Capacitação HTML e CSS

Como a criação de uma página na web possui uma complexidade grande, é necessário fazer algum tipo de organização para o seu desenvolvimento. Diferentes ferramentas possuem diferentes maneiras de fazê-lo, o React, por exemplo, que será visto ao final das capacitações, separada diferentes "componentes" básicos de uma página para a sua composição. No entanto, usando as ferramentas "vanilla", essa organização é feita separando a funcionalidade de cada arquivo. De maneira geral, uma página na web é composta por três elementos:

- HTML: responsável por definir a estrutura e conteúdo da página, ou seja, quais elementos ela possui;
- CSS: responsável por definir os estilos da página, ou seja, como ela se aparenta;
- JavaScript: responsável por adicionar a logica à página, ou seja, dar a sua funcionalidade.

Vale notar que dos três elementos citados, apenas o JavaScript é uma linguagem de programação propriamente dita e, portanto, terá uma capacitação dedicada somente para ele. As outras duas serão apresentadas a seguir:

# HTML

## Introdução

Como dito anteriormente, HTML **não** se trata de uma linguagem de programação propriamente dita, mas sim de uma Linguagem de Marcação de HiperTexto (**HyperText Markup Language**). Isso significa que ele é responsável por descrever a estrutura de elementos e conteúdos de uma página, como títulos, parágrafos, imagens, links, etc. O HTML desempenha um papel fundamental, sendo a base para a criação de páginas da web, pois permite aos desenvolvedores estruturar o conteúdo de forma significativa, além de facilitar a acessibilidade e indexação pelos mecanismos de busca através dos metadados da página como título, descrição, ícone, etc.

## Estrutura Básica

Os elementos básicos de um arquivo HTML são as chamadas **tags**, escritas entre os símbolos **<** e **>**. As tags geralmente possuem uma abertura e um fechamento correspondente, com o conteúdo (filhos) entre elas. A sintaxe básica é a seguinte:

```html
<tag>Conteúdo da tag</tag>
```

Porém existem diferentes tipos de tags: tags sem filhos, tags com parâmetro, tags que contêm outras tags ou alguma combinação entre elas. O exemplo a seguir apresenta as tags mencionadas, definindo uma página com uma imagem seguida de um texto (um título e dois parágrafos):

```html
<!-- Agrupa todo o conteúdo da página -->
<body>
  <!-- Tag com parâmetros e sem filhos -->
  <img src="images/logo.png" alt="Logo Ex Machina" height="200" />

  <!-- Tag com outras tags como filhos -->
  <div>
    <!-- Tag com filho -->
    <h1>Título do texto</h1>

    <!-- Mescla entre texto e outras tags nos filhos da tag -->
    <p>
      Parágrafo 1 do texto. <br />
      Parágrafo 2 do texto.
    </p>
  </div>
</body>
```

A funcionalidade de cada tag será explorada com mais detalhes nas seções seguintes.

**OBS: Todas tags HTML podem receber o parâmetro id, que é muito utilizado para a integração com JavaScript e CSS.**

Todo documento HTML possui a seguinte estrutura básica de tags:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Título da Página</title>
    <meta name="description" content="Descrição da página" />
    <link rel="icon" href="favicon.ico" type="image/x-icon" />
  </head>
  <body>
    Conteúdo da Página
  </body>
</html>
```

Onde:

- **\<!DOCTYPE html\>**: Define o tipo de documento como HTML5.
- **\<html\>**: É o elemento raiz da página, que engloba todo o HTML gerado.
- **\<head\>**: Contém informações sobre a página, como título, meta informações (descrição da página, ícone, entre outros), scripts e estilização (CSS).
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

### Parágrafos e formatação de texto

- **\<p\>**: Define parágrafos de texto.
- **\<br\>**: Define uma quebra de linha, sem criar um novo parágrafo.
- **\<strong\>**: Define o texto como negrito.
- **\<em\>**: Define o texto como itálico.
- **\<u\>**: Define o texto como sublinhado.

```html
<p>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus sagittis
  posuere felis aliquam accumsan. Mauris molestie bibendum urna, a dapibus justo
  egestas non. Interdum et malesuada fames ac ante ipsum primis in faucibus.
  Integer nec porta neque, in tincidunt dolor. Proin blandit semper nisl.
</p>

<p>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit.<br />Vivamus sagittis
  posuere felis aliquam accumsan.
</p>

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

- **\<a\>**: Cria um link para outra página. O atributo href define o destino do link, podendo ser relativo ou absoluto.
- **\<img\>**: Insere uma imagem na página. O atributo src especifica o caminho da imagem e o atributo alt fornece um texto alternativo para acessibilidade.

```html
<a href="https://linktr.ee/ExMachina">Link absoluto</a>
<a href="/sobre">Link relativo</a>

<img src="images/logo.png" alt="Logo Ex Machina" height="200" />
```

Também é possível fazer com que uma imagem atue como um link, ou seja, ao clicá-la, ser redirecionado para outra página. Isso pode ser feito definindo a imagem como filho da tag âncora:

```html
<a href="https://linktr.ee/ExMachina">
  <img src="images/logo.png" alt="Logo Ex Machina" height="200" />
</a>
```

Na realidade, qualquer elemento filho da tag \<a\> passará a se comportar como um link, porém muitos casos não fazem sentido, como utilizar uma tag de input, por exemplo.

### Formulários

- **\<form\>**: Define que o conteúdo contido se trata de um formulário.
- **\<label\>**: Define uma legenda para um item. Não é específico para formulários, mas comumente associado, pois permite definir de maneira acessível a qual atributo se refere um determinado input.
- **\<input\>**: Cria um campo de entrada de texto, onde os usuários podem digitar informações. O atributo type especifica o tipo de entrada desejado, como texto, email, número, etc.
- **\<button\>**: Cria um botão, como esperado. Em formulários é possível definir o atributo `type="submit"` para que, ao clicar no botão, o formulário seja enviado/validado.
- **\<select\>**: Cria uma caixa de seleção com opções pré-definidas pelo desenvolvedor.
- **\<option\>**: Cria as opções para a tag select.

```html
<form>
  <label>Nome:</label>
  <input type="text" name="nome" />

  <!-- Outra maneira de definir qual informação deve ser inserida -->
  <input type="number" name="idade" placeholder="Digite sua idade" />

  <label>Estado:</label>
  <select name="estado">
    <option value="MG">Minas Gerais</option>
    <option value="RJ">Rio de Janeiro</option>
    <option value="SP">São Paulo</option>
    <option value="ES">Espírito Santo</option>
  </select>

  <button type="submit">Enviar</button>
</form>
```

### Elementos de blocos e semânticos

Nos exemplos anteriores foi apresentada a **\<div\>**, que simplesmente agrupava uma certa região do arquivo. Essa é de fato a sua funcionalidade e pode ser muito útil para separar uma parte lógica da página e definir uma estilização própria. De maneira semelhante, é possível utilizar a tag **\<span\>**, mas que, diferentemente da div, não cria automaticamente uma quebra de linha e, portanto, usualmente agrupa uma área menor.

O HTML também oferece outros elementos que **aparentam** ter a mesma funcionalidade da div ou do span, os denominados elementos semânticos. Eles também agrupam uma certa seção lógica da página, porém têm o benefício de dar um siginificado para essa seção, tornando a página mais acessível e permitindo que os mecanismos de busca identifiquem mais facilmente os conteúdos da página.

O uso adequado desses elementos semânticos não apenas melhora a estrutura e a legibilidade do código HTML, mas também tem um impacto positivo no SEO. Os mecanismos de busca, como o Google, levam em consideração a estrutura semântica ao indexar e classificar páginas, portanto fornecer estas informações sobre a organização do conteúdo pode resultar em uma melhor classificação nos resultados de pesquisa relacionados.

**OBS: SEO - Search Engine Optimization - é um conjunto de práticas para melhorar o "desempenho" do site, ou seja, fazer com que, ao pesquisar palavras-chaves relacionadas, o site apareça mais acima na lista dos resultados.**

- **\<header\>**: Define o cabeçalho da página e normalmente contém elementos como o logotipo, o título da página e o menu de navegação. **Não confundir com head!**
- **\<nav\>**: Define um menu de navegação e contém justamente os links que direcionam os usuários para diferentes seções ou páginas do site.
- **\<main\>**: Define o conteúdo principal e significativo da página, excluindo cabeçalhos, rodapés, barras laterais, etc.
- **\<section\>**: Define uma seção lógica da página. Cada seção pode ter seu próprio cabeçalho descritivo usando as tags **\<h1\>** a **\<h6\>**.
- **\<article\>**: Define um conteúdo independente e autossuficiente, como um post de blog, uma notícia ou um artigo.
- **\<aside\>**: Define um conteúdo ao lado seção principal, como um menu, por exemplo.
- **\<footer\>**: Define o rodapé da página, que pode conter elementos como direitos da empresa e links para seção de FAQ e de contato.

```html
<header>
  <h1>Meu Site</h1>
  <nav>
    <ul>
      <li><a href="/">Home</a></li>
      <li><a href="/sobre">Sobre</a></li>
      <li><a href="/contato">Contato</a></li>
    </ul>
  </nav>
</header>
<main>
  <section>
    <h2>Título da Seção</h2>
    <p>Conteúdo da seção.</p>
  </section>
  <aside>
    <h3>Barra Lateral</h3>
    <p>Conteúdo relacionado.</p>
  </aside>
</main>
<footer>
  <p>© 2023 Meu Site. Todos os direitos reservados.</p>
</footer>
```

Ao rodar o exemplo apresentado, pode-se perceber que os elementos não ficam nos lugares que deveriam, de acordo com o que foi visto. Isso ocorre pois, mesmo com esses elementos semânticos, o HTML define somente a estrutura e o conteúdo. O posicionamento, espaçamento e tamanho devem ser definidos no CSS.

## Principais usos para React

Para o desenvolvimento de aplicações web e mobile com React, o atual foco do projeto, parte do HTML passa a ser abstraindo ou simplesmente não muito utilizado. Sempre é importante entender a base do desenvolvimento web, no entanto, não é necessário sentir sobrecarregado caso seja muito conteúdo. Tendo isso em vista, alguns tópicos merecem uma atenção especial, pois sempre aparecem quando desenvolvendo em React:

- Parâmetros para tags;
- Cabeçalhos;
- Listas;
- Links e imagens;
- Formulários.

## Conclusão

Esses são os conceitos básicos sobre HTML e alguns exemplos das tags mais comumente utilizadas. É importante testar e modificar os exemplos apresentados para uma maior compreensão, assim como conferir a playlist montada, ao final deste arquivo.

# CSS

## Introdução

Assim como HTML, CSS **não** se trata de uma linguagem de programação, mas sim de uma linguagem de estilização, ou uma Foha de Estilos em Cascata (**Cascading Style Sheets**). Isso significa que ele é responsável por definir a aparência e o layout de uma página da web, através da adição de propriedades nos elementos HTML como cor, tamanho, fonte, margens, posicionamento, etc. O CSS é fundamental para o design e a apresentação visual de uma página web, permitindo criar layouts atraentes, coesos e responsivos.

Um aspecto que pode ficar um pouco confuso com a nomenclatura é em relação à "cascata", mas isso simplesmente quer dizer que os estilos aplicados mais abaixo no arquivo terão prioridade para ser aplicados em relação aos de cima, caso seja a mesma propriedade a ser alterada.

## Utilização básica

Um arquivo CSS se consiste em blocos de estilizações, compostos por um seletor e declarações de estilo. O seletor especifica qual (ou quais) elementos HTML serão estilizados, enquanto que as declarações definem qual será essa estilização, através de propriedades. Por exemplo:

Imagine que se deseja criar uma lista de cards para apresentar os diferentes projetos de extensão da UNIFEI. Para isso o seguinte código pode ser utilizado:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Projetos de Extensão</title>
    <style>
      body {
        background-color: #111122;
      }

      section {
        background: #f0f8ff;
        border-radius: 25px;
        width: 600px;
        height: 200px;
        display: flex;
        justify-content: space-around;
        align-items: center;
      }

      div {
        display: flex;
        height: 100%;
        flex-direction: column;
        justify-content: space-evenly;
      }

      h1 {
        font-size: 36px;
        font-weight: bold;
        color: #3399ff;
        margin: 0px;
      }

      h2 {
        font-size: 18px;
        font-weight: normal;
        margin: 0px;
      }
    </style>
  </head>
  <body>
    <section>
      <img src="../../images/logo.png" alt="Logo Ex Machina" height="150" />

      <div>
        <h1>Ex Machina</h1>
        <h2>Projeto de desenvolvimento de tecnologia assistiva</h2>
      </div>
    </section>
  </body>
</html>
```

No entanto, deixar HTML e CSS no mesmo arquivo não é uma boa prática, então podemos criar um arquivo `styles.css` com os estilos desenvolvidos no mesmo diretório substituir a tag **\<style\>** por:

```html
<link rel="stylesheet" type="text/css" href="styles.css" />
```

## Seletores

O exemplo anterior apresenta algumas propriedades autoexplicativas, como font-size, width ou height, no entanto, algumas propriedades são um pouco mais confusas ao primeiro momento como display, flex-diretcion ou justify-content. Essas propriedades terão um tópico dedicado para elas, entretanto primeiro é necessário aprender sobre os seletores.

### Seletores de elemento

A maneira mais simples de aplicar um estilo a um determinado elemento da página é através do seletor de elemento, que foi utilizado no exemplo anterior. Para utilizá-lo basta declarar qual/quais tags HTML deseja que se aplique determinada estilização.

```css
h1,
h2 {
  font-size: 36px;
  font-weight: bold;
  color: #3399ff;
}

h2 {
  font-size: 24px;
}

h3 {
  font-size: 18px;
  font-weight: normal;
  color: rgb(255, 0, 100);
}
```

Ao colocar dois elementos separados por vírgula no primeiro bloco, o estilo é aplicado em todos. Em seguida o parâmetro "font-size" é sobreescrito em h2 - lembrando que a prioridade se deve pois 24px aparece abaixo no arquivo, caso aparecesse acima, 36px teria prioridade. Por fim, um terceiro estilo é aplicado para h3. Podemos analisar as estilizações com o seguinte trecho em HTML:

```html
<h1>Texto em h1</h1>
<h1>Outro texto em h1</h1>
<h2>Texto em h2</h2>
<h3>Texto em h3</h3>
```

É possível notar que a estilização acontece para todas ocorrências da tag estilizada.

### Seletores de classes e de IDs

Ao utilizar seletores de elemento, logo surge um problema: como estilizar dois elementos de mesma tag de maneiras distintas? A resposta são os seletores de classes e de IDs, que, no geral, são mais utilizados, pois permitem selecionar apenas os elementos desejados, definidos no arquivo HTML.

Os parâmetros class e id:
Durante a capacitação de HTML foi mencionado a existência do parâmentro id. Sua função, no contexto do CSS, é justamente distinguir **um** elemento específico dos demais, para que possa ter uma estilização própria. O parâmetro class funciona de maneira semelhante, no entanto, diferentemente do id, pode ser atribuído a mais de um elemento.

```html
<div id="container">
  <div></div>
  <div class="ball"></div>
  <div class="ball"></div>
  <div></div>
  <div class="rounded"></div>
</div>
```

Os seletores de classe se consistem em um ponto (.) e nome da classe, enquanto os seletores de IDs se consistem em um hashtag (#), seguido pelo id:

```css
body {
  margin: 0px;
}

div {
  height: 100px;
  width: 100px;
  background: #3399ff;
}

#container {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
  height: 100vh;
  width: 100vw;
  background: #def;
}

.ball {
  border-radius: 50px;
}

.rounded {
  border-radius: 25px;
}
```

No exemplo dado, é possível perceber que o id foi aplicado somente em um elemento, equanto que a class foi aplicada em um e em dois elementos, não havendo essa restrição de quantidade. Além de que, mesmo possuindo seletores diferentes, todas divs possuem a estilização do seletor de elemento.

### Seletores aninhados

Uma outra maneira de se especificar qual elemento deseja ser estilizado é através do aninhamento de seletores.

```html
<h1>Título</h1>
<p>
  Parágrafo de fora. Lorem ipsum dolor sit amet consectetur adipisicing elit.
</p>
<div>
  <p>
    Parágrafo de dentro. Lorem ipsum dolor sit amet consectetur adipisicing
    elit.
  </p>
</div>
```

```css
div {
  background: #123;
}

div p {
  color: white;
  padding: 10px;
}
```

Ao colocar seletores de elemento aninhados, o CSS irá aplicar o estilo somente no último seletor que esteja dentro dos seletores especificados anteriormente. Note que apenas o parágrafo de dentro foi alterado para branco, enquanto que o de fora continuou preto.

### Pseudo-classes

Também é possível selecionar elementos em estados específicos, utilizando ":" entre o elemento e o estado desejados.

- **:hover** - quando o cursor do mouse está sobre o elemento
- **:active** - quando o elemento está sendo clicado ou pressionado
- **:focus** - quando está em foco
- **:first-child** - seleciona o primeiro elemento filho de um elemento pai

```html
<section>
  <div></div>
  <div></div>
  <div class="item1"></div>
  <button id="item2">Enviar</button>
  <input class="input" type="text" />
</section>
```

```css
body {
  margin: 0px;
}

section {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  height: 100vh;
  background: #def;
}

section :first-child {
  background: #ff9933;
}

div {
  height: 100px;
  width: 100px;
  background: #3399ff;
  border-radius: 25px;
}

.item1:hover {
  background: #99ff33;
}

#item2:hover {
  background: #ffee55;
}

#item2:active {
  background: #ff9933;
}

section input:focus {
  color: #3399ff;
}
```

Isso conclui a utilização básica e mais cotidiana sobre seletores. Existem alguns outros pontos como seletores de atributos e pseudo-elementos, porém não precisam ser estudados nesse primeiro momento.

## Estilizações

Agora, com o conhecimento sobre seletores, é possível estudar o ponto principal do CSS, que são as estilizações propriamente ditas. Como dito anteriormente, nos exemplos foram apresentadas algumas propriedades autoexplicativas e outras um pouco mais complicadas, porém todas as mais importantes serão analisadas nas seções a seguir.

### Cores e imagens

As cores em CSS podem ser definidas de maneiras diferentes, conforme a conveniência do desenvolvedor.

- Nome: existe uma [lista de nomes de cores](https://www.w3.org/wiki/CSS/Properties/color/keywords) para utilizar no CSS
- RGB - red, green, blue: cada valor varia de 0 a 255
- RGBA - red, green, blue, alpha: cada valor varia de 0 a 255 e o alpha (opacidade) de 0 a 1
- Hexadecimal - RGB em base hexadecimal: cada valor varia de 00 a ff
- HSL - hue, saturation, lightness:
  hue define qual a cor no círculo cromático (0 a 360);
  saturation define a saturação da cor (0 a 100%);
  lightness define a claridade da cor (0 a 100%);
- HSLA - hue, saturation, lightness, alpha

```html
<div id="container">
  <div class="name"></div>
  <div class="rgb"></div>
  <div class="rgba"></div>
  <div class="hex"></div>
  <div class="hex-short"></div>
  <div class="hsl"></div>
  <div class="hsla"></div>
  <div></div>
</div>
```

```css
body {
  margin: 0px;
}

div {
  height: 100px;
  width: 100px;
}

#container {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
  height: 100vh;
  width: 100vw;
  background: #ccc;
}

.name {
  background: aliceblue;
}

.rgb {
  background: rgb(200, 10, 95);
}

.rgba {
  background: rgba(200, 10, 95, 0.5);
}

.hex {
  background: #3399ff;
}

.hex-short {
  background: #39f;
}

.hsl {
  background: hsl(120, 80%, 50%);
}

.hsla {
  background: hsla(120, 80%, 50%, 0.5);
}
```

Além da propriedade `background` ou `background-color` existem algumas outras que utilizam cor:

- color: altera a cor do texto
- border-color: altera a cor da borda
- accent-color: altera a cor de um elemento selecionado, como checkbox ou radio button
- outline-color: altera a cor fora da borda

O CSS também facilita o processo de trabalhar com imagens, oferecedno algumas opções.

```html
<img src="../../images/img_example.jpg" alt="fundo com casas" />
```

```css
img {
  max-width: 100%;
  height: auto;
}
```

Esse exemplo simples faz com que a imagem de torne responsiva, ou seja, mude de tamanho conforme o tamanho do navegador até que atinja seu tamanho máximo em contraste com o padrão, que simplesmente corta a imagem.

```css
img {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 100%;
}
```

Utilizando a estilização apresentada acima para a mesma imagem, pode-se perceber que ela apresenta um comportamento parecido, no entanto também oferece a possibilidade de diminuir ou esticar a imagem, sempre deixando-a no centro. Caso precise manter o tamanho original da imagem basta trocar a propriedade `width` por `max-width`, como no exemplo anterior.

```html
<div>
  <h1>Tem uma imagem aqui atrás</h1>
</div>
```

```css
div {
  background-image: url("../../images/img_example.jpg");
  background-color: #222;
  display: flex;
  justify-content: center;
}
```

Esse exemplo apresenta uma das forma de definir uma imagem como fundo de uma div. É importante lembrar de definir uma cor de fundo para caso a imagem não carregue.

### Texto e fontes

- color: altera a cor do texto
- background-color: altera a cor do fundo do texto
- text-align - left, center, right, justify: define o alinhamento do texto
- text-decoration - overline, line-through, underline: define uma linha de decoração para o texto
- text-indent: define o tamanaho do espaçamento do parágrafo do texto
- text-shadow: cria uma sombra para o texto
- font-weight: define o peso da fonte. Pode ser por extenso 'bold', 'normal' ou por numeração 100, 200, ..., 900
- font-family: define a fonte propriamente dita para o texto
- font-style - italic, normal: define se o texto será em itálico ou não

```html
<body>
  <h1>Lorem ipsum dolor sit amet consectetur adipisicing elit</h1>
  <h2>Lorem ipsum dolor sit amet consectetur adipisicing elit</h3>
  <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsam id aliquam quasi esse debitis, assumenda aspernatur dignissimos, adipisci obcaecati maiores, vel non voluptatem repudiandae iusto ipsa tempore. Ab, facere atque.</p>
  <p class="text1">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsam id aliquam quasi esse debitis, assumenda aspernatur dignissimos, adipisci obcaecati maiores, vel non voluptatem repudiandae iusto ipsa tempore. Ab, facere atque.</p>
  <p class="text2">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsam id aliquam quasi esse debitis, assumenda aspernatur dignissimos, adipisci obcaecati maiores, vel non voluptatem repudiandae iusto ipsa tempore. Ab, facere atque.</p>
  <p class="text3">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsam id aliquam quasi esse debitis, assumenda aspernatur dignissimos, adipisci obcaecati maiores, vel non voluptatem repudiandae iusto ipsa tempore. Ab, facere atque.</p>
  <p class="text4">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsam id aliquam quasi esse debitis, assumenda aspernatur dignissimos, adipisci obcaecati maiores, vel non voluptatem repudiandae iusto ipsa tempore. Ab, facere atque.</p>
  <p class="text5">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsam id aliquam quasi esse debitis, assumenda aspernatur dignissimos, adipisci obcaecati maiores, vel non voluptatem repudiandae iusto ipsa tempore. Ab, facere atque.</p>
</body>
```

```css
body {
  width: 50%;
}

h1 {
  color: tomato;
  background-color: black;
  text-decoration: line-through;
}

h2 {
  text-decoration: overline underline;
}

.text1 {
  text-align: center;
  text-shadow: 2px 2px blue;
}

.text2 {
  text-align: justify;
  text-indent: 30px;
  text-shadow: 2px 2px 5px blue;
  font-family: courier new;
}

.text3 {
  text-align: right;
  font-weight: bold;
  font-family: sans-serif;
  font-style: italic;
}

.text4 {
  text-indent: 30px;
  font-family: helvetica;
}

.text5 {
  font-family: Roboto;
}
```

O exemplo acima demonstra algumas propriedades de texto, que quando combinadas de forma mais lógica podem melhorar muito o design de uma página. O último parágrafo merece uma atenção especial, pois se trata de uma fonte que não vem por padrão nos navegadores, mas sim de uma fonte do Google (Google Fonts). Para utilizá-la basta adicionar a seguinte linha de código dentro da tag head do arquivo HTML e antes da adição do arquivo CSS:

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Roboto" />
```

Isso fará com que a fonte seja carregada e possa ser utilizada na aplicação. Para utilizar alguma outra fonte do Google, basta trocar o parâmetro family na url acima. A seção de materias para estudo, ao final do arquivo, contém um link para uma lista das fontes disponíveis.

### Box Model (Modelo de caixa)

O box model é essencialmente uma caixa que envolve todos elementos HTML e se consiste, de dentro para fora, em:
conteúdo, padding, border e margin, além das dimensões propriamente ditas de largura e altura (width e height). Esses elementos são utilizados para definir os espaçamentos em torno e dentro dos elementos.

- width: define a largura de um elemento
- height: define a altura de um elento
- padding: define o espaçamento interno de um elemento
- margin: define o espaçamento externo de um elemento
- border-width: define a grossura da borda de um elemento
- border-color: define a cor da borda
- border-style: define o estilo da borda
- border: atalho para border-width border-style e border-color
- border-radius: define o arredondamento dos cantos de um elemento, mesmo se ele não tiver borda
- box-sizing: define se o as bordas e paddings serão considerados ou não para o tamanho do elemento

```html
<section id="container">
  <div class="item1"><h1>1</h1></div>
  <div class="item2"><h1>2</h1></div>
  <div class="item3"><h1>3</h1></div>
  <div class="item4"><h1>4</h1></div>
</section>
```

```css
body {
  margin: 0px;
  background: #def;
}

div {
  background: #3399ff;
  height: 100px;
  width: 100px;
  overflow: hidden;
}

h1 {
  background: #fff;
  height: 100%;
  width: 100%;
  margin: 0px;
  text-align: center;
  line-height: 100px;
}

#container {
  height: 100vh;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}

.item1 {
  border: 5px solid #ff9933;
  border-radius: 25px;
}

.item2 {
  margin: 15px;
}

.item3 {
  padding: 20px;
}

.item4 {
  border-width: 5px;
  border-style: solid;
  border-color: #ff9933;
  border-radius: 25px;
  margin: 15px;
  padding: 20px;
}
```

O exemplo mostra o comportamento de cada uma das propriedades apresentadas. Note que os dois primeiros itens aparecem totalmente brancos, mesmo sendo definidos inicialmente como azul, isso ocorre pois não há nenhum padding neles, fazendo com que o conteúdo interno (a h1) ocupe todo o espaço disponível. No navegador, abra o Menu do Desenvolvedor (tecla F12) e selecione a aba elementos. Expanda os elementos e passe o mouse por cima de cada um, observando o espaçamento definido por cada propriedade e a alteração causada no tamanho. Caso seja necessário manter o tamanho dos elementos mesmo com borda e padding aplicados, é possível adicionar a propriedade `box-sizing: border-box;`:

```css
div {
  background: #3399ff;
  height: 100px;
  width: 100px;
  overflow: hidden;
  box-sizing: border-box;
}
```

Use o Menu do Desenvolvedor novamente para visualizar a alteração nos tamanhos. Perceba como a margem não é inclusa no tamanho, mesmo após essa opção ser adicionada.

**OBS: Ao passar o mouse sobre a tag section, aparecerá algumas bordas roxas, elas são referentes ao flexbox, conceito muito importante que será abordado ao final das estilizações.**

Nesse caso foi fácil aplicar a propriedade para todos elementos, pois eram todos divs, mas nem sempre isso acontece, sendo necessário aplicar em cada elemento desejado. Porém é possível "definir essa opção como padrão" (na verdade aplicá-la em todos elementos) utilizando o sentido bloco no CSS:

```css
* {
  box-sizing: border-box;
}
```

O seletor \* seleciona todos os elementos do HTML e aplica as propriedades definidas. De preferência coloque-o ao topo no arquivo ou logo após o body, pois dessa maneira, caso deseje que algum elemento não possua essa propriedade é possível revertê-la adicionando `box-sizing: content-box;` onde desejado.

### Opacidade e sombras

Ao longo dos exemplos foi falado um pouco sobre opacidade nas cores e sombras no texto. No entanto, também é possível aplicá-las em outros elementos através das propriedades:

- opactity - 0 a 100%: define a opacidade de uma imagem, cor, texto, etc.
- text-shadow: aplica uma sombra no texto
- box-shadow: aplica uma sombra em outros elementos

```html
<body>
  <section class="card1">
    <img src="../../images/logo.png" alt="Logo Ex Machina" height="150" />
    <h1>Tecnologia Assistiva</h1>
  </section>

  <section class="card2">
    <img src="../../images/logo.png" alt="Logo Ex Machina" height="150" />
    <h1>Tecnologia Assistiva</h1>
  </section>

  <section class="card3">
    <img src="../../images/logo.png" alt="Logo Ex Machina" height="150" />
    <h1>Tecnologia Assistiva</h1>
  </section>
</body>
```

```css
body {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  height: 100vh;
  background: #eef;
}

img {
  height: 250px;
  width: 250px;
}

.card1,
.card2,
.card3 {
  background: #f0f8ff;
  border-radius: 25px;
  width: 400px;
  height: 400px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}

.card1 {
  box-shadow: 0px 0px 10px gray;
}

.card2 {
  box-shadow: 10px 10px lightblue;
}

.card3 {
  opacity: 50%;
  box-shadow: 10px 10px lightblue;
}

h1 {
  background-color: white;
  width: 100%;
  font-size: 36px;
  color: #3399ff;
  font-family: helvetica;
  text-align: center;
  border-radius: 0px 0px 25px 25px;
  margin: 0px;
  padding: 40px 0px;
  text-shadow: 2px 2px black;
}
```

### Unidades de medida e Responsividade

Nos exemplos, foi utilizado apenas a unidade "px" - e em alguns casos % e vh - para definir tamanhos, porém existem outras formas de fazê-lo no CSS, com medidas absolutas e relativas.

- Medidas absolutas:

  São medidas que sempre valerão o mesmo tamanho, ou seja, não dependem de uma referência. Ex:

  - px ("pixels"): A unidade de tamanho mais comumente utilizada no CSS
  - pt (points), pc (paica): Unidades de medida de texto
  - in (inches), cm (centímetros), mm (milímetros) : Unidades de medida do "mundo real"

  OBS: 1 in = 2,54cm = 25,4mm = 72pt = 6pc

- Medidas relativas:

  São medidas que mudarão de tamanho conforme uma referência adotada. Ex:

  - % (porcento): porcentagem do tamanho do elemento pai
  - em (font-size), rem (root em): em utiliza a font-size do elemento pai como unidade básica, já o rem utiliza a font-size do root como unidade básica
  - vw (viewport width), vh (viewport height): 1/100 da largura e altura, respectivamente, do dispositivo

  A partir dessas medidas relativas, é possível inciar o conceito de responsividade: a capacidade de uma página se adaptar a diferentes dispositivos e tamanhos de tela. Ao utilizá-las, uma medida sempre manterá a mesma proporção em diferentes tamanhos de dispositivos, fazendo com o que o site se torne de certa forma mais acessível. Isso é, se os dispositivos não tiverem uma diferença muito grande de tamanho, para esse caso é necessário utilizar media queries, que não convêm serem explicadas por agora.

```html
<section id="container">
  <div class="item1">
    <h1>título</h1>
    <p>conteúdo</p>
  </div>
  <div class="item2">
    Texto do item 2
    <div></div>
  </div>
</section>
```

```css
body {
  margin: 0px;
  background: #def;
}

div {
  background: #3399ff;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

#container {
  height: 100vh;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}

.item1 {
  padding: 10px;
  border-radius: 25px;
  height: 5cm;
  width: 50mm;
}

.item1 h1 {
  font-size: 24pt;
  margin: 0px;
}

.item1 p {
  font-size: 1.5pc;
}

.item2 {
  height: 30vh;
  width: 40vw;
  font-size: 24pt;
}

.item2 div {
  height: 5em;
  width: 10em;
  background: #ff9933;
}
```

Para analisar esse exemplo, abra novamente o Menu do Desenvolvedor com a tecla F12, procure pela opção "emulação de dispositivo" e mexa com o tamanho da tela. Veja como o item 1 mantém seu tamaho constante, enquanto que o item 2 se ajusta conforme o tamanho é alterado. Altere também o tamanho do `font-size` no item 2 e veja os impactos na div laranja em seu interior.

Também é possível definir tamanhos mínimos e máximos fixos, para limitar a expansão ou encolhimento de um elemento através das propriedades:

- min-height
- min-width
- max-height
- max-width

```css
.item2 {
  height: 30vh;
  width: 40vw;
  font-size: 24pt;
  min-height: 150px;
  min-width: 300px;
  max-height: 250px;
  max-width: 500px;
}
```

## Flexbox

O CSS também ofere alguns modelos de layouts. O mais utilizado entre eles é o flexbox, que foi utilizado nos exemplos anteriores para que eles pudessem ser vistos de forma mais clara. Ele organiza e alinha elementos em uma única dimensão (linha ou coluna), através de um eixo principal e um eixo secundário. Para utilizar o flexbox, é necessário um elemento pai (flex container) com a propriedade `display: flex` e elementos filhos (flex items) que serão organizados, ajustando-se automaticamente ao espaço disponível.

Como à primeira vista o flexbox é um conceito complexo de se entender, ele será dividido em seções de acordo com as suas principais propriedades

### Eixo principal e secundário

O layout do flexbox é determinado pela existência de dois eixos, como um plano cartesiano. No entanto, no lugar de x e y, existem o eixo principal e o secundário, que são na prática o que determina a disposição dos elementos filhos. Na web, o eixo das linhas (no plano cartesiano o eixo x) é padronizado como o principal, devido ao formato nas telas de computador, já no desenvolvimento mobile, o eixo das colunas é padronizado como o principal.

- flex-direction - row, column, row-reverse, column-reverse: define o eixo principal dos itens dentro do contêiner.
- justify-content - flex-start, center, flex-end, space-around, space-evenly, space-between: controla a disposição dos itens no eixo principal.
- align-items - flex-start, center, flex-end, stretch: controla o alinhamento dos itens no eixo secundário.

Essas são as três propriedades mais importantes para se trabalhar com o flexbox, sua utilização será vista através de exemplos:

```html
<section id="container">
  <div></div>
  <div></div>
  <div></div>
  <div></div>
  <div></div>
</section>
```

```css
body {
  margin: 0px;
  background: #def;
}

div {
  height: 100px;
  width: 100px;
  border-radius: 25px;
  background: #3399ff;
}

#container {
  height: 100vh;
  display: flex;
  justify-content: space-around;
}
```

Nesse primeiro exemplo, o eixo principal é o eixo das linhas e existe um espaçamento ao redor de cada item dele. Note que o espaço nas laterais é metade do espaço entre um item e outro. O eixo secundário não foi alterado e, portanto, utiliza o alinhamento padrão flex-start, ou seja, no ínicio do contêiner.

```css
#container {
  height: 100vh;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}
```

Para o segundo exemplo podemos alterar somente a estilização do elemento pai. Agora, o espaçamento entre os elementos filhos está padronizado e estão alinhados ao centro do eixo secundário. OBS: para essa disposição funcionar na maneira intencionada, é necessário que o contêiner ocupe todo o espaço vertical da tela, veja o que acontece ao remover essa propriedade.

```css
#container {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-end;
}
```

Para esse exemplo, o eixo principal foi definido como o eixo das colunas e os itens estão dispostos ao seu centro. O alinhamento dos itens no eixo secundário está ao final.

```css
div {
  height: 100px;
  /* width: 100px; */
  border-radius: 25px;
  background: #3399ff;
}

#container {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: stretch;
}
```

Também é possível remover os espaços laterais e fazer com que os itens se estiquem no eixo secundário (mas para isso é necessário remover o tamanho fixo de 100px da div)

Para um melhor entendimento experimente testar cada combinação dessas propriedades e analisar o resultado.

### Quebra de linha

Mas o que acontece caso o tamanho dos itens seja maior que o disponível?

- flex-wrap - wrap, nowrap, wrap-reverse: determina se os itens devem quebrar ou não para a próxima linha (ou coluna) quando o espaço no contêiner é insuficiente.
- align-content - flex-start, center, flex-end, space-around, space-evenly, space-between: Controla a disposição das linhas quando há quebra de linha ou de coluna.

```html
<section id="container">
  <div>1</div>
  <div>2</div>
  <div>3</div>
  <div>4</div>
  <div>5</div>
  <div>6</div>
  <div>7</div>
  <div>8</div>
  <div>9</div>
  <div>10</div>
  <div>11</div>
  <div>12</div>
  <div>13</div>
  <div>14</div>
  <div>15</div>
</section>
```

```css
body {
  margin: 0px;
  background: #def;
}

div {
  height: 100px;
  width: 100px;
  border-radius: 25px;
  background: #3399ff;
  text-align: center;
  line-height: 100px;
  font-size: 36px;
  margin: 5px;
}

#container {
  height: 100vh;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

Com esse exemplo é possível ver que os itens ficam espremidos para caber na mesma linha. Veja o que acontece ao adicionar a propriedade `flex-wrap: wrap;` ao container. Veja também o comportamento com a opção "wrap-reverse". Nesse caso, é possível utilizar a propriedade `align-content` para determinar a disposição das linhas de maneira semelhante a `jusify-content`:

```css
#container {
  height: 100vh;
  display: flex;
  justify-content: space-between;
  align-items: center;
  align-content: space-between;
}
```

### Propriedades dos filhos

- align-self - flex-start, center, flex-end, stretch: permite alterar o alinhamento individual de um item no eixo secundário do contêiner.
- flex-grow e flex-shrink: controlam como os itens crescem ou encolhem em relação ao espaço disponível.

```html
<section id="container">
  <div class="item1">1</div>
  <div class="item2">2</div>
  <div class="item3">3</div>
  <div class="item4">4</div>
  <div class="item5">5</div>
</section>
```

```css
body {
  margin: 0px;
  background: #def;
}

div {
  height: 100px;
  width: 100px;
  border-radius: 25px;
  background: #3399ff;
  text-align: center;
  line-height: 100px;
  font-size: 36px;
  margin: 5px;
}

#container {
  height: 100vh;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}

.item1 {
  align-self: flex-start;
}

.item5 {
  align-self: flex-end;
}

.item3 {
  align-self: stretch;
  height: auto;
}
```

A propriedade `align-self` no geral é bem intuitiva.

```css
.item2 {
  flex-grow: 1;
}
```

Ao adicionar a estilização acima, o item2 passa a ocupar todo o espaço disponível no eixo principal, pois é o único elemento com `flex-grow` maior que 0 (padrão).

```css
div {
  height: 100px;
  width: 100px;
  border-radius: 25px;
  background: #3399ff;
  text-align: center;
  line-height: 100px;
  font-size: 36px;
  margin: 5px;
  flex-grow: 1;
}

.item2 {
  flex-grow: 2;
}
```

Dessa maneira, o item 2 crescerá o dobro do espaço dos demais, pois agora cada um possui `flex-grow: 1;`. Obs: remova a estilização dos outros itens para uma melhor visualização.

Por outro lado, existe a opção `flex-shrink`, que determina justamente quanto um item irá encolher quando faltar espaço.

```html
<section id="container">
  <div>1</div>
  <div>2</div>
  <div>3</div>
  <div>4</div>
  <div>5</div>
  <div>6</div>
  <div>7</div>
  <div>8</div>
  <div>9</div>
  <div>10</div>
  <div>11</div>
  <div>12</div>
  <div>13</div>
  <div>14</div>
  <div>15</div>
</section>
```

```css
body {
  margin: 0px;
  background: #def;
}

div {
  height: 100px;
  width: 100px;
  border-radius: 25px;
  background: #3399ff;
  text-align: center;
  line-height: 100px;
  font-size: 36px;
  margin: 5px;
  flex-grow: 1;
}

#container {
  height: 100vh;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}

.item1 {
  flex-shrink: 0;
}

.item2 {
  flex-shrink: 0.5;
}
```

Note como o primeiro elemento mantém seu tamanho original o segundo diminui somente a metade e os demais são encaixados no espaço restante.

Existem outras propriedades dos itens como order, flex-basis e flex, no entanto não são tão costumeiras.

## Conclusão

Isso encerra o conteúdo mais comumente utilizado em CSS. Vale repetir o que foi dito na seção de HTML: ver os exemplos apresentados na prática e interagir com eles, assim como conferir os conteúdos que não foram tão bem compreendidos, no material disponível ao final do arquivo. E caso tenha dúvidas, sinta-se livre para perguntar!

Joguem o [jogo do sapinho](https://flexboxfroggy.com/) também, é bem divertido e ajuda muito a decorar as propriedades do flexbox.

## Tailwind

### Introdução

Atualmente no projeto, utilizamos uma biblioteca feita a partir do CSS para o desenvolvimento web, o Tailwind. Ele tem como principal objetivo simplificar o processo de estilização e tornar os elementos naturalmente mais responsivos - utilizando rem como unidade básica no lugar de px, por exemplo. Tendo isso em vista, deixa-se claro que esse conteúdo é mais opcional no momento, para ter uma noção básica da existência e com o tempo, conforme conveniente, serão introduzidos mais conceitos.

O Tailwind em si não adiciona nenhuma propriedade de estilização própria, ele apenas compila as existentes do CSS em classes de fácil reutilização. Entretanto, ele adiciona algumas palhetas de cores, que também facilitam o processo, principalmente inicial, de design e desenvolvimento.

Uma última nota antes de partir para o conteúdo em si é que o Tailwind compila todo "código" desenvolvido de volta para CSS, fazendo que não haja acréscimos significativos no seu peso.

### Exemplo

Como a configuração é complicada e desnecessária no momento, o site [Tailwind Play](https://play.tailwindcss.com/) pode ser usado para visualizar e testar.

Diferentemente do CSS, a proposta do Tailwind é unir novamente a estilização com a definição do elemento HTML, por isso, usualmente, vem junto ao HTML.

```html
<div class="flex flex-col items-center justify-evenly min-h-screen">
  <div
    class="w-1/3 h-32 bg-green-400 border-0 rounded-full shadow-lg shadow-gray-700"
  ></div>
  <div
    class="w-1/3 h-32 bg-yellow-300 border-0 rounded-full shadow-lg shadow-gray-700"
  ></div>
  <div
    class="w-1/3 h-32 bg-red-500 border-0 rounded-full shadow-lg shadow-gray-700"
  ></div>
</div>
```

O Tailwind procura sempre utilizar nomes intuitivos para as classes e passando o mouse por cima delas é possível ver qual estilização do CSS está sendo de fato aplicada.

**OBS: vale sempre a pena estudar o CSS em si primeiro, para depois ver como o Tailwind utiliza a propriedade desejada.**

# Materiais para estudo

- **[Playlist HTML e CSS](https://www.youtube.com/playlist?list=PLPjSrtKJfMyfSH55NTT5RdHTeQqBr4wIM)**
- [Curso da Alura](https://cursos.alura.com.br/formacao-html-css-v534235)
- [Curso da Udemy](https://www.udemy.com/course/curso-web/learn/lecture/9646336#overview)
- [W3 Schools CSS](https://www.w3schools.com/css/css_intro.asp)
- [Nomes de cores](https://www.w3.org/wiki/CSS/Properties/color/keywords)
- [Google Fonts](https://fonts.google.com/)
- [Joguinho do sapo](https://flexboxfroggy.com/)
- [CSS animado](https://dev.to/jon_snow789/an-animated-lesson-on-css-will-teach-you-how-to-use-it-2dj4)
- [Unidades do CSS](https://www.alura.com.br/artigos/guia-de-unidades-no-css)
- [Tailwind em 13:37](https://www.youtube.com/watch?v=dHwY5lRfkoQ)
- [Tailwind Play](https://play.tailwindcss.com/)
