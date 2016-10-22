---
title: 'Fazer um pendrive do Tails no Debian'
date: '06-30-2016 09:00'
metadata:
    keywords: 'como usar Tails, baixar Tails, anonimato internet, pendrive Tails, armazenamento encriptado, criptografia'
    title: 'Fazer um pendrive do Tails no Debian'
    'og: title': 'Aufem | Fazer um pendrive com Tails no Debian'
    author: AuFem
    'og:description': 'Como fazer pendrive do Tails para usar em quase qualquer computador e preservar sua privacidade e anonimato.'
    'twitter:title': 'Aufem | Fazer um pendrive do Tails no Debian'
    'twitter:description': 'Como fazer pendrive do Tails para usar em quase qualquer computador e preservar sua privacidade e anonimato.'
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
        - armazenamento encriptado
        - criptografia
    categoria:
        - ferramentas
---

![Banner do Tails - The Amnesic Incognito Live System.](../../../images/tails-banner.png)

Embora a utopia do Autonomia Feminista Tecnológica seja embasada em software livre, a realidade que vivemos no momento nos obriga a trazer descrição de algo que não é 100% livre. Tails não é totalmente software livre porque, para que possa funcionar corretamente quando você coloca o pendrive em quase qualquer computador, Tails contém firmwares proprietários. Ainda assim, Tails em si tem código aberto e possui uma licença livre, GNU/GPLv3.

Assumimos que você tenha lido todo o artigo sobre [como utilizar Tails para se manter anônima](../como-utilizar-o-tails-para-se-manter-anonima-na-internet) antes de criar seu próprio pendrive começar a utilizar Tails.

A forma mais simples e rápida de você conseguir um Tails é clonando outro Tails. Se você tem alguém de confiança que já possui um Tails, pode usá-lo para instalar em seu pendrive. No caso de este ser seu primeiro contato, siga os passos abaixo. Você vai precisar de um pendrive de ao menos 4GB que possa ser formatado.

Baixar:

1. Vá ao site: [https://tails.boum.org/install/index.pt.html](https://tails.boum.org/install/index.pt.html)

2. Clique em "Let's start the journey!"

![Botão "Let's start the journey!"](../../../images/start_tails.png)

3. "Which operating system are you installing Tails from?" Escolha o sistema operacional que você utilizará para instalar o Tails. Nesse exemplo, usaremos o Debian.

![De qual sistema operacional você está instalando?](../../../images/sistema_operacional_Tails.png)

4. Como ainda não temos um Tails para clonar ("Install from another Tails"), vamos para "Download and Install" (Baixar e instalar), à direita. De acordo com sua experiência com a linha de comando, você pode escolher a opção "Install from Debian, Ubuntu, or Mint using the Command Line and GnuPG" (Instalar de Debian, Ubuntu ou Mint usando a linha de comando) ou simplesmente "Install from Debian, Ubuntu, or Mint". 

![Instalar do Debian, Ubuntu ou Mint](../../../images/baixar_e_instalar_Tails.png)

5. A página seguinte mostra os passos: a) "First you will install a Tails on your USB stick" (Primeiro, você vai instalar um Tails no seu pendrive USB); b) "Then you will configure it" (E aí você vai configurá-lo.). Clique em "Let's go!" (vamos lá!).

6. Inicialize seu computador com o sistema operacional desejado, nesse caso, Debian 8 (Jessie), Ubuntu 15.10 (Wily Werewolf), ou Linux Mint 18 (Sarah) - ou posterior.

## Parte 1/6:
* "Download and verify the Tails ISO image" (Baixe e verifique a imagem ISO do Tails).
Se você estiver usando Firefox ou Tor Browser, instale a extensão (add-on) para verificar a ISO "Install Firefox add-on". Após instalá-la, baixe a imagem ISO mais atualizada, clicando em "Download Tails 2.4 Image" (2.4 é a versão atual no momento de publicação desse artigo).

## Parte 2/6:
* "Install Tails Installer" (Instale o instalador de Tails)
Se está executando Debian:
1. Certifique-se de estar conectada à internet.
2. Inicialize o Gerenciador de Pacotes Sinapticos
3. Escolha "Configurações" ▸ Repositórios
4. Para adicionar o repositório jessie-backports, clique "Novo" no menu de Repositórios e especifique:

<code>URI: http://http.debian.net/debian/    
Distributions: jessie-backports    
Section(s): main</code>

5. Clique "ok"
6. No menu de confirmação, clique "Recarregar" e aguarde que o download da informação do pacote termine.
6. Na janela principal, clique "Buscar" e busque por "tails-installer".
7. Na lista de pacotes, dê um clique duplo em tails-installer para marcar o tails-installer para instalação.
8. No diálogo de confirmação, clique "Marcar".
9. Clique no botão "Aplicar" na barra de tarefas para aplicar as mudanças.
10. Depois das mudanças serem aplicadas, feche o gerenciador de pacotes.

## Parte 3/6:
* Instale Tails
Agora, vamos instalar Tails no pendrive USB utilizando o Tails Installer. ATENÇÃO! O pendrive será formatado, todos os dados que existirem nele serão perdidos.
1. Conecte o pendrive na porta USB
2. Abra o Tails Installer.
3. Clique no botão Install. (instala Tails em um pendrive USB)
![Tails Installer no Debian](../../../images/tails_installer_in_debian.png)
4. Click "Browse" (Navegar) e encontre a imagem ISO que você baixou no começo.
5. Escolha cuidadosamente a opção do seu pendrive USB na lista "Target Device".
6. Para instalar, clique no botão "Install Tails".
7. Veja a mensagem de aviso. O pendrive será formatado e TODOS os dados serão perdidos. Clique "YES" para confirmar. A instalação demora alguns minutos. No final, você precisa colocar sua senha de administrador. (É normal a barra de progresso travar durante a sincronização dos dados, seja paciente.)
8. Feche o Tails Installer.

## Parte 4/6:
Se ainda não fez, abra essas instruções em outro dispositivo ou imprima-as. Você precisará reiniciar o computador.

## Parte 5/6:
* Desligue o computador
Desligue o computador sem retirar o pendrive USB.

* Ligue novamente o computador
Se o computador inicializar no Tails, o menu de Boot Tails aparece. Escolha "Live" e aperte Enter.

![menu de Boot Tails](../../../images/tails_boot_menu.png)

Se o computador não inicializar no Tails (é bastante comum isso não acontecer), você pode precisar alterar a ordem de Boot do seu computador. Busque a tecla que acessa esse menu, de acordo com o fabricante, reinicie o computador pressionando-a até que o menu apareça, e selecione o pendrive USB. <center>


| Fabricante | Tecla   |
|------------|:---------------|
| Acer     | Esc, F12, F9   |
| Asus     | Esc, F8   |
| Dell     | F12   |
| Fujitsu  | F12, Esc   |
| HP       | Esc, F9   |
| Lenovo   | F12, Novo, F8, F10   |
| Samsung  | Esc, F12, F2   |
| Sony     | F11, Esc, F10   |
| Toshiba  | F12   |
| others…  | F12, Esc    |

</center>
Se nem isso funcionar, você pode ter de descobrir como alterar o Setup da BIOS do seu computador. 

Depois de aproximadamente 30-60 segundos, a tela de boas vindas ao Tails aparece. 

![Bem-vinda ao Tails!](../../../images/tails-greeter-welcome-to-tails.png)

Você pode selecionar: seu idioma preferido, configurações de região e configurações de teclado. Se escolher "mais opções", você pode ativar uma senha administrador e fazer configurações avançadas de conexão a rede Tor, caso haja censura ou bloqueio à internet na sua rede. Clique em "login". A área de trabalho do Tails aparece. 

![Área de trabalho](../../../images/desktop_tails.png)

Aguarde: sincronização do relógio, a cebola do Tor ficar verde, para abrir o navegador Tor e outros recursos que necessitem de internet.

<cite>Parabéns! Você instalou e rodou Tails de um pendrive com sucesso!</cite>

## Parte 6/6 - Coisas que você pode fazer agora:

#### Criar outros pendrives clonando seu Tails
Distribua Tails as suas amigas e ensine-as a usarem!

#### Navegar pelo Tor e experimentar todos os recursos do Tails
Lembre-se da regrinha de que você não se mantém anônima acessando pelo Tor contas que você acessa fora da rede Tor. Aproveite para criar um e-mail seguro (ex. Riseup, Protonmail, Openmailbox) com chaves GPG, descubra como fazer uso da criptografia da área de transferência (clipboard), experimente o [MAT](../exibir-e-excluir-metadados#remover-metadados-arquivo), e explore todos os recursos que Tails oferece!

#### Criar um armazenamento encriptado persistente
Lembra quando dissemos que Tails era Amnésico? Isso quer dizer que, ao desligá-lo, ele irá esquecer e apagar todos os arquivos que você tiver salvo. Para mantê-los e continuar trabalhando em algum arquivo, você deve salvar em algum armazenamento persistente. E nada melhor do que esse armazenamento ser criptografado, certo?

Você também poderá utilizar esse armazenamento persistente para salvar: configurações personalizadas (por exemplo: favoritos do navegador Tor), chaves de criptografia (GPG, OTR, SSH...). Todos os dados armanezados no armazenamento persistente permanecerá disponível não importa quantas vezes você reinicie - e estarão criptografados utilizando uma frase-senha de sua escolha.

**O que você precisa saber:**
* O armazenamento encriptado persistente não fica oculto. Um atacante que tiver acesso ao seu pendrive USB vai saber se dentro dele tem ou não um armazenamento persistente criptografado. Considere que você pode ser forçada ou enganada em entregar a frase-senha.

* É possível abrir o armazenamento encriptado persistente em outros sistemas operacionais, mas isso pode comprometer sua segurança. Outros sistemas operacionais provavelmente não devem ser confiados para que lidem com informações sensíveis ou para que não deixem rastros.

1. Escolha "Aplicativos ▸ Tails ▸ Configurar volume persistente"
2. Especifique a frase-senha de sua escolha nas duas caixas "frase senha" e "verificar frase senha". Recomendamos que escolha uma frase-senha longa feita de cinco a sete palavras aleatórias com erros propositais e caracteres especiais.
3. Clique no botão "Criar".
4. Aguarde que a criação termine. **ATENÇÃO!** Se você fechar o assistente antes que esse processo seja terminado, você pode não conseguir inicializar Tails desse pendrive USB novamente.
5. O assistente oferece uma lista de possíveis coisas a serem colocadas na persistência. Cada coisa corresponde a um conjunto de arquivos ou configurações a serem salvos no armazenamento. Recomendamos que você ative apenas "Dados Pessoais" por enquanto. Você pode ativar outras mais tarde, de acordo com a necessidade.
6. Clique "Salvar".
7. Reinicie e ative o armazenamento persistente, escolhendo "mais opções/usar persistência" e colocando sua frase-senha.
8. Agora você pode salvar os documentos que estiver trabalhando e seus arquivos pessoais no diretório Persistent. Para abrir esse diretório, escolha: Locais ▸ Persistent.