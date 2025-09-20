# resumo-do-lab
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO.

## Benefícios da Nuvem:
- Alta disponibilidade
- Escalabilidade
- Elasticidade
- Confiabilidade
- Previsibilidade
- Segurança
- Governança
- Gerenciabilidae


## Tipos de serviços na nuvem
1. SaaS (Software as a Service – Software como Serviço)
O que é? Aplicativos prontos para uso, hospedados e gerenciados pelo provedor.

Para quem? Usuários finais que querem acesso rápido a softwares sem preocupação com infraestrutura.

Exemplos: Gmail, Microsoft 365, Salesforce, Dropbox.

Responsabilidades:

Provedor cuida de tudo (infraestrutura, atualizações, segurança).

Cliente só usa o software.

2. PaaS (Platform as a Service – Plataforma como Serviço)
O que é? Ambiente para desenvolver, testar e implantar aplicações sem gerenciar a infraestrutura subjacente.

Para quem? Desenvolvedores que querem focar no código sem lidar com servidores.

Exemplos: Google App Engine, Heroku, Microsoft Azure App Services.

Responsabilidades:

Provedor gerencia servidores, redes, sistemas operacionais.

Cliente cuida do código e dos dados.

3. IaaS (Infrastructure as a Service – Infraestrutura como Serviço)
O que é? Recursos de computação virtualizados (servidores, armazenamento, redes) sob demanda.

Para quem? Empresas que querem controle total sobre a infraestrutura sem manter hardware físico.

Exemplos: AWS EC2, Google Compute Engine, Microsoft Azure VMs.

Responsabilidades:

Provedor cuida da infraestrutura física.

Cliente gerencia sistemas operacionais, aplicações e dados.

## Diferenças Principais:
## IaaS ->	Máquinas virtuais, redes	Hardware físico	Migração de servidores
## PaaS ->	Aplicações e dados	Infraestrutura e runtime	Desenvolvimento de apps
## SaaS -> 	Apenas configurações do app	Tudo (app, infra, segurança)	Uso de software pronto

## Resumo Visual:
# SaaS: Pronto para usar (menos controle).

# PaaS: Plataforma para desenvolver (controle médio).

# IaaS: Infraestrutura flexível (mais controle).

_______________________________________________
# Lab - Criação de Grupo de Recursos.

Esses modelos permitem que empresas escolham o nível de gerenciamento e personalização que melhor atende às suas necessidades.

## Gerenciamento e Governança no Azure (AZ-900)

# 1. Ferramentas de Gerenciamento
Portal do Azure: Interface web central para gerenciar todos os serviços do Azure.

Azure PowerShell & CLI: Ferramentas de linha de comando para automação e gerenciamento via script.

Azure Mobile App: Permite monitorar e gerenciar recursos diretamente de um dispositivo móvel.

Azure Cloud Shell: Shell baseado em navegador para trabalhar com CLI ou PowerShell, sem necessidade de instalação local.

# 2. Núcleo da Governança: Organização de Recursos
Hierarquia de Recursos do Azure:

Grupo de Gestão (Management Group): Agrupa várias assinaturas para aplicar políticas e governança em escala.

Assinatura (Subscription): Unidade lógica que agrupa recursos e define limites de faturamento.

Grupo de Recursos (Resource Group): Contêiner que agrupa recursos relacionados a uma solução específica (ex: um app e seu banco de dados). Recursos existem apenas dentro de um grupo de recursos.

Recurso (Resource): Instância individual de um serviço (ex: uma máquina virtual, uma conta de armazenamento).

# 3. Controle de Acesso e Segurança (Governança)
Azure RBAC (Role-Based Access Control): Controla quem tem acesso ao que e que ação pode realizar.

Princípio: Atribuir a Função (Role) menos privilegiada necessária a um Usuário/Grupo/Identidade em um Escopo específico (assinatura, grupo de recursos, recurso).

Exemplos de funções: Owner, Contributor, Reader.

# 4. Proteção e Conformidade de Recursos (Governança)
Azure Policy: Define e impõe regras para que os recursos estejam em conformidade com os padrões da empresa.

Exemplos: Permitir apenas tipos específicos de VMs, exigir que todos os recursos estejam em uma região específica, impor o uso de discos gerenciados.

Azure Blueprints: Permite empacotar e implantar um conjunto repeatável de recursos, políticas e modelos do ARM para acelerar o desenvolvimento de ambientes novos e em conformidade.

Gerenciamento de Custos:

Marcas (Tags): Metadados (pares chave-valor) aplicados a recursos para organizar e gerenciar custos por departamento, projeto, etc.

Azure Cost Management + Billing: Ferramenta para monitorar, analisar e otimizar os gastos na nuvem.

# 5. Monitoramento e Diagnóstico (Gerenciamento)
Azure Monitor: Serviço central para coletar, analisar e agir sobre dados de telemetria (métricas e logs) de seus recursos.

Azure Advisor: Fornece recomendações personalizadas para otimizar seus recursos (alta disponibilidade, segurança, desempenho, custo).

Azure Service Health: Oferece visibilidade sobre a saúde dos serviços e regiões do Azure que afetam seus recursos. Inclui status de serviço, manutenção planejada e avisos de avaria.

# 6. Implantação de Recursos (Gerenciamento)
ARM Templates (Azure Resource Manager Templates): Arquivos JSON que definem a infraestrutura e a configuração do projeto de forma declarativa (Infraestrutura como Código - IaC). Permite implantar recursos de maneira consistente e repetida.
