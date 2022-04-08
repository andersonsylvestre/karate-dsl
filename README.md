# Karatê DSL
O Karate DSL é uma ferramenta desenvolvida em Java que permite o desenvolvimento e execução de testes de APIs utilizando uma sintaxe semelhante à do Gherkin. Ela foi disponibilizada recentemente (a pouco mais de dois anos) e vem crescendo em popularidade desde então. Para maiores esclarecimento acesse o site do [Karatê-Dsl](https://github.com/karatelabs/karate)

## O que vamos usar

* Java SE Development Kit 8u202
* VSCode
* Karatê

## Requisitos de hardware

Para a instalação do Karatê-Dsl estou usando uma configuração de hardware:

* Processador Intel Core I5 7ª Geração
* Memória de 16 GigaBits
* HD de um TG
* Sistema operacional Windows 10 Pró

## Instalação do JDK 8 (Windows 10)

Para fazer a instalação do **JDK 8** vá ao site da Oracle e baixe [JDK8](https://www.oracle.com/java/technologies/downloads/#jdk18-windows) e siga os seguintes passos para instalação do JDK 8.

Após baixar o JDK 8, vá com o botão direito do mouse e executa o JDK 8 como administrador.

* Inicie a intalação do Java JDK 
* Clique no botão Next.
* Aguarde a finalização da instalação java JDK 8

### Variaveis de ambiente no windows ###

Agora verifique a existencia da variavel **JAVA_HOME**. Abrindo o **CMD** e digitando o seguente comando:

**echo %JAVA_HOME%**

A saida deve ser igual a esta:

**C:\Program Files\Java\jdk-18**

Se caso não encontrar deve-se entrar nas variaveis de ambiente e fazer o cadastro exemplo:

* Vá com o botão direito do mouse em **Este Computador** e clique em propriedades
* No lado esquerdo encontra-se link **Configurações avançadas** do sistema clique nesta opção
* Após abrir a tela da propriedade do Sistema clique no botão **Variaveis de Ambiente...**
* Após abrir a tela de Variáveis de ambiente clique no botão novo na opção **Variáveis de sistema**
* Após abrir a tela Nova variáveis de sistema insire o Nome da variável com **JAVA_HOME** e o valor da variável **C:\Program Files\Java\jdk-18**
* Após feito este procedimento clique no botão **OK** e reinicie o computador.

Agora abra novamente o **CMD** e digite:

**"%JAVA_HOME%"\bin\java -version**

O resultado deve ser a versão do Java como no exemplo abaixo

**java version "18" 2022-03-22 <br>
Java(TM) SE Runtime Environment (build 18+36-2087) <br>
Java HotSpot(TM) 64-Bit Server VM (build 18+36-2087, mixed mode, sharing)**

Agora vamos configurar a variavel de ambiente com **"%JAVA_HOME%"\bin**


* Vá com o botão direito do mouse em **Este Computador** e clique em propriedades
* No lado esquerdo encontra-se link **Configurações avançadas** do sistema clique nesta opção
* Após abrir a tela da propriedade do Sistema clique no botão **Variaveis de Ambiente...**
* Após abrir a tela de Variáveis de ambiente clique no botão novo na opção **Variáveis de sistema**
* Agora clique no botão **Novo** em Variáveis de usuário para <user> e de um duplo clique na opção Path.
* Após abrir a tela Editar a variável de ambiente clique no botão **Novo** e informe o caminho **%JAVA_HOME%\bin** e clique no botão **OK** e feche a tela de variaveis de ambiente.

## Instalação do JDK 8u65 (Mac OS) ##

Para fazer a instalação do **JDK 8u65** vá ao site da Oracle e baixe [JDK8](https://www.oracle.com/java/technologies/downloads/#jdk18-mac) e siga os seguintes passos para instalação do JDK 8u65.

* Faça download do arquivo jre-8u65-macosx-x64.dmg.
* Revise e concorde com os termos do contrato de licença antes de fazer o download do arquivo.
* Clique duas vezes no arquivo .dmg para inicializá-lo
* Clique duas vezes no ícone do pacote para iniciar o Assistente de instalação
* O Assistente de Instalação exibe a tela de instalação Bem-vindo ao Java. Clique em **Próximo**
* A Oracle tem parceria com empresas que oferecem vários produtos. O instalador pode apresentar a você a opção para instalação desses programas durante a instalação do Java. Após assegurar que os programas desejados sejam selecionados, clique no botão Próximo para continuar a instalação.

* Problemas Conhecidos <br>
[macosx] Problemas de acessibilidade (a11y) à tela de ofertas do patrocinador
Os usuários que utilizam o teclado para acessar interfaces de usuário no instalador do Java não poderão acessar hiperlinks e caixas de seleção nas telas de ofertas de add-on do software. Como solução alternativa para definir preferências relativas ao software de add-on na interface, os usuários podem desativar essas ofertas no painel de controle do Java ou especificar SPONSORS=0 na linha de comandos. Para obter mais informações, consulte as Perguntas Frequentes em Install Java without sponsor offers.

* Após a conclusão da instalação, uma tela de confirmação será exibida. Clique em Fechar para finalizar o processo de instalação.

* **Teste da instalação** <br>
Para testar se o Java foi instalado e está funcionando corretamente no computador, execute este [applet de teste.](https://www.java.com/pt-BR/download/uninstalltool.jsp)

### Configurando as variaveis de ambiente ###

* Iniciar o terminal
* Executar o comando **cd** ~
* Executar o comando vim **.bash_profile**
* Ativar o modo de edição de texto teclando a letra **i**
* Editar o arquivo para configurar as variáveis de ambiente. O arquivo deverá ficar da seguinte forma:

&#160; **export JAVA_HOME=`/usr/libexec/java_home`** <br>
&#160; **export PATH=$JAVA_HOME/bin:$PATH**

* Sair do modo de edição teclando ESC
* Salvar o arquivo teclando :wq e pressionando enter

## Baixando e configurando o Maven ##

* Baixar a versão binária zipada do Maven (-bin.zip). [Download Maven](https://maven.apache.org/download.cgi)
* Extrair o zip baixado em alguma pasta de sua preferência. Sugestão: Pasta Documents do seu usuário no sistema.

### Adicionando o Maven nas variáveis de ambiente ###

Para o **Windows:** <br>
* Adicionar o local da pasta extraída do Maven na variável de ambiente PATH, da seguinte forma: **C:\Users\nomeusuario\Documents\apache-maven-3.8.4** Adeque o diretório para que seja equivalente ao local onde foi feita a instalação do Maven (pasta do Zip extraído). Se atente também a versão do Maven, pois isso pode alterar o nome do diretório.
  
Configurando a variavel de ambiente
  
* Vá com o botão direito do mouse em **Este Computador** e clique em propriedades
* No lado esquerdo encontra-se link **Configurações avançadas** do sistema clique nesta opção
* Após abrir a tela da propriedade do Sistema clique no botão **Variaveis de Ambiente...**
* Após abrir a tela de Variáveis de ambiente clique no botão novo na opção **Variáveis de sistema**
* Agora clique no botão **Novo** em Variáveis de usuário para <user> e de um duplo clique na opção Path.
* Após abrir a tela Editar a variável de ambiente clique no botão **Novo** e informe o caminho **C:\Users\nomeusuario\Documents\apache-maven-3.8.4** e clique no botão **OK** e feche a tela de variaveis de ambiente.
  
Após o termino da configuração reinicie o **CMD** e execute o seguinte comando.

**mvn --version**

Para o **Mac OS**:
* Iniciar o terminal
* Executar o comando **cd** ~
* Executar o comando **vim .bash_profile**
* Acrescentar as variáveis do Maven:

* **export JAVA_HOME=`/usr/libexec/java_home`** <br>
**export MAVEN_HOME=~/Documents/apache-maven-3.8.4** <br>
**export PATH=$JAVA_HOME/bin:$PATH** <br>
**export PATH=$MAVEN_HOME/bin:$PATH**

* Sair do modo de edição teclando ESC
* Salvar o arquivo teclando :wq e pressionando enter




## Instalação e configuração do VSCode (Windows 10)

Para fazer a instalação do **VSCode** vá até o site [VSCode](https://code.visualstudio.com/) e baixe o executavel.   

Em seguida, execute o instalador baixado e siga as instruções na tela, não esqueça de marcar a opção "Add to Path" para adicionar o Visual Studio Code nas variáveis de ambiente.

Após a instalação abra o **CMD** e digite o seguinte comando:

**code --version**

O resultado deve ser a versão do VSCode como no exemplo abaixo

Exemplo

  1.66.0 <br>
  e18005f0f1b33c29e81d732535d8c0e47cafb0b5 <br>
  x64

### Configurando o VSCode ###

Abra o VSCode instale o seguintes plugins

* Cucumber(Gherkin)
* Language Support for Java
* Maven for Java
* VSCode-icons
* Hyper Term Theme

## Instalação e configuração do Karatê-Dsl ##
  
Para instalar e configurar o Karatê-DSL e nessa entrar no projeto do [Karatê-DSL](https://github.com/karatelabs/karate#quickstart) e pegar o comando de instalação do **Maven** que é igual a este, pode ser que mude a versão.
 
``` 
 mvn archetype:generate \
-DarchetypeGroupId=com.intuit.karate \
-DarchetypeArtifactId=karate-archetype \
-DarchetypeVersion=1.1.0 \
-DgroupId=com.mycompany \
-DartifactId=myproject
```

 Os paramentros que é aconselhavel alteração **DgroupId** colocar o nome da empresa, e **DartifactId** e este parametro colocar o nome do projeto exemplo **projetoKarate**

**Com alteração**
```
 mvn archetype:generate \
-DarchetypeGroupId=com.intuit.karate \
-DarchetypeArtifactId=karate-archetype \
-DarchetypeVersion=1.1.0 \
-DgroupId=com.nomedaempresa \
-DartifactId=projetoKarate  
```  
  
  
 Abra o **VSCode**, dentro do VSCode abra o terminal se atente para alterar para de **powershell** para o **cmd** e execute o comando acima.

  ```
  INFO] Scanning for projects...
[INFO] 
[INFO] ------------------< org.apache.maven:standalone-pom >-------------------
[INFO] Building Maven Stub Project (No POM) 1
[INFO] --------------------------------[ pom ]---------------------------------
[INFO] 
[INFO] >>> maven-archetype-plugin:3.2.1:generate (default-cli) > generate-sources @ standalone-pom >>>
[INFO] 
[INFO] <<< maven-archetype-plugin:3.2.1:generate (default-cli) < generate-sources @ standalone-pom <<<
[INFO]
[INFO]
[INFO] --- maven-archetype-plugin:3.2.1:generate (default-cli) @ standalone-pom ---
[INFO] Generating project in Interactive mode
[INFO] Archetype repository not defined. Using the one from [com.intuit.karate:karate-archetype:1.1.0] found in catalog remote
[INFO] Using property: groupId = com.nomedaempresa
[INFO] Using property: artifactId = projetokarate
Define value for property 'version' 1.0-SNAPSHOT: :
```
Na opção version 1.0-SNAPSHOT informe o numero da versão **exemplo: 1.0**                                                                                                            
```
INFO] Scanning for projects...
[INFO] 
[INFO] ------------------< org.apache.maven:standalone-pom >-------------------
[INFO] Building Maven Stub Project (No POM) 1
[INFO] --------------------------------[ pom ]---------------------------------
[INFO] 
[INFO] >>> maven-archetype-plugin:3.2.1:generate (default-cli) > generate-sources @ standalone-pom >>>
[INFO] 
[INFO] <<< maven-archetype-plugin:3.2.1:generate (default-cli) < generate-sources @ standalone-pom <<<
[INFO]
[INFO]
[INFO] --- maven-archetype-plugin:3.2.1:generate (default-cli) @ standalone-pom ---
[INFO] Generating project in Interactive mode
[INFO] Archetype repository not defined. Using the one from [com.intuit.karate:karate-archetype:1.1.0] found in catalog remote
[INFO] Using property: groupId = com.nomedaempresa
[INFO] Using property: artifactId = projetokarate
Define value for property 'version' 1.0-SNAPSHOT: :1.0
```
