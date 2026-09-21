# ☁️ Resumo: Nuvem e Sistemas Operacionais
**Disciplina:** Sistemas Operacionais  
**Professor:** Prof. Me. Deivison S. Takatu (`deivison.takatu@fatec.sp.gov.br`)  
**Instituição:** Fatec - Faculdade de Tecnologia  

---

## 📌 1. Fundamentos da Computação em Nuvem (Cloud Computing)

A transição da infraestrutura física tradicional para a computação em nuvem representa uma mudança de paradigma: a substituição de ativos físicos locais (**CAPEX**) por serviços contratados sob demanda (**OPEX**), reduzindo despesas operacionais e garantindo maior agilidade.
```
+-------------------------------------------------------------+
|                     COMPUTAÇÃO EM NUVEM                     |
+-------------------------------------------------------------+
│             │                  │                 │
▼             ▼                  ▼                 ▼
Acesso sob    Rede de            Pool de          Mensuração
Demanda     Acesso Amplo       Recursos          Automática
(Instantâneo) (Qualquer disp.)   (Multi-tenant)    (Pay-per-use)
```

### 📋 Características Essenciais (Modelo NIST)
* **Autoatendimento sob demanda:** O provisionamento de recursos ocorre sem intervenção humana com o fornecedor.
* **Amplo acesso à rede:** Mecanismos padronizados de acesso via Internet através de telemóveis, computadores portáteis e estações de trabalho.
* **Pool de recursos (*Multi-tenant*):** Recursos físicos e virtuais partilhados dinamicamente entre múltiplos utilizadores.
* **Elasticidade rápida:** Capacidade de escalar ou desprovisionar capacidade computacional de forma ágil mediante a necessidade.
* **Serviço mensurável:** Monitorização detalhada e tarifação estritamente sobre os recursos consumidos (*pay-per-use*).

---

## ⚙️ 2. Virtualização como Pilar e Alta Disponibilidade

O Sistema Operacional é a camada fundamental que abstrai o hardware. A virtualização viabiliza a criação de múltiplos ambientes isolados sobre o mesmo servidor físico, otimizando o consumo de infraestrutura.

* **Hardware Físico:** CPU, RAM, barramentos e controladores de rede.
* **Hypervisor (VMM):** Software de abstração (ex.: VMware ESXi, KVM) responsável por criar e coordenar as máquinas virtuais.
* **Máquinas Virtuais (VMs):** Instâncias independentes com o seu próprio SO e aplicações.

### 🛡️ Pilares da Alta Disponibilidade em Nuvem
1. **Zonas de Disponibilidade (AZs):** Datacenters distintos e isolados dentro de uma mesma região com redes e alimentação redundantes.
2. **Balanceamento de Carga (*Load Balancer*):** Distribuição equilibrada do tráfego entre diferentes instâncias[cite: 6].
3. **Replicação de Dados:** Mecanismos de escrita síncrona entre datacenters para prevenir perdas de integridade[cite: 6].
4. **Failover Automático:** Desvio automático de requisições de nós avariados para instâncias saudáveis[cite: 6].

---

## 🏗️ 3. Modelos de Serviço em Nuvem

| Modelo | Nome Completo | O que o Provedor gere? | O que o Cliente gere? | Exemplos Práticos |
| :--- | :--- | :--- | :--- | :--- |
| **IaaS**[cite: 6] | *Infrastructure as a Service*[cite: 6] | Hardware, rede, armazenamento e virtualização[cite: 6]. | Sistema Operacional, middleware, runtime e aplicações[cite: 6]. | AWS EC2, Azure VMs, Google Compute Engine[cite: 6]. |
| **PaaS**[cite: 6] | *Platform as a Service*[cite: 6] | Hardware, rede, SO, drivers, atualizações e runtime[cite: 6]. | Apenas o código-fonte da aplicação e dados[cite: 6]. | Google App Engine, Heroku, Render, AWS Elastic Beanstalk[cite: 6]. |
| **SaaS**[cite: 6] | *Software as a Service*[cite: 6] | Toda a infraestrutura, suporte, código e segurança[cite: 6]. | Apenas consome as funcionalidades através da web[cite: 6]. | Microsoft 365, Google Workspace, Slack, Salesforce[cite: 6]. |

---

## 🌐 4. Modelos de Implantação e Provedores

* **Nuvem Pública:** Infraestrutura partilhada mantida por grandes provedores (AWS, Microsoft Azure, Google Cloud Platform, Oracle Cloud) com escalabilidade massiva[cite: 6].
* **Nuvem Privada:** Estrutura dedicada exclusivamente a uma entidade organizacional única, mantida *on-premise* ou em instalações de colocation[cite: 6].
* **Nuvem Híbrida:** Integração orquestrada entre infraestruturas privadas e públicas, mantendo cargas de trabalho críticas isoladas e absorvendo picos na nuvem pública[cite: 6].

### ⚖️ Vantagens versus Desafios

| Vantagens 🚀 | Desafios ⚠️ |
| :--- | :--- |
| Redução expressiva de CAPEX em prol de OPEX[cite: 6] | Risco de aprisionamento tecnológico (*Vendor lock-in*)[cite: 6] |
| Escalabilidade e elasticidade automáticas[cite: 6] | Conformidade regulatória complexa (ex.: LGPD, GDPR)[cite: 6] |
| Resiliência geográfica e alta disponibilidade[cite: 6] | Despesas operacionais não planeadas sem governança (*FinOps*)[cite: 6] |
| Facilidade de inovação contínua com IA e Big Data[cite: 6] | Latência acrescida de comunicação de rede[cite: 6] |

> **Modelo de Responsabilidade Compartilhada:** O fornecedor assegura a segurança **da** infraestrutura física da nuvem; o cliente assegura a segurança **na** nuvem (configurações, acessos, dados e aplicações)[cite: 6].

---

## 📦 5. Containers e Microsserviços

Ao contrário das Máquinas Virtuais tradicionais (que exigem um SO Convidado completo para cada instância), os **Containers** empacotam o binário da aplicação e as suas dependências partilhando diretamente o **Kernel do SO hospedeiro**[cite: 6].
```
+-------------------------------------------------------------+
|                      APLICAÇÃO A | B                        |
+-------------------------------------------------------------+
|                 MOTOR DE CONTAINERS (DOCKER)                |
+-------------------------------------------------------------+
|                 SISTEMA OPERACIONAL / KERNEL                |
+-------------------------------------------------------------+
|                           HARDWARE                          |
+-------------------------------------------------------------+
```

* **Docker:** Plataforma padrão para criação, gestão e transporte de containers isolados e leves[cite: 6].
* **Kubernetes:** Ferramenta responsável pela orquestração, alta disponibilidade e auto-scaling dos containers[cite: 6].
* **Microsserviços:** Estruturação arquitetural de software distribuído em componentes de finalidade única integrados por APIs REST[cite: 6].

---

## 🚀 6. Prática com Express.js e Deploy no Render

### 🛠️ Configuração de uma API com Express
1. Inicialização do projeto e instalação de dependências[cite: 6]:
   ```bash
   npm install express cors
Criação do servidor Node.js com controlo de cabeçalhos de origem cruzada (CORS) para comunicação segura[cite: 6].

Execução local via terminal[cite: 6]:

Bash
node index.js
☁️ Publicação no Render (PaaS)
Submissão do código-fonte para um repositório no GitHub[cite: 6].

Acesso à consola do Render (dashboard.render.com) e criação de um novo Web Service ligado ao repositório[cite: 6].

Parâmetros de compilação e execução[cite: 6]:

Build Command: node

[cite: 6]

Start Command: node index.js

[cite: 6]

Implementação automática e disponibilização pública através do domínio seu-projeto.onrender.com com encriptação SSL automática[cite: 6].

📝 7. Roteiro das Atividades
Desenvolvimento Local (cloud-so-app): Desenvolver uma API em Express.js que aceda e apresente métricas do SO hospedeiro via módulo os do Node.js (nome do host, arquitetura, modelo/quantidade de CPUs, memória total/livre e uptime)[cite: 6].

Implementação em Nuvem: Enviar a base de código para o GitHub e realizar o deploy no Render[cite: 6].

Análise Comparativa de SO: Comparar a saída de dados da máquina local com o ambiente virtualizado do Render, correlacionando o comportamento da CPU, memória e SO convidado/hospedeiro[cite: 6].

Documentação Técnica: Estruturar a entrega em formato de Manual Markdown com o registo passo a passo de todas as etapas e conclusões técnicas[cite: 6].

📚 Referências Bibliográficas
TANENBAUM, Andrew S.; BOS, Herbert. Sistemas Operacionais Modernos. 4. ed. São Paulo: Pearson, 2016[cite: 6].

SILBERSCHATZ, Abraham; GALVIN, Peter B.; GAGNE, Greg. Fundamentos de Sistemas Operacionais. 9. ed. Rio de Janeiro: LTC, 2015[cite: 6].

STALLINGS, William. Sistemas Operacionais: Conceitos e Projetos. 8. ed. São Paulo: Pearson, 2015[cite: 6].
