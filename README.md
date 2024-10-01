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
- 
# Padrões estruturais
> São descritas como soluções para problemas relacionados à composição de classes e objetos para formar estruturas maiores e mais flexíveis. Esses padrões ajudam a organizar e otimizar o design de sistemas de software, facilitando como os componentes interagem e se conectam.

## Principais benefícios:
- **Flexibilidade na composição de objetos**
- **Desacoplamento**
- **Manutenção e extensão**
- **Simplificação de complexidade**

## ADAPTER
> O Adapter é um padrão de projeto estrutural que permite objetos com interfaces incompatíveis colaborarem entre si.
> Permite que interfaces incompatíveis trabalhem juntas. Ele converte a interface de uma classe em outra interface esperada pelos clientes. 
Assim, o Adapter atua como um intermediário que traduz as chamadas feitas pelo cliente para a interface da classe que não é compatível.
> **Usado quando é necessário integrar sistemas legados com novos sistemas ou quando se deseja adaptar uma API para uma nova interface.**
![image](https://github.com/user-attachments/assets/39057928-aea8-4ea9-ae01-b3fcef05c775)

## BRIDGE
> O Bridge é um padrão de projeto estrutural que permite que você divida uma classe grande ou um conjunto de classes intimamente ligadas em duas hierarquias separadas—abstração e implementação—que podem ser desenvolvidas independentemente umas das outras.
> Desacopla uma abstração da sua implementação, permitindo que ambas evoluam independentemente. 
> **É usado quando você quer separar uma abstração (a ideia principal ou conceito) de sua implementação concreta (a forma como o conceito é realizado). Isso é útil para evitar que mudanças em uma parte da estrutura (como uma classe) causem impacto na outra parte.**
![image](https://github.com/user-attachments/assets/628a2f99-bd4d-4891-accf-4cf43e396619)

## COMPOSITE
> O Composite é um padrão de projeto estrutural que permite que você componha objetos em estruturas de árvores e então trabalhe com essas estruturas como se elas fossem objetos individuais.
> O padrão Bridge permite separar a abstração (o controle remoto) da implementação (os dispositivos eletrônicos), possibilitando a criação de controles e dispositivos de forma independente, sem a necessidade de criar várias subclasses. Permite que você trate objetos individuais e composições de objetos de forma uniforme. Isso é útil quando você tem uma estrutura hierárquica de objetos, como uma árvore, onde cada nó pode ser um objeto simples ou um grupo de objetos.
> **Usado quando precisar representar hierarquias de objetos, como estruturas de diretórios de arquivos ou interfaces gráficas complexas.**
![image](https://github.com/user-attachments/assets/0da63548-52c6-4153-a77c-3f6202b64119)

## DECORATOR
> O Decorator é um padrão de projeto estrutural que permite que você acople novos comportamentos para objetos ao colocá-los dentro de invólucros de objetos que contém os comportamentos.
> Permite adicionar responsabilidades a um objeto dinamicamente, sem alterar o código da classe original. Ele usa um conjunto de classes de decoração que envolvem o objeto original, adicionando funcionalidades adicionais.
> **Utilizado para adicionar funcionalidades a objetos de maneira flexível e extensível, como adicionar estilos de janela em um sistema de GUI.**
![image](https://github.com/user-attachments/assets/5203b3a2-842a-4aa3-bc89-ecc8ca8d04b6)

## FACADE
> O Facade é um padrão de projeto estrutural que fornece uma interface simplificada para uma biblioteca, um framework, ou qualquer conjunto complexo de classes.
> Fornece uma interface simplificada para um conjunto de interfaces em um subsistema complexo. Em outras palavras, o Facade atua como uma "fachada" que oculta a complexidade de um sistema, oferecendo uma maneira mais fácil e direta para os interagirem com ele.
> **É recomendado para ser usado em situações em que se deseja simplificar a interface de um subsistema complexo, dividir subsistemas em camadas, simplificar dependências entre subsistemas, simplificar uma sequência de operações complexas, simplificar a interface com o usuário.**
![image](https://github.com/user-attachments/assets/eceac9fd-c807-4531-bd6d-f71cb8a00312)

## FLYWEIGHT
> O Flyweight é um padrão de projeto estrutural que permite a você colocar mais objetos na quantidade de RAM disponível ao compartilhar partes comuns de estado entre os múltiplos objetos ao invés de manter todos os dados em cada objeto.
> Visa reduzir o uso de memória e melhorar o desempenho ao compartilhar objetos semelhantes em vez de criar novos objetos para cada instância.
> **Ele é especialmente útil quando você precisa lidar com excesso de objetos que possuem características semelhantes.**
![image](https://github.com/user-attachments/assets/24626af8-d93d-4821-924f-a00667e68f6f)

## PROXY
> O Proxy é um padrão de projeto estrutural que permite que você forneça um substituto ou um espaço reservado para outro objeto. Um proxy controla o acesso ao objeto original, permitindo que você faça algo ou antes ou depois do pedido chegar ao objeto original.
> Fornece um substituto ou intermediário para outro objeto. Ele age como um "representante" do objeto real, controlando o acesso a ele e podendo adicionar funcionalidades extras, como controle de acesso, atraso na criação ou manipulação adicional.
> **Usado para adicionar funcionalidades como controle de acesso, cache, ou outras operações intermediárias.**
![image](https://github.com/user-attachments/assets/bc2f3986-bf1a-445b-ad24-9eb772226dd8)


# PADRÕES COMPORTAMENTAIS - 2º bim
> Os padrões comportamentais são focados em definir como os objetos interagem e se comunicam entre si dentro de um sistema. Eles abordam a atribuição de responsabilidades e a maneira como as classes colaboram, permitindo que o comportamento do sistema seja flexível e dinâmico sem a necessidade de modificações profundas no código.

> Segundo o livro "Design Patterns: Elements of Reusable Object- Oriented Software" (GoF), os padrões comportamentais "se preocupam com algoritmos e a atribuição de responsabilidades entre objetos... não descrevem apenas padrões de objetos ou classes, mas também o padrão de comunicação entre eles." (GoF, p. 211). Esses padrões auxiliam a separar a lógica de controle do comportamento real dos objetos, facilitando a extensão e manutenção do código.

## CHAIN OF RESPONSIBILITY

> Permite que um pedido passe por uma cadeia de objetos potenciais, onde cada objeto tem a chance de tratar o pedido ou passá-lo adiante. Isso **promove um desacoplamento entre o remetente e os receptores, permitindo que vários objetos possam processar o pedido de forma ordenada e flexível**.
> 
> É um padrão de projeto comportamental que permite que você passe pedidos por uma corrente de handlers. Ao receber um pedido, cada handler decide se processa o pedido ou o passa adiante para o próximo handler na corrente.

### Aplicações:
- **Validação de Dados em Sistemas Web:** permite que cada validação seja tratada por um handler específico. Se uma validação falhar, a cadeia pode interromper o processo e retornar um erro;
- **Sistemas de Autenticação e Autorização:** em sistemas complexos de autenticação, diferentes mecanismos (como autenticação por senha, autenticação OAuth, tokens JWT, etc.) podem ser processados de forma sequencial. O Chain of Responsibility pode ser utilizado para tentar várias formas de autenticação até que uma seja bem-sucedida;
- **Manipulação de Requisições HTTP:** em frameworks web (como Spring ou Express.js), o padrão é usado frequentemente para tratar requisições HTTP. Cada middleware pode processar a requisição ou repassá-la ao próximo middleware na cadeia até que a resposta seja gerada;
- **Manipulação de Exceções:** Ao lidar com exceções em uma aplicação, é possível encadear diferentes handlers para tratar exceções específicas de forma ordenada;
- **Processamento de Pagamentos:** em sistemas de e-commerce, o processo de pagamento pode passar por várias etapas, como verificação de saldo, validação de cartão de crédito, e autorização do pagamento. Cada etapa pode ser um handler na cadeia.
  
![image](https://github.com/user-attachments/assets/4b46b64d-9588-4c74-9857-1f59b611555c)

## COMMAND
> Transforma uma solicitação em um objeto autônomo, que encapsula toda a informação necessária para executar uma ação. Isso inclui o próprio pedido, o receptor que o processará e, eventualmente, os parâmetros necessários. O padrão permite que comandos sejam armazenados, enfileirados, desfeitos ou refeitos sem a necessidade de conhecer os detalhes sobre quem ou como a solicitação será processada.
>
> **Esse padrão promove o desacoplamento entre o objeto que faz a solicitação e os objetos que realizam a ação**.

### Aplicações:
- **Execução de Operações de Desfazer (Undo/Redo):** em aplicações com interfaces ricas, como editores de texto, gráficos ou planilhas, o padrão Command permite implementar funcionalidade de desfazer e refazer operações;
-  **Fila de Tarefas ou Jobs (Task Queues):** sistemas que precisam agendar ou enfileirar operações assíncronas, como sistemas de processamento em lotes, podem utilizar o padrão Command para encapsular cada tarefa como um comando;
-  **Macro Comandos:** sistemas que precisam agrupar várias ações como uma única operação, como a execução de macros, podem se beneficiar do padrão Command;
-  **Tratamento de Solicitações em Menu de Aplicações:** aplicações com interfaces gráficas que apresentam menus e botões podem usar o padrão Command para associar comandos a cada item de menu ou botão, permitindo a execução de ações de forma flexível;
-  **Transações Bancárias:** em sistemas bancários, operações como transferências de dinheiro, pagamentos e depósitos podem ser encapsuladas como comandos. Isso facilita o processamento dessas operações de maneira uniforme e com suporte a transações reversíveis (como estornos);
-  **Sistemas de Controle de Robôs:** em sistemas de controle de robôs ou dispositivos automatizados, comandos podem ser usados para encapsular diferentes ações do robô, como mover-se, parar, pegar um objeto, etc.

![image](https://github.com/user-attachments/assets/34b61ef4-d7a6-4845-b034-364f8a6db96a)

## INTERPRETER
> Define uma forma de interpretar ou avaliar a gramática de uma linguagem, representando-a por meio de uma estrutura de classes. Ele **é útil quando você precisa interpretar ou analisar sentenças ou expressões escritas em uma linguagem particular, e cada símbolo ou expressão tem uma regra gramatical associada**.
>
> Este padrão é normalmente usado em cenários onde uma linguagem específica, um script ou expressões complexas precisam ser processados repetidamente.

### Aplicações:
- **Interpretação de Linguagens de Script:** muitos sistemas embutem linguagens de script para permitir que usuários finais escrevam pequenos programas ou automatizem processos. O padrão Interpreter é útil para processar e avaliar esses scripts;
- **Interpretação de Expressões Matemáticas ou Lógicas:** sistemas que precisam avaliar expressões matemáticas ou lógicas podem se beneficiar do padrão Interpreter para processar essas expressões dinamicamente;
- **Compiladores e Interpretadores de Linguagens de Programação:** o Interpreter é frequentemente usado no desenvolvimento de compiladores e interpretadores para linguagens de programação. Ele pode interpretar diretamente o código fonte ou traduzir para outro formato;
- **Query Language (Linguagens de Consulta):** em sistemas de banco de dados ou análise de dados, o Interpreter pode ser usado para interpretar e executar linguagens de consulta personalizadas, como SQL ou DSLs para consultas.

![image](https://github.com/user-attachments/assets/27507586-71db-4029-b586-f94d87922a3f)

## ITERATOR
> Permite percorrer uma coleção de objetos (como listas, arrays ou árvores) de forma sequencial, sem expor sua estrutura interna. O padrão separa a lógica de iteração da coleção, fornecendo uma interface comum para acessar os elementos um por um, independentemente da implementação da coleção. **O objetivo do Iterator é garantir que diferentes tipos de coleções possam ser percorridos de forma uniforme, oferecendo métodos como next(), hasNext(), e currentItem() para controlar o fluxo de acesso aos elementos.**
>
> O Iterator é um padrão de projeto comportamental que permite a você percorrer elementos de uma coleção sem expor as representações dele (lista, pilha, árvore, etc.).

### Aplicações:
- **Percorrer Coleções em Estruturas de Dados:** o uso mais comum do Iterator é para percorrer coleções como listas, vetores, filas, pilhas, conjuntos, e mapas;
- **Sistemas de Banco de Dados:** em sistemas de banco de dados, o Iterator é útil para percorrer grandes conjuntos de resultados de consultas (result sets) sem carregar todos os dados na memória de uma vez;
- **Percorrer Componentes de Interfaces Gráficas:** em frameworks de interfaces gráficas, o Iterator pode ser usado para percorrer elementos de uma interface, como botões, campos de texto, e outros componentes UI, sem precisar conhecer a estrutura interna da interface;
- **Percorrer Documentos XML ou JSON:** em sistemas que precisam processar documentos estruturados, como XML ou JSON, o Iterator pode ser usado para percorrer os nós desses documentos de forma eficiente;
- **Histórico de Comandos em Editores de Texto:** em editores de texto ou gráficos que possuem um histórico de ações (como desfazer e refazer), o Iterator pode ser utilizado para percorrer os comandos anteriores de maneira controlada.

![image](https://github.com/user-attachments/assets/973bc02b-8420-4265-a066-c3e63339d677)


## MEDIATOR
> Centraliza a comunicação entre objetos, evitando que eles se comuniquem diretamente uns com os outros. Isso promove o desacoplamento entre os objetos, pois, ao invés de se comunicarem
diretamente, eles passam a interagir mediante um intermediário, o Mediator. Esse padrão **é útil quando há inúmeras interações complexas entre os objetos, o que poderia tornar o sistema difícil de manter e modificar**.

### Aplicações:
- **Sistemas de Interface Gráfica (GUI):** em interfaces gráficas de usuário, diversos componentes (botões, caixas de texto, menus) interagem uns com os outros para atualizar o estado da interface. O Mediator pode ser usado para centralizar essa comunicação entre componentes da GUI;
- **Sistemas de Chat ou Mensagens:** em sistemas de chat ou mensagens, os usuários podem se comunicar em grupos ou individualmente. O Mediator pode coordenar a troca de mensagens entre os usuários, garantindo que eles não precisem se conhecer diretamente;
- **Sistemas de Controle de Tráfego Aéreo:** em sistemas de controle de tráfego aéreo, diversos aviões precisam se coordenar para evitar colisões. O Mediator pode atuar como a torre de controle, recebendo informações de cada avião e enviando instruções para coordenar as suas rotas;
- **Jogos Multiplayer:** em jogos multiplayer, os jogadores precisam interagir entre si e com o ambiente de maneira coordenada. O Mediator pode centralizar essas interações, gerenciando o estado do jogo e a comunicação entre os jogadores.

![image](https://github.com/user-attachments/assets/422ac614-5262-4a1a-ad56-4556fcd42563)

## MEMENTO
> Permite capturar e armazenar o estado interno de um objeto em um determinado momento, sem expor os detalhes de sua implementação. Posteriormente, esse estado pode ser restaurado, permitindo que o objeto volte a uma configuração anterior. **A principal vantagem do Memento é que ele mantém a integridade do encapsulamento do objeto original, pois o estado armazenado não é exposto diretamente para o cliente ou outros objetos**.

### Aplicações:
- **Funcionalidade de "Desfazer" (Undo/Redo):** um dos usos mais comuns do Memento é na implementação de sistemas de "desfazer" e "refazer", que exigem a capacidade de retornar a um estado anterior;
- **Jogos de Vídeo com "Checkpoints" ou "Save Points":** em jogos de vídeo, especialmente em jogos de aventura ou RPG, o estado do jogo em um determinado ponto pode ser armazenado, permitindo ao jogador retomar o jogo do ponto salvo em vez de reiniciar do início;
- **Sistemas de Banco de Dados (Versões ou Snapshots):** em sistemas de banco de dados, pode ser útil armazenar um "snapshot" de dados em um ponto no tempo para que o sistema possa ser restaurado a esse estado mais tarde, em caso de erro ou corrupção de dados;
- **E-commerce – Carrinho de Compras:** em aplicações de e-commerce, capturar o estado do carrinho de compras de um usuário pode ser útil para restaurar o estado após uma falha no sistema ou após o usuário sair e retornar ao site.

![image](https://github.com/user-attachments/assets/0e9e4b7a-b28b-41c7-a271-719f9da918f3)



