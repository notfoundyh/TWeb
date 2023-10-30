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

