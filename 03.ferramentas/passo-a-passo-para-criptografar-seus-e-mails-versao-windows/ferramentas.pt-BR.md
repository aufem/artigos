---
title: 'Passo-a-passo para criptografar seus e-mails (versão Windows)'
process:
    markdown: true
    twig: true
taxonomy:
    tag:
        - criptografia
        - e-mail
        - segurança
        - Windows
        - GnuPG
        - PGP
        - ferramentas
    categoria:
        - ferramentas
---

# Como funciona GPG/PGP e a criptografia de chaves públicas: 

* Todos têm um par de chaves. Uma chave pública e uma privada.

* A chave PRIVADA do emissor da mensagem é combinada com a chave PÚBLICA de do recipiente da mensagem, para criar um problema matemático (o texto cifrado) que protege o texto da mensagem.

* Esse problema (texto cifrado) só pode ser resolvido pela chave PRIVADA do recipiente. A solução é a mensagem em somente texto.

GPG é relativamente seguro, a não ser que você perca sua chave privada – digamos, ao passar pela segurança de um aeroporto – ou tenha sua frase secreta comprometida.

## Baixando e utilizando o GPG4Win

1) Ir em [https://www.gpg4win.org/](https://www.gpg4win.org/ "https://www.gpg4win.org/") e clicar em: "Download Gpg4win".

![Imagem 04](https://cdn.pbrd.co/images/1GFOt8L6.jpg)

2) Baixar a versão mais atualizada (na caixa de diálogo, clicar em “download” ou “salvar arquivo)

![Imagem 05](https://cdn.pbrd.co/images/1GFRpFzd.jpg)

3) Verificar o arquivo com a ferramenta MD5 and SHA Checksum Utility conforme explicado em [verificar da integridade de arquivos com hashs MD5 e SHA (versão Windows)](../verificar-da-integridade-de-arquivos-com-hashs-md5-e-sha-versao-windows).
 
4) Instalar o GPG4Win. Escolha o idioma.

![Imagem 06](https://cdn.pbrd.co/images/1GFULI2A.jpg)

5) Vá avançando em “seguinte” até a terceira tela, mostrada abaixo. 

![Imagem 07](https://cdn.pbrd.co/images/1GFZpCss.jpg)

6) Marque e certifique-se que as seguintes opções estão marcadas: Kleopatra e GPA. (GpgOL é o componente para o Microsoft Outlook, deixe marcado apenas se você usa Outlook para seus e-mails). Continue avançando até terminar a instalação.

7) No Menu Iniciar, encontre GPA e abra o programa. Na primeira execução, vai aparecer a mensagem abaixo: “Você ainda não tem uma chave privada. Quer gerar uma agora ou mais tarde?” CLIQUE EM em “Do it later” (mais tarde), porque vamos configurar o programa primeiro.

![Imagem 08](https://cdn.pbrd.co/images/1GG6HVYf.jpg)

8) Vá no menu “Edit” e clique em “Preferences”

![Imagem 09](https://cdn.pbrd.co/images/1GG9U953.jpg)

9) Marque “Use advanced mode” para poder criar a chave mais segura possível.

![Imagem 10](https://cdn.pbrd.co/images/1GGdu9gL.jpg)

10) Para criar uma chave criptográfica, você vai utilizar o menu “Keys”, opção “New Key”.

![Imagem 11](https://cdn.pbrd.co/images/1GGhBcGZ.jpg)

O que você precisa:

**Algorithm:** Selecionar o algoritmo de encriptação. Há muitos debates sobre quais os melhores e mais fortes mas qualquer um deles serve. Vamos usar o “RSA” que é mais antigo e mais testado atualmente.

**Key size (bits):** Tamanho da chave. Quanto maior, mais difícil de quebrar, por isso vamos selecionar “3072”

**Name:** Nome pelo qual você quer ser identificado

**E-mail:** E-mail

**Comment:** Comentários (opcional)

**Expires:** Indica se a chave vai ter uma validade limitada 

![Imagem 12](https://cdn.pbrd.co/images/1GGr9Csy.jpg)

11) Após clicar em “ok”, você precisará colocar uma frase secreta. A segurança da sua chave depende dessa frase, então ela precisa ser o mais forte possível. 

<b>Boas senhas devem ser:</b>

1. longas e fáceis de memorizar
2. não conter nomes, datas ou outras coisas que podem ser associadas a você
3. conter ao menos um numeral, um caracter especial e uma letra minúscula/maiúscula. Cuidado com substituições comuns como "$" para "s", "@" para "a," "1" para "L", "3 para E" e por aí vai
4. não deve conter palavras comuns ou frases comuns ou que possam ser encontradas em um dicionário
5. erros de digitação intencionais, pessoais e fáceis de recordar são uma excelente forma de prevenir ataques baseados em palavras do dicionário. Por exemplo: “qando 20+ senhas nao eh Dificelt“ é muito mais forte do que “quando 20+ senhas nao é dificil!" e levaria 21 quattuordecilhões de anos para um computador quebrá-la por força bruta.</blockquote>

## Distribuição das chaves

Um dos objetivos de ter e publicar sua CHAVE PÚBLICA é para se autenticar perante os outros usuários, permitindo que eles verifiquem a autenticidade de qualquer mensagem ou dado que você assina – e para proteger/criptografar informações de forma que só você possa acessar.

Mas... como os outros usuários vão saber que aquela chave é realmente SUA? Por exemplo, se quero enviar uma mensagem para nosso teste <a href="mailto:{{'adele-en@gnupp.de'|safe_email}}">Adele</a>, usando a CHAVE PÚBLICA encontrada em [https://pgp.mit.edu/pks/lookup?search=adele-en%40gnupp.de&op=vindex&exact=on](https://pgp.mit.edu/pks/lookup?search=adele-en%40gnupp.de&op=vindex&exact=on), como eu sei que foi a VERDADEIRA Adele (test) que publicou essa chave? Seria muito fácil publicar minha PRÓPRIA chave PÚBLICA em qualquer lugar e assiná-la como Bill Gates, Beyonce, ou seja lá quem. O que lhe assegura que a chave não pertence realmente a uma dessas pessoas?

Nesse modelo de criptografia, geralmente não há uma autoridade centralizada de certificação. Em vez disso, o GPG se baseia em um modelo de redes-de-confiança onde, se alguém é confiável, essa pessoa pode atestar a identidade de um terceiro.

Por isso, além de publicar nossas chaves em um servidor público (conforme instruções abaixo), é interessante encaminhar um pedaço da nossa chave por um canal seguro. Se possível, repasse a seus amigos os últimos 8 dígitos da sua chave (são únicos) pessoalmente ou por outro meio, por exemplo, por telefone.

1) Agora que a chave foi gerada, vamos enviá-la a um servidor público, onde as pessoas poderão encontrá-la. Clicar em “Server” e em “Send Keys”. 

Clicar “Yes” na mensagem “The selected key(s) will be sent to a public key server "hkp://keys.gnupg.net"). Are you sure you want to distribute this key?” (A chave selecionada sera enviada para o servidor público "hkp://keys.gnupg.net". Você tem certeza que quer distribuir essa chave?). Você receberá uma confirmação que a chave foi enviada para o servidor (clicar em: “close”)

IMPORTANTE: após enviar a chave para um servidor público, você não pode excluí-la, a não ser que gere um “certificado de revogação”. Isso pode ser feito pelo GPA. Se você perder a sua chave, isso não poderá ser feito, então é importante fazer isso previamente e armazenar o certificado em um lugar seguro.

![Imagem 13](https://cdn.pbrd.co/images/1GGBZNEV.jpg)

2) Para encontrar as chaves de outras pessoas, vamos a um servidor público como o https://sks-keyservers.net/i/ e fazemos uma busca. Na caixa “search string” coloca-se um dos seguintes parâmetros:

- E-mail da pessoa OU

- Nome completo OU

- Key ID (últimos 8 números da chave), precedido de 0x. No caso da nossa chave, por exemplo, se coloca 0x27076BC7

Por fim, clicar em “Do the search!” (pesquisar)

![Imagem 14](https://cdn.pbrd.co/images/1GGEVZXG.jpg)

3) A chave que acabamos de gerar e publicar aparece nos resultados. Clicar no keyID para abri-la.

![Imagem 15](https://cdn.pbrd.co/images/1GGJunpu.jpg)

4) Para determinar se algo é uma chave ou uma mensagem criptografada, basta olhar os cabeçalhos. Se disser “PGP MESSAGE BLOCK” ou “BEGIN PGP MESSAGE”, quer dizer que é uma mensagem. Chaves dizem “PGP PUBLIC KEY BLOCK”, como nesse caso. 

Você tem de selecionar todo o texto a partir dos hífens até o final e copiar.

![Imagem 16](https://cdn.pbrd.co/images/1GGNd4QY.jpg)

5) Vá ao GPA e aperte “CTRL+V”. Isso vai importar a chave. Como buscamos nossa própria chave, nada foi mudado. 

## Criando e-mails

<center>
<h3 style="color:red">*** ATENÇÃO! ***</h3>

<p style="color:red">NUNCA ESCREVA SEUS E-MAILS NO NAVEGADOR (ou em qualquer janela vinculada a internet). Webmails como Gmail, Yahoo, Hotmail vão <em>salvar</em> uma cópia de rascunho do seu e-mail <u><b>antes que você possa criptografá-lo</b></u>. Somente coloque <em>mensagens criptografadas</em> (todo o bloco cifrado) no webmail. Dessa forma, o servidor de e-mails não tem acesso ao texto da sua mensagem. </p>

<p style="color:red">Use o bloco de notas ou o “Clipboard” do GPA para escrever. </p>

<p style="color:red"><em>Qualquer mensagem</em> em rascunho/enviada/recebida <u><b>é salva pelo webmail em texto simples</b></u> <em>e está fora de seu controle e <u>compromete sua privacidade</u></em>. Mesmo que você delete depois, eles ainda tem acesso a ela pelo servidor. Tenha cuidado para não contaminar suas comunicações utilizando os textos inapropriadamente. </p></center>

1) Escreva o e-mail no bloco de notas ou no Clipboard do GPA. (escrever diretamente no Clipboard poupa o trabalho de copiar e colar)

![Imagem 17](https://cdn.pbrd.co/images/1GGQAIwE.jpg)

2) Após escrever, você vai clicar em “Encrypt”.

![Imagem 18](https://cdn.pbrd.co/images/1GGTkSGo.jpg)

3) E vai: 

a)	Selecionar a chave do amigo para quem você quer mandar a mensagem. Nesse caso, estou usando a Adele, que é uma chave de teste – mas, segurando a tecla CTRL ao clicar, vou selecionar as duas chaves para permitir que eu também possa descriptografar esse texto.

b)	“Sign” (assinar) uma mensagem prova por criptografia que essa mensagem foi assinada por alguém que está no controle daquela chave e daquela frase senha.

![Imagem 19](https://cdn.pbrd.co/images/1GGXMIiS.jpg)

4) Pode aparecer a mensagem “However, it is not certain that the key belongs to that person. Do you really want to use this key” (Não há certeza que essa chave pertence a essa pessoa. Você tem certeza que quer usá-la?). Clique em “Yes”.

![Imagem 20](https://cdn.pbrd.co/images/1GH1RuGu.jpg)

5) Coloque sua frase secreta. No nosso caso, qando 20+ senhas nao eh Dificelt. 
E teremos nossa mensagem criptografada pronta para ser colada no e-mail.

![Imagem 21](https://cdn.pbrd.co/images/1GH5sIpD.jpg)


## Descriptografando e-mails

1) Copiar o bloco inteiro com a mensagem

![Imagem 22](https://cdn.pbrd.co/images/1GH8qwRL.jpg)

2) Em seguida:

a)	Colar no clipboard

b)	“Decrypt” (descriptografar)

c)	Coloque a frase senha da sua chave secreta

![Imagem 23](https://cdn.pbrd.co/images/1GHbUG9T.jpg)

3) E... voilà! Temos a mensagem em somente texto (o que só é possível se sua frase secreta estiver correta).

![Imagem 24](https://cdn.pbrd.co/images/1GHeHENY.jpg)


## Testando

adele-en@gnupp.de é uma chave teste automatizada. As dezenas de links abaixo dela são chaves de pessoas que ASSINARAM ESSA CHAVE (e não uma mensagem). Esse é um método em que o DONO DA CHAVE X certifica que o DONO DA CHAVE Y é quem ele(a) diz que é.

![Imagem 25](https://cdn.pbrd.co/images/1GHi6wms.jpg)

1) Você pode pegar a sua chave PÚBLICA (“PGP PUBLIC KEY BLOCK”) e colar em um novo e-mail a ser enviado para adele-en@gnupp.de. Isto é compartilhar sua chave sem a necessidade de encaminhá-la a um servidor.

![Imagem 26](https://cdn.pbrd.co/images/1GHls1As.jpg)

2) Ela responderá com uma mensagem criptografada. Copie no Clipboard, coloque a senha da sua CHAVE PRIVADA e leia e mensagem! (você vai precisar de um tradutor, se não souber inglês, mas uma das coisas você deve conseguir identificar, ao menos.)

Parabéns! Você concluiu esse tutorial com sucesso.

A partir de agora você pode, também, assinar seus próprios e-mails para facilitar a difusão da criptografia e dar possibilidade para os seus contatos que já usam esse método entrarem em contato com você. Busque nas suas caixas de entrada contatos que já assinam seus e-mails e informe-os que agora você tem uma chave. 

Boa sorte!

Crédito das instruções: [Cidadão Quatro](http://naofo.de/5ir2)