# TWeb
aula 16 outubro

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

cabeçalho <h1> cabeçalho de primeiro nível </h1>

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
