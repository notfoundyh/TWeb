# TWeb

---aula 16 outubro---

html - hyper text markup language, é uma linguagem de marcação e não programação

os ficheiros .html contêm conteúdo texto(informação que o utilizador deve ver)

elementos com conteúdo/elementos vazios

tipos de elementos - block e inline

atributo é informação adicional- está dentro de tag <>

//Estrura de uma página html divide-se em head e body

<! DOCTYPE html> // versão html usada

<html>

<head>
    <title>Primeira página </title> //O head não é visualizado no browser mas ajuda o motor de pesquisa
</head>

<base> //especifica um caminho para usar como base p imagens e isso

<link> // ligação a recursos externos

<style> //usade p definir o estilo


<meta>  //dados 
<meta name = "valor" content="xxx">
<meta http-equiv="valor" content="xx">
<meta charset="utf-8"> //define o tipo de caracteres que a página inclui tipo mandarim etc, este utf-8 é o mais comum

MIME type são tipos de dados tipo GIF, MP3, JPEG etc

//Elementos body

paragrafo <p> texto do paragrafo </p>

cabeçalho h1 cabeçalho de primeiro nível h1

//...até

<h6>

linha horizontal <hr>
imagens <img src="url" alt="descritivo">
links <a href="url"> conteudo </a>
enfase <em> texto 
quebra de linha
comentários <!--   é assim que se faz um comentário -->
listas não ordenadas        <!--   tópicos com bolinhas por exemplo -->
listas ordenadas        <!--   tópicos 1,2,3 ou abc -->
listas de definições
tabelas <table>
http://validator.w3.org //corrige o codigo

Ao criar um ficheiro html se fizermos !+tab o visual studio da  estrutura incial 

--- Aula 25 de outubro ---
CSS - linguagem de controlo de aparência, layout e apresentação
1. Para definir os estilos podemos usar diretamento os elementos html usando o atributo de style
2. na secção head como um elemento style
3. Num ficheiro externo com extensão .css aplicando à pagina através do elemento link (link rel="stylesheet" type"text/css" href="style.css")

é possível ligar várias css à mesma página, mas podem haver conflitos de estilo que o sistema resolve por aplicação de regras de precedência

Regra - especifica um ou mais elementos ou um conjunto de estilo que vao ser aplicados

Sintaxte de uma regra: 
selector{
property: value;
}
exemplo:
p, h1, h2{
    color: green;       /* ISTO É UM COMENTÀRIO EM CSS as propriedades devem ser escritas sempre em minisculas e se tiverem várias palavras devem ser ligadas por um hifen */
}
h2{
    background-color: yellow;
}
há tres formas de especificar cores
1. nomes predefinidos
2. codigo rgb
3. cores heaxdecimais

propriedades p fonte
font-family
font-size
font-weight
font-style
font /* p {
    font:italic bold 14x "Comic Sans MS" cursive;
} */

Os tamanhos podem ser
unidades - pixels, point, m-size
tamanhos vagos - xx-small, small, medium
percentuais - 90%, 120%

Podemos atribuir ao elemento html um atributo designado id que o identifica e assim por exemplo mudamos a cor só de uma palavra. 
/* #id{
    property: value
}

<h2> id="europa"> Europa </h2>
#europa{
    font-style: italic;
} */
Quando queremos aplicar um determinado estilo a mais que um elemento usamos class 
/* .class{
    property: value;
} */

--- Aula 30 outubro ----
Podemos controlar o background em nivel de bloco adicionado (cores, imagens)
/* background-image: #;
    background-position:bottom-right; (podemos colocar tmb em pixels ou %)
    background-repeat: no-repeat;
    background-attachement:fixed;
    background-color: lightgrey;
*/

---- Aula 6 novembro ----
Text Shadow/ Box Shadow - adicionar sombra no texto e é tido pelo deslocamento horizontal da sombra, deslocamento vertical, raio de desfoque e cor 
/* text-shadow -4px 4px 6px dimgrey; (add shadow)
font-size: 400% (inreasing font-size) */

Border radius - fillet, um border-radius maior que a metado do comprimento lateral mais curto faz com que a extremidade fiwue completamente curva
podemos especificar em border-top-left-radius, border-top-right-radius,border-bottom-left-radius e border-bottom-right-radius

Gradientes lineares - pode se fazer transição entre quantas cores nós quisermos, chamados color-stops
/* Dependendo do browser pode ser de maneiraa diferente pq em alguns browser pode não ser suportado por ser mais antigo mas atualmente todos suportam se for assim:
background linear-gradient(
    to bottom, white 15%, lightsteelblue 50%, navy 75%):
    float: left;
    margin-right: 15px;

    Gradientes Radiais - valores a definir são top, bottom, left e riht
    background: radial-gradient(center, yellow,red)
    */
Layout de multiplas colunas

para criar as colunas +e usado column-count e a propriedade column-gap que dá o espaçamento entre elas
p por uma linha a espaçar podemos usar column-rule

Media-queries - define os atributos mais adequeados conforme o utilizador está a vizualizar a página - personaliza a vizualização p mobile, tablet, desktop etc
/* criar colunas consoante o tamanho da tela
@media handheld and (max-width: 480px),
screen and (max-devide-widh: 480px),
screen and (max-width: 480px)
{
    div{
        column-count: 1;
    }
}
Escrever isto as vezes q foram necessárias tendo em conta ps tamanhos dos dispositivos q queremos abranger
o browser analisa a regra, o resultado é verdadeiro ou falso
*/
Grid - sistema de layout bidimensional trabalha horizontal e vertical, acaba por ser mais facil n é preciso usar flutuadores e posicionamento
Flexbox - layout unidimensional, é util na alocação e alinhamento do espaço entre itens num contentor

container - contem grid items
quando usamos o estilo de grelha temos de usar 
display:grid | inline-grid;
vertical - linhas de colunas
horizontal - linhas de grelhas
os espaços chama-se células e é p por o conteúdo do website
/*
HTML
<div id="layout" >
<div id="one">Um</div>
<div id="two">Dois</div>
<div id="three">Três</div>
<div id="four">Quatro</div>
<div id="five">Cinco</div>
</div>
css
#layout {
 display: grid;
 grid-template-rows : 100px 400px 100px;  // largura das colunas
grid-template-columns : 200px 500px 200px;
}

para ser mais facil em vez de numeros podemos dar nomes
#layout {
display: grid;
grid-template-rows: [header-start] 100px [header-end content-start] 400px [content-end footerstart] 100px;
grid-template-columns: [anúncios] 200px [principal] 500px [links] 200px;
*/
A função minmax() restringe o intervalo de tamanho da trilha
definindo uma dimensão mínima e máxima.
min-content é o menor que uma faixa pode ter.
max-contente aloca a quantidade máxima de espaço necessário.
auto permite que o navegador cuide disso. Comece com auto para
dimensionamento baseado em conteúdo.
repeat()permite repetir padrões em tamanhos de track:
repeat( # , track pattern)
O primeiro número é o número de repetições. Os tamanhos das tracks após a
vírgula fornecem o padrão.
/* ANTES:
grade-modelo-colunas: 200px 20px 1fr 20px 1fr 20px 1fr 20px 1fr
20px 1fr 20px 1fr 200px;
DEPOIS:
grid-template-columns: 200px repeat(5, 20px 1fr) 200px ; */
Grid areas - os nomes entre [] são opcionais é só p guiar
/* #layout {
display: grid;
grid-template-rows: [header-start] 100px [content-start] 400px [footer-start] 100px;
grid-template-columns: [anúncios] 200px [principal] 1fr [links] 200px;
 grid-template-areas:
"header header header"
"ads main links"
"footer footer footer"

#one { grid-area: header; }
#two { grid-area: ads; }
#three { grid-area: main; }
#four { grid-area: links; }
#five { grid-area: footer; }
*/

grid-auto-rows
grid-auto-column
Especifica se você deseja que os itens fluam por linha ou coluna . O padrão
é a direção de escrita do documento.
#listagens {
display: grid;
 grid-auto-flow: column dense;
 Use a propriedade auto-flow na propriedade de grid
abreviada para indicar que as linhas ou colunas devem ser geradas
automaticamente. As colunas são estabelecidas explicitamente, mas as linhas são geradas
automaticamente.
grid-row-gap grid-column-gap
Grid-gap: 20px 50px;
Layout Flexbox
oferece maior controle sobre a organização de
componentes de itens de página da Web ao longo de um eixo
Vantagens do Flexbox
• Capacidade de “flexionar” – esticar ou encolher dentro de seus containers
• Capacidade de fazer todos os itens vizinhos da mesma altura
• Fácil centralização horizontal e vertical
• Capacidade de alterar a ordem de exibição dos itens independentemente da
fonte html
.flex-container {
display: flex;
}
.flex-container {
display: inline-flex;
}
/* Itens flexíveis alinhados ao longo de
um eixo
eixo principal -ou- eixo transversal
O eixo principal é a direção do fluxo
que especificou para o
container flexível. O eixo transversal
é perpendicular ao eixo principal 

#container {
display: flex;
height: 350px;
flex-flow: column wrap // é um shortcut, por a direção e depois o estilo que queremos
*/
Flex item - Properties
flex item properties determines how space is distributed within items
flex
None | ‘flex-grow flex-shrink flex-basis’
Flex: flex-crescer flex-encolher flex-base
Exemplo
li {
flexível: 1 0 200px
}
Valores de 1 e 0 funcionam como on/off
1 “liga” ou permite que um item cresça ou diminua
0 “desliga” impede que o item cresça ou diminua
Exemplo
Este item da lista começa com 200px de largura
é permitido crescer para preencher o espaço extra
NÃO
é permitido encolher abaixo de 200px

Aula 18 dezembro
Frameworks (nós vamos usar o bootstrap)
Frameworks são conjuntos de estilos já predifinidos e reutilizaveis p website e app web
bootstrap
bluma
tailwind
materialize - é da google

no bootstrap tem tres tipos de containers
.container wich sets a max widh at each responsive breakpoint
.container-fluid, wich is widh: 100% at all breakpoints
.container-{breakpoint}

.container sm/md/lg/xl/xxl/fluid (são os tipos de container)

No bootstrap só podemos ter 12 colunas máximo por row




