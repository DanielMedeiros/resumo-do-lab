# resumo-do-lab
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO.

# Benefícios da Nuvem:
- Alta disponibilidade
- Escalabilidade
- Elasticidade
- Confiabilidade
- Previsibilidade
- Segurança
- Governança
- Gerenciabilidae


# Tipos de serviços na nuvem
## 1. SaaS (Software as a Service – Software como Serviço)
O que é? Aplicativos prontos para uso, hospedados e gerenciados pelo provedor.

Para quem? Usuários finais que querem acesso rápido a softwares sem preocupação com infraestrutura.

Exemplos: Gmail, Microsoft 365, Salesforce, Dropbox.

Responsabilidades:

Provedor cuida de tudo (infraestrutura, atualizações, segurança).

Cliente só usa o software.

## 2. PaaS (Platform as a Service – Plataforma como Serviço)
O que é? Ambiente para desenvolver, testar e implantar aplicações sem gerenciar a infraestrutura subjacente.

Para quem? Desenvolvedores que querem focar no código sem lidar com servidores.

Exemplos: Google App Engine, Heroku, Microsoft Azure App Services.

Responsabilidades:

Provedor gerencia servidores, redes, sistemas operacionais.

Cliente cuida do código e dos dados.

## 3. IaaS (Infrastructure as a Service – Infraestrutura como Serviço)
O que é? Recursos de computação virtualizados (servidores, armazenamento, redes) sob demanda.

Para quem? Empresas que querem controle total sobre a infraestrutura sem manter hardware físico.

Exemplos: AWS EC2, Google Compute Engine, Microsoft Azure VMs.

Responsabilidades:

Provedor cuida da infraestrutura física.

Cliente gerencia sistemas operacionais, aplicações e dados.

# Diferenças Principais:
## IaaS ->	Máquinas virtuais, redes	Hardware físico	Migração de servidores
## PaaS ->	Aplicações e dados	Infraestrutura e runtime	Desenvolvimento de apps
## SaaS -> 	Apenas configurações do app	Tudo (app, infra, segurança)	Uso de software pronto

# Resumo Visual:
## SaaS: Pronto para usar (menos controle).

## PaaS: Plataforma para desenvolver (controle médio).

## IaaS: Infraestrutura flexível (mais controle).

_______________________________________________
# Lab - Criação de Grupo de Recursos.

Esses modelos permitem que empresas escolham o nível de gerenciamento e personalização que melhor atende às suas necessidades.

# Arquitetura e Serviços na Azure (Resumo para AZ-900)
## 1. Estrutura Hierárquica da Azure (Governança e Gerenciamento)
Conta Azure: Associada a uma pessoa/empresa (e-mail) e usada para acessar o portal.

Tenant (Locatário Azure AD): Representa uma organização. Centraliza a identidade e gestão de usuários.

Subscription (Assinatura): Unidade lógica para agrupar recursos, faturamento e limites. Tudo é vinculado a uma assinatura.

Management Groups (Grupos de Gestão): Organizam assinaturas para aplicar políticas (governança) e controle de acesso em escala.

Resource Groups (Grupos de Recursos): Contêineres lógicos que agrupam recursos relacionados a uma solução específica (ex: um app e seu banco de dados). Região é a única característica obrigatória definida no recurso, não no grupo de recursos.

## 2. Conceitos Fundamentais de Computação
Azure Virtual Machines (VMs): Serviço de IaaS (Infraestrutura como Serviço). Oferece controle total sobre o SO e o software.

Azure App Service: Serviço de PaaS (Plataforma como Serviço) para hospedar aplicações web, APIs e back-ends móveis sem gerir infraestrutura.

Azure Container Instances (ACI): Maneira mais simples e rápida de executar contêineres sem gerenciar servidores.

Azure Kubernetes Service (AKS): Serviço de orquestração de contêineres para implantar e gerenciar aplicações em contêineres complexas.

Azure Functions: Serviço de computação serverless (sem servidor) para executar código sob demanda (por evento) sem provisionar infraestrutura.

## 3. Conceitos Fundamentais de Rede
Azure Virtual Network (VNet): Bloco fundamental para redes privadas e seguras na Azure. Isola e protege os recursos.

VPN Gateway: Conecta redes locais (on-premises) à VNet de forma segura através de uma VPN.

Azure ExpressRoute: Estabelece uma conexão privada e dedicada entre sua rede local e a Azure (mais rápida e confiável que VPN).

Azure Load Balancer: Distribui o tráfego de entrada entre recursos (máquinas) para garantir alta disponibilidade e desempenho (Camada 4 - TCP/UDP).

Application Gateway: Balanceador de carga para aplicações web (Camada 7 - HTTP/HTTPS), com funcionalidades como WAF (Firewall de Aplicação Web).

## 4. Conceitos Fundamentais de Armazenamento
Azure Blob Storage: Armazena grandes quantidades de dados não estruturados (ex: textos, imagens, vídeos, backups).

Azure Files: Oferece compartilhamentos de arquivos totalmente gerenciados na nuvem, acessíveis via protocolo SMB (como um file server).

Azure Disk Storage: Discos virtuais (HDs/SSDs) para uso com Azure Virtual Machines.

Tiers (Camadas de Acesso): Para otimizar custos (ex: no Blob Storage):

Hot: Acesso frequente.

Cool: Acesso infrequente (armazenamento mais barato, acesso um pouco mais caro).

Archive: Acesso raríssimo (mais barato, latência de recuperação de horas).

## 5. Conceitos Fundamentais de Banco de Dados
Azure Cosmos DB: Banco de dados NoSQL globalmente distribuído com baixa latência garantida. Oferece vários modelos de API (SQL, MongoDB, Cassandra, etc.).

Azure SQL Database: Banco de dados relacional (SQL) totalmente gerenciado (PaaS). Não requer gerenciamento de VM ou SO.

Azure Database for MySQL/PostgreSQL: Serviços de banco de dados relacionais de código aberto totalmente gerenciados.

## 6. Conceitos de Segurança e Identidade
Azure Active Directory (Azure AD): Serviço de identidade e gerenciamento de acesso baseado em nuvem.

SSO (Single Sign-On): Acesso único a vários aplicativos.

MFA (Multi-Factor Authentication): Autenticação em duas etapas.

Azure Security Center (agora parte do Microsoft Defender for Cloud): Fornece visibilidade e recomendações para fortalecer a segurança de seus recursos.

Azure Key Vault: Armazena e gerencia segredos (senhas, cadeias de conexão) e chaves criptográficas de forma segura.

## 7. Conceitos de Monitoramento e Governança
Azure Monitor: Serviço centralizado para coletar, analisar e agir sobre dados de telemetria (métricas e logs) de seus recursos.

Azure Advisor: Analisa sua configuração e uso e fornece recomendações personalizadas para otimizar custos, desempenho, segurança e confiabilidade.

Azure Policy: Define e aplica regras para seus recursos, garantindo a conformidade com os padrões de governança corporativa.

Azure Resource Manager (ARM): A API e o mecanismo por trás da implantação e gestão de todos os recursos. Permite implantar modelos (ARM templates) de forma declarativa.

## 8. Modelos de Nuvem (Crucial para a prova!)
IaaS (Infraestrutura como Serviço): Aluga infraestrutura (VMs, redes, armazenamento). Você gerencia o SO e aplicações. (Ex: Azure VMs)

PaaS (Plataforma como Serviço): Aluga uma plataforma para desenvolver e executar aplicações. Você gerencia apenas o código e os dados. A Azure gerencia o resto. (Ex: Azure App Service, Azure SQL Database)

SaaS (Software como Serviço): Consome um aplicativo completo rodando na nuvem. (Ex: Microsoft 365, Outlook)

Serverless (Sem Servidor): Foca apenas em fragmentos de código (funções). A plataforma escala automaticamente e você paga apenas pelo tempo de execução. (Ex: Azure Functions)



# Gerenciamento e Governança no Azure (AZ-900)

## 1. Ferramentas de Gerenciamento
Portal do Azure: Interface web central para gerenciar todos os serviços do Azure.

Azure PowerShell & CLI: Ferramentas de linha de comando para automação e gerenciamento via script.

Azure Mobile App: Permite monitorar e gerenciar recursos diretamente de um dispositivo móvel.

Azure Cloud Shell: Shell baseado em navegador para trabalhar com CLI ou PowerShell, sem necessidade de instalação local.

## 2. Núcleo da Governança: Organização de Recursos
Hierarquia de Recursos do Azure:

Grupo de Gestão (Management Group): Agrupa várias assinaturas para aplicar políticas e governança em escala.

Assinatura (Subscription): Unidade lógica que agrupa recursos e define limites de faturamento.

Grupo de Recursos (Resource Group): Contêiner que agrupa recursos relacionados a uma solução específica (ex: um app e seu banco de dados). Recursos existem apenas dentro de um grupo de recursos.

Recurso (Resource): Instância individual de um serviço (ex: uma máquina virtual, uma conta de armazenamento).

## 3. Controle de Acesso e Segurança (Governança)
Azure RBAC (Role-Based Access Control): Controla quem tem acesso ao que e que ação pode realizar.

Princípio: Atribuir a Função (Role) menos privilegiada necessária a um Usuário/Grupo/Identidade em um Escopo específico (assinatura, grupo de recursos, recurso).

Exemplos de funções: Owner, Contributor, Reader.

## 4. Proteção e Conformidade de Recursos (Governança)
Azure Policy: Define e impõe regras para que os recursos estejam em conformidade com os padrões da empresa.

Exemplos: Permitir apenas tipos específicos de VMs, exigir que todos os recursos estejam em uma região específica, impor o uso de discos gerenciados.

Azure Blueprints: Permite empacotar e implantar um conjunto repeatável de recursos, políticas e modelos do ARM para acelerar o desenvolvimento de ambientes novos e em conformidade.

Gerenciamento de Custos:

Marcas (Tags): Metadados (pares chave-valor) aplicados a recursos para organizar e gerenciar custos por departamento, projeto, etc.

Azure Cost Management + Billing: Ferramenta para monitorar, analisar e otimizar os gastos na nuvem.

## 5. Monitoramento e Diagnóstico (Gerenciamento)
Azure Monitor: Serviço central para coletar, analisar e agir sobre dados de telemetria (métricas e logs) de seus recursos.

Azure Advisor: Fornece recomendações personalizadas para otimizar seus recursos (alta disponibilidade, segurança, desempenho, custo).

Azure Service Health: Oferece visibilidade sobre a saúde dos serviços e regiões do Azure que afetam seus recursos. Inclui status de serviço, manutenção planejada e avisos de avaria.

## 6. Implantação de Recursos (Gerenciamento)
ARM Templates (Azure Resource Manager Templates): Arquivos JSON que definem a infraestrutura e a configuração do projeto de forma declarativa (Infraestrutura como Código - IaC). Permite implantar recursos de maneira consistente e repetida.
