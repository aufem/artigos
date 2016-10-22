---
title: 'Como utilizar o Tails para se manter anônima na internet'
date: '06-30-2016 03:00'
metadata:
    keywords: 'o que é Tails, como funciona Tails, como usar Tails, anonimato internet, anonima internet'
    title: 'Como utilizar o Tails para se manter anônima na internet'
    'og: title': 'Aufem | Como utilizar o Tails para se manter anônima na internet'
    author: AuFem
    'og:description': 'Tails: sistema operacional live baseado no GNU/Linux Debian que você pode usar em quase qualquer computador para preservar sua privacidade e anonimato.'
    'twitter:title': 'Aufem | Como utilizar o Tails para se manter anônima na internet'
    'twitter:description': 'Tails: SO live baseado em Debian que você pode usar em quase qualquer computador para preservar sua privacidade e anonimato.'
process:
    markdown: true
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
        - Tails
    categoria:
        - ferramentas
---

![Banner do Tails - The Amnesic Incognito Live System.](../../../images/tails-banner.png)

Tails é um sistema operacional *live* (ao vivo) baseado no GNU/Linux Debian que você pode usar em quase qualquer computador - a partir de um DVD, de um pendrive USB ou de um cartão de memória. Tem como objetivo preservar sua privacidade e anonimato, e auxilia a: 

* usar a Internet de forma anônima; 

* conectar com serviços que podem estar censurados na sua localidade;

* não deixar rastros no computador que você estiver utilizando, a menos que você explicitamente queira que isso aconteça; 

* usar ferramentas criptográficas para criptografar seus arquivos, e-mail e mensagens instantâneas. 

Tails vem com diversas aplicações pré-configuradas tendo como foco a segurança: navegador web, cliente de mensagens instantâneas, cliente de correio eletrônico, aplicativos de escritório, editor de imagens e som, etc.


## Use em qualquer lugar sem deixar rastros

Usar Tails em um computador não altera ou depende do sistema operacional instalado nele. Então, você pode usá-lo da mesma forma no seu computador, no computador de um amigo ou de uma biblioteca. Depois de desligar o Tails, o computador reiniciará usando seu sistema operacional normal.

Tails é configurado para evitar a todo custo usar os discos rígidos (HDs) do computador, mesmo que exista espaço de troca (swap) disponível neles. O único espaço de armazenamento usado pelo Tails é na memória RAM, que é automaticamente apagada quando o computador é desligado. Então, você não vai deixar rastro no computador seja do sistema Tails ou do que você tiver usado nele. Por isso chamamos Tails de “amnésico”.

Isso permite que você trabalhe com arquivos e documentos sensíveis em qualquer computador e protege seus dados de serem recuperados após o desligamento. Claro, você pode (e deve!) salvar documentos específicos em outro pen drive USB ou HD externo para que possa continuar trabalhando neles.


## Tor

Tor lhe protege passando suas comunicações através de relés mantidos por voluntários pelo mundo todo: ele impede que alguém que esteja vigiando sua conexão de internet saiba quais sites você visita – e impede que os sites que você visita saibam qual sua localização física.

Usando Tor você pode:

* navegar de forma anônima ao ocultar sua localização,
* conectar à serviços que de outra forma estariam censurados;
* resistir a ataques que bloqueiam o uso do Tor usando ferramentas de desvio tais como [bridges](https://bridges.torproject.org/) (pontes).

Se você ainda não sabe como "The Onion Router (TOR)" funciona, pare agora e vá ler o artigo "[Como usar Tor para navegar anônima na web](../como-usar-tor-para-navegar-anonima-na-web)", especialmente a parte sobre "precauções", para saber o que Tor pode ou não fazer por você.

Tails + Tor:

Tails utiliza a rede de anonimato Tor para proteger sua privacidade online:

* todos os programas são configurados para conectar à Internet através do Tor
* se uma aplicação tenta conectar à Internet diretamente, a conexão é automaticamente bloqueada por segurança.

## Programas inclusos:

**Rede**
* Tor com: 
- Isolamento de tráfego
- Suporte a bridges normal, obfs2, obfs3, obfs4 e ScrambleSuit 
- Gráfico dos circuitos da rede TOR 
- Gerenciador de rede para fácil configuração 
- Tor Browser, um navegador de internet baseado no Mozilla Firefox, modificado para proteger seu anonimato com: 
- Torbutton para anonimato e proteção contra JavaScript
- Tratamento de cookies por padrão
- HTTPS Everywhere que força conexões SSL para sites que possuem HTTPS disponível
- NoScript para controlar ainda melhor o uso do Javascript
- AdBlock Plus para remover propagandas
* Pidgin pré-configurado com OTR para conversas Não-registradas (Off-the-Record)
* Cliente de e-mail Icedove (Thunderbird) com Enigmail para suporte ao OpenPGP
* Agregador de feeds Liferea
* Gobby para escrita compartilhada de textos
* Aircrack-ng para auditoria de redes wi-fi
* Rede anonimizadora I2P
* Cliente bitcoin Electrum

**Edição de Desktop**
* LibreOffice
* Gimp e Inkscape para editar imagens
* Scribus para diagramação
* Audacity para gravar e editar áudio
* PiTiVi para edição de áudio/vídeo não-linear
* Poedit para editar arquivos .po
* Simple Scaney SANE para suporte a scanners
* Brasero para queimar CD/DVDs
* Sound Juicer para extrair CDs de áudio
* Traverso um gravador e editor de áudio multifaixas.

**Criptografia e privacidade**
* LUKS e GNOME Disks para criptogafar e utilizar dispositivos criptografados, como pendrives USB
* GnuPG, a implementação GNU do OpenPGP para email, criptografia e assinaturas digitais
* Monkeysign, uma ferramenta para assinatura e troca de chaves OpenPGP
* PWGen, um gerador de senhas fortes
* Shamir's Secret Sharing configurado com gfshare e ssss
* Teclado virtual Florence para proteger de keyloggers de hardware
* MAT para [anonimizar metadados de arquivos](../exibir-e-excluir-metadados)
* Gerenciador de senhas KeePassX
* GtkHash para calcular checksums
* Keyringer, uma ferramenta da linha de comando para criptografar segredos compartilhados pelo Git
* Paperkey, ferramenta da linha de comando para fazer backup de segredos OpenPGP em papel



## Permanecendo Anônima

Tor não tem como resolver todos problemas de anonimização. Ele se foca apenas no transporte de dados. Você precisa utilizar softwares de apoio específicos ao protocolo se você não quer que os sites que visita vejam suas informações identificáveis. Por exemplo, você pode usar o Tor Browser quando navegar pela internet para manter sigilosas as informações sobre a configuração do seu computador.

Para proteger seu anonimato, você também precisa ser inteligente. **Não forneça seu nome ou outras informações distintivas em formulários da internet**. Esteja ciente que, como todas outras redes anonimizadoras que são rápidas o suficiente para se navegar na internet, Tor não oferece proteção a ataques end-to-end (fim-a-fim): se seu atacante pode ver o tráfego que sai do seu computador e também o tráfego chegando ao seu destino, ele pode utilizar análises estatísticas para descobrir que isso faze parte do mesmo circuito.

## AVISOS

Sempre tenha em mente que nenhum navegador, sistema ou programa é 100% seguro. Esse artigo em si não traz garantia alguma quanto a sua segurança, portanto, é responsabilidade sua conhecer seus adversários ao máximo para mitigar os riscos a que você está sujeita ao conectar-se à internet, de forma a aumentar a segurança tanto quanto possível. Além dos detalhes específicos para utilização da rede Tor (e seu navegador), você também deve ter em mente as seguintes questões ao utilizar Tails:

* Tails não protege você de um hardware comprometido

Se o computador foi comprometido por alguém que tenha acesso físico a ele e que tenha instalado alguma peça não-confiável de hardware (como um keylogger), pode ser inseguro utilizar Tails.

* Tails pode ser comprometido se instalado ou ligado em sistemas não confiáveis

Quando inicializa seu computador com Tails, Tails não vai ser comprometido por um vírus no seu sistema operacional normal, porém:
a) Tails deve ser instalado de um sistema confiável, ou pode ser corrompido durante a instalação.
b) Conectar seu dispositivo Tails em um sistema operacional comprometido pode corromper sua instalação do Tails e destruir a proteção que Tails oferece. Use seu dispositivo Tails somente para inicializar Tails.

* Tails não lhe protege contra ataques de BIOS ou de Firmware

É impossível para Tails lhe proteger de ataques feitos através da BIOS ou de outro firmware embutido no computador. Esses não são gerenciados ou supridos pelo sistema operacional diretamente e nenhum sistema operacional pode lhe proteger desses ataques.

* Nós de saída do Tor podem vasculhar comunicações

Tor é sobre esconder sua localização, não sobre criptografar sua comunicação. 

Em vez de pegar uma rota direta da origem ao destino, as comunicações utilizando a rede Tor pegam um caminho aleatório através de diversos relés que escondem seus passos para impedir que o observador que esteja em só um desses pontos diga de onde os dados vieram e para onde estão indo.

O último relé nesse circuito, chamado de "nó de saída", é o que estabelece a real conexão com o servidor de destino. Como Tor não faz - e por desenho não pode fazer - criptografia do tráfego entre o nó de saída e o servidor de destino, qualquer nó de saída tem a possibilidade de capturar qualquer tráfego passando por si. 

Para se proteger desse tipo de ataque, você sempre deve utilizar criptografia fim-a-fim (end-to-end). Tails inclui diversas ferramentas para lhe ajudar a utilizar criptografia forte enquanto navega, envia um e-mail ou bate papo na internet.

* Tails deixa claro que você está usando Tor e, provavelmente, Tails

Seu provedor de serviços de internet (ISP) ou quem administra sua rede local pode ver que você está se conectando com um relé Tor e não com um servidor da web, por exemplo. Usar pontes Tor em certas condições pode ajudar a esconder o fato que você está utilizando Tor.

O servidor de destino, que você está conectando através do Tor, pode saber se a comunicação vem de um nó de saída Tor consultando a lista de nós de saída que está publicamente disponível. Por exemplo, utilizando a ferramenta Tor Bulk Exit List do Projeto Tor.

Então, usar Tails não faz você parecer como um usuário aleatório da internet. O anonimato oferecido por Tails e pelo Tor funciona fazendo com que todas pessoas que os utilizam são as mesmas, tornando impossível identificar quem é quem entre elas.

* Ataques MitM

Um ataque man-in-the-middle (MitM - Homem no meio) é uma forma de espionagem ativa em que o atacante faz conexões independentes com as vítimas e envia mensagens entre elas - fazendo com que elas acreditem que estão falando diretamente uma com a outra quando, na verdade, toda conversação está sendo controlada pelo atacante.

Usando Tor, ataques MitM ainda podem acontecer entre o nó de saída e o servidor de destino.  O nó de saída propriamente dito também pode atuar como um homem-no-meio. 

Mais uma vez, para se proteger desse tipo de ataque você deve utilizar criptografia ponto-a-ponto e enquanto o fizer deve tomar cuidados especiais para verificar a autenticidade do servidor.

Geralmente, isso é feito automaticamente pelos certificados SSL verificados pelo seu navegador contra uma lista de autoridades certificadoras reconhecidas. Mesmo assim, pode ocorrer que uma autoridade tenha sido comprometida. Se você receber uma mensagem de exceção de segurança como essa abaixo: 

!["Sua conexão não está segura: mensagem de certificado inválido"](../../../images/certificado_invalido.png)

Você pode estar sendo vítima de um ataque man-in-the-middle e não deve ignorar o aviso, ao menos que você tenha algum outro meio de verificar a impressão digital (fingerprint) do certificado com as pessoas que mantém o serviço.

Por um lado, por prover anonimato, Tor torna mais difícil a realização de ataques man-in-the-middle direcionados a uma pessoa específica, mesmo com a benção de um certificado SSL falsificado. Mas, por outro lado, o Tor faz com que seja mais fácil para pessoas e organizações que possuem nós de saída executarem tentativas de MiTM em larga escala, ou ataques direcionados a um servidor específico, especialmente contra aqueles usuários/as que estiverem usando Tor.


* Ataques de confirmação de tráfego

O desenho do Tor não tenta proteger contra um atacante que pode ver ou medir tanto o tráfego entrando na rede do Tor como também o tráfego saindo dessa rede. Isso ocorre porque se você pode ver ambos os fluxos, estatística simples permite que você decida se eles se equivalem.

Esse também pode ser o caso se seu provedor de internet (ou quem administra sua rede local) e o provedor de acesso do servidor de destino (ou quem administra o servidor de destino propriamente dito) cooperarem para te atacar.

Tor tenta proteger contra análise de tráfego, onde um atacante tenta descobrir quem deve investigar, mas Tor não tem como lhe proteger de ataques de confirmação de tráfego (também conhecido como correlação fim-a-fim), quando um atacante tenta confirmar uma hipótese monitorando as localizações corretas na rede e fazendo as contas

* Tails não criptografa seus documentos por padrão

Os documentos que você salva em dispositivos de armazenamento não serão criptografados por padrão, a não ser no volume persistente criptografado. Vale lembrar, entretanto, que Tails lhe fornece as ferramentas para criptografar seus documentos, como GnuPG, ou criptografar seus dispositivos de armazenamento, como LUKS.

É altamente provável que os arquivos que você criar possam contar evidências que eles foram criados utilizando Tails. 

Se você precisar acessar os discos rígidos locais do computador que você estiver usando, saiba que então você pode estar deixando neles um rastro das suas atividades.

* Tails não limpa os metadados dos seus documentos para você e não criptografa o "Assunto:" e outros cabeçalhos das suas mensagens de email criptografadas

Observe que o "Assunto:", assim como o resto dos cabeçalhos das suas mensagens de e-mail criptografadas com OpenPGP não são criptografadas. Isso não é um bug do Tails ou do protocolo OpenPGP - deve-se ao fato da compatibilidade reversa do protocolo SMTP original. Infelizmente, nenhum padrão RFC existe ainda quanto à criptografia da linha "Assunto:".

Como já falado no post sobre [metadados](../exibir-e-excluir-metadados), diversos formatos de arquivo armazenam dados escondidos, ou metadados, dentro dos próprios arquivos. Processadores de texto ou arquivos PDF podem armazenar o nome do autor, a data e hora de criação e, às vezes, até mesmo partes da história de edição do arquivo, dependendo do formado do mesmo e do programa que foi utilizado. Tails não limpa os metadados do seus arquivos para você. Por enquanto. Mesmo assim, é um dos objetivos de projeto do Tails lhe ajudar com isto. Por exemplo, Tails já vem com um kit de anonimização de metadados (MAT).

* Tor não lhe protege de um adversário global

Um adversário global passivo seria uma pessoa ou entidade capaz de monitorar, ao mesmo tempo, o tráfego entre todos os computadores em uma rede. Estudando, por exemplo, o tempo e os padrões de volume de diferentes comunicações através da rede, seria estatisticamente possível identificar os circuitos Tor e, portanto, corresponder quem utiliza Tor com os servidores destino.

É parte da escolha inicial do Tor não lidar com essa ameaça para permitir a criação de um serviço de comunicação de baixa latência utilizável para navegação na web, bate-papo via Internet e conexões SSH.

* Tails não separa magicamente suas diferentes identidades contextuais

Não é recomendável utilizar a mesma sessão do Tails para executar duas tarefas ou utilizar duas identidades contextuais que você quer manter separadas uma da outra. Por exemplo, escondendo sua localização para verificar seu e-mail e publicando um documento anonimamente.

Primeiro, porque Tor tende a reutilizar os mesmos circuitos, por exemplo, durante a mesma sessão de navegação. Desde que o nó de saída de um circuito saiba tanto o servidor de destino (e, possivelmente, o conteúdo da comunicação se ela não for criptografada) e o endereço do relé anterior de onde recebeu a comunicação, fica fácil correlatar diversas solicitações de navegação ao mesmo circuito e, possivelmente, ao mesmo usuário. Se você está encarando um adversário global como o descrito acima, ele também pode estar em posição de fazer essa correlação.

Em segundo lugar, no caso de uma falha de segurança, ou em um erro utilizando Tails ou uma de suas aplicações, informação sobre sua sessão pode acabar vazando. Isso pode revelar que a mesma pessoa estava por trás de diversas ações feitas durante aquela sessão.

A solução para ambas as ameaças é desligar e reiniciar Tails toda vez que você for usar uma nova identidade, se você realmente quiser isolá-las melhor.

* Tails não transforma suas senhas fracas em fortes

Tor permite que você fique anônima online; Tails permite que você não deixe rastros no computador que está usando. Ainda assim, nenhum desses dois recursos são feitiços mágicos para segurança do computador.

Se você usa senhas fracas, elas podem ser descobertas por ataques de força bruta da mesma forma, com ou sem Tails. Para saber se suas senhas são fracas e aprender boas práticas de criação de senhas melhores, você começar lendo [as observações que fizemos sobre criação de senhas](../passo-a-passo-para-criptografar-seus-e-mails-versao-windows#senhas).

Agora que você já sabe tudo isso sobre Tails, que tal começar a usá-lo? Dê uma lida em [nosso post sobre como criar seu próprio pendrive Tails](../fazer-um-pendrive-do-tails-no-debian) e depois venha nos contar como foi a experiência!

**Saiba mais:**

* [Site do Tails (nem tudo em português)](https://tails.boum.org/index.pt.html)