# Guia Completo AWS Cloud Practitioner (CLF-C02)

## Visão Geral do Exame

- **Código:** CLF-C02
- **Duração:** 90 minutos
- **Questões:** 65 questões (50 pontuadas + 15 não pontuadas)
- **Pontuação mínima:** 700/1000 pontos (~70%)
- **Formato:** Múltipla escolha (1 resposta) e múltipla seleção (2+ respostas)
- **Idiomas:** Disponível em português

### Estratégias para o Exame
- Procure palavras-chave: "mais econômico", "menor latência", "alta disponibilidade", "maior segurança"
- Elimine opções obviamente incorretas primeiro
- Foque nos serviços principais da AWS (não serviços de nicho)
- Gerencie o tempo: ~1,4 minutos por questão

---

# DOMÍNIO 1: CONCEITOS DE NUVEM (24%)

## 1.1 Fundamentos da Computação em Nuvem

### Características Essenciais NIST
1. **Autoatendimento sob demanda**
   - Provisionamento automático sem intervenção humana
   - Exemplos: Lançar EC2, criar bucket S3

2. **Amplo acesso à rede**
   - Acesso via internet por diversos dispositivos
   - APIs, Console Web, CLI, SDKs

3. **Pool de recursos**
   - Recursos compartilhados entre múltiplos clientes
   - Multi-tenancy com isolamento lógico

4. **Elasticidade rápida**
   - Escalabilidade automática up/down
   - Auto Scaling Groups, Lambda

5. **Serviço medido**
   - Pay-per-use, monitoramento detalhado
   - CloudWatch Metrics, Billing

## 1.2 Benefícios da AWS Cloud

### Vantagens Econômicas
- **CapEx → OpEx:** Elimina investimentos iniciais em hardware
- **Economias de escala:** AWS compra em volume, repassa economia
- **Capacidade otimizada:** Elimina over/under provisioning
- **Agilidade:** Deploy em minutos vs. semanas
- **Alcance global:** Presença mundial instantânea

### Dica para o Exame
*Questões sobre benefícios da nuvem sempre destacam: redução de custos, agilidade, escalabilidade global e eliminação de adivinhação de capacidade.*

## 1.3 Infraestrutura Global AWS

### Regiões (Regions)
- **Definição:** Clusters de datacenters geograficamente separados
- **Critérios de seleção:**
  - Latência para usuários finais
  - Conformidade legal/regulatória
  - Preços (variam por região)
  - Disponibilidade de serviços

### Zonas de Disponibilidade (AZs)
- **Definição:** Datacenters isolados dentro de uma região
- **Características:**
  - Mínimo 3 AZs por região
  - Conectadas por links de baixa latência
  - Isolamento de falhas físicas
  - Distância: 10s de km entre AZs

### Locais de Borda (Edge Locations)
- **Função:** Cache de conteúdo próximo aos usuários
- **Serviços:** CloudFront, Global Accelerator
- **Quantidade:** 400+ edge locations globalmente

### Wavelength Zones
- **Propósito:** Aplicações 5G de ultra-baixa latência
- **Localização:** Dentro de redes de operadoras de telecomunicações

## 1.4 Modelos de Implantação

### Nuvem Pública
- **Características:** 100% na AWS, sem hardware próprio
- **Vantagens:** Escalabilidade ilimitada, sem manutenção

### Nuvem Privada
- **Características:** Recursos dedicados
- **Soluções AWS:** Outposts, VMware Cloud on AWS

### Nuvem Híbrida
- **Características:** Combinação público + on-premises
- **Conectividade:** Direct Connect, VPN, Storage Gateway

## 1.5 Well-Architected Framework

### 6 Pilares
1. **Excelência Operacional:** Automação, monitoramento
2. **Segurança:** Proteção em todas as camadas
3. **Confiabilidade:** Recuperação automática de falhas
4. **Eficiência de Performance:** Uso otimizado de recursos
5. **Otimização de Custos:** Pagar apenas pelo necessário
6. **Sustentabilidade:** Minimizar impacto ambiental

---

# DOMÍNIO 2: SEGURANÇA E CONFORMIDADE (30%)

## 2.1 Modelo de Responsabilidade Compartilhada

### Responsabilidade da AWS: "Segurança DA Nuvem"
- Infraestrutura física (datacenters, hardware)
- Software de virtualização e hypervisor
- Rede global e isolamento entre clientes
- Serviços gerenciados (RDS, Lambda, S3)

### Responsabilidade do Cliente: "Segurança NA Nuvem"
- Dados do cliente e criptografia
- Sistema operacional e patches (EC2)
- Configuração de rede (Security Groups, NACLs)
- Gerenciamento de identidade (IAM)
- Aplicações e códigos

### Dica para o Exame
*Memorize: AWS cuida da infraestrutura, cliente cuida dos dados e configurações. Em serviços gerenciados, AWS assume mais responsabilidades.*

## 2.2 AWS Identity and Access Management (IAM)

### Componentes Principais
- **Usuários:** Identidades permanentes para pessoas
- **Grupos:** Coleções de usuários
- **Funções (Roles):** Identidades temporárias para serviços/aplicações
- **Políticas:** Documentos JSON definindo permissões

### Boas Práticas IAM
- Princípio do menor privilégio
- Usar funções em vez de usuários para aplicações
- Habilitar MFA para usuários privilegiados
- Rotacionar credenciais regularmente
- Usar AWS IAM Access Analyzer

## 2.3 Serviços de Segurança

### Proteção de Dados
- **AWS KMS:** Gerenciamento de chaves de criptografia
- **CloudHSM:** Hardware dedicado para chaves
- **Secrets Manager:** Rotação automática de credenciais
- **Macie:** Descoberta de dados sensíveis (PII)

### Segurança de Rede
- **Security Groups:** Firewall stateful (nível de instância)
- **NACLs:** Firewall stateless (nível de subnet)
- **AWS WAF:** Proteção contra ataques web
- **Shield:** Proteção DDoS (Standard gratuito, Advanced pago)

### Monitoramento e Detecção
- **GuardDuty:** Detecção de ameaças com ML
- **Inspector:** Vulnerabilidades em aplicações
- **Config:** Auditoria de configurações
- **CloudTrail:** Log de chamadas de API

## 2.4 Conformidade

### AWS Artifact
- Portal de acesso a relatórios de conformidade
- Acordos sob demanda (BAA, etc.)

### Principais Conformidades
- **GDPR:** Proteção de dados europeus
- **HIPAA:** Dados de saúde nos EUA
- **PCI DSS:** Dados de cartão de crédito
- **SOC 1/2/3:** Auditoria de controles
- **ISO 27001:** Segurança da informação

---

# DOMÍNIO 3: TECNOLOGIA E SERVIÇOS EM NUVEM (34%)

## 3.1 Serviços de Computação

### Amazon EC2 (Elastic Compute Cloud)

#### Tipos de Instâncias
- **General Purpose (T3, T4g, M5, M6i):**
  - Balanceamento CPU/memória/rede
  - Casos de uso: aplicações web, microserviços
  - T3/T4g: Burstable performance (créditos CPU)

- **Compute Optimized (C5, C6i):**
  - Alto desempenho de CPU
  - Casos de uso: HPC, gaming, modelagem científica

- **Memory Optimized (R5, R6i, X1e):**
  - Grande quantidade de RAM
  - Casos de uso: bancos de dados em memória, big data

- **Storage Optimized (I3, D2):**
  - Alto IOPS local
  - Casos de uso: data warehousing, sistemas distribuídos

- **Accelerated Computing (P3, G4):**
  - GPUs para ML/AI
  - Casos de uso: machine learning, renderização

#### Opções de Compra
1. **On-Demand:**
   - Pagamento por hora/segundo
   - Sem compromisso, máxima flexibilidade
   - Ideal para: cargas variáveis, desenvolvimento

2. **Reserved Instances (RI):**
   - Compromisso de 1 ou 3 anos
   - Desconto até 75% vs On-Demand
   - Tipos: Standard (maior desconto), Convertible (flexibilidade)
   - Pagamento: No upfront, Partial upfront, All upfront

3. **Savings Plans:**
   - Compromisso de gasto por hora
   - Flexibilidade entre tipos/regiões
   - Desconto até 72%

4. **Spot Instances:**
   - Usa capacidade ociosa da AWS
   - Desconto até 90%
   - Pode ser interrompida com 2min de aviso
   - Ideal para: processamento batch, análise de dados

#### Amazon Machine Images (AMIs)
- Templates para instâncias EC2
- Contém: SO, aplicações, configurações
- Tipos: Amazon Linux, Windows, Community, Marketplace

#### Auto Scaling
- **Auto Scaling Groups:** Ajuste automático de capacidade
- **Políticas:** Target tracking, step scaling, simple scaling
- **Métricas:** CPU, rede, custom metrics

### AWS Lambda (Serverless)

#### Características
- **Execução:** Código executado sob demanda
- **Linguagens:** Python, Node.js, Java, Go, .NET, Ruby
- **Limites:** 15min execução, 10GB RAM, 512MB /tmp
- **Triggers:** API Gateway, S3, DynamoDB, CloudWatch Events

#### Modelo de Preços
- Gratuito: 1M requisições/mês + 400.000 GB-segundos
- Cobrança por: número de requisições + duração × memória

#### Casos de Uso
- APIs serverless
- Processamento de eventos
- Automação de tarefas
- Backends para mobile/web

### Serviços de Contêineres

#### Amazon ECS (Elastic Container Service)
- **Orquestração:** Gerenciamento de contêineres Docker
- **Launch Types:**
  - EC2: Você gerencia a infraestrutura
  - Fargate: Serverless, AWS gerencia tudo
- **Task Definitions:** Blueprint dos contêineres

#### Amazon EKS (Elastic Kubernetes Service)
- **Kubernetes gerenciado** pela AWS
- **Compatibilidade:** 100% com Kubernetes vanilla
- **Integrações:** IAM, VPC, ELB, EBS

#### Amazon ECR (Elastic Container Registry)
- Registry privado para imagens Docker
- Integração com ECS/EKS
- Análise de vulnerabilidades

### Outros Serviços de Computação

#### AWS Elastic Beanstalk
- **PaaS:** Plataforma como Serviço
- **Linguagens:** Java, .NET, PHP, Node.js, Python, Ruby, Go
- **Gerenciamento:** AWS cuida da infraestrutura
- **Controle:** Acesso completo aos recursos subjacentes

#### Amazon Lightsail
- **VPS simplificado:** Servidores virtuais pré-configurados
- **Preço fixo:** Previsibilidade de custos
- **Casos de uso:** Websites simples, ambientes de desenvolvimento

## 3.2 Serviços de Armazenamento

### Amazon S3 (Simple Storage Service)

#### Características Principais
- **Durabilidade:** 99.999999999% (11 9's)
- **Disponibilidade:** 99.99% (Standard)
- **Capacidade:** Virtualmente ilimitada
- **Tamanho de objeto:** 0 bytes a 5TB

#### Classes de Armazenamento
1. **S3 Standard:**
   - Uso geral, acesso frequente
   - Disponibilidade: 99.99%
   - Casos de uso: aplicações, websites, CDN

2. **S3 Standard-IA (Infrequent Access):**
   - Dados acessados raramente
   - Menor custo de armazenamento
   - Taxa por recuperação

3. **S3 One Zone-IA:**
   - Uma única AZ (menor resiliência)
   - 20% mais barato que Standard-IA
   - Dados replicáveis

4. **S3 Glacier Instant Retrieval:**
   - Archive com acesso instantâneo
   - Dados acessados trimestralmente
   - 68% mais barato que Standard-IA

5. **S3 Glacier Flexible Retrieval:**
   - Archive tradicional
   - Recuperação: 1min a 12h
   - Casos de uso: backup, compliance

6. **S3 Glacier Deep Archive:**
   - Menor custo
   - Recuperação: 12-48h
   - Retenção longa (7-10 anos)

7. **S3 Intelligent-Tiering:**
   - Move automaticamente entre classes
   - Sem taxas de recuperação
   - Pequena taxa de monitoramento

#### Recursos Avançados
- **Versionamento:** Múltiplas versões do mesmo objeto
- **Replicação:** Cross-Region ou Same-Region
- **Lifecycle:** Transição automática entre classes
- **Event Notifications:** Trigger para Lambda, SQS, SNS
- **Transfer Acceleration:** CloudFront para uploads

#### Segurança S3
- **Bucket Policies:** Políticas baseadas em recursos
- **ACLs:** Access Control Lists (legado)
- **Access Points:** Simplificação de acesso
- **Block Public Access:** Proteção contra vazamento
- **Criptografia:**
  - SSE-S3: Chaves gerenciadas pela AWS
  - SSE-KMS: Integração com AWS KMS
  - SSE-C: Chaves fornecidas pelo cliente

### Amazon EBS (Elastic Block Store)

#### Tipos de Volume
1. **gp3 (General Purpose SSD):**
   - 3.000 IOPS baseline
   - IOPS e throughput independentes
   - Melhor custo-benefício

2. **gp2 (General Purpose SSD):**
   - 3 IOPS por GB (min 100, max 16.000)
   - Burst performance com créditos
   - Casos de uso: boot volumes, desenvolvimento

3. **io2/io2 Block Express (Provisioned IOPS):**
   - Alto desempenho, baixa latência
   - Até 256.000 IOPS
   - Casos de uso: bancos críticos, NoSQL

4. **st1 (Throughput Optimized HDD):**
   - Big data, data warehouses
   - Não pode ser boot volume
   - Alto throughput sequencial

5. **sc1 (Cold HDD):**
   - Menor custo
   - Acesso infrequente
   - Não pode ser boot volume

#### Características EBS
- **Snapshots:** Backup incremental para S3
- **Encryption:** Criptografia em repouso e trânsito
- **Multi-Attach:** Anexar a múltiplas instâncias (io1/io2)
- **Fast Snapshot Restore:** Restauração rápida

### Amazon EFS (Elastic File System)

#### Características
- **NFS v4.1** gerenciado
- **Escalabilidade:** Petabytes automaticamente
- **Concurrent access:** Milhares de instâncias
- **Performance Modes:**
  - General Purpose: latência mais baixa
  - Max I/O: maior throughput e IOPS

#### Throughput Modes
- **Bursting:** 100 MiB/s baseline + burst
- **Provisioned:** Throughput independente do armazenamento

#### Classes de Armazenamento
- **Standard:** Acesso frequente
- **IA (Infrequent Access):** 92% economia
- **Lifecycle Management:** Transição automática

### Amazon FSx

#### FSx for Windows File Server
- **SMB protocol** totalmente gerenciado
- **Active Directory integration**
- **Windows features:** Deduplicação, VSS, DFS

#### FSx for Lustre
- **High-performance computing** (HPC)
- **Machine learning workloads**
- **Integração S3:** Import/export automático

### AWS Storage Gateway

#### File Gateway
- **NFS/SMB interface** para S3
- **Cache local** para acesso frequente
- **Casos de uso:** File shares, content distribution

#### Volume Gateway
- **Stored Volumes:** Dados primários on-premises
- **Cached Volumes:** Dados primários na AWS
- **iSCSI protocol**

#### Tape Gateway
- **Virtual Tape Library (VTL)**
- **Substituição de fitas físicas**
- **Integração:** Veeam, Commvault, NetBackup




> [!parei aqui] Title
> Contents
## 3.3 Serviços de Banco de Dados

### Amazon RDS (Relational Database Service)

#### Engines Suportadas
- **MySQL, PostgreSQL, MariaDB:** Open source
- **Oracle Database, SQL Server:** Comerciais
- **Amazon Aurora:** Compatível MySQL/PostgreSQL

#### Recursos RDS
- **Multi-AZ Deployments:**
  - Standby síncrono em outra AZ
  - Failover automático (1-2 minutos)
  - Apenas para alta disponibilidade, não performance

- **Read Replicas:**
  - Réplicas assíncronas para leitura
  - Até 15 replicas (Aurora)
  - Cross-region suportado
  - Pode ser promovida a master

- **Automated Backups:**
  - Backup diário + transaction logs
  - Point-in-time recovery
  - Retenção: 0-35 dias

- **Manual Snapshots:**
  - Backup sob demanda
  - Retenção até exclusão manual

#### Amazon Aurora
- **Performance:** 5x MySQL, 3x PostgreSQL
- **Arquitetura:** Separação compute/storage
- **Storage:** Auto-scaling até 128TB
- **Replicas:** Até 15 Aurora Replicas
- **Global Database:** Replicação cross-region
- **Serverless:** Aurora Serverless v1/v2

### Amazon DynamoDB (NoSQL)

#### Características
- **Managed NoSQL:** Totalmente gerenciado
- **Performance:** Single-digit millisecond latency
- **Scaling:** Automatic scaling up/down
- **Availability:** Multi-AZ, 99.99% SLA

#### Modelos de Capacidade
1. **On-Demand:**
   - Pay-per-request
   - Escalabilidade automática
   - Sem planejamento de capacidade

2. **Provisioned:**
   - Especifica RCU/WCU
   - Auto Scaling opcional
   - Mais econômico para uso consistente

#### Recursos DynamoDB
- **Global Tables:** Multi-region, multi-active
- **DynamoDB Streams:** Change data capture
- **DAX (DynamoDB Accelerator):** Cache em memória
- **Point-in-time Recovery:** Backup contínuo
- **Encryption:** At rest e in transit

#### Consistência
- **Eventually Consistent Reads:** Padrão, melhor performance
- **Strongly Consistent Reads:** Dados mais recentes

### Outros Serviços de Dados

#### Amazon Redshift
- **Data Warehouse:** Análise de petabytes
- **Columnar storage:** Compressão eficiente
- **Massively Parallel Processing (MPP)**
- **Integration:** S3, EMR, Data Pipeline

#### Amazon ElastiCache
- **In-memory caching**
- **Engines:** Redis, Memcached
- **Casos de uso:** Session store, cache de aplicação

#### Amazon DocumentDB
- **MongoDB-compatible**
- **JSON document database**
- **Fully managed**

#### Amazon Neptune
- **Graph database**
- **Property Graph e RDF**
- **Casos de uso:** Social networks, recommendation engines

## 3.4 Serviços de Rede

### Amazon VPC (Virtual Private Cloud)

#### Componentes Principais
- **Subnets:**
  - Públicas: Route para Internet Gateway
  - Privadas: Sem route direto para internet
  - Isoladas: Sem conectividade externa

- **Route Tables:**
  - Controla roteamento de tráfego
  - Associadas a subnets
  - Local routes (automáticas)

- **Internet Gateway (IGW):**
  - Acesso bidirecional à internet
  - Um por VPC
  - Altamente disponível

- **NAT Gateway:**
  - Acesso unidirecional (outbound) para internet
  - Instâncias privadas para atualizações
  - Por AZ, managed pela AWS

- **Security Groups:**
  - Firewall virtual stateful
  - Nível de instância
  - Allow rules apenas

- **Network ACLs:**
  - Firewall stateless
  - Nível de subnet
  - Allow e Deny rules

#### Conectividade VPC
- **VPC Peering:** Conexão direta entre VPCs
- **Transit Gateway:** Hub central para múltiplas VPCs
- **VPN Gateway:** Site-to-site VPN
- **Customer Gateway:** Equipamento on-premises

### AWS Direct Connect
- **Conexão dedicada** AWS ↔ On-premises
- **Bandwidth:** 1Gbps a 100Gbps
- **Benefícios:**
  - Menor latência vs internet
  - Mais consistente
  - Redução custos de transferência
- **Virtual Interfaces (VIFs):**
  - Private VIF: Acesso VPC
  - Public VIF: Serviços públicos AWS

### Elastic Load Balancing (ELB)

#### Application Load Balancer (ALB)
- **Layer 7** (HTTP/HTTPS)
- **Content-based routing:** Path, host, headers
- **WebSocket support**
- **Targets:** EC2, IP addresses, Lambda functions

#### Network Load Balancer (NLB)
- **Layer 4** (TCP/UDP)
- **Ultra-high performance:** Milhões RPS
- **Static IP addresses**
- **Targets:** EC2, IP addresses, ALB

#### Gateway Load Balancer (GWLB)
- **Layer 3** (IP packets)
- **Third-party appliances:** Firewalls, IDS/IPS
- **GENEVE protocol**

#### Classic Load Balancer (CLB)
- **Legacy** (Layer 4 e 7)
- **Não recomendado** para novos projetos

### Amazon Route 53

#### Características
- **Authoritative DNS** service
- **100% SLA uptime**
- **Global anycast network**

#### Routing Policies
- **Simple:** Um registro, múltiplos IPs
- **Weighted:** Distribuição por peso
- **Latency-based:** Menor latência para usuário
- **Failover:** Primary/secondary
- **Geolocation:** Por localização geográfica
- **Geoproximity:** Por proximidade + bias
- **Multivalue Answer:** Healthcheck + múltiplos IPs

#### Health Checks
- **Endpoint monitoring**
- **Calculated health checks**
- **CloudWatch integration**

### Amazon CloudFront (CDN)

#### Características
- **Global CDN:** 400+ edge locations
- **Content caching:** Static e dynamic content
- **Origins:** S3, EC2, ELB, HTTP servers

#### Distribuições
- **Web Distribution:** HTTP/HTTPS content
- **RTMP Distribution:** Streaming media (deprecated)

#### Recursos
- **Edge Locations:** Cache mais próximo dos usuários
- **Regional Edge Caches:** Cache intermediário
- **Origin Shield:** Cache adicional no origin
- **Lambda@Edge:** Funções nas edge locations

#### Casos de Uso
- **Website acceleration**
- **API acceleration**
- **Video streaming**
- **Software distribution**

## 3.5 Serviços de Integração de Aplicações

### Amazon SQS (Simple Queue Service)

#### Tipos de Filas
1. **Standard Queues:**
   - Throughput ilimitado
   - At-least-once delivery
   - Best-effort ordering

2. **FIFO Queues:**
   - First-in-first-out ordering
   - Exactly-once processing
   - 300 TPS limit (batching: 3000 TPS)

#### Características
- **Message retention:** 1 minuto a 14 dias
- **Visibility timeout:** Tempo para processar
- **Dead Letter Queues:** Mensagens não processadas
- **Long polling:** Reduz chamadas vazias

### Amazon SNS (Simple Notification Service)

#### Modelo Pub/Sub
- **Topics:** Pontos de comunicação
- **Subscribers:** Endpoints que recebem mensagens
- **Publishers:** Aplicações que enviam mensagens

#### Protocolos Suportados
- **HTTP/HTTPS endpoints**
- **Email/Email-JSON**
- **SMS**
- **SQS queues**
- **Lambda functions**
- **Mobile push notifications**

#### Recursos
- **Message filtering:** Subscribers recebem apenas mensagens relevantes
- **Message attributes:** Metadados estruturados
- **Fanout pattern:** SQS + SNS para processamento paralelo

### Amazon EventBridge (CloudWatch Events)

#### Características
- **Event-driven architecture**
- **Default event bus:** AWS services
- **Custom event buses:** Aplicações próprias
- **Partner event buses:** SaaS integrations

#### Componentes
- **Events:** Mudanças de estado
- **Rules:** Filtros para events
- **Targets:** Destinos (Lambda, SQS, SNS)

### AWS Step Functions

#### Características
- **State machine orchestration**
- **Visual workflow**
- **Error handling e retry**
- **Parallel execution**

#### Estados
- **Task:** Executa trabalho
- **Choice:** Branching lógico
- **Wait:** Delay
- **Succeed/Fail:** Terminação
- **Pass:** Transformação de dados

## 3.6 Ferramentas de Gerenciamento e Governança

### AWS CloudFormation

#### Infrastructure as Code (IaC)
- **Templates:** JSON ou YAML
- **Stacks:** Coleção de recursos
- **Change Sets:** Preview de mudanças
- **Drift Detection:** Detecta alterações manuais

#### Recursos
- **Cross-stack references:** Compartilhar outputs
- **Nested stacks:** Modularização
- **StackSets:** Deploy multi-account/region

### AWS CloudWatch

#### Métricas
- **Default metrics:** CPU, network, disk
- **Custom metrics:** Aplicação específica
- **Detailed monitoring:** 1-minute intervals

#### Logs
- **Log Groups:** Organização de logs
- **Log Streams:** Sequência de eventos
- **Log Insights:** Query e análise
- **Log retention:** 1 dia a forever

#### Alarmes
- **Metric alarms:** Baseado em métricas
- **Composite alarms:** Múltiplos alarmes
- **Actions:** SNS, Auto Scaling, EC2

### AWS CloudTrail

#### Características
- **API call logging**
- **Governance e compliance**
- **Security analysis**
- **Change tracking**

#### Tipos de Events
- **Management events:** Control plane (padrão)
- **Data events:** Data plane (S3, Lambda)
- **Insight events:** Padrões anômalos

### AWS Config

#### Características
- **Configuration compliance**
- **Resource inventory**
- **Change tracking**
- **Compliance rules**

#### Recursos
- **Config Rules:** Avaliam conformidade
- **Remediation:** Ações automáticas
- **Aggregators:** Multi-account/region view

### AWS Systems Manager

#### Recursos Principais
- **Session Manager:** Shell access sem SSH
- **Parameter Store:** Configurações centralizadas
- **Patch Manager:** Gerenciamento de patches
- **Run Command:** Execução remota

### AWS Trusted Advisor

#### Categorias de Verificação
1. **Cost Optimization:**
   - Instâncias ociosas
   - Volumes EBS não utilizados
   - Reserved Instance optimization

2. **Performance:**
   - High utilization instances
   - CloudFront configuration
   - EBS throughput optimization

3. **Security:**
   - Security groups unrestricted
   - IAM use
   - MFA em root account

4. **Fault Tolerance:**
   - EBS snapshots
   - Multi-AZ RDS
   - Route 53 health checks

5. **Service Limits:**
   - Aproximação de quotas
   - Usage vs limits

#### Planos de Suporte
- **Basic/Developer:** 7 verificações básicas
- **Business/Enterprise:** Todas as verificações + API

---

# DOMÍNIO 4: FATURAMENTO, PREÇOS E SUPORTE (12%)

## 4.1 Modelos de Preços AWS

### Princípios Fundamentais
1. **Pay-as-you-go:** Pague apenas pelo que usar
2. **Pay less when you reserve:** Desconto por compromisso
3. **Pay even less per unit by using more:** Economia de escala
4. **Pay even less as AWS grows:** Reduções de preço passadas

### Reserved Instances (RI)
- **Compromisso:** 1 ou 3 anos
- **Desconto:** Até 75% vs On-Demand
- **Tipos:**
  - Standard RI: Maior desconto, menos flexibilidade
  - Convertible RI: Troca por outras RIs

- **Opções de Pagamento:**
  - No Upfront: Sem pagamento inicial
  - Partial Upfront: Pagamento parcial + mensal
  - All Upfront: Pagamento total antecipado (maior desconto)

### Savings Plans
- **Compromisso:** Valor por hora por 1 ou 3 anos
- **Flexibilidade:** Instance family, size, OS, tenancy, region
- **Tipos:**
  - Compute Savings Plans: EC2, Lambda, Fargate
  - EC2 Instance Savings Plans: Específico EC2

### Spot Instances
- **Conceito:** Capacidade ociosa da AWS
- **Desconto:** Até 90% vs On-Demand
- **Interrupção:** 2 minutos de aviso
- **Spot Fleet:** Múltiplos tipos de inst