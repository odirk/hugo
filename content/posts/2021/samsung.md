---
title: "As propagandas estão fora de controle"
date: "2021-08-24"
tags: ["tech", "privacidade"]
description: "'I'm sorry, Dave. I'm afraid I can't do that.'"
draft: true
---

Estou com uma TV nova da Samsung há uns meses e percebi que ela fica motrando anúncios na barra de input (aonde você escolhe a fonte de entrada ou acessa apps).

{{< figure align=center src="/samsung/ad.jpg" title="Enfurecedor, não é?" >}}

Minha primeira reação foi de total indiganação, como a Samsung pode exibir anúncios na minha TV sem o meu consentimento? Eu paguei por ela e eles não têm o direito de ganhar ainda mais dinheiro às minhas custas. (["You double-dipped the chip!"](https://www.youtube.com/watch?v=RfprRZQxWps))

Eu verifiquei se é possível formatar o sistema operacional da TV e instalar algo de código aberto mais orientado para privacidade, mas essa opção pareceu muito tediosa e demorada.

Mas, para minha surpresa, bloquear anúncios na sua TV é muito simples do que esperava. Basta seguir as etapas abaixo:

&nbsp;
&nbsp;

### 1. Acesse o router

Abra a página de configuração do seu roteador. Para isso, acesse o endereço do roteador em um navegador em um dispositivo conectado à sua rede.

Esse endereço deve estar escrito na lateral de seu roteador (geralmente é [http://192.168.0.1](http://192.168.0.1)), junto com login e senha.

&nbsp;
&nbsp;

### 2. Acesse a página de DNS

Localize a página sobre o DNS. Na NET/Claro, fica dentro do menu nas *Configurações avançadas*, em *Rede*.

> O [AdGuard](https://adguard.com/pt_br/adguard-dns/overview.html) possui servidores de DNS que bloqueiam propagandas na web, e isso funciona contra as propagandas da Samsung e com outras incoveniências também.

Adicione os seguintes endereços na página:

| IPv4 | IPv6 |
| ---- | ---------- |
| 94.140.14.14 | 2a10:50c0::ad1:ff |
| 94.140.15.15 | 2a10:50c0::ad2:ff |

{{< figure align=center src="/samsung/claro.png" title="Todo router é diferente, mas costuma ser uma página parecida com essa." >}}

&nbsp;
&nbsp;

### 3. Salve as alterações

Clique em salvar e é só isso!

As propagandas ainda vão continuar aparecendo por um ou dois dias (pois estão salvas na televisão), mas **elas deixarão de aparecer em breve**. :tada: