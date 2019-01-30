---
title: "Word Embedding"
output: 
  html_document:
    keep_md: true
author: Sayuri Takeda 
---

## Word Embedding

Técnica de NLP onde palavras são mapeadas para vetores.

É dificil representar a ideia de <span style="color:#ff3300">contexto</span>. Também existe uma limitação em representar palavras <span style="color:#ff3300">idiomáticas</span>.

Exemplo de palavra idiomática:

![](/README-unnamed-chunk-2-1.png)<!-- -->

Duas possíveis **aplicações** de word embedding podem ser:

+ extrair contexto de uma palavra em um documento
+ determinar relação com outras palavras

## Futuro com Word Embedding...

Facebook AI Research (FAIR)
</br>
</br>
<center><img src="/futuro.PNG" width="690" height = "250"></center>

## One Hot Encoding

É possível representar palavras de um determinado vocabulário utilizando one hot encoding, vamos ilustrar um exemplo:

+ O TAP é bom
+ O TAP é ótimo

Vocabulário ={"O", "TAP", "é", "bom", "ótimo"}

Representando o vocabulário por one hot encoding:

+ O -> (1,0,0,0,0)
+ TAP -> (0,1,0,0,0)
+ é -> (0,0,1,0,0)
+ bom -> (0,0,0,1,0)
+ ótimo -> (0,0,0,0,1)

## Continuação One Hot Encoding

Sabemos que, dentro do contexto, <span style="color:#ff3300">**"bom"**</span> deveria ser próximo de <span style="color:#ff3300">**"ótimo"**</span>.

<center><img src="/formulas.PNG"></center>

## Função Softmax

Softmax pega um vetor não normalizado e retorna um vetor normalizado baseado em uma distribuição de <span style="color:#ff3300">probabilidade</span>.

<center><img src="/CodeCogsEqn.PNG"></center>
</br>
</br>
<center><img src="/ex_sofmax.PNG"></center>

## Word2vec

A forma mais popular de se trabalhar com word embedding é o word2vec que utiliza rede neural e foi criado por Thomas Mikolov da Google.
</br>
</br>
</br>
<center><img src="/Thomas.PNG"></center>

## Continuação Word2vec

<center><img src="/formulas_2.PNG"></center>

## 

Não existe função de ativação com sigmoide, than ou relu:

<center><img src="/functions.PNG"></center>

## Exemplo da rede

Modelo CBOW simples com apenas uma palavra do contexto.

<center><img src="/simple-CBOW.png"></center>

## Modelo CBOW 

<center><img src="/CBOW.png"></center>

## Modelo Skip-gram 

<center><img src="/Skip-Gram.png"></center>


## CBOW X Skip-gram 

![](/README-unnamed-chunk-3-1.png)<!-- -->


## Skip-gram 

Tenta predizer o vizinho, esse é o "contexto", por exemplo:

<center><img src="/france.PNG"></center>

## Melhorias Skip-gram 

</br>
</br>
Duas inovações que foram feitas em um segundo paper que aumentam a <span style="color:#ff3300">qualidade do resultado</span> e reduz o <span style="color:#ff3300">esforço computacional</span>:

+ Subamostra de palavras frequentes 
+ Amostra negativa 

## Continuação Skip-gram 

![](/README-unnamed-chunk-4-1.png)<!-- -->


## Opinion

</br>
<center>
<table>
<tr>
<td><img src="/opinion.PNG"></td>
</tr>
</table>
</center>

## Ideia de output:

</br>
</br>
</br>
<center>
<table>
<tr>
<td><img src="\Capture_7.PNG"></td>
<td><img src="\Capture_8.PNG"></td>
</tr>
</table>
</center>

## Ideia de output:

<center>
<table>
<tr>
<td><img src="\Capture_9.PNG"></td>
<td><img src="\Capture_10.PNG"></td>
</tr>
</table>
</center>

<center><img src="\Capture_11.PNG" width="300" height="300"></center>

## Prática

<center><img src="/jupyter.PNG" width="500" height="250"></center>
</br>
<center>
<table>
<tr>
<td><img src="/gensim.PNG" width="350" height="140"></td>
<td><img src="/bokeh.PNG" width="280" height="140"></td>
</tr>
</table>
</center>

