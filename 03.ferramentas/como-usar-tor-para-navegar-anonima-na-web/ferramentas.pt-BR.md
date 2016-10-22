---
title: 'Como usar Tor para navegar anônima na web'
metadata:
    keywords: 'o que é tor, como funciona Tor, quem utiliza Tor, cuidados com Tor, Como usar Tor'
    'og:title': 'Como usar Tor para navegar anônima na web'
    'og:description': 'Saiba o que é, como funciona, quais cuidados e como usar Tor para navegar anônima na web.'
    'og:image': 'https://naoenoveladasoito.com.br/images/tor-logo.jpg'
    'twitter:title': 'Como usar Tor para navegar anônima na web'
    'twitter:description': 'Saiba o que é, como funciona, quais cuidados e como usar Tor para navegar anônima na web.'
taxonomy:
    author:
        - aufem
    tag:
        - internet
        - privacidade
        - segurança
        - navegação
        - ferramentas
        - Tor
        - anonimato
    categoria:
        - ferramentas
---

![Logo do Tor - the Onion Router](../../../images/tor-logo.jpg)

**Conteúdo**

[O que é Tor](#oqueeTor)   
[Como o Tor funciona](#comofuncionaTor)   
[Quem utiliza o Tor](#quemutilizaTor)   
[Precauções](#cuidadoscomTor)   

## O que é o Tor<a id="oqueeTor"></a>

Tor (the Onion Router) é um programa que protege você encaminhando suas comunicações através de uma rede distribuida de relés mantidas por pessoas voluntárias do mundo inteiro. Isso previne que alguém que esteja vigiando sua conexão de internet descubra quais sites você visita, previne que os sites que você visita descubram sua localização física e permite que você acesse sites que estejam bloqueados.

Para navegação na web utilizando Tor você pode usar: o [navegador Tor](https://www.torproject.org/projects/torbrowser.html.en), disponível para Windows, Linux e OS X, ou o aplicativo [Orbot](https://guardianproject.info/apps/orbot/), disponível para Android - no Google Play, no [F-Droid](https://guardianproject.info/fdroid) ou para [download direto do .apk](https://guardianproject.info/releases/orbot-latest.apk).

Você pode usar o navegador Tor em Windows, Mac OS X, ou Linux mesmo sem instalar nenhum programa: pode utilizar diretamente de um pendrive USB, que já vem configurado para proteger seu anonimato e é auto-contido (portátil). Para baixar a versão mais atualizada, vá direto ao [site do projeto Tor](https://www.torproject.org/projects/torbrowser.html.en), selecione seu sistema operacional, o idioma e arquitetura (quando em dúvida, baixe a versão 32 bits que funciona em processodores 32 E 64 bits). **Não esqueça de forma alguma** de verificar a assinatura GnuPG do arquivo baixado. Para isso, você deve [ter o GnuPG instalado](../passo-a-passo-para-criptografar-seus-e-mails-versao-windows) e seguir as instruções [detalhadas aqui](https://www.torproject.org/docs/verifying-signatures.html.en).


## Como o Tor funciona<a id="comofuncionaTor"></a>

Tor conecta você a um site ou serviço através de túneis virtuais, em vez de fazer uma conexão direta. Isso permite que tanto pessoas quanto organizações compartilhem informações por redes públicas sem comprometer sua privacidade. Tor também é uma ferramenta muito efetiva contra a censura, permitindo que quem o utiliza alcance destinos ou conteúdos que de outra forma estariam bloqueados. 

A imagem abaixo mostra como o Tor funciona. As setas vermelhas indicam tráfego às claras (não criptografado) e, as verdes, tráfego criptografado.

![Como funciona o Tor: Cliente Tor da Alice escolhe um caminho aleatório para o servidor de destino. Conexão de Alice ao primeiro relé é criptografada, desse relé ao segundo relé é criptografada, do segundo relé ao nó de saída é criptografada. Conexão do nó de saída ao servidor destino não é criptografada.](../../../images/htw2-tails-pt_br.png)

## Quem utiliza o Tor<a id="quemutilizaTor"></a>

Pessoas usam o Tor para impedir que sites rastreiem a si ou as pessoas de sua família, ou para se conectar a sites de notícias, mensagens instantâneas, ou outros que possam estar bloqueados pelos seus provedores de serviço de internet (ISP). Os serviços ocultos (hidden services) do Tor permitem que suas usuárias publiquem websites e outros serviços (por exemplo, e-mail) sem que tenham que revelar a localização do site. Indivíduos também utilizam o Tor para comunicação que pode ter informações sensíveis: existem chats e fórums para sobreviventes de abusos e estupros, ou para pessoas com doenças específicas.

Jornalistas utilizam Tor para se comunicar com segurança com informantes e dissidentes. Ativistas e membros de Organizações Não-Governamentais (ONGs) usam o Tor para permitir que seus colaboradores se conectem com seu site enquanto estão em um país estrangeiro, sem que ninguém ao redor (indivíduos, provedores, governos...) precise ficar sabendo que essa pessoa está trabalhando com aquele grupo ou organização.

Militares utilizam para buscar informações de inteligência. Agentes de segurança do Estado utilizam para visitar ou vigiar sites sem deixar um endereço de IP governamental registrado no servidor - e para segurança durante operações.

A variedade de pessoas que utilizam o Tor é um dos motivos que o faz ser tão seguro. Tor esconde quem você é em meio aos outros usuários da rede, então, quanto mais diversa e populosa é a base de usuários do Tor, mais seu anonimato será protegido.

## Precauções<a id="cuidadoscomTor"></a>

**Use o Navegador Tor**

Tor não protege todo seu tráfego na internet quando você o utiliza - ele só protege as aplicações que estão corretamente configuradas para encaminhar seu tráfego da internet através do Tor. Para evitar problemas de configuração, utilize o navegador Tor - qualquer outro navegador com configurações Tor não oferece a mesma segurança do navegador Tor.

**Não baixe torrents através do Tor**

Aplicações de torrent tendem a ignorar configurações de proxy e fazer conexões diretas mesmo quando recebem instruções para utilizar o Tor. Mesmo que seu programa de torrents conecte-se somente pelo Tor, ele frequentemente entrega seu endereço de IP real na requisição GET do tracker, porque é assim que os torrents funcionam. Não só você desanonimiza seu tráfego de torrent - e todo seu tráfego pelo Tor - através disso, você também faz com que toda rede Tor fique mais lenta, para você e para todas as outras pessoas que a utilizam.

**Não ative ou instale plugins no navegador**

O navegador Tor irá bloquear plugins como Flash, RealPlayer, Quicktime, e outros: eles podem ser manipulados em revelar seu endereço de IP. Também não recomendamos instalar extensões ou plugins adicionais no Tor Browser, pois esses podem desviar do Tor ou colocar em risco seu anonimato e privacidade.

Veja um exemplo de como isso acontece: 

![Desenho mostrando uTorrent, Skype, Flashplayer e outras aplicações conectando diretamente à internet, enquanto o navegador utiliza somente a rede Tor](../../../images/TOR_tunnel.png)

Além disso, como já falamos em [Qual a impressão digital do seu navegador?](../blog/qual-a-impressao-digital-do-seu-navegador-browser-fingerprint), o conjunto de plugins e extensões instalados no navegador pode ser utilizado para identificar você. Usando o padrão que vem com Tor, você garante que sua identificação está idêntica a diversos outros computadores que também utilizam Tor, dificultando o trabalho de sites ou entidades que queiram lhe vigiar.

**Não maximize a janela do navegador**

Como já falamos, um dos itens que faz o Tor seguro é que, devido às configurações, todas pessoas que o utilizam parecem ser iguais. Tor mascara, por exemplo, seu sistema operacional, para que pareça que você utiliza Windows NT 6.1 em vez de _insira seu sistema operacional aqui_. Quando você maximiza a janela, está se distinguindo das outras pessoas que utilizam Tor e passando para o site de destino a sua resolução de tela original, que também é utilizada para identificação (fingerprinting).

**Saiba que nós de saída do Tor podem vasculhar comunicações**

Tor é sobre esconder sua localização, não sobre criptografar sua comunicação. Como mostrado na imagem acima, o último relé no circuito Tor, chamado de "nó de saída", é o que estabelece a real conexão com o servidor de destino. Tor não faz - e, por desenho, não pode fazer - criptografia do tráfego entre o nó de saída e o servidor de destino, qualquer nó de saída tem a possibilidade de capturar qualquer tráfego passando por si. Para se proteger desse tipo de ataque, você sempre deve utilizar criptografia fim-a-fim (end-to-end). Exemplos de criptografia fim-a-fim incluem SSH, HTTPS e OpenGPG.

**Utilize as versões HTTPS dos sites**

Como dissemos acima, Tor irá criptografar seu tráfego de e para a rede Tor, mas a criptografia do seu tráfego ao destino final depende do site. Para garantir criptografia privada nessa parte, o navegador Tor inclui HTTPS Everywhere, que força o uso de criptografia HTTPS com a maioria dos sites que a suporta. Entretanto, você deve ficar de olho na barra de endereços do navegador para se assegurar que os sites aos quais dá informações sensíveis apresentam um botão verde ou azul na barra, que incluem https:// na URL, e mostram o nome correto e esperado.

**Não abra documentos baixados pelo Tor enquanto estiver online**

O navegador Tor vai avisar antes de abrir automaticamente um documento que seja lidado por uma aplicação externa. NÃO IGNORE ESSE AVISO. Você deve ter muito cuidado quando baixar arquivos pelo Tor (especialmente arquivos DOC e PDF, a menos que você use o visualizador de PDF incluido no navegador Tor), pois esses documentos podem conter recursos da internet que serão baixados por fora do túnel Tor pela aplicação que os abre (como mostrado anteriormente). Isso revelará seu IP real (não-Tor). Se você precisa trabalhar com arquivos DOC ou PDF, recomendamos utilizar um computador desconectado, utilizar uma máquina virtual (VirtualBox), ou utilizar o Tails.

**Tor não separa magicamente suas diferentes identidades contextuais**

Não é recomendável utilizar a mesma sessão do Tor para executar duas tarefas ou utilizar duas identidades contextuais que você quer manter separadas uma da outra. Por exemplo, escondendo sua localização para verificar seu e-mail e publicando um documento anonimamente. 

Primeiro, porque o Tor tende a reutilizar os mesmos circuitos, por exemplo, durante a mesma sessão de navegação. Desde que o nó de saída de um circuito saiba tanto o servidor de destino (e, possivelmente, o conteúdo da comunicação se ela não for criptografada) e o endereço do relé anterior de onde recebeu a comunicação, fica fácil correlatar diversas solicitações de navegação ao mesmo circuito e, possivelmente, ao mesmo usuário. Se você está encarando um adversário global, ele também pode estar em posição de fazer essa correlação.

Em segundo lugar, no caso de uma falha de segurança, informação sobre sua sessão pode acabar vazando. Isso pode revelar que a mesma pessoa estava por trás de diversas ações feitas durante aquela sessão. A solução para ambas as ameaças é desligar e reiniciar o Tor toda vez que você for usar uma nova identidade, se você realmente quiser isolá-las corretamente. Para uma separação ainda mais segura, recomendamos utilizar o Tails, que será discutido em outro post em breve aqui no Aufem!

**Não acesse fora do Tor contas criadas dentro da rede Tor**

Se você criou uma conta em qualquer serviço, seja de e-mail, rede social ou qualquer outra coisa, utilizando Tor para manter sua privacidade e anonimato, **não acesse essa conta fora da rede Tor**, pois estará comprometendo-a, deixando seu IP real, com a sua localização, registrado em log na conta. 

**Use pontes e/ou encontre companhia!**

Tor tenta evitar que atacantes saibam qual os sites de destino aos quais você se conecta. Entretanto, por padrão, não impede que alguém vigiando seu tráfego de internet saiba que você está utilizando o Tor. Se isso importa para você, pode reduzir esse risco configurando Tor para utilizar uma ponte Tor como relé, em vez de conectar diretamente na rede Tor. Por fim, a melhor proteção é através de um ponto de vista social: quanto mais usuárias Tor houverem próximo de você - e quanto mais diversos seus interesses, menos perigo que você seja identificada. Convença outras pessoas a utilizarem Tor, também!

Seja inteligente e continue aprendendo sobre o assunto. Entenda o que o Tor oferece ou não. Não se limite a esse artigo. Se possível, leia mais sobre o Tor, principalmente [sua documentação](https://www.torproject.org/docs/documentation.html.en) e [Wiki](https://trac.torproject.org/projects/tor).

**Saiba mais:**
* [Site oficial](https://www.torproject.org)
* [Folder do Tor em PDF](https://naoenoveladasoito.com.br/files/tor-brochure-pt-BR.pdf)
* [Folder do Tor em texto simples](https://naoenoveladasoito.com.br/files/tor-brochure-pt-BR.txt)