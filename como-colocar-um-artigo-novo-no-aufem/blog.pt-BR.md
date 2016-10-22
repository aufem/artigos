---
title: 'Como colocar um artigo novo no AuFem'
---

1. Ir no endereço:
[https://naoenoveladasoito.com.br/admin](https://naoenoveladasoito.com.br/admin)

2. Logar com seu usuário e senha. Se você não tem usuário e senha ainda, arrume um e-mail com GPG para que possa ser enviado.

3. Clicar em "Pages".

4. Na barra superior, à direita, clicar em "Add Page".

5. Por favor, preste muita atenção nas configurações necessárias:
	* Você vai colocar: "Page title" (título do artigo)
	* Folder name vem automático, vai ser a URL do artigo
	* Parent page E Page File *DEVEM SER IGUAIS*! **Isso é onde o artigo vai ser publicado.** Se for no "Blog", deve selecionar "Blog" nos dois campos, para que vá para a seção certa e com o "template" certo. 
		Blog abrange todo e qualquer artigo, deixemos o "Ferramentas" para apresentação e dicas de softwares, plugins e outras coisas e o "Aprenda" para dicas de cursos e treinamentos.  Se você tem dúvidas sobre onde deve ir o seu artigo, pode consultar o [nosso pad](https://pad.riseup.net/p/au-23femme) ou perguntar para nós.
	* Visible: pode deixar em "Auto" mesmo.
	* Clicar em "Continue"

6. Vai abrir a parte para você criar o artigo. O título já está em "Title" (e não precisa ser repetido no corpo do texto). O texto deve ser formatado em Markdown. Algumas dicas:

a) Para novo parágrafo, basta dar dois ENTER (ou seja, deixar uma linha em branco).

b) Itálico: coloque * (asterisco) antes e depois da palavra ou parágrafo.

c) Negrito: ** (dois anteriscos) antes e depois do parágrafo.

d) Lista numerada: número e um parágrafo imediatamente depois.

e) Lista não-numerada: pode usar * ou - antes de cada item.

f) Para títulos: usa-se # de acordo com o nível do título. O título do post é formatado automaticamente com h1, ou seja, é como se ele tivese apenas # no início. Sugiro que começe os subtítulos com ##. Vai até ###### (h6), que é o menor dos subtítulos.

g) Linha horizontal: --- (vários traços ou asteriscos + ENTER)

h) Para uma citação com uma barra vertical à esquerda (como no manifesto): coloque um > no início do parágrafo.
> Citação com barra vertical à esquerda

i) Para uma citação no texto, com duas barras horizontais antes e depois: Coloque < cite > no início da frase ou parágrafo - e feche-a com < /cite > no final, sem os espaços. Por exemplo:
<cite>Citação no texto</cite>

j) Código: se você quer mostrar algum código, para que ele não seja interpretado pelo site em si - e, sim, exibido, precisa colocar 4 espaços antes de cada linha do código.

<code>Isso é um código</code>

### Para colocar um link (sempre remova os espaços): 
	
* Link externo:
<code>[texto do link]( url )</code>

* Link interno em outra categoria:
<code>[manifesto]( ../manifesto )</code>
<code>[TEXTO]( ../ferramentas/alternativas-ao-google )</code>

(você tem de pegar o que tem depois de [https://naoenoveladasoito.com.br/](https://naoenoveladasoito.com.br/) na página em si, por exemplo)

* Link interno na mesma categoria:
<code>[TEXTO]( redes-sociais-livres )</code>

(você tem de pegar o que tem depois de blog/ na página específica, por exemplo)

### Para colocar uma imagem:

Primeiro, por favor cuide o tamanho da imagem, não coloque imagens muito pesadas com mais de 1mb, por exemplo, se possível, sempre converta as imagens para que sejam o mais leves possíveis. Você pode fazer isso usando um software como GIMP ou Inkscape. Formatos de imagem suportados: jpg, jpeg, png, svg, gif

* Se estiver em outro site:
![SEMPRE escrever aqui um texto alternativo da imagem, para quem não pode vê-la ou se houver erro no carregamento]( URL-DA-IMAGEM )

* Se estiver no seu computador:
Abaixo da caixa de texto, tem algo chamado "Page Media". Ali diz "Drag files here to upload". Ou seja, arraste os arquivos para cá para carregá-los. Você pode fazer isso ou clicar ali - no segundo caso, abre janela para você navegar até a localização da imagem no seu computador. Clicar em "Open/Abrir". A imagem vai ser carregada no servidor. Posicione o cursor no texto onde você quer inserir a imagem. Passe o mouse sobre a imagem, aparece "Insert" e você clica ali. Com isso vai aparecer algo assim no seu texto:
![]( Nome da imagem.png )
Você vai fazer o seguinte: 
![SEMPRE escrever aqui um texto alternativo da imagem, para quem não pode vê-la ou se houver erro no carregamento]( deixar isso aqui como está )


Depois de escrito o artigo, você pode clicar naquele "olho" da barra de ferramentas para ver como vai ficar a visualização do mesmo. (Para voltar e continuar editando, clicar no botão à esquerda do olho, que volta ao markdown)

Depois, vá em "Options", onde você vai poder selecionar algumas coisas, como por exemplo:

* Metadata

Você clica na caixinha, escreve "keywords" em "Key" e coloca algumas palavras-chave. Essas palavras-chave serão usadas pelos sites de busca para encontrar o seu artigo. Use minúsculas e separe com vírgula

* Categoria

Aqui você vai colocar a mesma coisa que colocou em "Parent page", ou seja, a que parte do site pertence o seu post. "Blog", "Ferramentas", "Aprenda", etc.

* Tag

As tags/etiquetas aplicáveis a seu post. Não precisam ser muitas, mas algumas é interessante para as usuárias buscarem posts relacionados. A caixinha ali já lhe dá algumas sugestões para selecionar as aplicáveis (podem ser mais de uma). 

* Author

Você pode escrever ou selecionar seu nome e de quem mais contribuiu com o artigo


Depois de tudo isso, é só clicar em "Salvar" e... voilà! Seu post estará no site.

Não esqueça de clicar em "Logout" no painel de administração do AuFem!