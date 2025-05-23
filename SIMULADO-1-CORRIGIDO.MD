20 Questões - Com Correções e Explicações

QUESTÃO 1 - Domínio 1: Conceitos de Cloud (24%)
Uma empresa está considerando migrar sua infraestrutura on-premises para a AWS. Qual dos seguintes é um dos principais benefícios de usar a AWS Cloud?
A) A empresa deve gerenciar toda a infraestrutura física
B) A empresa pode converter despesas de capital (CAPEX) em despesas operacionais (OPEX)
C) A empresa precisa prever exatamente a capacidade necessária por anos
D) A empresa deve manter contratos de longo prazo para todos os serviços
✅ Resposta: B
Explicação: CAPEX → OPEX é um benefício fundamental da cloud. Alternativas A, C e D são desvantagens/responsabilidades on-premises.

QUESTÃO 2 - Domínio 2: Segurança e Compliance (30%)
No modelo de responsabilidade compartilhada da AWS, qual das seguintes é uma responsabilidade do CLIENTE?
A) Segurança física dos data centers da AWS
B) Aplicação de patches no hypervisor
C) Configuração de grupos de segurança
D) Manutenção da infraestrutura de rede global
✅ Resposta: C
Explicação: Cliente gerencia "segurança NA nuvem" (configurações, dados). AWS gerencia "segurança DA nuvem" (infraestrutura física, hypervisor).

QUESTÃO 3 - Domínio 3: Tecnologia e Serviços Cloud (34%)
Qual serviço AWS é MELHOR para hospedar uma aplicação web que precisa de alta disponibilidade e escalabilidade automática?
A) Amazon S3
B) Amazon EC2 com Auto Scaling
C) Amazon RDS
D) AWS Lambda
✅ Resposta: B
Explicação: EC2 + Auto Scaling = máquinas virtuais que escalam automaticamente. S3 é storage, RDS é banco, Lambda é serverless (limitado em tempo).

QUESTÃO 4 - Domínio 1: Conceitos de Cloud (24%)
Qual dos seguintes é um pilar do AWS Well-Architected Framework?
A) Disponibilidade
B) Eficiência de Performance
C) Compatibilidade
D) Popularidade
✅ Resposta: B
Explicação: 6 pilares: Excelência Operacional, Segurança, Confiabilidade, Eficiência de Performance, Otimização de Custos, Sustentabilidade.

QUESTÃO 5 - Domínio 2: Segurança e Compliance (30%)
Qual serviço AWS fornece proteção contra ataques DDoS (Distributed Denial of Service)?
A) Amazon GuardDuty
B) AWS Shield
C) Amazon Inspector
D) AWS Config
✅ Resposta: B
Explicação: Shield = proteção DDoS. GuardDuty = detecção de ameaças, Inspector = vulnerabilidades de aplicação, Config = conformidade.

QUESTÃO 6 - Domínio 3: Tecnologia e Serviços Cloud (34%)
Uma empresa precisa armazenar grandes quantidades de dados que são acessados raramente, mas devem estar disponíveis em algumas horas quando solicitados. Qual classe de armazenamento do Amazon S3 é mais apropriada?
A) S3 Standard
B) S3 Standard-IA (Infrequent Access)
C) S3 Glacier Flexible Retrieval
D) S3 One Zone-IA
✅ Resposta: C
Explicação: "Algumas horas" = Glacier Flexible Retrieval (1-12h). Standard = acesso imediato, Standard-IA = acesso ocasional mas rápido.

QUESTÃO 7 - Domínio 4: Billing, Pricing e Support (12%)
Qual ferramenta AWS ajuda a monitorar custos e criar alertas quando os gastos excedem limites predefinidos?
A) AWS Cost Explorer
B) AWS Budgets
C) AWS Billing Dashboard
D) AWS Trusted Advisor
✅ Resposta: B
Explicação: Budgets = alertas e limites de gastos. Cost Explorer = análise de custos históricos, Trusted Advisor = recomendações gerais.

QUESTÃO 8 - Domínio 3: Tecnologia e Serviços Cloud (34%)
Qual serviço AWS é um banco de dados NoSQL totalmente gerenciado?
A) Amazon RDS
B) Amazon DynamoDB
C) Amazon Aurora
D) Amazon Redshift
✅ Resposta: B
Explicação: DynamoDB = NoSQL. RDS e Aurora = relacionais (SQL), Redshift = data warehouse.

QUESTÃO 9 - Domínio 2: Segurança e Compliance (30%)
Qual é a MELHOR maneira de fornecer acesso temporário a recursos AWS para aplicações que executam em instâncias EC2?
A) Incorporar credenciais AWS no código da aplicação
B) Usar roles do IAM
C) Compartilhar chaves de acesso via email
D) Criar um usuário IAM permanente para cada aplicação
✅ Resposta: B
Explicação: IAM Roles = credenciais temporárias e seguras para EC2. Evitar hardcoding ou compartilhamento de credenciais.

QUESTÃO 10 - Domínio 1: Conceitos de Cloud (24%)
Qual dos seguintes descreve melhor a "elasticidade" na AWS Cloud?
A) A capacidade de manter dados seguros
B) A habilidade de escalar recursos para cima ou para baixo automaticamente baseado na demanda
C) A capacidade de acessar recursos de qualquer localização geográfica
D) A habilidade de fazer backup de dados automaticamente
✅ Resposta: B
Explicação: Elasticidade = escalabilidade automática conforme demanda. Não confundir com segurança, disponibilidade global ou backup.

QUESTÃO 11 - Domínio 3: Tecnologia e Serviços Cloud (34%)
Qual serviço AWS é usado para distribuir conteúdo globalmente com baixa latência?
A) Amazon Route 53
B) Amazon CloudFront
C) AWS Direct Connect
D) Amazon VPC
✅ Resposta: B
Explicação: CloudFront = CDN (Content Delivery Network). Route 53 = DNS, Direct Connect = conexão dedicada, VPC = rede privada.

QUESTÃO 12 - Domínio 2: Segurança e Compliance (30%)
Qual serviço AWS fornece detecção de ameaças e monitoramento contínuo de segurança usando machine learning?
A) AWS CloudTrail
B) Amazon GuardDuty
C) AWS Config
D) Amazon Inspector
✅ Resposta: B
Explicação: GuardDuty = detecção inteligente de ameaças com ML. CloudTrail = logs de API, Config = conformidade, Inspector = vulnerabilidades.

QUESTÃO 13 - Domínio 4: Billing, Pricing e Support (12%)
Qual plano de suporte AWS fornece acesso 24/7 ao suporte técnico via telefone, email e chat?
A) Basic
B) Developer
C) Business
D) Enterprise
✅ Resposta: C
Explicação: Business = 24/7 phone/chat. Basic = gratuito limitado, Developer = business hours apenas, Enterprise = inclui TAM.

QUESTÃO 14 - Domínio 3: Tecnologia e Serviços Cloud (34%)
Qual serviço AWS é MELHOR para executar código sem provisionar ou gerenciar servidores?
A) Amazon EC2
B) AWS Lambda
C) Amazon ECS
D) AWS Batch
✅ Resposta: B
Explicação: Lambda = serverless computing. EC2 = máquinas virtuais, ECS = containers, Batch = processamento em lote.

QUESTÃO 15 - Domínio 1: Conceitos de Cloud (24%)
O que significa "pay-as-you-go" na AWS?
A) Você paga apenas pelos recursos que usar
B) Você deve pagar antecipadamente por todos os recursos
C) Você paga uma taxa fixa mensal independente do uso
D) Você só paga se os recursos falharem
✅ Resposta: A
Explicação: Pay-as-you-go = pagamento por uso real. Modelo fundamental da cloud vs. investimento antecipado ou taxa fixa.

QUESTÃO 16 - Domínio 2: Segurança e Compliance (30%)
Qual ferramenta AWS fornece recomendações baseadas em melhores práticas?
A) AWS CloudFormation
B) AWS Trusted Advisor
C) AWS Systems Manager
D) Amazon CloudWatch
✅ Resposta: B
Explicação: Trusted Advisor = recomendações de otimização (custos, performance, segurança). CloudFormation = IaC, CloudWatch = monitoramento.

QUESTÃO 17 - Domínio 3: Tecnologia e Serviços Cloud (34%)
Uma empresa quer migrar 50TB de dados para a AWS de forma segura e rápida. Qual serviço AWS seria MAIS apropriado?
A) AWS Direct Connect
B) Amazon S3 Transfer Acceleration
C) AWS Snowball
D) AWS DataSync
✅ Resposta: C
Explicação: 50TB = Snowball (dispositivo físico). Transfer Acceleration = internet mais rápida, DataSync = sincronização online.

QUESTÃO 18 - Domínio 2: Segurança e Compliance (30%)
Qual característica do Amazon S3 fornece proteção adicional contra exclusão acidental de objetos?
A) Server-side encryption
B) Versioning
C) Cross-region replication
D) Transfer acceleration
✅ Resposta: B
Explicação: Versioning = múltiplas versões do objeto, proteção contra exclusão. Encryption = segurança, não proteção contra exclusão.

QUESTÃO 19 - Domínio 4: Billing, Pricing e Support (12%)
Qual ferramenta AWS permite visualizar e analisar custos e uso ao longo do tempo?
A) AWS Cost Explorer
B) AWS Billing Dashboard
C) AWS Budgets
D) AWS Cost and Usage Report
✅ Resposta: A
Explicação: Cost Explorer = análise visual de custos históricos. Budgets = alertas, Billing Dashboard = visão atual, CUR = relatórios detalhados.

QUESTÃO 20 - Domínio 3: Tecnologia e Serviços Cloud (34%)
Qual serviço AWS fornece um ambiente de desenvolvimento integrado (IDE) baseado em cloud?
A) AWS CodeCommit
B) AWS Cloud9
C) AWS CodeBuild
D) AWS CodeDeploy
✅ Resposta: B
Explicação: Cloud9 = IDE na nuvem. CodeCommit = repositório Git, CodeBuild = compilação, CodeDeploy = deployment.
