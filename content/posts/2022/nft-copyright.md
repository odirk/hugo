---
title: "NFTs generativas podem ter um problema de direitos autorais"
date: "2022-05-25"
tags: ["tech"]
description: "oh no another law post"
author: "gabriel"
showToc: true
TocOpen: true
draft: false
---

A maioria das coisas que leio sobre NFTs costuma se concentrar em dois tópicos: quais direitos o comprador adquire ao adquirir um token e a questão da violação de direitos autorais. Mas eu ando pensando que talvez um dos assuntos mais interessantes esteja passando relativamente despercebido, que é o fato de que muitos **NFTs podem nem estar protegidos por direitos autorais em primeiro lugar**.

No momento, a maior parte do mercado de NFTs está em itens colecionáveis, especificamente em Colecionáveis de Foto de Perfil (CFP), como [Bored Apes](https://en.wikipedia.org/wiki/Bored_Ape), [CryptoPunks](https://en.wikipedia.org/wiki/CryptoPunks), etc. Eles tendem a ser personagens com traços gerais similares, mas cada token proporciona um conjunto de características únicas, como cabelo, óculos, chapéus, roupas, plano de fundo, etc.

Normalmente, qualquer obra de arte usada para a criação de um NFT terá direitos autorais se atender ao requisito de proteção, ou seja, deve ser uma obra artística original. Originalidade, nesse caso, tem um significado diferente do uso comum, significa que a obra é uma criação intelectual que **reflete a personalidade do autor**. É neste ponto que muitos projetos de CFP podem ficar aquém da proteção legal, porque em muitos casos esses projetos são criados automaticamente em um processo que é conhecido como **arte generativa**. Há muito pouca intervenção humana e a imagem final é um resultado aleatório de um código.

Vamos usar os Bored Apes para ilustrar o ponto. Este projeto é composto por uma imagem de base, com oito categorias que totalizam 175 características disponíveis. 

Essa imagem é então embelezada com uma série de adornos, alguns mais raros que outros, que muitas vezes fazem parte da escassez que dá valor à imagem resultante. Há chapéus, roupas, brincos, planos de fundo, etc.

{{< figure align=center src="/nft-copyright/traits.png" >}}

Cada imagem na coleção (10.000 no total) é gerada por algoritmos para ter uma combinação única de características, com uma distribuição de raridade para algumas das características para aumentar seu valor. Você pode conferir a lista [nesse site](https://raritysniper.com/bored-ape-yacht-club/traits).

Aqui é onde os projetos têm uma escolha. Eles podem gerar as imagens antes de criar os tokens ou podem colocar um pouco de emoção à própria criação, e gerar a imagem somente quando alguém compra um NFT, assim não se sabe de antemão quais características receberão. O que é comum na maioria dos projetos é que a imagem resultante será gerada aleatoriamente com a mistura de características pré-determinadas, e esse resultado é então transformado em um NFT.

A maioria dessas etapas não requer nenhuma intervenção humana além da criação artística do personagem base e dos adornos, que são aleatoriamente escolhidos.

O processo generativo é tão difundido que existem tutoriais online que ensinam as pessoas como ter CFP generativas em menos de 15 minutos, [a maior parte do código é aberto e facilmente acessível](https://whiteboardcrypto.com/python-nft-generative-art-code/). Há até mesmo obras que podem ser reutilizadas por um projeto. Não sabe programar? Não se preocupe, [também existem geradores online para isso](https://www.bueno.art/)! Não encontrei um número preciso de quantos projetos usam código generativo, mas certamente os maiores nomes em NFT colecionáveis geram suas fotos reunindo um personagem-base com adornos através de um código.

É essa combinação que pode ser problemática do ponto de vista dos direitos autorais. É necessária alguma originalidade e/ou criatividade para que os direitos autorais existam. Caso contrário, todas imagens estarão em domínio público e poderão ser usadas à vontade por qualquer pessoa (talvez com a exceção do primeiro personagem-base). 

---

> "Mas, dirk, e não existem direitos autorais na imagem de base? E possivelmente nos vários adereços adicionais à ela? Alguém desenhou esse chapéu, óculos de sol, etc."

Em princípio cada um dos elementos podem ser individualmente protegidos, mas as coisas ficam complicadas ao juntá-los através de código. Dependendo da jurisdição, essas obras derivadas não terão direitos autorais por falta de originalidade. Às vezes você pode pegar elementos protegidos e o resultado da combinação não necessariamente será protegido.

---

Essa é geralmente uma área do direito que tem estado em alta nos últimos anos devido ao aumento de trabalhos gerados por Inteligência Artificial. No entanto, no caso de CFPs generativos **não há inteligência artificial envolvida**, estamos falando de um código raso que é facilmente implantado. É apenas um algoritmo simples que reúne personagem-base e adornos, mas é um processo automatizado e aleatório.

Essa matéria é totalmente dependente da jurisdição. Há um bom argumento a ser feito de que a arte generativa de CFP tem proteção de direitos autorais no Reino Unido sob o (controverso) [s9(3) do CDPA](https://www.legislation.gov.uk/ukpga/1988/48/section/9), que afirma que o autor de um trabalho gerado por computador é a pessoa que fez os arranjos necessários para que o trabalho fosse criado. Isso significaria que quem escrevesse o código para gerar as imagens seria o autor. Disposição semelhante existe em alguns outros países de common law.

No droit d’auteur, vertente adotada pelo Brasil e maior parte da Europa, é geralmente entendido que, para que haja direitos autorais em uma obra, ela precisa ser uma criação intelectual que reflita a personalidade do autor. Por isso, pode-se argumentar que apenas codificar um algoritmo para gerar milhares de imagens pode não cumrprir esse requisito. Tudo vai depender se escrever o código, desenhar a arte do personagem-padrão e dos adornos é suficiente para provar a existência de um processo intelectual que deu origem às obras.

Muitos projetos que estão sendo desenvolvidos nos Estados Unidos, e estamos começando a ver também questões sobre se as coleções generativas de CFP têm direitos autorais. Recentemente, o [US Copyright Office recusou](https://www.copyright.gov/rulings-filings/review-board/docs/a-recent-entrance-to-paradise.pdf) um pedido do Dr. Stephen Thaler (o mesmo do [caso DABUS](https://www.bailii.org/ew/cases/EWCA/Civ/2021/1374.html)) para registro de um trabalho gerado usando um agente de inteligência artificial chamado “Creativity Machine”. O registro foi negado porque os autores têm que ser humanos, a decisão foi apelada, e o Conselho de Revisão negou o recurso afirmando que “a autoria humana é um pré-requisito para a proteção de direitos autorais nos Estados Unidos e que a obra, portanto, não pode ser registrada."

{{< figure align=center src="/nft-copyright/thaler.png" title="'A Recent Entrance to Paradise', a obra em questão." >}}

Essa decisão pode ter consequências importantes para os NFTs, principalmente aqueles baseados em personagens generativos. Há pouca interação humana na geração de cada imagem final, eles são uma combinação algorítmica. Se interpretarmos a decisão do US Copyright Office de forma restrita, essas imagens não têm direitos autorais e são de domínio público.

A decisão me parece correta, inclusive à luz do direito internacional.

Embora a Convenção de Berna não defina quem pode ser considerado autor, a partir de seu texto e contexto histórico, parece que apenas pessoas físicas que criaram a obra podem ser consideradas autores. Em particular, apesar da Convencão não estabelecer explicitamente um requisito de originalidade, isso já existia nas leis nacionais de direitos autorais no momento da redação da Convenção. [De acordo com Ricketson](https://heinonline.org/HOL/LandingPage?handle=hein.journals/cjla16&div=8&id=&page=), ficou claramente entendido que este também era um requisito para os fins de proteção da Convenção, e inerente à frase "obras literárias e artísticas" no artigo 2º. A condição de que uma obra possua suficiente grau de originalidade requer "a necessidade de o autor ser um ser humano e de haver alguma contribuição intelectual além do simples esforço ([suor da testa](https://en.wikipedia.org/wiki/Sweat_of_the_brow)) ou o que pode ser chamado de mero *valor de troca*”.

Analisando a autoria do ponto de vista da UE, o artigo 1(5) da [Diretiva Sat-Cab](https://eur-lex.europa.eu/legal-content/EN/ALL/?uri=celex%3A31993L0083) estabelece que, para obras cinematográficas ou audiovisuais, o realizador principal será considerado o seu autor ou um dos seus autores, permitindo que os Estados-Membros considerem outros como co-autores. O artigo 2(1), da [Diretiva de Softwares](https://eur-lex.europa.eu/legal-content/EN/ALL/?uri=CELEX%3A32009L0024) prevê que o autor de um programa de computador seja a pessoa natural, ou grupo de pessoas, que criou o programa ou, se a legislação do Estado-Membro permitir, uma pessoa jurídica designada como titular do direito por essa legislação. Igualmente, o artigo 4(1), da [Diretiva de Banco de Dados](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=CELEX:31996L0009:EN:HTML) admite a possibilidade semelhante.

De qualquer forma, a [Diretiva de Prazos](https://eur-lex.europa.eu/legal-content/EN/ALL/?uri=CELEX%3A32006L0116) refere o cálculo do prazo de proteção dos direitos autorais à vida dos autores como pessoas naturais. Além disso, o preâmbulo da [Diretiva DSM](https://eur-lex.europa.eu/eli/dir/2019/790/oj) especifica que os autores e intérpretes que poderão invocar as disposições dos seus contratos apenas devem ser pessoas naturais, excluindo assim do âmbito de aplicação os autores e intérpretes não humanos.

A Corte de Justiça da União Europeia ainda não abordou especificamente a questão de quem ou o que é um autor. No entanto, parece que sua própria compreensão de originalidade – como uma noção que pressupõe um **toque pessoal** ([Painer](https://curia.europa.eu/juris/liste.jsf?&num=C-145/10)) e a realização de **escolhas livres e criativas** (mais recentemente, [Brompton](https://curia.europa.eu/juris/liste.jsf?num=C-833/18)) – é, de fato, baseada na ideia de que os autores de direitos autorais precisam ser humanos.

No Brasil, a solução é ainda mais simples. O autor não pode ser outro senão o criador da obra intelectual, ou seja, a “pessoa física” (art. 11, [LDA](http://www.planalto.gov.br/ccivil_03/Leis/L9610.htm)). A titularidade originária de direito autoral por pessoa jurídica somente quando ela a for organizadora de obra coletiva (art. 17, §2º, LDA), que não se aplica nesse caso.

Qual seria a consequência para os NFTs? Na prática, nada de muito relevante. Nunca me canso de repetir que um NFT é apenas um código que se vincula a um ativo digital, não é próprio ativo. Portanto, o proprietário de um NFT não é o proprietário da imagem subjacente. Assim, mesmo que essa imagem seja de domínio público, o proprietário da NFT ainda é dono do token.

A consequência pode ser que, se todos esses milhares e milhares de fotos de perfil não tiverem direitos autorais, qualquer um pode fazer o que quiser com elas, você pode imprimi-las, colocá-las em camisetas e até mesmo criar suas próprias NFTs dessas imagens sem infringir nenhum direito autoral. Projetos de sucesso como o Bored Apes ainda podem proteger sua propriedade industrial através do registro de marcas, mas as imagens em si seriam de domínio público e podem ser reutilizadas pelo público como acharem melhor.

Tenho certeza de que essa revelação não terá nenhum efeito no mercado de NFTs, já é uma bolha onde links para imagens custam milhões de dólares, então o fato de as imagens serem de domínio público pode não mudar o tratamento irracional das pessoas aos tokens. Além disso, o direito autoral ainda tem pouca relevância nesse espaço. Mas isso pode mudar quando um litígio surgisse ([Seth Green, estou olhando para você](https://web3isgoinggreat.com/?id=four-pricey-nfts-stolen-from)), posso ver a argumentação um caso de infração de que as imagens em uma disputa estão em domínio público. É o que eu faria.