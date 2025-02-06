---
title: "“How to Grow Old” by Bertrand Russell"
date: "2023-01-17"
tags: ["tech", "law"]
# description: "Costumávamos falar sobre a internet na vida real, agora usamos a internet para falar sobre a vida real."
author: "gabriel"
showToc: false
TocOpen: true
draft: true
---

https://www.technollama.co.uk/artists-file-class-action-lawsuit-against-stability-ai-deviantart-and-midjourney

O inevitável finalmente aconteceu, artistas processaram algumas empresas de IA por violação de direitos autorais, bem como um site de repositório de arte (reclamação aqui). Seria esse o fim das ferramentas de IA? Eu acho que não. Vou tentar explicar o motivo, não será uma análise detalhada do processo, essa é minha opinião sobre alguns dos problemas técnicos da ação. Também sei que o processo está em um estágio muito inicial, e que as coisas podem mudar.

# As reclamações

Três artistas estão iniciando uma ação coletiva contra Stability.ai, Midjourney e DeviantArt alegando violação de direitos autorais, violações de DMCA, violação de direitos de publicidade e concorrência desleal. DeviantArt parece ser incluído como punição por “traição de sua comunidade de artistas”, então vou ignorar a parte deles nesta análise por enquanto. Especificamente com relação às reivindicações de direitos autorais, o processo alega que Stability.ai e Midjourney invadiram a Internet para copiar bilhões de obras sem permissão, incluindo obras pertencentes aos reclamantes. Eles alegam que essas obras são armazenadas pelos réus e essas cópias são usadas para produzir obras derivadas.

Este é o cerne do processo. A ação diz de que as imagens produzidas por Stable Diffusion e Midjourney não estão reproduzindo diretamente as obras dos reclamantes, nenhuma prova é apresentada (nem mesmo de uma reprodução aproximada) de uma de suas obras. O que eles afirmam é algo bem extraordinário: “Toda imagem resultante do sistema é derivada exclusivamente das imagens latentes, que são cópias de imagens protegidas por direitos autorais. Por essas razões, toda imagem híbrida é necessariamente uma obra derivada.” :raised_eyebrow: 

Leia isso de novo. Toda imagem resultante é derivada de cada originária, então, seguindo esta lógica, qualquer pessoa inclusa na coleta de dados de cinco bilhões de imagens poderia processar por violação de direitos autorais. 

> Eu tenho algumas imagens nos banco de dados de treinamento, talvez eu deva participar!

O raciocínio é mais ou menos assim: as imagens são extraídas da Internet sem permissão. Essas imagens são copiadas, comprimidas e armazenadas pelos réus, e essas cópias são usadas como uma “ferramenta de colagem moderna” para reunir imagens dos banco de dados de treinamento. Isso ocorre porque as máquinas não podem raciocinar como as pessoas, então é lógico que elas apenas juntam elementos, portanto, todas as imagens resultantes são necessariamente obras derivadas.

# A tecnologia

Acho que o argumento é falho porque não reproduz a tecnologia com precisão, então tentarei fazer uma explicação rápida de como essas ferramentas produzem imagens.

Gosto de classificar o que acontece nas ferramentas geradoras de IA em dois estágios, a **fase de entrada** e a **fase de saída**. 

A **fase de entrada** é composta pela coleta de dados para criar um conjunto de dados, e isso é usado para treinar um modelo. No caso do Stable Diffusion, ele usa um conjunto de dados chamado LAION, que possui mais de 5 bilhões de entradas, consistindo no conjunto de um hiperlink para uma imagem da web (não a imagem em si) com sua descrição de texto ALT. Esse conjunto de dados então é usado para treinar um modelo, não vou entrar em detalhes dos modelos, mas basta dizer que um modelo é uma representação matemática de um processo do mundo real que é treinado usando um conjunto de dados, isso pode ser usado para fazer previsões ou decisões sem ser explicitamente programado para executar a tarefa. Existem vários tipos de modelos, mas Stable Diffusion e Midjourney usam modelos de difusão. Para resumir, os modelos de difusão pegam uma imagem, adicionam ruído a ela e depois a juntam novamente.

Mas o que é o modelo do ponto de vista prático? É um erro comum achar que o modelo de aprendizado de máquina seja apenas um armazenamento de imagens que gera uma colagem, a ação usa a palavra "colagem" repetidamente, portanto, está perpetuando esse mito. É aqui que entra outro modelo, conhecido como CLIP, projetado para melhorar o desempenho dos modelos de IA em uma ampla gama de tarefas que envolvem linguagem e imagens. O modelo é treinado usando um grande conjunto de dados de imagens e suas descrições de texto correspondentes e aprende a entender a relação entre linguagem e imagens. Isso permite que ele execute tarefas como legendas e classificação de imagens com precisão. Assim, as ferramentas de IA usam uma combinação de um modelo de difusão treinado na reconstrução de imagens, bem como o CLIP para entender as palavras usadas para descrever uma imagem.

Há outro elemento muito importante envolvido nos modelos generativos, chamado de "espaço latente". Para treinar um modelo com milhões e, às vezes, bilhões de dados únicos, seria ineficiente tratar todos os dados da mesma maneira, podendo haver agrupamentos (clusters) de trabalhos semelhantes. Se estivermos pensando em imagens, talvez você não precise olhar para todas as fotos de gatos, pode ser suficiente agrupar dados semelhantes. Imagine os dados como uma sala, você colocaria as fotos do gato no mesmo espaço, as fotos do cachorro em outro espaço, etc. O espaço latente é o espaço dos fatores ocultos ou subjacentes que podem explicar os dados observados, agrupando dados semelhantes, é usado em modelos generativos onde o objetivo é aprender uma representação dos dados que pode ser usada para gerar novas amostras semelhantes às do conjunto de treinamento. Isso é muito importante porque ajuda a compactar as entradas, não há necessidade de copiar todas as imagens de gatos, o modelo contém representações latentes de gatos.

A **fase de saída** é a geração da imagem usando todos os modelos acima, e é feita usando aplicativos que podem receber um prompt de texto e gerar uma nova imagem com base em uma combinação de dados estatísticos, modelos de linguagem e espaço latente.

Em outras palavras, isso não é uma colagem.

# Analisando os pedidos

Como vimos acima, há um grande problema em como as coisas são descritas no processo que se chocam com a forma como as coisas funcionam na realidade. A disparidade é que parece haver um grande salto na compreensão entre o treinamento de um modelo e como o modelo armazena esse conhecimento. De acordo com a petição inicial, o Stability.ai pega as imagens no conjunto de dados de treinamento e estas são “armazenadas e incorporadas ao Stable Diffusion como cópias compactadas”. Isso não é o que acontece, um modelo treinado não tem cópias dos dados de treinamento, isso criaria um banco de dados gigante de tamanho insondável. O que ocorre é a criação de clusters de representação das coisas, ou seja, o espaço latente.

O que provavelmente acontecerá durante o julgamento, se chegarmos a isso, com os depoimentos de especialistas, essa alegação provavelmente cairá por terra. Claro, há alguma cópia temporária em algum estágio, é importante lembrar que o LAION também não copia imagens, mas há raspagem (scrapping) de imagens no processo de treinamento, mas estas não são armazenadas no modelo como reivindicado.

Este será um ponto vital, porque a inicial não faz nenhuma alegação de que as saídas são reproduções de qualquer uma das imagens de treinamento pertencentes aos reclamantes.

A outra questão problemática na reclamação é a alegação de que todas as imagens resultantes são necessariamente derivadas dos cinco bilhões de imagens usadas para treinar o modelo. Isso é direito autoral homeopático: qualquer traço de um trabalho nos dados de treinamento resultará em um derivado responsável. É loucura.

# Outras considerações legais

Talvez a maior curiosidade na inicial seja quem falta como réu, em particular dois nomes muito conspícuos: LAION e OpenAI. Acho que o LAION é mais fácil de explicar, é uma organização de pesquisa alemã, e o que eles fazem é coletar hiperlinks e descrições de texto. Acredito que isso se enquadre na exceção de mineração de texto e dados contida na Diretiva DSM da UE. A ausência da OpenAI é mais difícil de explicar. Acho que o principal motivo é que o OpenAI não divulga qual conjunto de dados está usando, portanto, não é muito fácil para um autor provar que foi usado nos dados de treinamento. Como esse processo é inteiramente baseado na fase de entrada, essa informação ausente é vital.

A outra questão é se o processo terá sucesso, e a resposta honesta é que não sei. Não estou impressionado com os erros técnicos descritos acima e acho que isso será uma parte importante da defesa. É provável que os réus reivindiquem fair use, e este caso tem o potencial de ser o caso de teste para saber se o treinamento de uma IA sem permissão pode atender aos requisitos de fair use. Acho que esse processo é uma aposta arriscada para os artistas. Uma derrota finalmente resolveria a questão que ficou em aberto desde o Google Books, e não acho que esse seja o caso mais forte, pelo menos do jeito que está.

# Concluindo

Esta é a crônica de um processo anunciado. Agora que chegou, será analisado infinitamente e derramado durante as próximas semanas, e estou ansioso para ler o que os outros pensam, talvez meu ceticismo se mostre equivocado, veremos. Minha primeira impressão é que isso tem “acordo extrajudicial” escrito por toda parte, mas se não houver acordo, esse processo pode durar anos, pois qualquer resultado provavelmente será apelado.

A guerra contra a IA começou.

---




Esse vai ser um ano agitado! O mesmo escritório que entrarou com a ação coletiva contra o GitHub e a Microsoft sobre o Copilot e Codex alguns meses atrás, entraram com outra ação contra Stability AI, DeviantArt e Midjourney relacionada ao Stable Diffusion. O centro da ação é em torno de Stability AI e seu produto Stable Diffusion, mas Midjourney e DeviantArt entram em cena porque têm produtos que incorporam Stable Diffusion. O DeviantArt também tem algumas reivindicações lançadas diretamente contra eles porque eles permitiram que a Rede Aberta de Inteligência Artificial em Grande Escala (LAION) incorporasse obras de arte enviadas a seu serviço. Como o caso Copilot, as reivindicações incluem:

* Violação das seções 1201-1205 do Digital Millennium Copyright Act (DMCA) relacionadas à remoção de imagens de informações relacionadas a direitos autorais;
* Concorrência desleal, decorrente da lei de direitos autorais e violações do DMCA;
* Quebra de contrato, neste caso relacionado à suposta violação do DeviantArt, de disposições relacionadas a dados pessoais em seus Termos de Serviço e Política de Privacidade.

Ao contrário do caso Copilot, este inclui reivindicações adicionais para:

* Violação direta de direitos autorais para treinar o Stable Diffusion nas imagens da classe, incluindo as imagens no modelo Stable Diffusion, e reproduzir e distribuir trabalhos derivados dessas imagens
* Infração vicária de direitos autorais por permitir que os usuários criem e vendam obras falsas de artistas conhecidos (essencialmente representando os artistas)
* Violação dos direitos estatutários e de direito comum de publicidade relacionados à capacidade da Stable Diffusion de solicitar arte no estilo de um artista específico

# A ação

    Assim como o caso Copilot, este tem falhas potenciais semelhantes na definição da classe. A definição da classe de medida cautelar e da classe de danos na reclamação não condiciona realmente a participação no dano. A classe é definida como todas as pessoas ou entidades com direitos autorais em qualquer trabalho que foi usado para treinar a Stable Diffusion. Mas, simplesmente ter trabalho que faz parte do conjunto de treinamento não significa que o trabalho é 1) realmente parte do modelo, 2) realmente gerado pelo modelo (ou um derivado dele), ou 3) gerado pelo modelo em detalhes suficientes para ainda estar sujeito a direitos autorais. Como no caso do Copilot, a reclamação afirma explicitamente que é difícil ou impossível para os demandantes identificar seu trabalho na produção do Copilot.

    Uma vez que este caso envolve reivindicações de violação de direitos autorais, também é surpreendente que a classe não se limite a pessoas com direitos autorais registrados, mas apenas a pessoas “com interesse em direitos autorais”, já que pessoas que não possuem direitos autorais registrados não podem fazer valer seus direitos autorais no tribunal. Além disso, o litigante Noorjahan Rahman apontou que alguns tribunais também estendem a exigência de registro à aplicação do DMCA, enfraquecendo ainda mais as chances dos demandantes de conseguir definir a classe dessa maneira e/ou trazer reivindicações de direitos autorais ou DMCA como uma ação coletiva.

    Também vale ressaltar que apenas uma fração do conjunto de dados supostamente usado pelo Stable Diffusion originou-se do DeviantArt. Com relação às imagens que vieram do DeviantArt, a questão da violação de direitos autorais deve girar em torno da licença concedida ao DeviantArt em seus Termos de Serviços. Mas o restante do conjunto de dados veio de outras fontes. Alguns deles provavelmente são apenas protegidos por direitos autorais e não estão sujeitos a nenhuma outra licença, alguns deles provavelmente são dedicados ao domínio público, mas o restante deles está sob várias licenças, incluindo várias licenças Creative Commons, licenças comerciais, outras Termos de uso, etc. É claro que os autores de tais trabalhos ainda mantêm direitos autorais sobre eles, mas a questão de saber se o uso dos trabalhos constitui ou não violação de direitos autorais dependerá da licença subjacente. Como provavelmente existe uma cornucópia de licenças subjacentes nesse conjunto de dados, é difícil argumentar que todos os membros da classe realmente compartilham as mesmas questões de direito e fatos.

    Lembre-se de que, no caso do Copilot, a classe relevante estava vinculada às 13 licenças de código aberto disponíveis no menu suspenso do GitHub para autoseleção. Essa foi uma escolha calculada, pois é claro que você pode encontrar qualquer licença sob o sol no GitHub, não apenas as 13 sugeridas pelo GitHub. Não é difícil argumentar que as questões de direito e fato provavelmente variam em 13 contratos de licença diferentes. No entanto, pelo menos essas 13 licenças tinham o requisito comum de que o detentor dos direitos autorais fosse atribuído como condição de uso da licença, o que provavelmente é o motivo pelo qual os demandantes concordaram com apenas essas 13 (essas 13 provavelmente também cobrem 80% ou mais do que está em GitHub, então isso ajuda). Esse fio comum pode ser suficiente nesse caso, principalmente porque não envolve uma reivindicação de direitos autorais. Aqui, no entanto, é impossível traçar qualquer linha comum porque o número de licenças subjacentes provavelmente está na casa das centenas ou milhares, talvez mais. Cada jornal, revista, arquivo, site de compartilhamento de imagens, museu, etc., cada um tem seus próprios Termos de Uso com linguagem bastante variável sobre como as imagens em seus sites podem ser usadas e, claro, muitos sites permitem que os contribuidores de imagens forneçam seus próprios licença para o trabalho, seja algo padrão como uma licença Creative Commons, ou algo totalmente personalizado.

# As reivindicações de direitos autorais

A reclamação inclui uma seção que tenta explicar como funciona a difusão estável. Ele argumenta que o modelo Stable Diffusion é basicamente apenas um arquivo gigante de imagens compactadas (semelhante à compressão MP3, por exemplo) e que, quando Stable Diffusion recebe um prompt de texto, ele “interpola” ou combina as imagens em seus arquivos para fornecer sua saída. A reclamação chama literalmente Stable Diffusion de nada mais do que uma “ferramenta de colagem” em todo o documento. Isso sugere que a saída é apenas uma mistura dos dados de treinamento.

Esta é uma tomada fascinante porque certamente a maneira exata como a interpolação é feita e como a difusão estável responde aos prompts de texto parecem ser parâmetros que podem variar amplamente. A interpretação imediata do texto pode ser muito sensível à fala humana natural com todas as suas nuances ou pode ser horrível. E a interpolação, especialmente de 3 ou 12 ou 100 ou 1000 imagens, pode ser feita em um número ilimitado de combinações, algumas melhores, outras piores. Mas, Stable Diffusion não interpola um subconjunto de imagens de treinamento para criar sua saída: ela interpola TODAS as imagens nos dados de treinamento para criar sua saída. Calibrar cuidadosamente os parâmetros de interpolação para levar a imagens úteis, realistas, estéticas e não perturbadoras é em si uma forma de arte, pois a Internet está repleta de imagens de saída de IA generativas excelentes e horríveis. É relativamente fácil ver melhorias na saída do Stable Diffusion em seus lançamentos e essas melhorias são o resultado de ajustes no modelo, não adicionando mais imagens aos dados de treinamento. Mesmo as várias empresas que usam o Stable Diffusion como uma biblioteca e o treinam com o conjunto de dados LAION parecem estar produzindo resultados com qualidades marcadamente diferentes. Portanto, a alegação de que a saída nada mais é do que a entrada é profundamente ilusória.1

Acho que isso é um pouco como argumentar que não há diferença entre, digamos, ouvir um mashup criado aleatoriamente do White Album dos Beatles com o Black Album de Jay-Z (criando um ruído abominável) e ouvir o poderoso e evocativo som de Danger Mouse. Grey Album, que é uma mistura criativa dos dois. Mesmo que a saída seja um “mero” mashup, a maneira exata de mashup ainda importa muito e faz a diferença entre algo que os humanos reconhecem com alegria como arte e algo que os humanos veem como nada mais do que ruído. Danger Mouse pode ter feito um mashup, mas também fez uma contribuição significativa de sua própria arte para o álbum, criando um tom, som, estilo e mensagem totalmente diferentes dos artistas originais, vale a pena ouvir por seus próprios méritos e não simplesmente para pegar pedaços das obras originais.

Essa questão de quanto da saída deve ser creditada aos dados de treinamento versus o processamento do modelo dos dados de treinamento deve estar no centro do debate sobre se o uso de Stable Diffusion das várias imagens como dados de treinamento é verdadeiramente transformador e, portanto, elegível para defesa de uso justo de direitos autorais (ou talvez até mesmo para a questão de saber se a saída é elegível para proteção de direitos autorais). Acho que será fácil para a defesa apresentar analogias e narrativas alternativas àquelas apresentadas pelos demandantes aqui. A saída representa a compreensão do modelo sobre o que é útil, estético, agradável, etc. e isso, junto com a filtragem e limpeza de dados que as empresas de IA geradoras de imagem fazem,2 é o que as empresas consideram mais valioso, não os dados de treinamento.3 Exceto em casos extremos em que a saída é muito restrita (como “mostre-me cachorros no estilo de Picasso”), pode-se argumentar que o “uso” de qualquer imagem dos dados de treinamento é mínimo e/ou não substancial o suficiente para chamar a saída de um trabalho derivado de qualquer imagem. Claro, nada disso sequer começa a tocar na contribuição do usuário para a saída por meio da especificidade do prompt de texto.4 Em certo sentido, é verdade que não há difusão estável sem os dados de treinamento, mas há igualmente algum sentido em que não há difusão estável sem que os usuários coloquem sua própria energia criativa em seus prompts.

# Conclusão

A Stability AI já anunciou que está removendo a capacidade dos usuários de solicitar imagens no estilo de um artista específico e, além disso, que os lançamentos futuros do Stable Diffusion atenderão às solicitações de qualquer artista para remover suas imagens do conjunto de dados de treinamento. Com essa remoção, os exemplos de saída mais indutores de indignação e problemáticos desaparecem deste caso, deixando um conjunto de fatos muito mais complexo e confuso para o júri percorrer. As reivindicações de publicidade e reivindicações indiretas de violação de direitos autorais, pelo menos conforme declarado nesta reclamação, também desaparecem.5 Não está claro se o processo que resta é aquele que os queixosos ainda desejam litigar, principalmente porque a classe provavelmente também será reduzida .

footnotes 

Isso não cobre o fato de que a Stability AI não usou o conjunto de dados na forma bruta. Eles disseram que removeram o conteúdo ilegal e o filtraram. Dependendo da extensão dessa manipulação, eles podem ser elegíveis para direitos autorais reduzidos na compilação resultante, o que também corroeria o argumento de que a saída é 100% protegida por direitos autorais dos demandantes.

Observe que isso é altamente específico do contexto. Imagens para AIs geradoras de imagens de escopo geral estão amplamente disponíveis e um subconjunto gigantesco delas é de domínio público. Em outros contextos, os dados podem ser extremamente valiosos se forem difíceis de coletar, exigirem anotação ou interpretação humana, etc. Acho que realmente vale a pena distinguir IAs generativas que se baseiam essencialmente em todo o conhecimento da humanidade em um determinado domínio (que também poderíamos chamamos de nossa cultura) de IAs generativas que se baseiam em fontes de dados mais estreitas que não podem ser consideradas como pertencentes a todos nós da mesma maneira.

Apesar de sua propensão autoproclamada para “aberto”, a Stability AI não hesitou em insistir em uma remoção quando um de seus parceiros tornou o modelo público.

Atualmente, o Escritório de Direitos Autorais não permite que trabalhos criados com a assistência de IA generativa recebam registro de direitos autorais. No entanto, o principal advogado de PI Van Lindberg está trabalhando em um caso para reverter essa posição e um número considerável de especialistas em PI acredita que ele pode ter sucesso. A ideia de que nenhuma parte de um trabalho pode ser protegida por direitos autorais apenas porque parte do trabalho foi criada com a ajuda de ferramentas de IA generativas não parece resistir ao teste do tempo, especialmente porque essas ferramentas entram no conjunto padrão de ferramentas que os artistas já estão usando, como o Photoshop. Tal vitória lançaria mais dúvidas sobre as alegações mais amplas dos queixosos de que cada saída do Stable Diffusion é apenas a soma de suas entradas e, portanto, as imagens usadas aqui foram meramente "roubadas" (ou seja, violação de direitos autorais) em vez de "transformadas" (ou seja, justas). usar).

É claro que não há nada que proíba os queixosos de processar por várias reivindicações que ocorreram em versões anteriores do Stable Diffusion. Mas, como esta é uma ação coletiva e os advogados provavelmente estão recebendo uma parte dos danos concedidos aos autores, os danos meramente pelas reivindicações anteriores podem não justificar as despesas legais de prosseguir com o caso.

https://katedowninglaw.com/2023/01/26/an-ip-attorneys-reading-of-the-stable-diffusion-class-action-lawsuit/