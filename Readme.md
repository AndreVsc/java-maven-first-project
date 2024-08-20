# Criando um Projeto Java com Maven

Este guia fornece os passos necessários para criar um novo projeto Java usando o Maven, um popular gerenciador de dependências e ferramenta de construção para projetos Java.

## Passo 1: Gerar o Projeto via Prompt de Comando

Abra o Prompt de Comando (cmd) no diretório onde você deseja criar seu novo projeto e execute o seguinte comando:

~~~~powershell
mvn archetype:generate -DgroupId=andrevsc -DartifactId=java-maven-first-project -Darchetype=maven-archetype-quickstart -DinteractiveMode=false
~~~~

### Explicação dos Parâmetros:

- **`DgroupId`**: Especifica o ID do grupo para o projeto. No Maven, o ID do grupo é um identificador exclusivo para seu projeto, geralmente no formato de um domínio reverso (ex: `com.exemplo`).

- **`DartifactId`**: Define o ID do artefato. Este é o nome do seu projeto. O Maven cria um diretório com esse nome para o seu projeto.

- **`Darchetype`**: Indica o tipo de projeto que você deseja criar. O valor `maven-archetype-quickstart` é um arquétipo básico para começar um novo projeto Java.

- **`DinteractiveMode=false`**: Desativa o modo interativo, permitindo que o Maven use os valores padrão fornecidos sem solicitar informações adicionais.

## Passo 2: Navegar para o Diretório do Projeto

Após executar o comando acima, o Maven criará um diretório chamado `java-maven-first-project`. Navegue até este diretório usando o comando:

~~~~powershell
cd java-maven-first-project
~~~~

## Passo 3: Compilar e Executar o Projeto

Para compilar o projeto, use o comando:

~~~~powershell
mvn compile
~~~~

Para executar o projeto, use o comando:

~~~~powershell
mvn exec:java -Dexec.mainClass="com.example.App"
~~~~

Certifique-se de substituir `com.example.App` pelo nome da classe principal do seu projeto.

## Passo 4: Adicionar Dependências

Para adicionar dependências ao seu projeto, edite o arquivo `pom.xml` e adicione as dependências necessárias na seção `<dependencies>`.

## Passo 5: Executar Testes

Para executar os testes incluídos no seu projeto, use o comando:

~~~~powershell
mvn test
~~~~

## Recursos Adicionais

- [Documentação Oficial do Maven](https://maven.apache.org/guides/index.html)
- [Arquetipos do Maven](https://maven.apache.org/archetypes/)
