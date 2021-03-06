# Karatê-DSL #
O Karatê-DSL é uma ferramenta desenvolvida em Java que permite o desenvolvimento e execução de testes de APIs utilizando uma sintaxe semelhante à do Gherkin. Ela foi disponibilizada recentemente (a pouco mais de dois anos) e vem crescendo em popularidade desde então. Para maiores esclarecimento acesse o site do [Karatê-Dsl](https://github.com/karatelabs/karate)

## O que vamos usar ##

* Java SE Development Kit 8u322b06
* Maven apartir da versão 3.8.5
* VSCode
* Karatê-DSL

## Instalação do JDK 8 (Windows 10) ##

Para fazer a instalação do **JDK 8** vá ao site da Oracle e baixe [JDK8](https://www.azul.com/downloads/?package=jdk#download-openjdk) e procure a versão **8u322b06** para o Windows na arquitetura x86 64 bits e baixe **.MSI** siga os seguintes passos para instalação do JDK 8.

Após baixar o **zulu8.60.0.21-ca-jdk8.0.322-win_x64**, vá com o botão direito do mouse e executa como administrador.

* Na inicialização altere a configuração para setar o **JAVA_HOME** nas varialveis de ambiente.
* Também altere a configuração **JavaSoft** para registrar o Java na Oracle.
* Agora clique no botão **"Next"**.
* Clique no botão **"Install"**.
* Aguarde a finalização da instalação java zulu8.60.0.21-ca-jdk8.0.322-win_x64.
* Após a instalação clique no botão **"Finish"**.

Agora abra o terminal e digite o comando a baixo para ver se o Java foi instalado e sua versão.

```
java -version
```

O resultado do comando:

**openjdk version "1.8.0_322"** <br>
**OpenJDK Runtime Environment (Zulu 8.60.0.21-CA-win64) (build 1.8.0_322-b06)** <br>
**OpenJDK 64-Bit Server VM (Zulu 8.60.0.21-CA-win64) (build 25.322-b06, mixed mode)**

### Variaveis de ambiente no windows ###

Agora verifique a existência da variavel **JAVA_HOME**. Abrindo o **CMD** e digitando o seguente comando:
```
echo %JAVA_HOME%
```

A saida deve ser igual a esta:
```
C:\Program Files\Zulu\zulu-8\
```


Se caso não encontrar deve-se entrar nas variaveis de ambiente e fazer o cadastro exemplo:

* Vá com o botão direito do mouse em **Este Computador** e clique em "propriedades"
* Procure por **Configurações avançadas** do sistema clique nesta opção
* Após abrir a "tela da propriedade" do Sistema clique no botão **"Variaveis de Ambiente..."**
* Após abrir a "tela de Variáveis de ambiente" clique no botão *"Novo"* na opção **Variáveis de sistema**
* Após abrir a "tela nova variáveis de sistema" insira o nome da variável como **JAVA_HOME** e o valor da variável  **C:\Program Files\Zulu\zulu-8\**
* Após feito este procedimento clique no botão **OK** e reinicie o computador.


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

**export JAVA_HOME=`/usr/libexec/java_home`** <br>
**export PATH=$JAVA_HOME/bin:$PATH**

* Sair do modo de edição teclando ESC
* Salvar o arquivo teclando :wq e pressionando enter

## Baixando e configurando o Maven ##

* Baixar a versão binária zipada do Maven **Binary zip archive** (-bin.zip). [Download Maven](https://maven.apache.org/download.cgi) apartir da versão apache-maven-3.8.5-bin.zip.
* Extrair o zip baixado em alguma pasta de sua preferência. <br>
  Sugestão: Salve o arquivo na pasta onde deseja criar o seu projeto. <br>
  Exemplo: C:\projeto\Karate-dsl

### Adicionando o Maven nas variáveis de ambiente ###

Para o **Windows:** <br>
* Após salvar o arquivo no diretório "C:\projeto\Karate-dsl" temos que adicionar o local da pasta do Maven em variável de ambiente PATH do usuário, da seguinte forma. <br>
  
* Vá com o botão direito do mouse em **Este Computador** e clique em propriedades
* Procure pela funcionalidade **Configurações avançadas** do sistema clique nesta opção
* Após abrir a tela da propriedade do Sistema clique no botão **Variaveis de Ambiente...**
* Após abrir a tela de Variáveis de ambiente clique no botão novo na opção **Variáveis de sistema**
* Agora clique no botão **Novo** em Variáveis de usuário dê um duplo clique na opção Path.
* Após abrir a tela **Editar a variável de ambiente** clique no botão **Novo** e informe o caminho **C:\projeto\Karate-dsl\apache-maven-3.8.5\bin** e clique no botão **OK** e feche a tela de variaveis de ambiente.
  
Após o termino da configuração reinicie o **CMD** e execute o seguinte comando, para sabermos se está em funcionamento.

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

**code -version**

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
* VSCode-icons - opcional
* Hyper Term Theme - opcional
* KarateIDE Classpath Jar --> para mais informaçoes [link](https://marketplace.visualstudio.com/items?itemName=KarateIDE.karate-classpath-jar)
* ZenWave Karate IDE --> para mais informações [link](https://marketplace.visualstudio.com/items?itemName=KarateIDE.karate-ide)

## Instalação e configuração do Karatê-Dsl ##
  
Abra o **VSCode** entre na opção "Arquivo> Abrir Pasta" e dentro do VSCode abra o terminal se atente para alterar de **powershell** para o **cmd**.
  
Para instalar e configurar o Karatê-DSL entre no projeto do [Karatê-DSL](https://github.com/karatelabs/karate#quickstart) e pegue o comando de instalação do **Maven** <br>
Exemplo: 

``` 
 mvn archetype:generate -DarchetypeGroupId=com.intuit.karate -DarchetypeArtifactId=karate-archetype -DarchetypeVersion=1.1.0 -DgroupId=com.mycompany -DartifactId=myproject
 
```
**Atenção** <br>
Ideal que seja alterado os parametros e executado no terminal dentro do VSCode <br>
**DgroupId**: Colocar o nome da empresa. <br>
**DartifactId**: Colocar o nome projeto desejado, exemplo **projetoKarate**  <br>

**Exemplo com alteração**
```
 mvn archetype:generate -DarchetypeGroupId=com.intuit.karate -DarchetypeArtifactId=karate-archetype -DarchetypeVersion=1.1.0 -DgroupId=com.nomedaempresa -DartifactId=projetoKarate
```  
**Exemplo após execução do comando** <br>
No término da execução apresentará a opção **SNAPSHOT:** onde será necessário determinarmos número inical da versão do projeto, ex: 1.0 e clicarmos no botão **Enter**                                                                                                          
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
Após informar a versão devemos confirmar as alterações informando a letra **Y** e clicar no botão **Enter**

**Exemplo:**
```
property: package = com.nomedaempresa
Confirm properties configuration:
groupId: com.nomedaempresa
artifactId: projetokarate
version: 1.0
package: com.nomedaempresa
 Y: :Y
```

### Conhecendo a estruturas de pastas ###                                                                                                 
                                                                                                            
Após a instalação o projeto do Karatê-DSL a estrutura do projeto vai ficar assim:
```
projetokarate
|--> src\test\java
|     |-->examples
|     |   |-->users
|     |   |    |-->users.feature
|     |   |    |-->usersRunner.java
|     |   |-->ExamplesTest.java
|     |--> Karate-config.js
|     |--> logback-test.xml
|--> pom.xml
```  

#### Explicando a estrutura do projeto Karatê. ####

**projetokarate** --> É o nome da pasta do projeto, mas conseguimos alteramos para qual quer nome link do exemplo [nome do projeto](https://github.com/andersonsylvestre/karate-dsl/blob/master/README.md#instala%C3%A7%C3%A3o-e-configura%C3%A7%C3%A3o-do-karat%C3%AA-dsl). <br>
**src\test\java** --> Esta pasta é onde se escrevem os testes(Estrutura padrao do Java). <br>
**examples** --> Esta pasta vai ser a organização da pastas exemplos: <br>

* useres ou o nome da que desejar


**users.feature** --> Este arquivo com a extenção **.feature** são arquivos da escrita gherkin
**usersRunner.java** --> Este arquivo é o que dispara os testes e aonde vc faz as configurações, por exemplo nele é possível fazer filtros de tags para disparar somente os testes com aquela tag, você pode criar um Runner pra cada feature que fica dentro da mesma pasta que ela ou coloca uma fora dessas pastas e deixa geral.

**ExamplesTest.java** --> Segue a mesma idea do arquivo usersRunner.java, a diferença é que o usersRunner só roda a feature Users e o ExamplesTest roda tudo que tiver na pasta Examples, e dá pra fazer paralelismo ou seja roda vários testes ao mesmo tempo.

**Karate-config.js** --> Este arquivo é aonde se faz configurações gerais que impactarão todo o projeto, tudo que vc colocar nele será disparado antes de rodar qualquer teste, por exemplo, é possível definir uma variável nele que poderá ser utilizada em qualquer teste criado, no projeto de testes de api, a gente defini lá as urls base e também uma lógica pra definir o ambiente aonde serão rodados os testes.

**logback-test.xml** --> Este arquivo de configuração de logs
**pom.xml** --> Este arquivo consegue fazer a injeção de dependência, tipo é possível usar plugins e frameworks externos, aí nesse arquivo vc pode por o endereço e algumas configurações para a utilização desses recursos

## Executando o Karatê-Dsl a primeira vez ##
## Configurando o proxy ##
