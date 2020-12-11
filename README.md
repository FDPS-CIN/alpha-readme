[![Java](https://img.shields.io/badge/Language-java-yellow)]() [![MAven](https://img.shields.io/badge/Build-Maven-blue)]() [![MAven](https://img.shields.io/badge/Testing-JUnit5-yellow)](https://opensource.org/licenses/MIT) [![License:MIT](https://img.shields.io/github/license/aretw0/ga_tutorial)](https://opensource.org/licenses/MIT) 

 
[![Github](https://raw.githubusercontent.com/FDPS-CIN/images-readme/master/logo_github.png)](https://github.com/)[![Github Actions](https://raw.githubusercontent.com/FDPS-CIN/images-readme/master/logo_workflow.png)]()

# Tópicos
  - [Introdução](README.md#introdução)
  - [Projeto e Repositório](README.md#projeto-e-repositório)
  - [Configuração](README.md#configuração)
  - [Execução](README.md#execução)
  - [Tecnologias](README.md#tecnologias)
  - [Autores](README.md#autores)
  - [Referência](README.md#referências)

# Introdução

O Github Actions permite que você crie fluxos de trabalho personalizados do ciclo de vida de desenvolvimento de software diretamente no seu repositório Github. Esses fluxos de trabalho são compostos por diferentes tarefas, chamadas ações, que podem ser executadas automaticamente em determinados eventos. Isso permite que você inclua recursos de integração contínua (CI) e implantação contínua (CD) e muitos outros recursos diretamente em seu repositório.

Esta apresentação demonstra a configuração e uso do GA (Github Actions) em um repositório de um projeto java. O projeto java utilizado foi criado usando o Maven. O maven faz uso de um arquivo xml geralmente chamado ‘pom.xml’ que descreve tudo o que maven precisa e pode fazer para testar, buildar e empacotar aquele projeto.

# 1. Projeto e repositório 

Crie um projeto usando maven e o coloque em um repositório no github

Usando o maven é possível criar um projeto java básico:

```
mvn archetype:generate \ 
-DgroupId=br.ufpe.cinmoto.testingtools_ga.app \
-DartifactId=testingtools_ga -DarchetypeArtifactId=maven-archetype-quickstart \ -DarchetypeVersion=1.4 -DinteractiveMode=false
```

# Configuração 
Configurando o repositório para usar Github Actions

Em seu repositório clique na aba "`actions`":

[![Aba Actions](https://raw.githubusercontent.com/FDPS-CIN/images-readme/master/00_step_06_pag.png)]()

Sugestões aparecerão baseadas no projeto:

[![Sugestões](https://raw.githubusercontent.com/FDPS-CIN/images-readme/master/01_step_07_pag.png)]()

Na sugestão ‘Java with Maven’ clique em  "`set up this workflow`":

[![workflow](https://raw.githubusercontent.com/FDPS-CIN/images-readme/master/02_step_08_pag.png)]()

Aparecerá este editor de texto abaixo:

[![Sugestões](https://raw.githubusercontent.com/FDPS-CIN/images-readme/master/03_step_09_pag.png)]()

Preencha o editor de texto com o conteúdo abaixo respeitando a indentação mostrada. Após isso clique no botão para fazer o commit "`start commit`":

[![Commit](https://raw.githubusercontent.com/FDPS-CIN/images-readme/master/04_step_10_pag.png)]()

# Execução 

Github Actions em ação ( Acompanhando o seu workflow )

Agora na aba "`Actions`" será possível acompanhar as execuções dos workflows do repositório:

[![Follow](https://raw.githubusercontent.com/FDPS-CIN/images-readme/master/05_step_12_pag.png)]()

Cada execução será acionada automaticamente a partir de eventos que definimos no arquivo do workflow (push e pull request). Nesse caso o evento foi um push do commit que fizemos do novo arquivo (maven.yml). Com certeza esta é a primeira execução de qualquer repositório que passe a usar o GA.

Clicando na execução em andamento do workflow que adicionados temos esta página:

[![Follow](https://raw.githubusercontent.com/FDPS-CIN/images-readme/master/06_step_13_pag.png)]() 

Na lateral esquerda clicando em build (nome do job) podemos ver sua execução de forma mais detalhada

[![Follow](https://raw.githubusercontent.com/FDPS-CIN/images-readme/master/07A_step_14_pag.png)]() 

[![Follow](https://raw.githubusercontent.com/FDPS-CIN/images-readme/master/07B_step_14_pag.png)]()

[![Follow](https://raw.githubusercontent.com/FDPS-CIN/images-readme/master/07C_step_14_pag.png)]()

Ao fim de uma execução bem sucedida (todos os testes passaram) é possível fazer download do artefato (.jar) zipado.

[![Follow](https://raw.githubusercontent.com/FDPS-CIN/images-readme/master/08C_step_15_pag.png)]()

# Tecnologias

  - [Java](https://www.java.com/pt-BR/) - Java is a class-based, object-oriented programming language that is designed to have as few implementation dependencies as possible
  - [Junit](https://junit.org/junit5/) - JUnit is one of the most popular unit-testing frameworks in the Java ecosystem
  - [Maven](https://maven.apache.org/) -  Maven is a software project management and comprehension tool
  

# License :warning:
Este projeto é licenciado sobre a licença MIT - Veja o arquivo LICENSE.MD para detalhes.

# Autores
- [@aretw0](https://github.com/aretw0) - Arthur Aleksandro
- [@jV1ct0r](https://github.com/jV1ct0r) - João Victor
- [@Telemaco98](https://github.com/Telemaco98) - Shirley Ohara
- [@RuanBahia](https://github.com/RuanBahia) - Ruan Bahia
- [@jcrbsa](https://github.com/jcrbsa) - Richardson Bruno


# Referências

- [Iniciando Started Maven in Cinco Minutos](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html)
- [Pom File](https://maven.apache.org/pom.html)
- [Construindo e Testando Java com Maven](https://docs.github.com/en/free-pro-team@latest/actions/guides/building-and-testing-java-with-maven)
- [Introdução ao Github Actions](https://gabrieltanner.org/blog/an-introduction-to-github-actions)

