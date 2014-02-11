---
layout: post
title:  Por Que Usar Git?
---
**Nota**: essa é a tradução do texto de [Luis Pedro
Coelho](http://luispedro.org/) originalmente publicado
[aqui](http://teaching.software-carpentry.org/2014/01/29/a-motivation-to-learn-version-control/).

Essa é minha história motivacional para utilizar um sistema de controle
de versão.

Alguns anos atrás, subimeti um artigo para algum jornal e ele foi
aceito. Depois de alguns meses pediram para eu enviar a versão final do
artigo.

Para gerar a versão de alta qualidade das minhas figuras executei, mais
uma vez, o script que gerava as figuras mudando apenas alguns parâmetros
de saída para obter a versão de alta qualidade. Entretanto, as figuras
obtidas não pareciam com a que tinha inicialmente submetido! Elas não
estavam diferentes o suficiente para alterar as conclusões, acredite,
mas era possível notar um pequeno deslocamento do gráfico quando
examinados lado-a-lado.

Primeiramente, revisei calmamente o código fonte do script para
verificar se algo óbivio aparecia, então, já preocupado, re-executei o
script agora refazendo todos os passos intermediários, e finalmente
comecei a entrar em pânico. O que estava errado? Teria submetido um
artigo com resultados que eu não sabia como reproduzir?

Como mantinha o script sob controle de versão, retornei ao código da
versão que utilizei na data da submissão. Agora o script gerava as
imagens exatamente como tinha submetido. Que alívio.

Utilizando busca binária (que o [git suporta
nativamente](https://www.kernel.org/pub/software/scm/git/docs/git-bisect.html)),
fui capaz de isolar a parte exata do código que causava a diferença na
imagem. Descobri que uma pequena mudança na forma como algumas contas
eram feitas, elas são matematicamente equivalentes mas não numericamente
(i.e., a figura não teria sido alterada se o computador tivesse uma
precisão infinita, mas como fazemos aproximações obtive resultados
diferentes). Isso significa que uma decisão arbitrária em um ponto do
algoritmo feito de maneira diferente e então o resultado mudou o
suficiente para ser visível.

Então, devido ao controle de versão, fui capaz tando de (1) reproduzir
as figuras nas alta resolução necessária como também (2) entender o
motivo do resultado ter mudado. Isso foi muito gratificante.
