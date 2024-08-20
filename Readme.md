# Criando um Projeto Java com Maven

Este guia fornece os passos necessários para criar um novo projeto Java usando o Maven, um popular gerenciador de dependências e ferramenta de construção para projetos Java.

## Passo 1: Gerar o Projeto via Prompt de Comando

Abra o Prompt de Comando (cmd) no diretório onde você deseja criar seu novo projeto e execute o seguinte comando:

~~~~powershell
mvn archetype:generate -DgroupId=andrevsc -DartifactId=java-maven-first-project -Darchetype=maven-archetype-quickstart -DinteractiveMode=false
~~~~

### Explicação dos Parâmetros:

- **`-DgroupId`**: Especifica o ID do grupo para o projeto. No Maven, o ID do grupo é um identificador exclusivo para seu projeto, geralmente no formato de um domínio reverso (ex: `com.exemplo`).

- **`-DartifactId`**: Define o ID do artefato. Este é o nome do seu projeto. O Maven cria um diretório com esse nome para o seu projeto.

- **`-Darchetype`**: Indica o tipo de projeto que você deseja criar. O valor `maven-archetype-quickstart` é um arquétipo básico para começar um novo projeto Java.

- **`-DinteractiveMode=false`**: Desativa o modo interativo, permitindo que o Maven use os valores padrão fornecidos sem solicitar informações adicionais.

## Passo 2: Navegar para o Diretório do Projeto

Após executar o comando acima, o Maven criará um diretório chamado `java-maven-first-project`. Navegue até este diretório usando o comando:

~~~~powershell
cd java-maven-first-project
~~~~

## Passo 3: Compilar o Projeto

Para compilar o projeto, use o comando:

~~~~powershell
mvn compile
~~~~

Este comando compilará o código-fonte do projeto e gerará os arquivos `.class` correspondentes na pasta `target/classes`.

## Passo 4: Empacotar o Projeto

Depois de compilar o projeto, você pode empacotá-lo em um arquivo JAR usando o comando:

~~~~powershell
mvn package
~~~~

### O que o `mvn package` faz?

O comando `mvn package` compila o código-fonte, executa os testes (se houver) e empacota o aplicativo em um arquivo JAR (ou WAR, dependendo do projeto). O arquivo gerado será encontrado na pasta `target`.

Por exemplo, se o `artifactId` do seu projeto for `java-maven-first-project`, o Maven criará um arquivo chamado `java-maven-first-project-1.0-SNAPSHOT.jar` dentro da pasta `target`.

## Passo 5: Limpar o Diretório de Compilação

Para limpar o diretório de compilação (remover a pasta `target` e todos os arquivos gerados durante a compilação anterior), use o comando:

~~~~powershell
mvn clean
~~~~

### O que o `mvn clean` faz?

O comando `mvn clean` remove todos os arquivos gerados pelo Maven durante a compilação, teste e empacotamento do projeto. Isso inclui a pasta `target` e todos os arquivos `.class`, arquivos JAR, e outros artefatos de construção. É útil quando você deseja iniciar uma nova compilação do zero.

## Passo 6: Executar o JAR Gerado

Após empacotar o projeto, você pode executar o arquivo JAR gerado com o seguinte comando:

~~~~powershell
java -jar target/java-maven-first-project-1.0-SNAPSHOT.jar
~~~~

Certifique-se de substituir o nome do arquivo JAR conforme necessário.

## Passo 7: Adicionar Dependências

Para adicionar dependências ao seu projeto, edite o arquivo `pom.xml` e adicione as dependências necessárias na seção `<dependencies>`.

## Passo 8: Executar Testes

Para executar os testes incluídos no seu projeto, use o comando:

~~~~powershell
mvn test
~~~~

## Recursos Adicionais

- [Documentação Oficial do Maven](https://maven.apache.org/guides/index.html)
- [Arquetipos do Maven](https://maven.apache.org/archetypes/)
