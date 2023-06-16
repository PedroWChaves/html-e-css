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

No entanto, deixar HTML e CSS no mesmo arquivo não é uma prática boa, então podemos criar um arquivo `styles.css` com os estilos desenvolvidos no mesmo diretório substituir a tag **\<style\>** por:

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

### Aninhamento de seletores

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
  background: #def;
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

# Materiais para estudo

- **[Playlist HTML e CSS](https://www.youtube.com/playlist?list=PLPjSrtKJfMyfSH55NTT5RdHTeQqBr4wIM)**
- [Curso da Alura](https://cursos.alura.com.br/formacao-html-css-v534235)
- [Curso da Udemy](https://www.udemy.com/course/curso-web/learn/lecture/9646336#overview)
- [Joguinho do sapo](https://flexboxfroggy.com/)
- [CSS animado](https://dev.to/jon_snow789/an-animated-lesson-on-css-will-teach-you-how-to-use-it-2dj4)
