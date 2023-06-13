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

Daqui em diante será utilizada essa separação.

# Materiais para estudo

- **[Playlist HTML e CSS](https://www.youtube.com/playlist?list=PLPjSrtKJfMyfSH55NTT5RdHTeQqBr4wIM)**
- [Curso da Alura](https://cursos.alura.com.br/formacao-html-css-v534235)
- [Curso da Udemy](https://www.udemy.com/course/curso-web/learn/lecture/9646336#overview)
- [Joguinho do sapo](https://flexboxfroggy.com/)
- [CSS animado](https://dev.to/jon_snow789/an-animated-lesson-on-css-will-teach-you-how-to-use-it-2dj4)
