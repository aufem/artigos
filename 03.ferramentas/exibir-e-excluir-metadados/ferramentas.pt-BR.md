---
title: 'Exibir e excluir metadados'
metadata:
    keywords: 'metadados, metadados imagem, metadados arquivos, remover metadados, MAT'
    'og:title': 'Aufem | Exibir e excluir metadados'
    author: AuFem
    'og:description': 'Sobre metadados de imagens e arquivos - como exibi-los e excluí-los.'
    'twitter:title': 'Aufem | Exibir e excluir metadados'
    'twitter:description': 'Sobre metadados de imagens e arquivos - como exibi-los e excluí-los.'
taxonomy:
    author:
        - aufem
    tag:
        - privacidade
        - segurança
        - ferramentas
        - tutorial
        - metadados
        - fotografia
        - arquivo
    categoria:
        - ferramentas
featherlight:
    active: true
---

** Conteúdo **

[Tipos de metadados](#tipos)  
[Exibir os metadados de uma imagem](#exibir)  
[Como remover metadados de uma imagem](#remover-metadados-imagem)  
[Como remover metadados de um arquivo](#remover-metadados-arquivo)  

Como já vimos no artigo "[Por que a privacidade é importante?](/blog/por-que-a-privacidade-e-importante)", quase toda ação que realizamos no mundo virtual carrega consigo informações, metadados que são constantemente utilizados por empresas, governos e até mesmo pessoas de má fé não apenas para nos identificar, mas também para rastrear e registrar nosso comportamentos online. Agora, vamos ver como verificar os metadados de um arquivo que vai ser publicado online e algumas técnicas para remover essas informações, tornando mais difícil nossa identificação e rastreamento.

Um arquivo normalmente carrega consigo muitos dados. Uma imagem, por exemplo, não apenas os pixels que são necessários para sua exibição, mas traz também informações que servem para descrever *e* identificar a imagem. Essas informações é o que chamamos de metadados.

<a id="tipos"></a>Os metadados podem ser:

a) internos: embutidos no arquivo, em formatos como JPEG2000 ou RAW proprietários, por exemplo; ou

b) externos: fora do arquivo, em um sistema de gerenciamento digital, ou em um arquivo "anexado" (XMP ou baseado-XML)

Nem todos os arquivos ou imagens possuem o mesmo tipo de metadados. Os formatos mais comuns de arquivos de imagem geralmente trazem consigo:

- EXIF :

Esses metadados são auto-gerados pelas câmeras e por outros dispositivos de captura, principalmente em arquivos JPEG e TIFF. A principal função do EXIF é gravar as informações da câmera no momento da captura no arquivo de imagem. Incluem-se no EXIF: fabricante, modelo da câmera, número de série, data e hora da captura, velocidade de exposição, aperture, as lentes utilizadas, configurações de ISO e até a informação de GPS do dispositivo (!). Pode incluir até outros detalhes técnicos como balanço de luz e a distância que a câmera estava do objeto no momento da captura.  

- IPTC-IIM :

Esse é um padrão mais antigo e, com ele, informações como o nome de quem tirou a foto, direitos autorais, localização, legendas e descrição podem ser escritas de forma automática ou manual. É armazenado de em binários (sequência de zeros e uns). Pode ser utilizado em imagens JPEG, TIFF, JPEG2000, PSD ou PNG. GIF e PCX não suportam esse padrão.

- IPTC Core : 

Atualização do IPTC-IIM, também pode receber muitos dados de forma automática ou manual, que embute essas informações utilizando XML ([Extensible Markup Language](http://www.w3.org/XML/)) e RDF ([Resource Description Framework](http://www.w3.org/RDF/))

- XMP:

Padrão introduzido pela Adobe com o Photoshop 7. Como o IPTC Core, é produzido com XML e RDF.

Esses padrões coexistem nas imagens - em alguns casos, os dados podem se repetir ou se sobrepor. Muitas vezes, os atributos de um padrão acabam podendo ser lidos/suportados por outros padrões. Quer ter mais uma ideia de todos os campos que podem ser incluídos nos metadados de uma imagem? Dá uma olhada nessa lista (em inglês):
[http://www.photometadata.org/meta-resources-field-guide-to-metadata](http://www.photometadata.org/meta-resources-field-guide-to-metadata)

## Exibir os metadados de uma imagem <a id="exibir"></a>

Se você quer simplesmente ter ideia de quais metadados estão escritos em uma imagem, a maioria dos softwares de exibição de imagens geralmente lhe informam isso - embora, muitas vezes, não seja uma visão ampla e detalhada. 

Caso isso seja essencial para sua segurança, não confie que apenas a meia dúzia de dados exibida pelas propriedades do arquivo no Windows estarão lhe mostrando todas as informações contidas em uma imagem. Em vez disso, considere...

## Como remover metadados de uma imagem <a id="remover-metadados-imagem"></a>

É possível remover metadados da imagem - e, em certas circunstâncias, é extremamente recomendável fazê-lo, como em casos de denúncias que a autora da imagem necessite o anonimato para sua própria proteção.

A exemplo do [Ver Exif](http://www.verexif.com/), existem sites que oferecem ferramentas online, no próprio navegador, para remover metadados das imagens. Entretanto, como isso envolve transmitir a imagem com essas informações pela internet e para uma terceira parte, o mais *recomendado* é realmente fazer essa tarefa localmente. Como?

O ExifTool é um software livre que trabalha com quase todo tipo de imagem. Ele tem para Linux, Windows e Mac OS X e está disponível para download nesse endereço: [http://www.sno.phy.queensu.ca/~phil/exiftool/](http://www.sno.phy.queensu.ca/~phil/exiftool/)

#### Instalar Image-ExifTool no GNU/Linux e em plataformas Unix

* Baixar o programa no site. O arquivo será algo como "Image-ExifTool-##.##.tar.gz"

* [Verificar as somas SHA e MD5 do arquivo](/ferramentas/verificar-da-integridade-de-arquivos-com-hashs-md5-e-sha-versao-windows)

No Terminal:  

    $ cd diretorio-do-download    
    $ gzip -dc Image-ExifTool-##.##.tar.gz | tar -xf -   
    $ cd Image-ExifTool-##.##

[você vai substituir ##.## pela versão que está no arquivo que baixou]

Com isso, você já pode executar o exiftool escrevendo:

    $ exiftool nome-da-imagem.extensao-da-imagem

Ex.:

    $ exiftool DSC0001.jpg

ou com a localização em outra pasta/diretório:

    $ exiftool '/media/amnesia/pendrive/imagens/DSC0001.jpg'

Exibindo os metadados da imagem, você decide se e quais quer remover.   

![Foto de uma flor](../../../images/flower.jpg?lightbox=1024&cropResize=300,300)

Para a imagem acima, veja nesse arquivo texto os dados que o exiftool deu: [Metadados originais](https://naoenoveladasoito.com.br/files/flower-data.txt)

Para remover tudo que fosse possível, usa-se o comando:

     $ exiftool -exif:all= '/home/amnesia/Desktop/flower.jpg' 
     Resultado: 1 image files updated

A foto ficou da seguinte forma: [Com metadados removidos](https://naoenoveladasoito.com.br/files/flower-removed.txt)

Como pode perceber, as informações mais importantes como, inclusive, a localização da foto, foram removidas. Não tem como se garantir que os metadados de uma imagem serão *todos* removidos quando se utiliza o comando para remover "all" (tudo). *Em geral*, ele funciona bem com arquivos JPEG, pode não acontecer o mesmo com outros formatos.

## Como remover metadados de um arquivo <a id="remover-metadados-arquivo"></a>

E se você quer remover metadados de um arquivo que não é uma imagem? Por exemplo, uma gravação de áudio? Para isso temos...

#### MAT (Metadata Anonymisation Toolkit ou Kit de Ferramentas de Anonimização de Metadados) 

Arquivos atualmente suportados pelo MAT: 

- Imagens: png, jpg, jpeg, tif, tiff,   
- Documentos: odt, odx, ods, docx, pptx, xlsx, pdf  
- Áudio e vídeo: mp3, mp2, mp1, ogg, flac  
- Torrent: torrent  
- Arquivos Tape: tar, tar.bz2  

**Como se consegue o MAT?** 

MAT já vem com o [Tails](https://tails.boum.org/blueprint/doc/mat/), mas também está disponível como pacote Debian/Ubuntu, no repositório GIT, e no [site oficial do MAT](https://mat.boum.org/)

**Como utilizar o MAT?**

O MAT tem uma interface gráfica extremamente fácil de se utilizar.

![Interface gráfica do MAT](../../../images/interface_MAT.png)

Você adiciona o arquivo clicando em "Add", MAT vai dar o estado do arquivo (Dirty quer dizer que os metadados não foram limpos), você clica em "clean" (limpar) e... pronto. Se quiser exibir metadados no MAT *antes* de excluí-los, basta clicar no nome do arquivo.

![Exibir metadados no MAT](../../../images/exibindo_metadados_no_MAT.png)

Esse artigo foi mais uma parte da introdução à questão dos metadados. Recomendamos sempre que você leia mais sobre o assunto e aprimore esse conhecimento, ainda mais se sua segurança pessoal depende disso.


Fontes:

[GeoIPTC - geocode your images using metadata standards](http://peccatte.karefil.com/GeoIPTC/EN/)

[The Top 12 Myths about Embedded Photo Metadata](http://www.controlledvocabulary.com/blog/top-metadata-myths.htmls)

[MAT: Metadata Anonymisation Toolkit](https://mat.boum.org/)