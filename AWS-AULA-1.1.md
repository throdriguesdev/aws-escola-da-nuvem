### Domínio 1: Conceitos de Nuvem (24%)

#### 1.1 Definição de Computação em Nuvem

- **Características essenciais**:
    - **Autoatendimento sob demanda**: Provisionamento sem intervenção humana
    - **Amplo acesso à rede**: Acesso por plataformas heterogêneas
    - **Pooling de recursos**: Recursos compartilhados entre múltiplos clientes
    - **Elasticidade rápida**: Escalabilidade automática conforme necessidade
    - **Serviço medido**: Pagamento apenas pelo que é usado

#### 1.2 Benefícios da AWS Cloud

- **Vantagens econômicas**:
    - **Despesa de capital (CapEx) → Despesa variável (OpEx)**: Elimina investimentos iniciais
    - **Economias de escala**: Custos unitários menores
    - **Capacidade otimizada**: Elimina provisão excessiva/insuficiente
    - **Agilidade**: Implantação rápida de recursos
    - **Alcance global imediato**: Presença internacional em minutos

#### 1.3 Infraestrutura Global AWS

- **Componentes principais**:
    - **Regiões**: Clusters de datacenters geograficamente isolados
        - Critérios de seleção: latência, preço, conformidade, disponibilidade de serviços
    - **Zonas de Disponibilidade (AZs)**: Datacenters isolados dentro de uma região
        - Conectadas por links de alta velocidade
        - Projetadas para isolamento de falhas
    - **Locais de Borda (Edge Locations)**: Pontos de presença para serviços CDN
        - Amazon CloudFront
        - AWS Global Accelerator
    - **Wavelength Zones**: Infraestrutura para aplicações 5G de baixa latência

#### 1.4 Modelos de Implantação em Nuvem

- **Tipos e características**:
    - **Nuvem pública**: 100% na AWS
        - Vantagens: sem hardware local, escalabilidade ilimitada
    - **Nuvem privada**: Recursos dedicados a uma única organização
        - AWS Outposts, VMware Cloud on AWS
    - **Nuvem híbrida**: Combinação de nuvem pública e infraestrutura local
        - AWS Direct Connect, VPN, Storage Gateway
    - **Multi-nuvem**: Uso de múltiplos provedores de nuvem

#### 1.5 Princípios de Design da Nuvem AWS

- **Well-Architected Framework**:
    - **Excelência operacional**: Automatização, documentação
    - **Segurança**: Proteção de dados, controle de acesso
    - **Confiabilidade**: Recuperação de falhas, alta disponibilidade
    - **Eficiência de performance**: Uso eficiente de recursos
    - **Otimização de custos**: Monitoramento e ajuste de gastos
    - **Sustentabilidade**: Minimização de impacto ambiental

### Domínio 2: Segurança e Conformidade (30%)

#### 2.1 Modelo de Responsabilidade Compartilhada

- **Responsabilidades da AWS**:
    - Segurança física dos datacenters
    - Hardware e infraestrutura global
    - Software de virtualização
    - Segurança da rede
- **Responsabilidades do Cliente**:
    - Configuração de IAM
    - Dados sensíveis do cliente (criptografia)
    - Sistema operacional, rede e aplicações
    - Configuração de firewalls e segurança de rede
- **Controles compartilhados**:
    - Gestão de patches
    - Configuração
    - Conscientização e treinamento

#### 2.2 Serviços de Segurança AWS

- **Gerenciamento de Identidade**:
    - **IAM (Identity and Access Management)**:
        - Políticas baseadas em identidade vs. baseadas em recursos
        - Federação de identidade e SSO
        - IAM Access Analyzer
    - **AWS Organizations**: Gerenciamento centralizado de múltiplas contas
        - SCPs (Service Control Policies)
        - OUs (Organizational Units)
- **Proteção de Dados**:
    - **AWS KMS (Key Management Service)**: Gerenciamento de chaves de criptografia
    - **AWS Secrets Manager**: Rotação automática de segredos
    - **Amazon Macie**: Descoberta e proteção de dados sensíveis
    - **CloudHSM**: Hardware para gerenciamento de chaves
- **Segurança de Rede**:
    - **Security Groups**: Firewall stateful para controle de entrada/saída
    - **Network ACLs**: Firewall stateless no nível de sub-rede
    - **AWS WAF**: Firewall de aplicações web
    - **AWS Shield**: Proteção contra DDoS
        - Standard (gratuito) vs. Advanced (pago)
    - **AWS Firewall Manager**: Gerenciamento centralizado de políticas
- **Monitoramento e Detecção**:
    - **Amazon GuardDuty**: Detecção de ameaças
    - **Amazon Inspector**: Avaliação de vulnerabilidades
    - **AWS Config**: Avaliação, auditoria e inventário de recursos
    - **AWS CloudTrail**: Registro de atividades de API
    - **Amazon Security Hub**: Visão unificada de segurança

#### 2.3 Conformidade e Governança

- **Programas de Conformidade**:
    - **AWS Artifact**: Portal de acesso a relatórios de conformidade
    - **Conformidades específicas**: GDPR, HIPAA, PCI DSS, SOC, ISO
    - **AWS Control Tower**: Governança para múltiplas contas
- **Recursos de Conformidade**:
    - **Atestações/Certificações**: Validações por terceiros
    - **Leis/Regulamentos**: Conformidade com requisitos legais
    - **Frameworks de Alinhamento**: Mapeamento para padrões da indústria

#### 2.4 Boas Práticas de Segurança

- **Princípio do privilégio mínimo**
- **Autenticação Multifator (MFA)**
- **Criptografia em trânsito e em repouso**
- **Rotação regular de credenciais**
- **Monitoramento e logging contínuos**

### Domínio 3: Tecnologia e Serviços em Nuvem (34%)

#### 3.1 Serviços de Computação

- **Amazon EC2 (Elastic Compute Cloud)**:
    - **Tipos de instâncias**: General Purpose, Compute Optimized, Memory Optimized, etc.
    - **Opções de compra**: On-Demand, Reserved, Spot, Savings Plans
    - **AMIs (Amazon Machine Images)**: Templates para instâncias
    - **Auto Scaling**: Ajuste automático de capacidade
- **Tecnologias Serverless**:
    - **AWS Lambda**: Funções como serviço
        - Triggers e integrações
        - Modelo de precificação por execução
    - **AWS Fargate**: Containers serverless
- **Serviços de Contêineres**:
    - **Amazon ECS (Elastic Container Service)**
    - **Amazon EKS (Elastic Kubernetes Service)**
    - **Amazon ECR (Elastic Container Registry)**
- **Outros Serviços de Computação**:
    - **AWS Elastic Beanstalk**: PaaS para desenvolvimento web
    - **Amazon Lightsail**: VPS simplificado
    - **AWS Batch**: Processamento em lote

#### 3.2 Serviços de Armazenamento

- **Amazon S3 (Simple Storage Service)**:
    - **Classes de armazenamento**: Standard, Intelligent-Tiering, One Zone-IA, Glacier
    - **Recursos**: Versionamento, Replicação, Ciclo de vida
    - **Controle de acesso**: Políticas de bucket, ACLs, Pontos de acesso
- **Amazon EBS (Elastic Block Store)**:
    - **Tipos de volumes**: SSD, HDD, IOPS provisionadas
    - **Snapshots e backups**
    - **Criptografia**
- **Armazenamento de Arquivos**:
    - **Amazon EFS (Elastic File System)**: NFS gerenciado
    - **Amazon FSx**: Windows File Server, Lustre
- **Storage Gateway**:
    - **File Gateway**
    - **Volume Gateway**
    - **Tape Gateway**

#### 3.3 Serviços de Banco de Dados

- **Amazon RDS (Relational Database Service)**:
    - **Engines suportadas**: MySQL, PostgreSQL, Oracle, SQL Server, MariaDB
    - **Amazon Aurora**: Compatível com MySQL/PostgreSQL com performance 5x melhor
    - **Multi-AZ**: Alta disponibilidade
    - **Read Replicas**: Escalabilidade de leitura
- **DynamoDB (NoSQL)**:
    - **Modelo sem servidor**
    - **Escalabilidade automática**
    - **Consistência eventual vs. forte**
    - **DAX (DynamoDB Accelerator)**: Cache em memória
- **Outros Serviços de Dados**:
    - **Amazon Redshift**: Data warehousing
    - **ElastiCache**: Memcached/Redis
    - **Neptune**: Banco de dados de grafos
    - **DocumentDB**: Compatível com MongoDB
    - **Amazon Keyspaces**: Compatível com Cassandra

#### 3.4 Serviços de Rede

- **Amazon VPC (Virtual Private Cloud)**:
    - **Subnets**: Públicas vs. privadas
    - **Route Tables**: Controle de roteamento
    - **Internet Gateway, NAT Gateway**
    - **VPC Peering, Transit Gateway**
- **Conectividade**:
    - **AWS Direct Connect**: Link privado dedicado
    - **VPN**: Site-to-site, Client VPN
- **Distribuição de Tráfego**:
    - **Elastic Load Balancing**:
        - Application Load Balancer (Camada 7)
        - Network Load Balancer (Camada 4)
        - Classic Load Balancer (legado)
    - **Amazon Route 53**: DNS gerenciado
        - Políticas de roteamento
- **Amazon CloudFront (CDN)**:
    - **Edge Locations** e **Regional Edge Caches**
    - **Origem: S3, EC2, ELB, etc.**
    - **Configurações de cache e expiração**

#### 3.5 Serviços de Integração de Aplicações

- **Amazon SQS (Simple Queue Service)**:
    - Filas padrão vs. FIFO
    - Desacoplamento de aplicações
- **Amazon SNS (Simple Notification Service)**:
    - Publicação/assinatura
    - Notificações push
- **Amazon EventBridge (CloudWatch Events)**:
    - Barramento de eventos
    - Integração com serviços AWS e SaaS
- **AWS Step Functions**:
    - Orquestração de fluxos de trabalho
    - Máquinas de estado

#### 3.6 Ferramentas de Gerenciamento e Governança

- **AWS Management Console**
- **AWS CLI (Command Line Interface)**
- **AWS SDK (Software Development Kit)**
- **AWS CloudFormation**: Infraestrutura como código
- **AWS CloudWatch**:
    - Métricas, logs, alarmes, eventos
    - Painéis personalizados
- **AWS CloudTrail**: Auditoria de API
- **AWS Config**: Conformidade e inventário
- **AWS Systems Manager**: Gerenciamento de recursos
- **AWS Trusted Advisor**: Otimização e recomendações

### Domínio 4: Faturamento, Preços e Suporte (12%)

#### 4.1 Modelos de Preços AWS

- **Estruturas de preços**:
    - **Pay-as-you-go**: Pagamento pelo uso
    - **Save when you commit**: Desconto por compromisso
    - **Pay less by using more**: Descontos por volume
    - **Savings Plans**: Descontos por compromisso de uso
    - **Reserved Instances**: Compromisso de 1 ou 3 anos
        - Opções de pagamento: No upfront, Partial upfront, All upfront
    - **Spot Instances**: Capacidade não utilizada com desconto

#### 4.2 Compreendendo os Preços por Serviço

- **Fatores comuns de preço**:
    - **Computação**: Hora ou segundo de uso
    - **Armazenamento**: GB/mês
    - **Transferência de dados**: GB de saída
    - **Requisições/chamadas de API**
- **Exemplos específicos**:
    - **EC2**: Tipo de instância, tempo de uso, região, opção de compra
    - **S3**: Classe de armazenamento, volume armazenado, transferência, requisições
    - **RDS**: Classe de instância, armazenamento, backups, multi-AZ
    - **Lambda**: Número de requisições, duração, memória alocada

#### 4.3 AWS Free Tier

- **Camadas do Free Tier**:
    - **Sempre gratuito**: Serviços com uso gratuito permanente
    - **12 meses gratuitos**: Após criação da conta AWS
    - **Trials**: Testes de curto prazo para serviços específicos
- **Exemplos de serviços**:
    - **Sempre gratuito**: Lambda (1 milhão de requisições/mês), DynamoDB (25GB)
    - **12 meses**: EC2 (750 horas/mês), S3 (5GB), RDS (750 horas/mês)

#### 4.4 Ferramentas de Gerenciamento de Custos

- **AWS Billing Console**:
    - Visibilidade de custos atuais e previstos
    - Uso do Free Tier
- **AWS Cost Explorer**:
    - Análise de custos históricos
    - Previsões de custos
    - Granularidade por serviço, tag, região, etc.
- **AWS Budgets**:
    - Criação de orçamentos personalizados
    - Alertas de ultrapassagem
    - Orçamentos de uso e cobertura de RI/SP
- **AWS Cost and Usage Report**:
    - Relatório detalhado de custos
    - Integração com Amazon Athena e QuickSight
- **AWS Cost Anomaly Detection**:
    - Detecção de gastos anormais
    - Alertas proativos

#### 4.5 AWS Organizations e Faturamento Consolidado

- **AWS Organizations**:
    - Gerenciamento centralizado de contas
    - Contas múltiplas com faturamento único
- **Benefícios do Faturamento Consolidado**:
    - Fatura única
    - Visibilidade dos custos de todas as contas
    - Descontos por volume compartilhados
    - Compartilhamento de RI e Savings Plans

#### 4.6 Planos de Suporte AWS

- **Basic Support**: Gratuito para todos os clientes
    - Suporte para problemas de conta e faturamento
    - Fóruns de comunidade
    - Service Health Dashboard
    - Documentação, whitepapers e guias
- **Developer Support**: Para ambientes de teste/desenvolvimento
    - Suporte técnico por e-mail em horário comercial
    - 1 contato de suporte
    - Tempo de resposta: 12-24 horas
- **Business Support**: Para ambientes de produção
    - Suporte técnico 24/7 por chat e telefone
    - Número ilimitado de contatos
    - Tempo de resposta: 1-4 horas
    - Trusted Advisor completo
    - AWS Support API
- **Enterprise Support**: Para aplicações críticas
    - Gerente técnico de conta (TAM)
    - Revisões arquiteturais
    - Tempo de resposta: 15 min para críticos
    - Suporte concierge
    - Workshop de arquitetura

#### 4.7 AWS Trusted Advisor

- **Categorias de verificação**:
    - **Otimização de custos**: Recursos ociosos, reservas
    - **Desempenho**: Otimização de throughput e latência
    - **Segurança**: Vulnerabilidades, permissões
    - **Tolerância a falhas**: Redundância, backups
    - **Limites de serviço**: Aproximação de quotas

## Simulados e Avaliação

### Tipos de Questões

- Múltipla escolha (uma resposta correta)
- Múltipla seleção (duas ou mais respostas corretas)

### Estratégias para o Exame

- Leia as questões com atenção
- Procure palavras-chave como "mais rentável", "mais seguro", "menor latência"
- Elimine respostas obviamente incorretas
- Priorize serviços principais da AWS em vez de serviços de nicho
- Gerencie seu tempo (90 minutos para 65 questões)

### Pontuação Mínima de Aprovação

- 700/1000 pontos (aprox. 70%)

## Prática Recomendada

### Serviços para Laboratórios Práticos

- EC2
- S3
- IAM
- VPC
- RDS
- CloudWatch
- Billing Dashboard

https://d1.awsstatic.com/whitepapers/pt_BR/aws-overview.pdf
https://docs.aws.amazon.com/pt_br/glossary/latest/reference/glos-chap.html
https://d1.awsstatic.com/pt_BR/training-and-certification/docs-cloud-practitioner/AWS-Certified-Cloud-Practitioner_Sample-Questions.pdf
