---
title: "Sobre redesign do Spotify"
date: "2021-06-16"
tags: ["tech"]
description: "Because new isn't always better"
showToc: false
TocOpen: false
draft: true
---

*sigh*

Por que, Spotify? Por que?

Quem liderou esse novo projeto de interface merece um prêmio. Remover funcionalidades e aumentar o número de cliques para realizar ações comuns é vergonhoso.

Conseguiram transformar um software que não era bom em ruim.

&nbsp;
&nbsp;

## 13 Reasons Why

### 1. Por que esconder os álbuns?

Antigamente os álbuns eram um botão fixo no menu de navegação à esquerda. Bastava um clique para ir para lá.

Agora você deve primeiro clicar em Your Library (primeiro clique) e depois clicar em "Albums" (segundo clique). 

Soa total como *problema de primeiro mundo*, mas se você tem o hábito de ouvir primariamente álbuns (como eu), é um saco ser obrigado a clicar o dobro das vezes para fazer a mesma coisa. 

> É um aumento de 100% de cliques :woozy_face:

Solução: tragam os álbuns de volta para o menu (d'oh). Ou permitam que o usuário possa editar o menu de navegação para colocar seus artistas/álbuns/podcasts que desejem ter à mão.

&nbsp;
&nbsp;

### 2. Por que diabos os álbuns não ficam salvos no cache do programa?

Antigamente todos os álbuns eram carregados instantaneamente. E, se você usasse o atalho Cmd/Ctrl + End, você iria para o final da lista. Fim.

Agora apenas os primeiros 50 álbuns são carregados. Quando você rola a página para baixo, os próximos 50 serão carregados (mas apenas se você chegar ao final dos primeiros 50). 

Dependendo do número de álbuns salvos, quando você está rolando para baixo usando a roda do mouse, a UX é prejudicada porque o programa leva frações de segundo para carregar o próximo lote de álbuns. Agora imagine quando você tem centenas de álbuns na biblioteca. 

Além do mais, como apenas 50 álbuns são carregados de cada vez, eu não posso arrastar a barra de rolagem para a letra inicial que eu gostaria de ir (diferentemente da versão mobile). 

E o pior, como a listagem dos álbuns não fica salva no cache, toda vez que eu reabro os álbuns, eu sou obrigado a me arrastar por toda biblioteca novamente. Que inferno.

```
Update:
Yay! Eles consertaram isso!
```

&nbsp;
&nbsp;

### 3. O Spotify não lembra de onde você saiu das páginas

Quando saio de uma playlist/álbum que estou ouvindo no momento, vou para outra página e depois volto, ela me envia para o topo da playlist/álbum, não onde eu não estava quando saí.

Uma funcionalidade tão simples, mas faz toda a diferença em playlists grandes.

```
Update: Consertado!
```

&nbsp;
&nbsp;

### 4. Sem barra de pesquisa persistente

POR QUE A BARRA DE PESQUISA ESTÁ ESCONDIDA ATRÁS DE UM CLIQUE?

```Felizmente o Cmd/Ctrl + L ainda funciona.```

&nbsp;
&nbsp;

### 5. Não consigo ver quando novos álbuns/singles foram lançados

No design anterior, você podia ver isso no topo da página do artista na seção Latest Release. 

Agora está na seção Discografia, e só clicando nele você vê o ano de lançamento.

&nbsp;
&nbsp;

### 6. Por que unir o título da música e o artista em uma coluna? 

Enquanto mantém o álbum, a data adicionada e a duração da música em colunas exclusivas. 

Isso confunde. As colunas devem ser: título da música, artista, álbum, duração e data adicionada.

&nbsp;
&nbsp;

### 7. Os espaçamentos das colunas são mal distribuídos

Por que dar a mesma quantidade de espaço na tela ao Álbum e à Data Adicionada quanto ao título da música?

O título tende a ser o item mais comprido. Por isso, ele frequentemente fica cortado e você não pode passar o mouse sobre ele para revelar o título completo.

{{< figure align=center src="/spotify/introspective.png" >}}

&nbsp;
&nbsp;

### 8. Todas páginas são feias

Eu odeio os retângulos pretos altos enormes que eles colocam ao redor das imagens nas páginas dos artistas, playlists, meu perfil, etc. 

Ocupam metade da tela e são feios de doer. Parece que eles estão tentando esconder as músicas.

&nbsp;
&nbsp;

### 9. Clicar no meu perfil no canto superior direito me leva a um menu

Deveria me levar direto ao perfil.

Acho que mais apropriado trocar o botão de perfil por uma :gear:, já que o menu oferece opções de conta, configurações, etc.

&nbsp;
&nbsp;

### 10. Não entendo o Find More na parte inferior de uma playlist

Quando você clica, uma barra de pesquisa é exibida? 

{{< figure align=center src="/spotify/find-more.png" >}}

&nbsp;
&nbsp;

### 11. O Friend Activity possui informações repetidas

O ponto azul na parte superior dos perfis na barra do Friend Activity e o ícone de escuta ativa após o nome são redundantes. 

Além disso, as barras estáticas são menos interessantes do que os alto-falantes animados.

&nbsp;
&nbsp;

### 12. Eles não sabem o que fazer com o Friend Activity (?)

Eles condensaram o título da música e o artista na mesma linha no feed da atividade, **o que torna difícil de ler**, só para que mais pessoas apareçam na lista. 

Por que? Não é como se o Spotify fosse realmente uma rede social.

O Friend Activity nada mais é que um BBB das pessoas que você segue.

É uma função com tantas oportunidades perdidas.

Por que não implementar mensagens/reações para interagir com os seguidores?

Por que eu não posso sabem quem segue as minhas playlists?

Por que eu não posso bloquear usuários da minha conta?

Então por que dificultar a leitura do feed condensando as informações?

E como eles ousam colocar a título da música antes do artista!! Que sacrilégio.

No fim, esse feed "informativo" é pouco explorado e acaba meio sem propósito, meio que um apêndice do serviço.

&nbsp;
&nbsp;

### 13. Eu não gosto de como eles apresentam as músicas dentro de um álbum

Eu meio que gosto que eles incluam o número mais concreto de execuções, mas ao mesmo tempo eu não me importo? 

As barras de popularidade eram muito mais elegantes (e poderiam mostrar o número exato se você pairasse o mouse sobre ela).

&nbsp;
&nbsp;

## O que vou fazer agora

Sei lá, cara.

Fiquei bem decepcionado com as mudanças, tanto que estou ouvindo bem menos música do que antigamente.

O que é ótimo para o Spotify, que continua recebendo minha mensalidade e paga menos royalties para os artistas. ~~Seria isso proposital?~~

Sendo bem sincero, eu considero deixar o serviço e ir do [Apple Music](https://music.apple.com/br/). O catálogo de músicas é parecido, o valor mensal é até um pouco mais baixo (R$ 16,90), e, mais importante, eles transmitem áudio **sem perda de qualidade** ([Lossless](https://www.apple.com/br/newsroom/2021/05/apple-music-announces-spatial-audio-and-lossless-audio/)).

Ainda não bati o martelo nessa decisão, mas é algo bem tentador.

As únicas coisas que ainda me prendem no serviço são o **Spotify Connect** e a integração facilitada com o **Last.fm**, que são duas funções que eu uso bastante. Se a Apple anunciasse funções equivalentes, eu mudaria em um segundo.

Se fosse para ficar no Spotify, eu vejo as seguintes soluções.

Eu cheguei a baixar a última versão do design antigo para fazer um downgrade, mas eu precisaria fazer uns ajustes para que ela fosse permanente (já que o software se atualiza automaticamente :roll_eyes:).

Seria necessário instalar a versão antiga e alterar o chmod dos arquivos para read-only. Nada difícil, só mildly annoying. Assim o Spotify não se atualizaria sozinho (aliás, é um absurdo que não exista a opção para desligar as atualizações automáticas).

Mas, considerando que eles estão forçando essa atualização aos usuários, é bem provável que as versões antigas estejam condenadas a uma obsolescência planejada. Vejo isso como uma solução paliativa.

Outra alternativa que encontrei foi o [**Spicetify**](https://github.com/khanhas/spicetify-cli). 

Ele injeta CSS's para customizar a versão de desktop, além de oferecer umas extensões que corrigem outras reclamações que eu tenho com o Spotify (p. ex. o Shuffle).

Por enquanto estou usando ele. É interessante.

Resolve alguns problemas de design que eu mencionei, mas outros (como a questão do carregamento de álbuns) não.

O tema que eu uso se parece com isso:

{{< figure src="https://raw.githubusercontent.com/morpheusthewhite/spicetify-themes/v2/Dribbblish/nord-dark.png" title="Você pode redimensionar o feed e menu (e customizá-lo)." >}}

O grande senão desse enjambre é que você acaba empilhando uma penca de CSS que ~~vai~~ pode quebrar com qualquer atualização do software original do Spotify, **o que vai lhe levar novamente para a estaca zero**.

*sigh*.

Eu li [o post dos desenvolvedores a respeito da atualização](https://engineering.atspotify.com/2021/04/07/building-the-future-of-our-desktop-apps/) e, do ponto de vista deles, faz sentido integrar os sistemas dos clientes web e desktop.

O problema é que a atualização da versão desktop foi para pior, apesar de ter sido uma preocupação da equipe deles:

```There were risks, of course. Desktop had (and has) many more users than Web Player, and Spotify’s Desktop client is the place most of Spotify’s “power users” call home. We knew we would have a lot of work to do to bring our Web Player up to those power users’ exacting standards.```

Não é à toa que vários usuários estão sugerindo na [página de suporte](https://community.spotify.com/t5/Ideas/ct-p/newideas) a inclusão de várias funcionalidades antigas.

Mas sei lá, eu não estou com altas esperanças delas voltarem.

Se os engenheiros arrumassem os três primeiros itens desse post eu já me daria por satisfeito.

Enquanto isso não acontece, quem sabe eu não vou testando o Apple Music.