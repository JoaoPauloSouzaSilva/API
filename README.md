<h1>🔧 Criando minha primeira API</h1>

<h3>📃 Descrição do projeto: </h3>
<hr>
<p>
  O projeto em questão foi muito importante para desenvolver meu conhecimento com relação a API, desde de o que significa, para que serve, como utilizar, como criar, o que seria a API rest, como unir com um banco de dados e entre outros assuntos. A partir desse estudo, foi possível criar minha primeira API que representa a lista de alunos de uma escola, para o desenvolvimento do projeto foi utilizado o Python, o Django juntamente como o Sqlite, por meio do Visual Studio Code. Durante a criação, tive algumas dificuldades, como: a utilização de comandos no terminal, tendo em vista que não possuía costume em utilizar, a utilização do Django, pois já tinha conhecimento da existência do mesmo, mas esse foi meu primeiro contato direto, entre outras dificuldades. Entretanto, por mais que tive algumas dificuldades, fiquei deslumbrado com os "poderes mágicos" do Django, principalmente com a possibilidade de criar uma super usuário, em outras palavras, um admin que consegue administrar todo o conteúdo da API.
</p>
<br>

<h3>🔨 Ferramentas utilizadas: </h3>
<hr>
<p>
  Para desenvolver este projeto, é necessário um editor de código, recomendo o Visual Studio Code, que pode ser baixado gratuitamente. Por precaução, é necessário ter um navegador web instalado em seu computador, nesse projeto foi usado o Chrome. Além desses, será necessário a instalação de algumas dependências e será utilizadas algumas ferramentas online, essas dependências e ferramentas são descritas e explicadas na seção "Como replicar o projeto", visto que desse modo ficará mais simples a compreensão.
</p>

  <h4>Visual Studio Code v1.76</h4>
  <ul>
      <li>Acesse o site oficial do Visual Studio Code em https://code.visualstudio.com/.</li>
      <li>Clique no botão "Download" na página inicial.</li>
      <li>Escolha o download apropriado para o seu sistema operacional (Windows, Mac ou Linux).</li>
      <li>Após o download, execute o arquivo de instalação e siga as instruções na tela.</li>
  </ul>

  <h4>Google Chrome v110</h4>
  <ul>
      <li>Acesse o site oficial do Google Chrome em https://www.google.com/chrome/</li>
      <li>Clique no botão "Download" (ou "Baixar") para baixar o instalador do Chrome para o seu sistema operacional (Windows, Mac ou Linux)</li>
      <li>Após o download, execute o arquivo de instalação e siga as instruções na tela.</li>
  </ul>
<br>

<h3>🔁 Como replicar o projeto: </h3>
<hr>
<p>
  Inicialmente deve ser criado uma pasta para colocarmos a nossa API dentro, no exemplo a pasta vai ser chamada de API. Agora iremos criar o ambiente virtual, no terminal do vscode, o botão está localizado na parte superior esquerda, após aberto, digite o comando:

  <p>
    <strong>
      >>> python3 -m venv ./venv
    </strong>
  </p>

  ⚠️ É importante ressaltar que sempre após a escrita de um comando no terminal, deve-se pressionar o enter, para que o comando seja executado.

  ❌ Nesse momento, no meu projeto deu um erro pois não havia instalado o python 3, caso o mesmo aconteça, na mensagem de erro irá aparecer um link para baixar, aperte Ctrl e clique nele e abrirá a opção de instalar, após o fim da instalação, reescreva o comando anterior ou aperte a tecla de seta para cima e pressione enter. Se aparecer uma pasta chamada “ venv ” dentro da pasta API no caso do exemplo, significa que o ambiente virtual foi criado.

  Agora devemos ativar a venv, também no terminal deve-se digitar o comando:

  <p>
    <strong>
      >>> venv/Scripts/activate
    </strong>
  </p>

  ⚠️ É importante ressaltar que esse comando é para o sistema operacional windows, caso o sistema operacional seja o mac ou linux, use o comando ( <strong> source venv/bin/activate </strong> ).

  Após apertar o enter, na nova linha que aparecer, deve conter como primeira palavra o (venv), isso significa que o ambiente virtual foi ativado. 

  Agora iremos iniciar a instalação das dependências do ambiente virtual, primeiramente instalaremos o Django com o seguinte comando 

  <p>
    <strong>
      >>> pip install django
    </strong>
  </p>

  Possivelmente o terminal indicará um upgrading, e lhe dará o comando, o mesmo estará amarelo, caso não encontre o comando para o upgrading, digite o seguinte comando ( <strong> pip install –upgrade pip </strong> ) 

  Para termos certeza de que o django foi instalado, usaremos o seguinte comando para visualizarmos quais as dependências que o projeto possui

  <p>
    <strong>
      >>> pip freeze 
    </strong>
  </p>

  O terminal retornará uma lista  de dependências e é necessário que o django esteja presente para prosseguirmos. 

  Agora iremos criar a nossa aplicação, a partir do comando  

  <p>
    <strong>
      >>> django-admin startproject config .
    </strong>
  </p>

  O <strong> django-admin </strong> será responsável por todas as configurações da nossa aplicação, para confirmarmos que deu tudo certo, dentro da nossa pasta API, terá uma nova pasta chamada config e um arquivo .py chamado manage. 

  Para rodar o nosso servidor devemos utilizar o comando 

  <p>
    <strong>
      >>> python manage.py runserver .
    </strong>
  </p>

  ❌ Após apertar enter, aparecerá uma mensagem dizendo que existem algumas migrações pendentes, mais a frente resolveremos esse ponto. 

  ⚠️ É importante ressaltar que quando instalamos o Django a gente já terá o sqlite integrado nele, sendo assim, não vamos precisar instalar um outro banco de dados. 

  Juntamente com a mensagem citada anteriormente, aparecerá no terminal o link para o servidor que está na nossa máquina, entretanto, o mesmo está em inglês, para mudarmos isso, vamos seguir o seguinte passo a passo

  Dentro da nossa pasta <strong> API </strong>, vamos acessar a aba <strong> config </strong> e o arquivo <strong> settings.py </strong>, nesse arquivo terá todas as configrações da nossa aplicação, devemos procurar dentro dele duas linhas a primeira é <strong> LANGUAGE_CODE = ‘en-us’ </strong> e mudar para <strong> LANGUAGE_CODE = ‘pt-br’ </strong> e a segunda é <strong> TIME_ZONE = ‘UTC’ </strong> e mudar para <strong> TIME_ZONE = ‘America/Sao_Paulo’ </strong>, após essas mudanças, quando atualizarmos a página do servidor, ela estará em portugues Brasil, essas alterações são importantes pois vai manter toda nossa infraestrutura em portugues.

  As mudanças ficaram da seguinte forma

  <p>
    <strong> LANGUAGE_CODE = ‘en-us’ </strong> → <strong> LANGUAGE_CODE = ‘pt-br’ </strong>
  </p>

  <p>
    <strong> TIME_ZONE = ‘UTC’ </strong> → <strong> TIME_ZONE = ‘America/Sao_Paulo’ </strong>
  </p>


</p>