# SISTEMAS OPERACIONAIS MODERNOS — RESUMO EXPANDIDO E DETALHADO (PÁGS. 5 A 13) 📚🚀

---

## 📌 1. VISÃO GERAL EXECUTIVA

* **Obra de Referência:** *Sistemas Operacionais Modernos* (4ª Edição) — Andrew S. Tanenbaum & Herbert Bos.
* **Recorte Analisado:** Capítulo 1, Seção 1.2 — *História dos Sistemas Operacionais* (Páginas 5 a 13).
* **Objetivo:** Oferecer uma análise exaustiva e estruturada sobre a evolução dos Sistemas Operacionais (SO), relacionando as transformações de hardware com os avanços nas abstrações de software, desde a era das válvulas até os dispositivos móveis e a computação em nuvem.

---

## 🗺️ 2. MAPA MENTAL GERAL DA HISTÓRIA DOS SOs

```mermaid
mindmap
  root((Evolução dos Sistemas Operacionais))
    1ª Geração 1945-1955
      Hardware: Válvulas e Relés
      Entrada: Painéis de fios e Cartões
      Software: Sem Sistema Operacional
      Aplicações: Cálculos Numéricos Diretos
    2ª Geração 1955-1965
      Hardware: Transistores e Mainframes
      Sistemas: Processamento em Lote Batch
      Equipamentos: IBM 1401 E/S e IBM 7094 CPU
      Sistemas Operacionais: FMS e IBSYS
    3ª Geração 1965-1980
      Hardware: Circuitos Integrados CIs
      Inovações: Multiprogramação e Spooling
      Sistemas Destacados: IBM System/360 e MULTICS
      Nascimento do UNIX: Ken Thompson PDP-7
    4ª Geração 1980-Presente
      Hardware: LSI e VLSI Microprocessadores
      Sistemas Pessoais: CP/M e MS-DOS
      Interfaces Gráficas GUIs: Xerox PARC, Apple e Windows
      Diversificação: SOs de Rede e Distribuição
    5ª Geração 1990-Presente
      Hardware: Dispositivos Móveis e SOCs
      Pioneiros: Nokia N9000 e Symbian OS
      Sistemas Dominantes: Google Android e Apple iOS
      Paradigmas Modernos: Nuvem e Múltiplos Núcleos
⏳ 3. LINHA DO TEMPO COMPLETA DA COMPUTAÇÃO (1945 – PRESENTE)
Snippet de código
timeline
    title Evolução Cronológica dos Sistemas Operacionais
    section 1ª Geração (Válvulas)
        1945 : ENIAC, Z3, Colossus e Mark I
             : Programação manual via painéis de fios
        1950 : Introdução dos cartões perfurados
    section 2ª Geração (Transistores)
        1955 : Surgimento dos Transistores
             : Introdução dos Sistemas em Lote (Batch)
        1959 : Domínio do IBM 7094 e FMS
        1961 : Lançamento do DEC PDP-1
    section 3ª Geração (CIs & Multiprogramação)
        1964 : Lançamento do IBM System/360
        1965 : Início do Projeto MULTICS (MIT/Bell/GE)
        1969 : Ken Thompson cria o UNIX no PDP-7
        1974 : Lançamento da CPU Intel 8080
    section 4ª Geração (Computadores Pessoais)
        1977 : Lançamento do CP/M pela Digital Research
        1981 : Lançamento do IBM PC com o MS-DOS
        1984 : Lançamento do Apple Macintosh (GUI)
        1987 : Andrew Tanenbaum lança o MINIX
        1991 : Linus Torvalds lança o Kernel Linux
        1995 : Lançamento do Windows 95
    section 5ª Geração (Móveis & Nuvem)
        1996 : Nokia N9000 (1º Smartphone comercial)
        2007 : Apple lança o iPhone (iOS)
        2008 : Google lança o Android (Linux)
        Atual : Domínio de Processadores Multinúcleo e Nuvem
⌛ 1.2 HISTÓRIA DOS SISTEMAS OPERACIONAIS
A evolução dos sistemas operacionais está historicamente vinculada à arquitetura dos computadores nos quais eles são executados. As mudanças tecnológicas no hardware impulsionaram a criação de novas abstrações e técnicas de gerenciamento de recursos.  
PDF
+ 1

Princípio de Evolução Cíclica: A evolução do hardware aumenta a capacidade de processamento. Isso gera novos gargalos de software, que exigem novas abstrações do SO, influenciando o projeto dos hardwares futuros.  
PDF
+ 1

Snippet de código
graph TD
    A[Avanço do Hardware] -->|Aumenta capacidade física| B[Surgimento de Novos Gargalos]
    B -->|Exige abstrações de software| C[Desenvolvimento do Sistema Operacional]
    C -->|Cria novas necessidades| A
🔌 1.2.1 A Primeira Geração (1945–1955): Válvulas
A primeira geração de computadores digitais operava sem sistemas operacionais. Os computadores eram construídos com válvulas termiônicas e relés eletromagnéticos.  
PDF
+ 1

🛠️ Principais Marcos e Equipamentos
Antecedentes Históricos: Charles Babbage projetou a máquina analítica mecânica, contratando Ada Lovelace como a primeira programadora do mundo.  
PDF

Computadores Primordiais:

ABC (Atanasoff-Berry Computer): Projetado por John Atanasoff e Clifford Berry na Universidade do Estado de Iowa.  
PDF

Z3: Construído por Konrad Zuse em Berlim usando relés eletromagnéticos.  
PDF

Colossus: Desenvolvido em Bletchley Park por cientistas como Alan Turing para decifrar códigos de guerra.  
PDF

Mark I: Construído por Howard Aiken na Universidade de Harvard.  
PDF

ENIAC: Construído por William Mauchly e J. Presper Eckert na Universidade da Pensilvânia.  
PDF

Snippet de código
graph LR
    A[Programador Reserva Horário] --> B[Entra na Sala de Máquinas]
    B --> C[Conecta Cabos nos Painéis]
    C --> D[Executa o Cálculo Numérico]
    D --> E[Torce para Nenhuma Válvula Queimar]
📋 Características Técnicas do Período
Parâmetro	Descrição Detalhada
Tecnologia Principal	
Válvulas termiônicas (~20.000 por máquina).  
PDF

Modo de Programação	
Código de máquina absoluto e ligação física via cabos em painéis de conexões (plugboards).  
PDF

Linguagens	
Inexistentes (sem assembly, sem linguagens de alto nível).  
PDF

Sistema Operacional	
Inexistente.  
PDF

Aplicações	
Cálculos numéricos e matemáticos diretos (tabelas trigonométricas, trajetórias balísticas).  
PDF

Avanço no fim da era	
Introdução dos cartões perfurados no início da década de 1950.  
PDF

🔲 1.2.2 A Segunda Geração (1955–1965): Transistores e Sistemas em Lote (Batch)
A introdução do transistor reduziu drasticamente o tamanho e o consumo de energia dos computadores, aumentando sua confiabilidade a ponto de permitirem sua comercialização regular.  
PDF

👥 Separação de Funções Profissionais
Com a segunda geração, surgiu uma clara divisão de trabalho na computação:  
PDF

Projetistas e Construtores: Engenheiros de hardware.  
PDF

Operadores: Profissionais dedicados a operar as máquinas na sala de computadores.  
PDF

Programadores: Escreviam os códigos em cartões perfurados.  
PDF

Equipe de Manutenção: Responsáveis pela conservação do equipamento.  
PDF

💻 Fluxo de Funcionamento de um Sistema em Lote (Batch)
Para evitar o desperdício de tempo decorrente do deslocamento manual dos operadores, foi desenvolvido o sistema em lote (batch system).  
PDF

Snippet de código
flowchart LR
    Prog[Programadores] -->|Entregam Cartões| IBM1401_In[IBM 1401]
    IBM1401_In -->|Grava Lote| FitaIn[(Fita Magnética de Entrada)]
    FitaIn -->|Transportada Manualmente| IBM7094[IBM 7094 Mainframe]
    IBM7094 -->|Processa Lote| FitaOut[(Fita Magnética de Saída)]
    FitaOut -->|Transportada Manualmente| IBM1401_Out[IBM 1401]
    IBM1401_Out -->|Imprime Saída Off-line| Relatorios[Relatórios Impressos]
📜 Estrutura Típica de uma Tarefa em FMS (Fortran Monitor System)
As tarefas eram submetidas como maços de cartões perfurados contendo comandos de controle:  
PDF

+-------------------------------------------------------+
| $END                                                  |  <-- Fim do Lote / Tarefa
+-------------------------------------------------------+
| Dados do Programa                                     |  <-- Entrada de dados
+-------------------------------------------------------+
| $RUN                                                  |  <-- Comanda a execução
+-------------------------------------------------------+
| $LOAD                                                 |  <-- Carrega o código-objeto
+-------------------------------------------------------+
| Programa FORTRAN (Código-fonte nos cartões)           |  <-- Código fonte
+-------------------------------------------------------+
| $FORTRAN                                              |  <-- Carrega o compilador
+-------------------------------------------------------+
| $JOB, 10.7710802, MARVIN TANENBAUM                    |  <-- Identificação e Conta
+-------------------------------------------------------+
Cartão de Controle	Função Executada pelo SO Ancestral
$JOB	
Define o tempo máximo de CPU, número da conta a ser debitada e nome do programador.  
PDF

$FORTRAN	
Instruía o SO a carregar o compilador FORTRAN armazenado na fita do sistema.  
PDF

$LOAD	
Ordenava o carregamento do programa-objeto recém-compilado na memória.  
PDF

$RUN	
Mandava o SO executar o programa com os dados fornecidos nos cartões subsequentes.  
PDF

$END	
Indicava o fim do processamento daquela tarefa específica.  
PDF

Sistemas Operacionais Típicos: FMS (Fortran Monitor System) e IBSYS (sistema da IBM para o 7094).  
PDF

🔲 1.2.3 A Terceira Geração (1965–1980): CIs e Multiprogramação
Na década de 1960, os fabricantes mantinham duas linhas de produtos incompatíveis:  
PDF

Científica (Ex: IBM 7094): Orientada a palavras, para cálculos numéricos complexos.  
PDF

Comercial (Ex: IBM 1401): Orientada a caracteres, para ordenação de fitas e impressão de dados.  
PDF

🏢 O IBM System/360
A IBM solucionou essa dualidade lançando a família System/360. Era uma linha de máquinas com arquitetura e conjunto de instruções únicos, utilizando Circuitos Integrados (CIs) de pequena escala.  
PDF
+ 1

Snippet de código
graph TD
    System360[IBM System/360]
    System360 --> Sci[Mercado Científico: Processamento Pesado]
    System360 --> Com[Mercado Comercial: E/S e Ordenação]
    Sci --> LinhaUnica[Arquitetura e Conjunto de Instruções Únicos]
    Com --> LinhaUnica
Problemas do OS/360: Tentava satisfazer todas as necessidades (grandes e pequenos sistemas, científicos e comerciais). O resultado foi um sistema operacional massivo, com milhões de linhas em assembly e milhares de erros (bugs).  
PDF
+ 1

Fred Brooks: Um dos projetistas do OS/360, escreveu o livro O Mítico Homem-Mês, descrevendo as dificuldades do projeto.  
PDF

🚀 Avanços Tecnológicos Fundamentais
1. Multiprogramação
Nos sistemas em lote simples, a CPU ficava ociosa durante as operações de Entrada/Saída (E/S). A multiprogramação solucionou isso dividindo a memória em partições para manter múltiplas tarefas simultaneamente.  
PDF
+ 1

SISTEMA COM UNIPROGRAMAÇÃO:
┌───────────┬───────────────────────┬───────────┬───────────────────────┐
│ Processo  │ Espera E/S (CPU Ociosa)│ Processo  │ Espera E/S (CPU Ociosa)│
└───────────┴───────────────────────┴───────────┴───────────────────────┘

SISTEMA COM MULTIPROGRAMAÇÃO:
┌───────────────────────────────────────────────────────────────────────┐
│ Partição 3: Tarefa 3 (Em execução enquanto Tarefa 1 espera E/S)       │
├───────────────────────────────────────────────────────────────────────┤
│ Partição 2: Tarefa 2                                                  │
├───────────────────────────────────────────────────────────────────────┤
│ Partição 1: Tarefa 1 (Aguardando E/S de disco ou fita)                │
├───────────────────────────────────────────────────────────────────────┤
│ Núcleo do Sistema Operacional                                         │
└───────────────────────────────────────────────────────────────────────┘
2. Spooling (Simultaneous Peripheral Operation On Line)
Técnica de carregar tarefas diretamente dos cartões perfurados para o disco rígido assim que chegavam. Sempre que uma tarefa terminava, o SO carregava automaticamente uma nova tarefa do disco para a partição vaga, eliminando computadores intermediários como o IBM 1401.  
PDF
+ 1

3. Compartilhamento de Tempo (Timesharing)
Variante da multiprogramação na qual cada usuário interagia diretamente via terminal on-line. A CPU alocava pequenos fatias de tempo para cada usuário ativo.  
PDF
+ 1

CTSS (Compatible Time Sharing System): Desenvolvido no M.I.T. em um IBM 7094 modificado, foi o primeiro sistema de compartilhamento de tempo para fins gerais.  
PDF

4. O Projeto MULTICS
O M.I.T., Bell Labs e General Electric desenvolveram o MULTICS (MULTiplexed Information and Computing Service), projetado para ser um "computador utilitário" capaz de atender centenas de usuários simultâneos.  
PDF

Snippet de código
graph TD
    MULTICS[MULTICS - 1965] -->|Ken Thompson no PDP-7| UNIX[UNIX - 1969]
    UNIX --> SystemV[System V - AT&T]
    UNIX --> BSD[BSD - UC Berkeley]
    SystemV --> POSIX[Padrão POSIX - IEEE]
    BSD --> POSIX
    POSIX --> MINIX[MINIX - 1987 Tanenbaum]
    MINIX --> Linux[Linux - 1991 Linus Torvalds]
    BSD --> macOS[macOS / FreeBSD]
Relevância Histórica do MULTICS: Embora comercialmente limitado, introduziu conceitos fundamentais implementados no UNIX e em seus derivados modernos.  
PDF

MINIX e Linux:

MINIX: Criado em 1987 por Andrew Tanenbaum para fins educacionais, em conformidade com o padrão POSIX.  
PDF

Linux: Desenvolvido em 1991 por Linus Torvalds, inspirado no MINIX.  
PDF

💻 1.2.4 A Quarta Geração (1980–Presente): Computadores Pessoais
O surgimento dos circuitos integrados LSI (Large Scale Integration) permitiu colocar milhares de transistores em um único chip de silício, dando início à era do microprocessador e dos computadores pessoais.  
PDF

Snippet de código
graph TD
    Micro[Microprocessador Intel 8080 - 1974] --> CPM[CP/M - Gary Kildall / Digital Research]
    CPM --> IBM_PC[IBM PC - 1981]
    IBM_PC --> MSDOS[MS-DOS - Bill Gates / Microsoft / Tim Paterson]
    MSDOS --> Win_Evol[Windows 95/98 -> Windows NT -> Win 7/8/10/11]
    
    PARC[Xerox PARC - Engelbart / GUI] --> Lisa[Apple Lisa / Macintosh - Steve Jobs]
    Lisa --> macOS[Mac OS X - Baseado em UNIX/Mach/FreeBSD]
📜 A Saga dos SOs Pessoais
CP/M (Control Program for Microcomputers):

Desenvolvido por Gary Kildall (Digital Research) em 1974 para a CPU Intel 8080.  
PDF

Dominou o mercado de 8 bits por cerca de 5 anos.  
PDF

MS-DOS (MicroSoft Disk Operating System):

A IBM contatou a Digital Research para licenciar o CP/M para o IBM PC, mas a reunião falhou.  
PDF

Bill Gates comprou o QDOS (Quick and Dirty Operating System) da Seattle Computer Products por cerca de US$ 75.000, contratou o autor Tim Paterson e o adaptou para a IBM sob o nome MS-DOS.  
PDF

Interfaces Gráficas (GUIs):

Invenção: Doug Engelbart inventou a GUI (janelas, ícones, menus, mouse) no SRI na década de 1960. A tecnologia foi aprimorada no Xerox PARC.  
PDF
+ 1

Apple Macintosh: Steve Jobs visitou o PARC e aplicou o conceito no Lisa e, posteriormente, no Apple Macintosh (1984), popularizando as interfaces amigáveis.  
PDF

Windows: A Microsoft lançou o Windows em 1985 como um ambiente gráfico rodando sobre o MS-DOS. Em 1995, lançou o Windows 95, e posteriormente a linha de 32/64 bits nativa com o Windows NT (projeto liderado por David Cutler).  
PDF
+ 1

📑 Quadro Comparativo dos Sistemas da 4ª Geração
Sistema Operacional	Criador / Mantenedor	Tipo de Interface	Filosofia de Arquitetura
CP/M	Gary Kildall (Digital Research)	Linha de Comando (CLI)	
Monotarefa de 8 bits sem proteção de memória.  
PDF

MS-DOS	Tim Paterson / Microsoft	Linha de Comando (CLI)	
Monotarefa de 16 bits baseada na arquitetura x86.  
PDF

Windows 95/98	Microsoft	Interface Gráfica (GUI)	
Híbrido 16/32 bits sobre camada MS-DOS.  
PDF

Windows NT/XP/7/8	Microsoft	Interface Gráfica (GUI)	
Multiprogramação nativa de 32/64 bits, preemptivo.  
PDF

UNIX / Linux	Comunidade / Open Source	Shell CLI / X11 (Gnome/KDE)	
Multiusuário, multitarefa, modular com suporte POSIX.  
PDF

Mac OS X	Apple	Interface Gráfica Aqua	
Baseado em UNIX (núcleo Mach e código FreeBSD).  
PDF

📱 1.2.5 A Quinta Geração (1990–Presente): Computadores Móveis
A convergência entre a telefonia celular e a computação deu origem aos smartphones e tablets.  
PDF

Snippet de código
graph LR
    Symbian[Symbian OS: Nokia, Sony Ericsson - Dominante nos anos 2000] --> Decline[Declínio no mercado]
    RIM[BlackBerry OS: Foco Corporativo] --> Decline
    iOS[Apple iOS: Lançado em 2007 com o iPhone] --> ModernTop[Liderança do Mercado Atual]
    Android[Google Android: Lançado em 2008 base Linux] --> ModernTop
📱 A Evolução dos Telefones ao Smartphone
1946: Primeiro telefone móvel (pesava ~40 kg, instalado em automóveis).  
PDF

Década de 1970: Primeiro telefone portável individual ("o tijolo", ~1 kg).  
PDF

Mid-1990: Primeiro smartphone real: Nokia N9000 (combinava telefone e PDA).  
PDF

1997: A Ericsson cunhou o termo smartphone para o modelo GS88 "Penelope".  
PDF

📊 Batalha dos Sistemas Operacionais Móveis
Sistema Operacional	Desenvolvedor	Base Técnica	Modelo de Licença	Status de Mercado
Symbian OS	Consórcio Nokia/Sony	Proprietário	Fechada	
Descontinuado em 2011.  
PDF

BlackBerry OS	RIM (Research in Motion)	Proprietário	Fechada	
Descontinuado.  
PDF

iOS	Apple	Derivado do Mac OS X (UNIX/Mach)	Proprietária Fechada	
Liderança no segmento premium.  
PDF

Android	Google / OHA	Núcleo Linux + VM Java (Dalvik/ART)	Código Aberto (Permissiva)	
Líder absoluto em participação global.  
PDF

⚙️ 1.3 REVISÃO SOBRE HARDWARE DE COMPUTADORES
O sistema operacional precisa conhecer detalhadamente o hardware sobre o qual é executado para gerenciar seus recursos de maneira otimizada.  
PDF

Snippet de código
flowchart TD
    subgraph CPU_Block[Processador CPU]
        CPU[CPU Central]
        MMU[MMU - Unidade de Gerenciamento de Memória]
        Reg[Registradores: PC, SP, PSW]
    end

    Bus[BARRAMENTO DO SISTEMA] <--> CPU_Block
    Bus <--> RAM[Memória Principal RAM]
    Bus <--> Vid[Controlador de Vídeo -> Monitor]
    Bus <--> Kbd[Controlador de Teclado -> Teclado]
    Bus <--> USB[Controlador USB -> Impressora]
    Bus <--> SATA[Controlador SATA -> Disco Rígido]
🧠 1.3.1 Processadores (CPUs)
A CPU busca instruções da memória, as decodifica e as executa.  
PDF

Snippet de código
graph LR
    A[Buscar Instrução - Fetch] --> B[Decodificar Instrução - Decode]
    B --> C[Executar Instrução - Execute]
    C --> A
📋 Registradores Principais
PC (Program Counter): Armazena o endereço da próxima instrução a ser buscada.  
PDF

SP (Stack Pointer): Aponta para o topo da pilha de execução contendo parâmetros e variáveis locais.  
PDF

PSW (Program Status Word): Armazena os bits de estado da CPU (prioridade, modo núcleo/usuário, códigos de condição).  
PDF

🔒 Modos de Execução da CPU
Modo Núcleo (Kernel Mode): A CPU pode executar todas as instruções do seu conjunto e gerenciar qualquer recurso físico. O SO roda neste modo.  
PDF
+ 1

Modo Usuário (User Mode): Programas de usuários operam restritamente. Instruções que afetam o controle do sistema ou realizam Entrada/Saída são proibidas.  
PDF
+ 1

Chamadas de Sistema (System Calls): Utilizam a instrução TRAP para alternar o processador do modo usuário para o modo núcleo, permitindo solicitar serviços ao SO.  
PDF

💾 1.3.2 Memória e Hierarquia de Armazenamento
A memória do computador é organizada em uma hierarquia de camadas. As camadas superiores oferecem maior velocidade, mas possuem menor capacidade e alto custo por bit.  
PDF
+ 1

                     HIERARQUIA DE MEMÓRIA
                             /\
                            /  \          Registradores (< 1 KB) | ~1 ns
                           /----\
                          / Cache\        Cache L1 / L2 / L3 (MB) | ~2 ns
                         /--------\
                        /  Memória \      Memória Principal RAM (GB) | ~10 ns
                       /  Principal \
                      /--------------\
                     / Discos Magnét. \   Disco Magnético / SSD (TB) | ~10 ms
                    /__________________\
📊 Especificações Técnicas da Hierarquia
Nível da Hierarquia	Tempo de Acesso Típico	Capacidade Típica	Elemento Gerenciador
Registradores	
≈1 ns

  
PDF

<1 KB

  
PDF

Compilador / Programador  
PDF

Cache (L1/L2/L3)	
≈2 ns

  
PDF

4 a 64 MB

  
PDF

Hardware de Cache  
PDF

Memória Principal (RAM)	
≈10 ns

  
PDF

1 a 64 GB

  
PDF

Sistema Operacional  
PDF

Disco Magnético / SSD	
≈10 ms

  
PDF

1 a 16 TB

  
PDF

Sistema Operacional  
PDF

💽 1.3.3 Discos e Estrutura Física
Os discos magnéticos fornecem armazenamento permanente a um custo acessível, mas possuem latência mecânica.  
PDF

                ESTRUTURA FÍSICA DE UM DISCO RÍGIDO
               
       Trilha (Círculo concêntrico)
          ┌──────────┐
     ┌────┴──────────┴────┐
    /   ┌──────────────┐   \
   /   /    Setor       \   \
  │   │    (512 B)       │   │   ◄─── Cabeça de Leitura/Escrita
   \   \                /   /         montada em um Braço Móvel
    \   └──────────────┘   /
     └────────────────────┘
          ▲
          └─ Cilindro (Conjunto de trilhas alinhadas em todas as superfícies)
⏱️ Etapas do Acesso Físico ao Disco
Tempo de Busca (Seek Time): Deslocamento mecânico do braço até o cilindro correto (5 a 10 ms).  
PDF

Atraso Rotacional (Rotational Latency): Espera até o setor girar sob a cabeça de leitura (5 a 10 ms).  
PDF

Transferência de Dados: Leitura/escrita dos bits (50 a 160 MB/s).  
PDF

🔌 1.3.4 Dispositivos de Entrada/Saída e Interrupções
Os dispositivos de Entrada/Saída são compostos pelo controlador (chip que gerencia a interface do dispositivo) e pelo dispositivo físico propriamente dito.  
PDF

Snippet de código
sequenceDiagram
    autonumber
    participant Driver as Driver de Dispositivo
    participant Ctrl as Controlador de E/S
    participant Dev as Dispositivo Físico
    participant InterruptCtrl as Controlador de Interrupção
    participant CPU as CPU

    Driver->>Ctrl: 1. Escreve nos registradores de E/S
    Ctrl->>Dev: Inicia operação física
    Dev-->>Ctrl: Finaliza operação de E/S
    Ctrl->>InterruptCtrl: 2. Sinaliza linha de interrupção
    InterruptCtrl->>CPU: 3. Alerta a CPU sobre conclusão
    CPU->>InterruptCtrl: 4. Solicita identificação do dispositivo
    CPU->>Driver: Executa Tratador de Interrupção
⚡ Estratégias de Controle de Entrada e Saída
┌───────────────────────────────────────────────────────────────────────────┐
│                       MÉTODOS DE CONTROLE DE E/S                          │
│                                                                           │
│ 1. ESPERA OCUPADA (*Polling*):                                            │
│    O driver testa continuamente o registrador do controlador em laço.    │
│    Desvantagem: Desperdiça tempo de processamento da CPU.                 │
│                                                                           │
│ 2. E/S ORIENTADA A INTERRUPÇÃO:                                           │
│    O driver inicia o dispositivo e suspende o processo.                   │
│    O controlador emite uma interrupção de hardware ao concluir.          │
│    Vantagem: Libera a CPU para executar outros processos.                │
│                                                                           │
│ 3. DMA (*Direct Memory Access*):                                          │
│    Um chip dedicado gerencia a transferência de blocos entre a RAM e o   │
│    controlador sem intervenção contínua da CPU.                           │
│    Vantagem: Altíssima eficiência no manuseio de grande volume de dados.  │
└───────────────────────────────────────────────────────────────────────────┘
🚏 1.3.5 Barramentos e Arquitetura x86 Moderna
Os computadores modernos possuem uma hierarquia complexa de barramentos seriais dedicados de ponto a ponto.  
PDF

Snippet de código
graph TD
    CPU[CPU: Núcleos + Caches + GPU + Controlador RAM]
    CPU <-->|DDR3 Bus| RAM[Memória DDR3]
    CPU <-->|PCIe Bus| GPU[Placa Gráfica]
    CPU <-->|DMI Bus| PCH[Centro Controlador da Plataforma - PCH]
    
    PCH <-->|SATA| HDD[Discos SATA / SSD]
    PCH <-->|USB 2.0 / 3.0| USB[Periféricos USB]
    PCH <-->|PCIe| Net[Placa de Rede Gigabit]
    PCH <-->|PCI Tradicional| Legacy[Dispositivos Antigos PCI]
🔄 1.3.6 O Processo de Inicialização do Computador (Booting)
Snippet de código
flowchart TD
    A[1. ENERGIA LIGADA: CPU roda o BIOS/UEFI armazenado na Flash RAM] --> B[2. POST: Teste de hardware da memória RAM e barramentos]
    B --> C[3. CONSULTA CMOS: Obtém a ordem de boot dos dispositivos]
    C --> D[4. LER SECTOR DE BOOT: Carrega o MBR/GPT do disco selecionado]
    D --> E[5. BOOTLOADER SECUNDÁRIO: Carrega o núcleo do SO na RAM]
    E --> F[6. INICIALIZAÇÃO DO NÚCLEO: SO consulta o BIOS, carrega drivers e inicia a GUI]
🦁 1.4 O ZOOLÓGICO DOS SISTEMAS OPERACIONAIS
Devido à diversidade de hardware e de aplicações, surgiram diferentes categorias de sistemas operacionais.  
PDF

Snippet de código
graph TD
    Zoo[O Zoo dos Sistemas Operacionais]
    Zoo --> Mainframe[Computadores de Grande Porte]
    Zoo --> Server[Sistemas de Servidores]
    Zoo --> Multi[Sistemas Multiprocessadores]
    Zoo --> PC[Computadores Pessoais]
    Zoo --> Mobile[Computadores Portáteis / Móveis]
    Zoo --> Embed[Sistemas Embarcados]
    Zoo --> Sensor[Nós Sensores - Sensor Node]
    Zoo --> RTOS[Sistemas de Tempo Real]
    Zoo --> Smartcard[Cartões Inteligentes - Smartcards]
🐾 Matriz Comparativa do Zoo de Sistemas Operacionais
Categoria do SO	Hardware Alvo	Escopo e Aplicação Principal	Exemplos Notáveis
Computadores de Grande Porte	
Mainframes (centenas de discos, TBs de RAM)  
PDF

Lote (batch), processamento de transações bancárias maciças.  
PDF

OS/390, z/OS, Linux  
PDF

Servidores	
PCs grandes ou estações de trabalho  
PDF

Servir páginas web, compartilhamento de arquivos e impressão.  
PDF

Solaris, FreeBSD, Linux, Windows Server  
PDF

Multiprocessadores	
Chips multinúcleo e computadores paralelos  
PDF

Computação científica de alto desempenho e servidores em escala.  
PDF

Linux, Windows, macOS  
PDF

Computadores Pessoais	
Desktops e Laptops  
PDF

Uso individual, edição de texto, navegação na internet, jogos.  
PDF

Windows 7/8/10/11, macOS, Linux  
PDF

Computadores Portáteis	
Smartphones e Tablets  
PDF

Computação móvel, consumo de mídia e aplicativos móveis.  
PDF

Android, iOS  
PDF

Embarcados	
Eletrodomésticos, automóveis, TVs  
PDF

Controle de dispositivos sem suporte a softwares instalados pelo usuário.  
PDF

Embedded Linux, QNX, VxWorks  
PDF

Nós Sensores	
Microprocessadores com rádio e bateria  
PDF

Coleta de dados ambientais, segurança e monitoramento de rede.  
PDF

TinyOS  
PDF

Tempo Real (Real-Time)	
Processadores industriais e aviônica  
PDF

Sistemas com prazos rígidos de resposta (deadlines).  
PDF

eCos, QNX, RTLinux  
PDF

Cartões Inteligentes	
Chips em cartões de crédito  
PDF

Pagamentos eletrônicos, autenticação e segurança.  
PDF

JavaCard, SOs proprietários  
PDF

🎯 RESUMO FINAL & RECAPITULAÇÃO
Evolução Histórica: A computação evoluiu de sistemas sem SO programados via painéis de fios para sistemas em lote (batch), multiprogramados, de tempo compartilhado (timesharing), pessoais (GUIs) e móveis/nuvem.  
PDF

Dependência de Hardware: O projeto de um SO está atrelado às características do processador (modos núcleo/usuário, registradores), hierarquia de memória (RAM/Cache) e gerenciamento de E/S (interrupções e DMA)[cite: 1].

Especialização: O mercado moderno conta com sistemas operacionais adaptados para diferentes nichos, desde cartões inteligentes de recursos mínimos até mainframes e supercomputadores em nuvem[cite: 1].

Documento gerado com base no conteúdo das páginas 5 a 13 da obra Sistemas Operacionais Modernos (4ª Edição) de Andrew S. Tanenbaum & Herbert Bos[cite: 1].
