# Anotações de Arquitetura de Software
> Sintaxe de markdown

> Apresentação de estilos arquiteturais e padrões arquiteturais
---
## Client-Server:
- **Thin client:** uma arquitetura cliente-servidor que depende fortemente do servidor para realizar a maior parte do processamento e armazenamento de dados. Em contraste com um fat client, o thin client executa apenas funções básicas e utiliza o servidor para processar aplicações e armazenar dados. Isso resulta em menor custo de hardware e manutenção no lado do cliente. Exemplos comuns de thin clients incluem terminais de acesso remoto e soluções de desktop virtual, onde a maior parte do trabalho é realizada no servidor central. É um front-end sem lógica, apenas com poucas validações, sem muita lógica; um código HTML sem tag de script, por exemplo.
- **Fat-Client:** (ou thick client) é um tipo de cliente em uma arquitetura cliente-servidor que realiza a maior parte do processamento de aplicações. Diferente de um thin client, que depende fortemente do servidor para realizar a maioria das tarefas, um fat client possui capacidade de processamento, armazenamento de dados e pode executar aplicações de forma independente, necessitando do servidor principalmente para armazenamento e sincronização de dados. Exemplos comuns de fat clients incluem aplicativos de desktop como editores de texto, softwares de design gráfico e jogos.
---
## Component-based
> É uma abordagem de desenvolvimento de software onde a aplicação é construída a partir de componentes reutilizáveis e independentes. Cada componente encapsula uma funcionalidade específica, promovendo modularidade, manutenção facilitada e reutilização de código. Exemplos dessa abordagem incluem frameworks como React e Angular, que utilizam componentes para criar interfaces de usuário de forma eficiente e escalável.

Exemplos de sistemas que utilizam a abordagem component-based incluem:

- **React:** Utilizado por plataformas como Facebook, Instagram e Airbnb para construir interfaces de usuário interativas e modulares.
- **Angular:** Usado por empresas como Google, Microsoft, e Forbes para criar aplicações web robustas e escaláveis.
- **Vue.js:** Adotado por Alibaba, Xiaomi e GitLab para desenvolvimento de interfaces de usuário dinâmicas e reativas.
- **Salesforce Lightning:** Plataforma da Salesforce que utiliza componentes para desenvolver aplicativos empresariais personalizados.
- **Microservices architectures:** Muitas aplicações empresariais modernas utilizam componentes independentes (microservices) para criar sistemas escaláveis e fáceis de manter.
- Sistemas de gestão empresarial (ERP), plataforma de comércio eletrônico, sistema de gerenciamento de conteúdo (CMS) como Drupal e WordPress, componentes de aplicações web.
---
## Layered e N-tiers
> Layered Architecture e N-tier Architecture são abordagens de design de software que ajudam a estruturar e organizar sistemas complexos. Ambos os padrões ajudam a criar sistemas modulares, escaláveis e mais fáceis de manter. É parecido com o padrão MVC, porém aqui se chamam de camadas e no MVC são chamados de níveis.

### Layered Architecture:
- Divide o sistema em camadas distintas, onde cada camada tem responsabilidades específicas e interage apenas com a camada diretamente acima ou abaixo dela.
- Tipicamente, inclui camadas como apresentação, lógica de negócios e acesso a dados.
- Facilita a manutenção e evolução, permitindo alterações em uma camada sem afetar as outras.
- Exemplo: Aplicações web onde a camada de apresentação é separada da camada de lógica de negócios e da camada de persistência de dados.
- É uma divisão lógica, tendo todo o sistema em uma única aplicação/máquina.

  
### N-tier Architecture:

- É uma forma mais específica de arquitetura em camadas, onde "N" se refere ao número de camadas (ou tiers) que podem incluir, por exemplo, apresentação, lógica de aplicação, lógica de negócios, e banco de dados.
- Cada camada pode ser fisicamente distribuída em servidores distintos, melhorando a escalabilidade e a separação de responsabilidades.
- É uma divisão física, onde as partes de um sistema rodam em máquinas ou servidores distintos.
- Exemplo: Sistemas corporativos onde a camada de apresentação está em um cliente web, a lógica de negócios em servidores de aplicação e o armazenamento de dados em um servidor de banco de dados.

![image](https://github.com/user-attachments/assets/bb0aea02-5434-4ac1-96e8-3cf059300709)
---
## Micro-kernel

> O padrão micro-kernel é uma arquitetura de software que foca em criar um núcleo minimalista (kernel) que fornece apenas as funcionalidades básicas necessárias para o sistema, enquanto a funcionalidade adicional é implementada através de plugins ou módulos externos. Essa abordagem tem várias características e benefícios:

- **Núcleo Reduzido:** O micro-kernel oferece um conjunto mínimo de serviços e funcionalidades essenciais, como gerenciamento de processos e comunicação entre componentes, mantendo o núcleo do sistema leve e simples.
- **Extensibilidade:** Funcionalidades adicionais são implementadas como módulos ou plugins que se conectam ao núcleo, permitindo a adição de novos recursos sem modificar o núcleo.
- **Modularidade:** Facilita a manutenção e evolução do sistema, uma vez que os módulos podem ser atualizados ou substituídos independentemente.
- **Isolamento de Falhas:** Como a funcionalidade adicional está separada do núcleo, falhas ou problemas em um módulo têm menos impacto no núcleo e nos outros módulos.
  
Exemplos de sistemas que utilizam a arquitetura micro-kernel incluem:

- **Sistemas Operacionais:** Como o MINIX e o QNX, que utilizam um núcleo reduzido e extensível para oferecer serviços básicos enquanto suportam uma variedade de drivers e serviços adicionais.
- **Plataformas de Desenvolvimento:** Eclipse, que usa um micro-kernel para permitir extensões e plugins que adicionam novas funcionalidades à plataforma de desenvolvimento.
- **Servidores de Aplicações:** Alguns servidores, como o JBoss e o Apache Tomcat, adotam uma abordagem micro-kernel para modularidade e extensibilidade.
O padrão micro-kernel é útil para sistemas que requerem alta flexibilidade e extensibilidade, permitindo personalizar e expandir funcionalidades de forma eficiente.

## Microsserviços

> Pergunta de prova: **Quais as principais vantagens de utilizar microsserviços? R.: Escalabilidade e descentralização de times de desenvolvimento.**

## Pipes and Filters

> Os filtros processam os dados, enquanto os pipes transportam os dados entre os filtros. um exemplo clássico é o shell do Linux.

## Arquitetura limpa

> Enfatiza a separação de preocupações e a independência dos frameworks, interfaces de usuário, bancos de dados e outros detalhes externos; é um avanço da estrutura onion; **Ela diz que regras de negócio devem ser separadas de frameworks e interfaces de usuário.**
> **Supre alguns _gaps_ da arquitetura hexagonal.**

## Arquitetura hexagonal

> Visa criar sistemas de software altamente desacolpados  testáveis, podendo as partes centrais da aplicação permanecerem independentes das interfaces de entrada e saída.

![image](https://github.com/user-attachments/assets/2e3cd33f-7179-444d-86c8-247b8d56b0dc)

> **Pergunta de prova: No que se resume arquitetura limpa e arquitetura hexagonal?**
> - **Arquitetura limpa: foca na separação de responsabilidades em camadas concêntricas, com o domínio no centro e dependências externas nas camadas mais externas.**
> - **Arquitetura hexagonal: enfatiza a modularidade através de portas e adaptadores, permintindo que o núcleo da aplicação permaneça independente das interações externas.**

![image](https://github.com/user-attachments/assets/2bdd2538-b4ea-4b09-9985-5bc7f5a48bbf)

# Padrões de projeto

> Design Patterns (ou padrões de projeto) são soluções típicas para problemas recorrentes no desenvolvimento de software. Eles representam boas práticas adotadas por desenvolvedores experientes e foram criados para facilitar a manutenção, escalabilidade e a clareza do código.

## Benefícios
- **Reutilização de código** - Design patterns promovem a reutilização de soluções testadas, evitando a necessidade de "reinventar a roda" e economizando tempo durante o desenvolvimento.
- **Manutenção** - O uso de padrões facilita a manutenção do código, pois as soluções são reconhecíveis e compreendidas por desenvolvedores familiarizados com os padrões.
- **Comunicação** - Ao usar design patterns, desenvolvedores podem se comunicar de maneira mais eficiente, referindo-se a uma solução complexa com um nome simples e amplamente compreendido, como "Factory Method" ou "Observer".
- **Escalabilidade e flexibilidade** - Ajudam a criar sistemas facilmente estendidos ou modificados à medida que novos requisitos surgem.

## Onde não utilizar
- **Complexidade desnecessária:** Aplicar um pattern em um problema que pode ser resolvido com uma solução mais simples pode adicionar complexidade desnecessária ao código.
- **Problemas mal definidos:** Não tente forçar um padrão em um problema que não é claramente compreendido. Primeiro, compreenda completamente o problema antes de buscar uma solução padrão.
- **Overengineering:** Evite overengineering, que é a tendência de criar uma solução mais complexa do que o necessário, por aplicar padrões de design onde não são necessários.

|         Criacionais          |         Estruturais         |         Comportamentais         |
| :-------------------------:  | :------------------------:  | :-----------------------------: |
| Tratam do processo de criação de objetos, promovendo a flexibilidade e a reutilização de código.  | Lidam com a composição de classes ou objetos, formando estruturas maiores de forma eficiente.  | Lidam com a comunicação entre os objetos e com a maneira como eles interagem e suas responsabilidades.  |

![image](https://github.com/user-attachments/assets/3378f0cb-c106-4f2b-abae-a14739366b63)

![image](https://github.com/user-attachments/assets/e7e4ea59-5f9b-43d8-9a0f-c3c53212b7f4)

## Singleton
> É um padrão de design criacional que garante que uma classe tenha apenas uma única instância e fornece um ponto global de acesso a essa instância. 
> É útil em situações onde é importante que apenas um objeto de uma classe seja criado, como em gerenciadores de recursos, conexões de banco de dados ou configurações globais de uma aplicação.

### Características:
- **Única instância:** Apenas uma instância da classe é criada durante o ciclo de vida da aplicação.
- **Controle de acesso:** A classe controla como e quando sua única instância é criada.
- **Ponto de acesso global:** Fornece uma forma global de acessar essa instância única.

## Abstract Factory
> Padrão que permite criar famílias de objetos relacionados ou dependentes sem especificar suas classes concretas. 
> Define uma interface para criar diferentes tipos de objetos (como botões e checkboxes),
permitindo que o cliente trabalhe com essas famílias de objetos de forma independente de
suas implementações específicas.

### Características:
- **Criação de famílias de objetos:** Permite criar grupos de objetos relacionados que devem ser usados juntos.
- **Independência de implementação:** O cliente usa interfaces abstratas, sem saber quais classes concretas estão sendo instanciadas.
- **Flexibilidade:** Facilita a troca entre diferentes famílias de objetos, como mudar a interface do usuário de Windows para macOS sem alterar o código cliente.

## Factory Method
> Define um método para criar objetos em uma classe, permitindo que as subclasses decidam qual classe concreta será instanciada.
> Em vez de instanciar objetos diretamente com new, o Factory Method delega essa responsabilidade para métodos especializados, oferecendo flexibilidade para criar diferentes tipos de objetos.

### Características
- **Delegação da criação:** Define um método para criar objetos, delegando às subclasses a decisão de qual classe concreta instanciar.
- **Desacoplamento:** Desacopla a criação de objetos da sua utilização, facilitando a adição de novas classes sem modificar o código existente.
- **Flexibilidade:** Permite que uma classe defina a interface de criação, enquanto subclasses concretas implementam a lógica específica para diferentes tipos de produtos.

## Prototype
> Permite criar novos objetos copiando instâncias existentes (protótipos), ao invés de instanciar novos objetos do zero. 
> É útil quando a criação direta de um objeto é cara (em termos de tempo ou recursos) ou quando você deseja evitar subclasses para criar diferentes instâncias.

### Características
- **Clonagem de objetos:** Cria novos objetos copiando (clonando) instâncias existentes, sem depender de classes concretas.
- **Flexibilidade:** Permite criar objetos complexos com uma configuração inicial específica, evitando a repetição de código ou configurações.
- **Independência de implementação:** Você pode criar novos objetos sem depender de suas classes concretas, utilizando cópias de protótipos existentes.

## Builder
> Permite a construção de objetos complexos passo a passo. Ele separa o processo de construção do objeto da sua representação, permitindo criar diferentes representações do mesmo objeto.

### Características
- **Construção passo a passo:** Permite criar objetos complexos em etapas, adicionando um nível de controle sobre o processo de construção.
- **Separação de preocupações:** Separa a lógica de construção do objeto (Builder) de sua representação final, permitindo que o mesmo processo construa diferentes tipos de objetos.
- **Flexibilidade:** Facilita a criação de objetos com configurações variadas sem precisar de múltiplos construtores ou parâmetros opcionais.

