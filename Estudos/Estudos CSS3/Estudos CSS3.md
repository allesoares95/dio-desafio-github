# ESTUDOS CSS3 

No módulo de HTML descobrimos que podemos adicionar CSS de duas formas, com o elemento *style*, e assim suas regras ficarão no arquivo HTML, ou podemos criar um arquivo CSS e adicioná-lo na página através do elemento *link* 



- **Box-model**

  Quando estamos criando o layout de um site o navegador representa cada elemento HTML como uma caixa retangular, isso é o box-model. E com CSS nós alteramos a aparência dessa caixa (largura, altura, cor de fundo, etc.). Essa caixa é composta por 4 áreas: o conteúdo, o padding, a borda e a margem.

  - As margens (margin) são espaçamentos entre elementos;
  - As bordas (border) ;
  - O padding é um espaçamento entre as bordas e o conteúdo, a diferença para as margens é que declarações de imagem de fundo funcionam nele;
  - O conteúdo (content) é o que o seu bloco representa, um texto, uma imagem, um vídeo;

  

  # Padding e Margin 

  

  - A primeira é colocando um valor para as partes superior e inferior e depois para os lados esquerdo e direito.

    O valor de 10 *pixels* se refere ao eixo Y, ou partes superior e inferior, e os 5 *pixels* se referem aos lados esquerdo e direito.

    A segunda forma é dando valores para cada lado do *box*.

    Então começamos pelo topo com 15 pixels, passamos o lado direito com 10 pixels, depois para a parte inferior com 5 pixels e por último o lado esquerdo com 0, e sempre nessa ordem.

    Uma boa dica também é que quando o valor for 0 não precisamos não precisamos colocar a unidade.

  Essa opção é mais usada quando temos o mesmo valor para 3 lados, e o quarto precisa ter um valor diferente, então usamos o padding com apenas um valor e uma dessas opções para representar o lado diferente.



- Pode usar também a formula que você coloca o tamanho especifico para cada lado .

  

​		. post {

​			padding-top: 15px;

​			padding-right: 10px ;

​			padding-bottom: 5px ;

​			padding-left: 0 ;

}



Serve para colocar separadamente cada ''**px**''.



	# Background



A opção Background pode ser usada para mudar a cor de fundo, colocar uma imagem ou alterar posicionamento dessa imagem.

Tem 3 formas de colocar uma cor de fundo e outras.

A primeira é pelo nome da cor em inglês, a segunda é pelo código hexadecimal e a terceira é usando apenas o atalho *background*.



.post {

​	background-color: 	green;	**"Usando nome em inglês"**

​	background-color: 	#008800;	**"Código Hexadecimal"**

​	background:	#008800;	**"Atalho background"**

}





# Border



Vimos que a propriedade *border* pode ter 3 valores: a largura, a cor e o estilo.

A largura pode ser usada com várias unidades, como px, em e mm. Assim como **background**, a  cor pode ser atribuída pelo nome ou por um código hexadecimal.



**Ex :** 	.post {

​	border: 3px solid blue;

​	border-top: 2px dotted green;

​	border-right:4px dashed pink;

}



**Ex 2 :** Como separar cada borda .

​	.post {

​		border-top: 2px dotted green;

​		border-right:4px dashed pink;

​		border-bottom:1px solid purple;

​		border-left: 4px dotted cyan;

}

Em cada uma delas usamos o valor como largura, estilo e cor.

Ce você não quiser o **Border** você pode utilizar as propriedades especificas para cada lado das bordas.



**border-width:** Para largura.

**border-color:** Cor.

**border-style**: Para o contorno da borda.



# Border-radius

E a última propriedade é o *border-radius*, ele permite arredondar os cantos de um elemento. Podemos usar várias unidades, mas as mais comuns são os pixels e a porcentagem.

Colocando apenas um valor mudamos todos os cantos do elemento, mas seguindo aquela mesma ordem que vimos no *padding* e *margin* - topo, direita, inferior e esquerda - conseguimos alterar cada canto separadamente.



###  font-family

Com o font-family podemos alterar a fonte dos nossos textos, como uma fonte da internet ou uma que esteja instalada no nosso computador, mas vamos nos ater às fontes seguras, chamadas de web safe fonts.

Essas fontes são chamadas assim pois são encontradas em quases todos os sistemas e podem ser usadas sem preocupação.

 

#title {

​	font-family: Verdana;

}



.post_title {

​	font-family: Verdana, Arial;

}





### font-size

O font-size nos ajuda a mudar o tamanho do texto, existem algumas unidades de medida para ele mas por enquanto os pixels são suficientes para nós.

 

#title {

​	font-style: normal;

}



.subtitle {

​	font-style: italic;

}





### font-style

Usamos o font-style para tornar um texto itálico, na maioria das vezes você usará apenas o valor *italic* para ele, mas se precisar tirar o itálico de um texto você pode usar o valor *normal*.

#title {

​	font-weight: normal;

}



.subtitle {

​	font-weight: bold;   	**( bold = Negrito )**

}



# Text- Transform 

Altera o texto entre maiúscula e minúscula.

- O valor **uppercase**; coloca todo o texto em caixa alta.

- O valor **lowercase**; coloca todo o texto em caixa baixa. 

- O valor **capitalize**; coloca todas as primeiras letras de cada palavra em Maiúscula.



#title {

​	text-transform: uppercase;

}



.subtitle {

​	text-transform:lowercase;

}



.post-title{

​	text-transform:capitalize;

}



# Text-decoration

- **underline**; para dar destaque em algum texto pois ele coloca linhas, coloca uma linha abaixo da palavra.
- **overline**;  coloca uma linha acima da palavra .
- **line-through**; coloca uma linha ao centro cortando essa palavra .



#title {

​	text-decoration: underline;

}





.subtitle {

​	text-decoration:overline;

}



.post_title {

​	text-decoration: line-through;

}



# list-style-type



Para alterar o marcador das lista usamos o **list-style-type** .



*EX 1:* list-style-type para uma lista não ordenada, alterando o simbolo para um quadrado.



ul {

​	list-style-type: square;

}



*Ex 2:* Alterando um marcador para uma lista ordenada, para um algoritmo romano maiúsculo.

ol {

​	list-style-type: upper-roman;

}



*Ex 3:* Alterando um marcador de uma lista não oredenada, para um simbolo **"\1F44D"** = um emoji de uma joinha.

ul {

​	list-style-type: "\1F44D" ;

}





# list-style-image



Pode ser usado para adicionar uma imagem tambem.



ul {

​	list-style-image: url("imagem.png")

}



