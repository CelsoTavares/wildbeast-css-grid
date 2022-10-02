# Wildbeast-css-grid
#### Estudo e criação de [site](https://celsotavares.github.io/Wildbeast-css-grid/) usando css grid com a Origamid.
## Grid Container
O Grid Container é a tag que envolve os itens do grid, ao indicar display: grid, essa tag passa a ser um Grid Container.
<hr>

* ### display

display: grid;
Torna o elemento um grid container.

display: inline-grid;
Torna o elemento um grid container porém com comportamento inline.

display: subgrid;
Para grids dentro de grids (ainda não é suportado, porém você pode normalmente colocar display: grid; no grid dentro do grid que funciona).
<hr>

* ### grid-template-columns

grid-template-columns: 100px 100px 100px 100px;
Quatro colunas de 100px de largura são criadas

grid-template-columns: 1fr 2fr;
Duas colunas são criadas, sendo a segunda com o dobro do tamanho da primeira. fr é uma unidade fracional. O tamanho do conteúdo é respeitado, ou seja, se o conteúdo na primeira coluna for maior que o da segunda, a primeira será maior.

grid-template-columns: minmax(200px, 1fr) 1fr 1fr;
Três colunas são criadas, a primeira terá no mínimo 200px de largura e no máximo 1fr(isso significa que após 200px ela se expande da mesma forma que as outras colunas). As outras duas colunas vão ter 1fr.

grid-template-columns: repeat(3, 1fr);
Cria 3 colunas com 1fr de tamanho. O repeat seria a mesma coisa que escrever 1fr 1fr 1fr.

grid-template-columns: repeat(auto-fit, minmax(100px, auto));
Cria automaticamente um total de colunas que acomode itens com no mínimo 100px de largura.
<hr>

* ### grid-template-rows

grid-template-rows: 50px 100px 50px 150px;
Cria 4 linhas no grid, sendo a primeira com 50px, segunda 100px, terceira 50px e quarta 150px. Caso o grid necessite de mais linhas, elas terão o tamanho de acordo com o conteúdo.

grid-template-rows: 1fr 2fr;
Cria 2 linhas no grid, sendo a segunda com cerca de duas vezes o tamanho da primeira.
<hr>

* ### grid-template-areas

grid-template-areas:

"logo nav nav"

"sidenav content advert"

"sidenav footer footer";

Cria 3 colunas e 3 linhas. 
logo ocupa a coluna 1, linha 1.
nav ocupa coluna 2 a 3, linha 1.
sidenav ocupa colina 2, da linha 2 e 3.
content ocupa a coluna 2, linha 2.
advert ocupa a coluna 3, linha 2.
footer ocupa da coluna 2 a 3, linha 3.
<hr>

* ### grid-template

grid-template:

"logo nav nav" 50px

"sidenav content advert" 150px

"sidenav footer footer" 100px
100px 1fr 50px;
 
 A primeira linha com 50px, segunda com 150px e terceira com 100px. A primeira coluna com 100px, a segunda 1fr e a terceira com 50px.
 <hr>
 
 * ### gap
 
 gap: 20px

Define 20px entre os elementos do grid (linha e coluna).
column-gap: 20px

Define 20px de distância entre as colunas.

row-gap: 20px
Define 20px de distância entre as linhas
<hr>

 * ### grid-auto-columns
 
grid-auto-columns: 100px
As colunas implícitas, geradas automaticamente, terão 100px de largura.
<hr>

 * ### grid-auto-rows
 
grid-auto-rows: 100px
As linhas implícitas, geradas automaticamente, terão 100px de altura.
<hr>

* ### grid-auto-flow

grid-auto-flow: row
Automaticamente gera novas linhas.

grid-auto-flow: column
Automaticamente gera novas colunas.

grid-auto-flow: dense
Tenta posicionar o máximo dos elementos que existirem nas primeiras partes do grid (pode desorganizar o conteúdo).
<hr>

* ### grid

grid: 100px / 1fr 1fr
Gera uma linha com 100px de altura e 2 colunas com 1fr.

grid: 100px / auto-flow 100px 50px
Gera uma linha com 100px de altura. O grid-auto-flow é definido como column (pois está logo antes da definição das colunas). Ele também define o grid-auto-columns com 100px 50px
<hr>

* ### justify-content

justify-content: start
Justifica os itens ao início.

justify-content: end
Justifica os itens ao final.

justify-content: stretch
Estica os itens.

justify-content: space-around
Distribui espaço entre os elementos. (O início e final são menores que os espaços internos).

justify-content: space-between
Cria um espaço entre os elementos, ignorando o início e final.

justify-content: space-evenly
Cria um espaço igual entre as colunas (no início e final também).

justify-content: center
Centraliza o conteúdo.
<hr>

* ### align-content

align-content: start
Alinha os itens ao início.

align-content: end
Alinha os itens ao final.

align-content: stretch
Estica os itens.

align-content: space-around
Distribui espaço entre os elementos. (O início e final são menores que os espaços internos).

align-content: space-between
Cria um espaço entre os elementos, ignorando o início e final.

align-content: space-evenly
Cria um espaço igual entre as colunas (no início e final também).

align-content: center
Centraliza o conteúdo.
<hr>

* ### justify-items

justify-items: start
Justifica os itens ao início.

justify-items: end
Justifica os itens ao final.

justify-items: center
Centraliza o conteúdo.

justify-items: stretch
Estica os itens.
<hr>

* ### align-items

align-items: start
Alinha os itens ao início.

align-items: end
Alinha os itens ao final.

align-items: center
Centraliza o conteúdo.

align-items: stretch
Estica os itens.
<hr>

##  Grid Item
Os Grid Itens são os filhos diretos do Grid Container. Um grid item pode ser explicito ou implícito. Explicito é quanto você define ele explicitamente no container e implícito é quanto ele é criado automaticamente para preencher o conteúdo no grid.

* ### grid-column

grid-column: 1
O item ocupará a coluna 1.

grid-column: 1 / 3
O item ocupará a coluna 1 e 2 (Sim, isso mesmo, 1 e 2, pois os valores 1 / 3 são referentes as linhas da coluna. Isso significa que começa na linha 1 (início do grid) e vai até a linha 3, que é o começo da terceira coluna).

grid-column-start: 2
O item vai começar na linha 2.

grid-column-end: 4
O item vai terminar na linha 4.

grid-column: span 2
O item irá ocupar duas colunas a partir de onde ele estiver.
<hr>

* ### grid-row

grid-row: 1
O item ocupará a linha 1.

grid-row: 1 / 3
O item ocupará a linha 1 e 2 (Sim, isso mesmo, 1 e 2, pois os valores 1 / 3 são referentes as linhas do grid. Isso significa que começa na linha 1 (início do grid) e vai até a linha 3 do grid, que é o começo da terceira linha).

grid-row-start: 2
O item vai começar na linha do grid 2.

grid-row-end: 4
O item vai terminar na linha do grid 4.

grid-row: span 2
O item irá ocupar duas linhas a partir de onde ele estiver.
<hr>

* ### grid-area

grid-area: 1 / 2 / 4 / 3;
Este é um atalho para:

grid-row-start: 1;

grid-column-start: 2;

grid-row-end: 4;

grid-column-end: 3;

grid-area: header;
Vai posicionar o item na área definida como header.
<hr>

* ### justify-self

justify-self: start
Justifica o item ao início.

justify-self: end
Justifica o item ao final.

justify-self: center
Centraliza o conteúdo.

justify-self: stretch
Estica o item.
<hr>

* ### align-self

align-self: start
Alinha o item ao início.

align-self: end
Alinha o item ao final.

align-self: center
Centraliza o conteúdo.

align-self: stretch
// Estica o item.






 
