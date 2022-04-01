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

## Instalação do JDK 8u202 (Windows 10)

Para fazer a instalação do **JDK 8u202** vá ao site da Oracle e baixe [JDK8](https://www.oracle.com/java/technologies/downloads/) e siga os seguintes passos para instalação do JDK 8.

Após baixar o JDK 8, vá com o botão direito do mouse e executa o JDK 8 como administrador.

* Inicie a intalação do Java JDK 8u202
* Clique no botão Next.
* Aguarde a finalização da instalação java JDK 8u202

Agora verifique a existencia da variavel JAVA_HOME. Abrindo o **CMD** e digitando o seguente comando:

**echo %JAVA_HOME%**

A saida deve ser igual a esta:

**C:\Program Files\Java\jdk1.8.0_202**

Se caso não mostrar deve entrar em variaveis de ambiente e fazer o cadastro exemplo:

* Vá com o botão direito do mouse em Este Computador e clique em propriedades
* No lado esquerdo encontra-se link Configurações avançadas do sistema clique nesta opção
* Após abrir a tela da propriedade do Sistema clique no botão Variaveis de Ambiente...
* Após abrir a tela de Variáveis de ambiente clique no botão novo na opção Variáveis de sistema
* Após abrir a tela Nova variáveis de sistema insire o Nome da variável com **JAVA_HOME** e o valor da variável **C:\Program Files\Java\jdk1.8.0_202**
* Após feito este procedimento clique no botão OK

Agora abra novamente o **CMD** e digite:

**"%JAVA_HOME%"\bin\java -version**

O resultado deve ser a versão do Java como no exemplo abaixo

**java version "1.8.0_202" <br>
Java(TM) SE Runtime Environment (build 1.8.0_202-b08) <br>
Java HotSpot(TM) 64-Bit Server VM (build 25.202-b08, mixed mode)**



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

## Instalação e configuração do Karatê-Dsl
