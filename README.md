# IT Workshop Meetup — Cloud Concepts

## Descrição do Workshop

Este repositório contém os materiais de estudo e laboratórios práticos do workshop **Cloud Concepts**, apresentado no IT Workshop Meetup. O conteúdo aborda os fundamentos de computação em nuvem, serviços AWS, arquiteturas serverless, estratégias de migração e padrões modernos de sistemas. O objetivo é oferecer uma visão sólida e prática para quem deseja iniciar ou aprofundar seus conhecimentos em cloud computing.

## Tópicos Abordados

- Definição e benefícios da computação em nuvem (pay-as-you-go, escalabilidade, elasticidade)
- Comparação com infraestrutura on-premise
- Visão geral da AWS e seus serviços centrais (EC2, S3, RDS)
- Arquitetura serverless e Function-as-a-Service (FaaS)
- Modelos de serviço: IaaS, PaaS, SaaS, FaaS
- Estratégias de migração para nuvem: os 6 Rs (Rehost, Replatform, Repurchase, Re-architect, Retire, Retain)
- Modernização de aplicações e padrões de arquitetura (microservices, DDD, Event Sourcing, CQRS)
- Conceitos modernos: load balancing, caching, CDN, message queues, API gateway, circuit breaker
- Multicloud e cloud híbrida
- Laboratórios práticos: construção de backend API serverless com integração de IA

## Visão Geral de Computação em Nuvem

Computação em nuvem é a entrega de recursos computacionais (servidores, armazenamento, bancos de dados, redes, software) sob demanda, pela internet, com cobrança baseada no uso (pay-as-you-go). Os principais benefícios incluem:

- **Escalabilidade horizontal e vertical**: ajuste dinâmico de recursos conforme a demanda
- **Elasticidade**: provisionamento rápido e automático
- **Redução de custos operacionais**: eliminação de investimento inicial em hardware
- **Alta disponibilidade e recuperação de desastres**: infraestrutura redundante e distribuída

Em contraste com o modelo **on-premise**, onde a empresa é responsável por todo o ciclo de vida dos servidores, a nuvem transfere grande parte da gestão para o provedor.

## AWS e Serviços Centrais

A **Amazon Web Services (AWS)** é o provedor de nuvem mais utilizado globalmente. Seus serviços mais citados no workshop:

- **EC2 (Elastic Compute Cloud)**: servidores virtuais sob demanda, com controle total do sistema operacional
- **S3 (Simple Storage Service)**: armazenamento de objetos altamente escalável e durável
- **RDS (Relational Database Service)**: bancos de dados relacionais gerenciados (MySQL, PostgreSQL, etc.)

Outros serviços mencionados: Lambda (computação serverless), API Gateway, SQS (filas), CloudFront (CDN) e DynamoDB (NoSQL).

## Serverless e FaaS

**Serverless** não significa ausência de servidores, mas sim que a gestão da infraestrutura é abstraída do desenvolvedor. O **Function-as-a-Service (FaaS)** é o modelo mais representativo, onde funções individuais são executadas em resposta a eventos.

Características do FaaS:
- **Event-driven**: execução acionada por eventos (HTTP, upload de arquivo, alteração em banco de dados)
- **Auto-scaling**: escala automaticamente de zero a milhares de execuções concorrentes
- **Zero administration**: sem gerenciamento de servidores ou sistemas operacionais
- **Pay-per-execution**: cobrança por tempo de execução e número de invocações
- **Cold start**: latência inicial quando a função não está aquecida

**Vantagens**: redução de custos operacionais, foco no código, escalabilidade automática.  
**Desafios**: cold start, vendor lock-in, monitoramento complexo e depuração limitada.

## Estratégias de Migração para Nuvem (Os 6 Rs)

1. **Rehost** (lift & shift): mover a aplicação exatamente como está para a nuvem
2. **Replatform** (lift, tinker and shift): fazer pequenas otimizações sem mudar a arquitetura central
3. **Repurchase**: substituir o software atual por uma versão SaaS
4. **Re-architect** (refactor): reescrever a aplicação para aproveitar ao máximo os serviços nativos da nuvem
5. **Retire**: desligar sistemas obsoletos
6. **Retain**: manter parte da infraestrutura on-premise

A escolha da estratégia depende do custo, prazo, necessidades de modernização e maturidade da equipe.

## Modelos XaaS (Tudo como Serviço)

- **IaaS (Infrastructure as a Service)**: recursos de infraestrutura fundamentais (VMs, armazenamento, redes) — exemplo: EC2
- **PaaS (Platform as a Service)**: plataforma gerenciada para desenvolvimento e implantação de aplicações — exemplo: Elastic Beanstalk
- **SaaS (Software as a Service)**: software pronto para uso entregue pela internet — exemplo: Gmail, Salesforce
- **FaaS (Function as a Service)**: execução de funções isoladas sem gerenciar servidores — exemplo: AWS Lambda

## Conceitos Modernos de Arquitetura de Sistemas

- **Microservices**: decomposição de uma aplicação monolítica em serviços independentes e fracamente acoplados
- **Domain-Driven Design (DDD)**: modelagem de software baseada no domínio do negócio
- **Event Sourcing**: persistência de eventos como fonte da verdade, permitindo reconstrução de estados
- **CQRS (Command Query Responsibility Segregation)**: separação de operações de leitura e escrita
- **Load Balancing**: distribuição de tráfego entre múltiplos servidores
- **Caching**: armazenamento temporário de dados para reduzir latência (ex: Redis, CloudFront)
- **CDN (Content Delivery Network)**: entrega de conteúdo a partir de pontos de presença distribuídos
- **Message Queues**: comunicação assíncrona entre serviços (ex: Amazon SQS)
- **API Gateway**: ponto único de entrada para APIs, com autenticação, cache e roteamento
- **Circuit Breaker**: padrão para evitar falhas em cascata em sistemas distribuídos

## Aprendizados Práticos / Laboratórios

Durante o workshop foram propostos laboratórios práticos:

1. **Construção de uma backend API serverless**: criação de endpoints REST utilizando AWS Lambda, API Gateway e DynamoDB
2. **Arquitetura serverless completa**: implementação de funções acionadas por eventos, como upload de arquivos no S3
3. **Integração de inteligência artificial**: adição de serviços de IA (Amazon Rekognition, Comprehend) usando FaaS
4. **Arquitetura resultante pronta para portfólio/currículo**: uma aplicação serverless funcional que pode ser demonstrada

Esses laboratórios visam consolidar os conceitos teóricos e gerar um projeto real para apresentação profissional.

## Referências e Continuidade de Estudo

- Documentação oficial da AWS: [aws.amazon.com/documentation](https://aws.amazon.com/documentation/)
- AWS Well-Architected Framework: [wa.aws.amazon.com](https://wa.aws.amazon.com/)
- Guia de Serverless: [serverlessland.com](https://serverlessland.com/)
- Cursos gratuitos na AWS Skill Builder: [aws.amazon.com/training](https://aws.amazon.com/training/)
- Livros sugeridos: "The Phoenix Project", "Designing Data-Intensive Applications" e "Building Microservices" de Sam Newman

## Como Usar Este Material

1. **Estudo teórico**: leia as seções acima para entender os fundamentos
2. **Reprodução dos laboratórios**: siga as instruções dos scripts e arquivos de configuração neste repositório (caso disponíveis)
3. **Adaptação**: modifique os exemplos para suas próprias necessidades
4. **Contribuição**: sinta-se à vontade para abrir issues ou pull requests para melhorias

## Pré-requisitos Conceituais

- Noções básicas de programação (qualquer linguagem)
- Conhecimento superficial de redes (HTTP, DNS)
- Familiaridade com terminal/linha de comando
- Vontade de aprender e experimentar!

## Possíveis Próximos Passos

1. Explorar mais serviços AWS (ECS, EKS, DynamoDB, CloudFormation)
2. Obter certificações de entrada, como **AWS Cloud Practitioner** (fundamentos) e **AWS Developer Associate** (prática)
3. Aprofundar em padrões avançados de serverless (Lambda Layers, Step Functions)
4. Estudar estratégias de migração mais complexas (re-architect de aplicações monolíticas)
5. Participar de meetups, hackathons ou fóruns de cloud para ganhar experiência colaborativa
