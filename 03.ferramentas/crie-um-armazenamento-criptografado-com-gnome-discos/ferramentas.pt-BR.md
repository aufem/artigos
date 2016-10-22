---
title: 'Crie um armazenamento criptografado com GNOME Discos'
published: true
date: '09-01-2016 12:00'
metadata:
    keywords: 'armazenamento criptografado, pendrive, criptografar HD'
    title: 'Crie um armazenamento criptografado com GNOME Discos'
    'og: title': 'Aufem | Crie um armazenamento criptografado com GNOME Discos'
    author: AuFem
    'og:description': 'A forma mais simples se assegurar que seus arquivos não foram acessados ou modificados é armazená-los em um volume criptografado.'
    'twitter:title': 'Aufem | Crie um armazenamento criptografado com GNOME Discos'
    'twitter:description': 'A forma mais simples se assegurar que seus arquivos não foram acessados ou modificados é armazená-los em um volume criptografado'
process:
    markdown: true
taxonomy:
    categoria:
        - ferramentas
    tag:
        - privacidade
        - segurança
        - criptografia
        - 'armazenamento encriptado'
        - tutorial
        - Tails
        - arquivo
    author:
        - aufem
sitemap:
    changefreq: weekly
---

Você usa HD externo, pendrives ou algum outro dispositivo de armazenamento? Criptografa eles? 

A forma mais simples se assegurar que seus arquivos não foram acessados ou modificados é armazená-los em um volume criptografado: uma partição dedicada em um pendrive USB ou em um HD externo.

O GNU discos é uma ferramenta que facilita muito esse processo. 

Vamos dar um exemplo de como criar um criar um armazenamento criptografado em um dispositivo USB (nesse caso, um pendrive) utilizando o Tails (lembra dele?), porém, essas instruções servem para qualquer distribuição que utilize o GNOME Discos, como Debian, Ubuntu, Fedora, Red Hat Enterprise e CentOS. 

## Formatar com GNOME Discos

Antes de criar o armazenamento, você deve apagar todo e qualquer arquivo que exista no dispositivo, formatando-o.

1) Insira o dispositivo na porta USB do computador.

2) Abra GNOME Discos usando Aplicativos ▸ Utilitários ▸ Discos.
![GNU Discos](../../../images/GNUdiscos.jpg)

3) O dispositivo deve aparecer na lista à esquerda. Selecione-o.

4) Certifique-se que a descrição da seleção corresponde perfeitamente à descrição do seu dispositivo, para não formatar outro por engano.

5) Para formatar o dispositivo, selecione no menu apropriado (ou escolhendo CTRL+F).

![Primeiro botão do menu, à esquerda, ou CTRL+F](../../../images/formatar_pendrive.jpg)

6) Escolha "Compatível com todos os sistemas e dispositivos (MBR/DOS)" na lista. E, para uma formatação segura, que impeça os dados anteriores de serem recuperados, é altamente recomendável que você [sobreescreva os dados existentes com zeros](https://web.archive.org/web/20121110053501/http://grot.com/wordpress/?p=154). É um processo lento que pode demorar vários minutos, dependendo do tamanho do armazenamento, mas bastante relevante se você tiver arquivos que precisam ser apagados por completo. Clique **"Formatar"**.

![Sobrescrever com zeros](../../../images/sobrescrever_com_zeros.jpg)

![Formatando o dispositivo](../../../images/apagando_dispositivo.jpg)

## Criar a nova partição criptografada

Após ter formatado, o esquema de partições deve aparecer na sua tela mostrando um dispositivo vazio:

1) Clique no botão "+" para criar uma nova partição no dispositivo.

2) Na janela "Criar partição":

*Tamanho da partição:* você pode criptografar todo armazenamento no dispositivo ou apenas parte dele. Nesse exemplo, estamos criptografando todo o dispositivo.

*Tipo:* escolha "Criptografado, compatível com sistemas Linux (LUKS + Ext4)"

![Criptografado, compatível com sistemas Linux](../../../images/LUKS_Ext4.jpg)

**Nome:** escolha um nome para a partição. Esse nome ficará invisível até quando a partição for carregada, mas servirá para você identificá-la quando estiver utilizando-a.

**Frase-senha:** crie uma frase-senha forte e memorável - repita-a para confirmar.

Então, clique em **"Criar"**.

![Criar partição](../../../images/criar_particao.jpg)

Nota: Se algum erro ocorrer ao criar a nova partição, tente desconectar o dispositivo, reiniciar o GNOME Discos, e seguir o passo-a-passo desde o começo.

3) Criar uma partição pode demorar de alguns segundos a alguns minutos. Quando estiver pronto, a nova partição criptografada deve aparecer no dispositivo.

![Partição criptografada](../../../images/particao_criptografada.jpg)

4) Se você criptografou só uma parte do dispositivo - e quiser criar uma nova partição no espaço livre, basta que siga esses passos a partir de "Clique no botão "+" para criar uma nova partição no dispositivo.".

## Usar a partição criptografada

Você pode abrir essa nova partição na barra lateral do gerenciador de Arquivos que você utiliza. No Tails, a partição não será carregada automaticamente, mas mesmo assim você pode abri-la clicando nela, escrevendo a frase-senha e clicando em "Desbloquear". Se você escolher a opção "Lembrar senha" e tiver a Persistência ativada no Tails, a senha será gravada e lembrada nas próximas sessões.

## AVISOS

* Volumes criptografados não ficam escondidos. Um atacante em posse de um dispositivo consegue ver que tem um armazenamento criptografado nele. Lembre-se que você pode ser forçada ou enganada a ponto de entregar a frase-chave. (Mais saiba, também, que, no Brasil, nenhuma força do Estado pode obrigá-la a entregar a frase-chave voluntariamente.)

* Se você criou um volume criptografado no Tails, é possível que esse volume seja lido em outros sistemas operacionais - porém, isso pode ameaçar sua segurança. Outros sistemas operacionais *não devem ser confiados* para lidar com informações sensíveis sem deixar rastros.

Fonte: 
[Documentação Tails - Create and use encrypted volumes](
https://tails.boum.org/doc/encryption_and_privacy/encrypted_volumes/index.en.html)