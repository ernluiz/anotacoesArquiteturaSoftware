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

