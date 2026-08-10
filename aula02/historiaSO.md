# SISTEMAS OPERACIONAIS MODERNOS — RESUMO EXPANDIDO (PÁGS. 5 A 13) 📚🚀

---

## 📌 SUMÁRIO EXECUTIVO & VISÃO GERAL
* **Obra original:** *Sistemas Operacionais Modernos* (4ª Edição) — Andrew S. Tanenbaum & Herbert Bos.
* **Recorte textual:** Capítulo 1, Seção 1.2 — *História dos Sistemas Operacionais* (Páginas 5 a 13).
* **Objetivo:** Mapear e detalhar a evolução histórica dos Sistemas Operacionais (SO), desde a era das válvulas termiônicas e painéis de ligações até a revolução dos dispositivos móveis e da computação em nuvem.

---

## 🗺️ MAPA MENTAL GERAL DOS SISTEMAS OPERACIONAIS

```mermaid
mindmap
  root((Evolução dos SOs))
    1ª Geração 1945-1955
      Válvulas Termiônicas
      Painéis de Ligações
      Sem Sistema Operacional
      Código Absoluto de Máquina
    2ª Geração 1955-1965
      Transistores
      Sistemas em Lote Batch
      IBM 7094 e FMS
      Cartões Perfurados e Fitas
    3ª Geração 1965-1980
      Circuitos Integrados CIs
      Multiprogramação
      Spooling e Timesharing
      IBM System/360
      MULTICS e UNIX
    4ª Geração 1980-Presente
      LSI e VLSI
      Computadores Pessoais
      GUIs e Mouse
      CP/M, MS-DOS, Windows, Mac
    5ª Geração 1990-Presente
      Dispositivos Móveis
      Smartphones e Tablets
      Android e iOS
      Computação em Nuvem
⏳ LINHA DO TEMPO DA COMPUTAÇÃO (1945 – PRESENTE)Snippet de códigotimeline
    title Linha do Tempo da Computação e dos Sistemas Operacionais
    section 1ª Geração (Válvulas)
        1945 : ENIAC, Z3, Colossus : Programação manual por fios e painéis
    section 2ª Geração (Transistores)
        1955 : Transistores & Sistemas Batch : Surgimento do IBM 7094 e FMS
        1961 : DEC PDP-1 : Início da era dos minicomputadores
    section 3ª Geração (CIs & Multiprogramação)
        1964 : IBM System/360 : Unificação de linhas comerciais e científicas
        1965 : Projeto MULTICS : Conceito de computador utilitário
        1969 : Criado o UNIX : Ken Thompson no PDP-7
        1974 : Intel 8080 & CP/M : Início da era dos microcomputadores
    section 4ª Geração (PCs & GUIs)
        1981 : IBM PC & MS-DOS : Domínio da Microsoft no mercado
        1984 : Apple Macintosh : Popularização da Interface Gráfica (GUI)
        1987 : Criado o MINIX : Sistema educacional de Andrew Tanenbaum
        1991 : Criado o Kernel Linux : Linus Torvalds baseado no MINIX
    section 5ª Geração (Móvel & Nuvem)
        1995 : Windows 95 & Nokia N9000 : Primeiro smartphone do mercado
        2007 : Apple iPhone (iOS) : Revolução da interface sensível ao toque
        2008 : Google Android : Lançamento do SO móvel open source
        Atualidade : Multinúcleo & Nuvem : Virtualização e computação ubíqua
⌛ 1.2 HISTÓRIA DOS SISTEMAS OPERACIONAISA evolução dos sistemas operacionais está umbilicalmente ligada às mudanças na arquitetura do hardware. Cada avanço tecnológico nos componentes físicos reduziu custos e tamanho, exigindo novas abstrações de software.  Snippet de códigograph TD
    A[Evolução do Hardware] -->|Aumenta Capacidade| B[Novos Paradigmas de Software]
    B -->|Gera Gargalos| C[Exigência de Novas Abstrações]
    C -->|Impulsiona| A
🔌 1.2.1 A Primeira Geração (1945–1955): VálvulasParâmetroDetalhes Técnicos / HistóricosTecnologia BaseVálvulas termiônicas e relés eletromagnéticos. 💡  PioneirosJohn Atanasoff & Clifford Berry (ABC), Konrad Zuse (Z3), Alan Turing (Colossus), Howard Aiken (Mark I), Eckert & Mauchly (ENIAC).  Modo de OperaçãoInserção direta de cabos em painéis de ligações (plugboards).  LinguagemCódigo de máquina absoluto (sem assembly, sem linguagens de alto nível). 🔣  Sistema OperacionalInexistente. O usuário agendava tempo de máquina na parede.  Tipo de ProblemaCálculos numéricos e matemáticos diretos (tabelas trigonométricas, trajetórias balísticas).  🛠️ Dinâmica de Trabalho na Era das VálvulasO programador reservava um bloco de tempo em uma folha na parede. 📝  Descia até a sala de máquinas.  Conectava milhares de cabos aos painéis de ligação para definir a lógica do programa.  Torcia para que nenhuma das ~20.000 válvulas queimasse durante a execução. 🔥  No início da década de 1950, introduziram-se os cartões perfurados, eliminando a necessidade dos painéis de fios.  🔲 1.2.2 A Segunda Geração (1955–1965): Transistores e Sistemas em Lote (Batch)Com a introdução do transistor em meados dos anos 1950, a confiabilidade dos computadores aumentou drasticamente. Pela primeira vez, surgiram papéis profissionais bem definidos: projetistas, operadores, programadores e equipe de manutenção.  Snippet de códigoflowchart LR
    Prog[Programador] -->|Perfura Cartões| IBM1401_In[IBM 1401]
    IBM1401_In -->|Grava Lote| FitaIn[(Fita de Entrada)]
    FitaIn -->|Levada ao| IBM7094[IBM 7094 Processador]
    IBM7094 -->|Grava Resposta| FitaOut[(Fita de Saída)]
    FitaOut -->|Levada ao| IBM1401_Out[IBM 1401]
    IBM1401_Out -->|Imprime| Relatorio[Relatório Final]
💻 Equipamentos EmblemáticosIBM 1401: Computador menor e barato, excelente para leitura de cartões, cópia de fitas e impressão de relatórios (E/S).  IBM 7094: Mainframe caro e veloz, voltado exclusivamente para cálculos numéricos científicos pesados.  📜 Estrutura de uma Tarefa em FMS (Fortran Monitor System)+-------------------------------------------------------+
| $END                                                  |  <-- Fim da tarefa
+-------------------------------------------------------+
| Dados do Programa                                     |  <-- Entradas numéricas
+-------------------------------------------------------+
| $RUN                                                  |  <-- Executa o código
+-------------------------------------------------------+
| $LOAD                                                 |  <-- Carrega objeto
+-------------------------------------------------------+
| Programa FORTRAN (Cartões perfurados do código fonte) |  <-- Código fonte
+-------------------------------------------------------+
| $FORTRAN                                              |  <-- Carrega compilador
+-------------------------------------------------------+
| $JOB, 10.7710802, MARVIN TANENBAUM                    |  <-- Identificação
+-------------------------------------------------------+
ComponenteFunção$JOBEspecifica tempo máximo de CPU, conta bancária/devedora e nome do usuário.  $FORTRANOrienta o sistema operacional a carregar o compilador FORTRAN da fita do sistema.  $LOADDetermina o carregamento do código-objeto recém-compilado na memória.  $RUNExecuta o programa com os dados que seguem no lote.  $ENDMarca o término definitivo da tarefa no lote.  🔲 1.2.3 A Terceira Geração (1965–1980): CIs e MultiprogramaçãoA terceira geração foi marcada pelo surgimento dos Circuitos Integrados (CIs) e pelo lançamento do histórico IBM System/360.  Snippet de códigograph TD
    360[IBM System/360]
    360 --> Sci[Cálculo Científico 7094 - Palavras]
    360 --> Com[Processamento Comercial 1401 - Caracteres]
    Sci --> Uni[Linha Única de Software e Hardware Compatível]
    Com --> Uni
📊 Comparativo: Uniprogramação vs. MultiprogramaçãoUNIPROGRAMAÇÃO (2ª Geração):
┌───────────┬───────────────────────┬───────────┬───────────────────────┐
│  Executa  │   Espera E/S (Ocioso) │  Executa  │   Espera E/S (Ocioso) │
└───────────┴───────────────────────┴───────────┴───────────────────────┘
0% CPU ───────────────────────────────────────────────────────────► 100%

MULTIPROGRAMAÇÃO (3ª Geração):
┌───────────────────────────────────────────────────────────────────────┐
│ Tarefa 3  ▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒               │
├───────────────────────────────────────────────────────────────────────┤
│ Tarefa 2  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░               │
├───────────────────────────────────────────────────────────────────────┤
│ Tarefa 1  █████████████████████████████████████████████               │
├───────────────────────────────────────────────────────────────────────┤
│    SO     ─────────────────────────────────────────────               │
└───────────────────────────────────────────────────────────────────────┘
🚀 Árvore Genealógica UNIX e Padrões DerivadosSnippet de códigograph TD
    MULTICS[MULTICS - 1965] -->|Ken Thompson| UNIX[UNIX - 1969]
    UNIX --> SystemV[System V - AT&T]
    UNIX --> BSD[BSD - UC Berkeley]
    SystemV --> POSIX[Padrão POSIX]
    BSD --> POSIX
    POSIX --> MINIX[MINIX - 1987 Tanenbaum]
    MINIX --> Linux[Linux - 1991 Torvalds]
    BSD --> macOS[macOS / iOS]
💻 1.2.4 A Quarta Geração (1980–Presente): Computadores PessoaisCom a tecnologia LSI (Large Scale Integration) e VLSI, milhares e depois milhões de transistores foram integrados em um único chip microprocessador, tornando o computador um bem individual.  Snippet de códigograph TD
    PC[Era dos Microcomputadores]
    PC --> DR[Digital Research / Gary Kildall]
    PC --> MS[Microsoft / Bill Gates]
    PC --> AP[Apple / Steve Jobs]
    
    DR --> CPM[CP/M - Dominou Era 8 Bits]
    MS --> MSDOS[MS-DOS / Paterson]
    MSDOS --> WIN[Windows 95/98 -> NT/XP/7/11]
    
    AP --> MAC[Macintosh - GUI Xerox PARC]
    MAC --> OSX[macOS - Base UNIX/FreeBSD]
📑 Comparativo Técnico: Principais Famílias de SOs PessoaisCaracterísticaCP/MMS-DOSWindows (Linha NT)UNIX / Linux / Mac OS XOrigemDigital Research (1974)  Microsoft (1981)  Microsoft (1993 - NT 3.1)  AT&T / BSD / Torvalds / Apple  Arquitetura Base8 bits (Intel 8080/Z80)  16 bits (Intel 8086/8088)  32/64 bits híbrido  32/64 bits modular / monolítico  Interface PadrãoLinha de Comando (CLI)  Linha de Comando (CLI)  Interface Gráfica (GUI)  Shell / GUI (X11, Wayland, Aqua)  MultiprogramaçãoInexistente  Não (Monotarefa)  Sim (Preemptiva)  Sim (Preemptiva)  Segurança/ProteçãoNenhuma  Nenhuma  Elevada (Acessos, ACLs)  Elevada (Permissões, POSIX)  📱 1.2.5 A Quinta Geração (1990–Presente): Computadores MóveisA miniaturização extrema e a integração de componentes permitiram o surgimento de smartphones e tablets, transformando a telefonia móvel em uma plataforma de computação de propósito geral.  Snippet de códigograph LR
    Symbian[Symbian OS - Dominante até 2010] --> Decline[Declínio]
    RIM[BlackBerry OS - Foco Corporativo] --> Decline
    iOS[Apple iOS - Lançado em 2007] --> Top[Liderança Atual]
    Android[Google Android - Lançado em 2008] --> Top
ParâmetroAndroidiOSNúcleo (Kernel)Linux  Mach / XNU (Derivado do FreeBSD)  LicenciamentoAberto (Open Source / Licença Apache)  Proprietário (Fechado)  Linguagem PrimáriaJava / Kotlin (Executado em Dalvik/ART)  Objective-C / Swift  Participação de MercadoLiderança global no mercado móvel  Segunda posição global  ⚙️ 1.3 REVISÃO SOBRE HARDWARE DE COMPUTADORESPara gerenciar recursos de forma eficiente, um sistema operacional precisa interagir diretamente com os componentes físicos subjacentes.  Snippet de códigoflowchart TD
    CPU[CPU + MMU] <--> Bus[BARRAMENTO DO SISTEMA]
    RAM[Memória RAM] <--> Bus
    Video[Controlador de Vídeo] <--> Bus
    SATA[Controlador Disco SATA] <--> Bus
    USB[Controlador USB] <--> Bus
🧠 1.3.1 Processadores (CPUs)A CPU é o cérebro do sistema. Seu ciclo básico é: Buscar (Fetch) $\rightarrow$ Decodificar (Decode) $\rightarrow$ Executar (Execute).  📋 Registradores Principais da CPURegistradorNome / FunçãoPC (Program Counter)Aponta para o endereço da próxima instrução a ser buscada na memória.  SP (Stack Pointer)Aponta para o topo da pilha de execução (parâmetros, variáveis locais, endereços de retorno).  PSW (Program Status Word)Contém os bits de estado da CPU: modo de execução (núcleo/usuário), prioridade, códigos de condição.  🔒 Modos de OperaçãoModo Núcleo (Kernel Mode / Supervisor): A CPU pode executar todas as instruções do seu conjunto de instruções e acessar qualquer recurso de hardware. O SO opera neste modo.  Modo Usuário (User Mode): Apenas um subconjunto de instruções é permitido. Instruções de E/S e manipulação direta de memória/proteção são estritamente proibidas.  💾 1.3.2 Memória e Hierarquia de ArmazenamentoA memória é organizada em uma hierarquia estrita: quanto mais rápida e próxima da CPU, menor a sua capacidade e maior o seu custo por bit.  Snippet de códigograph TD
    Reg[Registradores - < 1 KB - ~1 ns]
    Cache[Cache L1 / L2 / L3 - MB - ~2-5 ns]
    RAM[Memória Principal RAM - GB - ~10-100 ns]
    Disk[Disco Magnético / SSD - TB - ~10 ms]
    
    Reg --> Cache
    Cache --> RAM
    RAM --> Disk
🔌 1.3.4 Dispositivos de Entrada/Saída e InterrupçõesDispositivos de Entrada/Saída (E/S) são divididos em duas partes primordiais: o controlador físico (chip de controle) e o dispositivo em si.  Snippet de códigosequenceDiagram
    autonumber
    participant Driver as Driver (SO)
    participant Ctrl as Controlador E/S
    participant Dev as Dispositivo Físico
    participant CPU as CPU

    Driver->>Ctrl: 1. Grava comandos nos registradores
    Ctrl->>Dev: Inicia operação física
    Dev-->>Ctrl: Conclui leitura/escrita
    Ctrl->>CPU: 2. Emite sinal de Interrupção
    CPU->>Driver: 3. Executa o Tratador de Interrupção
🔄 1.3.6 O Processo de Inicialização do Computador (Booting)Snippet de códigoflowchart TD
    A[1. ENERGIA LIGADA: CPU executa BIOS/UEFI na Flash ROM] --> B[2. POST: Teste de hardware RAM, discos, PCIe]
    B --> C[3. LER CMOS: Identifica ordem dos dispositivos de Boot]
    C --> D[4. SETOR DE BOOT: Lê MBR/GPT do disco selecionado]
    D --> E[5. CARREGADOR SECUNDÁRIO: Carrega o núcleo do SO na RAM]
    E --> F[6. INICIALIZAÇÃO DO SO: Carrega drivers e inicia tela de login]
  🦁 1.4 O ZOOLÓGICO DOS SISTEMAS OPERACIONAISA diversidade de hardware e de cenários de uso resultou no surgimento de várias categorias especializadas de SOs.  🐾 Matriz Comparativa do Zoo de Sistemas OperacionaisTipo de SOHardware AlvoAplicação PrincipalExemplos NotáveisComputadores de Grande PorteMainframes (centenas de discos, TBs de RAM)  Processamento em lote, transações maciças (bancos, reservas).  OS/390, z/OS, Linux  ServidoresPCs grandes, estações de trabalho  Servir páginas web, impressão, arquivos e banco de dados.  Solaris, FreeBSD, Linux, Windows Server  MultiprocessadoresChips multinúcleo / Computadores paralelos  Computação científica de alto desempenho, servidores de grande porte.  Linux, Windows, macOS  Computadores PessoaisDesktops e Laptops  Uso pessoal, navegação, edição de texto, jogos.  Windows 7/8/10/11, macOS, Linux  Computadores PortáteisSmartphones e Tablets  Comunicação móvel, consumo de mídia, aplicativos diversos.  Android, iOS  EmbarcadosEletrodomésticos, carros, TVs  Controle de dispositivos físicos fechados (sem software de usuário).  Embedded Linux, QNX, VxWorks  Nós SensoresMicroprocessadores com rádio e bateria  Monitoramento ambiental, defesa, medição de dados em rede.  TinyOS  Tempo Real (Real-Time)Processadores de controle industrial  Sistemas críticos com prazos rígidos de resposta (deadlines).  eCos, QNX, RTLinux  Cartões InteligentesChips em cartões de crédito (smartcards)  Pagamentos eletrônicos, autenticação segura.  JavaCard, SOs proprietários  🎯 RESUMO FINAL & RECAPITULAÇÃO DAS PÁGINAS 5 A 13Evolução Histórica: Passou de sistemas sem SO programados por painéis de fios (válvulas) para os sistemas em lote (batch - transistores), evoluindo para a multiprogramação e compartilhamento de tempo (CIs), consolidando-se nos computadores pessoais (LSI) e explodindo nos dispositivos móveis (VLSI).  Fundamentos de Hardware: O SO precisa entender o funcionamento de CPUs (registradores, pipelines, modos núcleo/usuário), memórias (hierarquia RAM/Cache/Disco), controladores de E/S e arquiteturas de barramento (PCIe, SATA, USB)[cite: 1].Aplicações Práticas: A escolha da arquitetura do SO depende diretamente das limitações de hardware e dos requisitos do ambiente — desde um sistema de Smartcard baseado em Java de recursos mínimos até mainframes capazes de processar milhões de transações por segundo[cite: 1].Documento gerado com base no conteúdo das páginas 5 a 13 da obra Sistemas Operacionais Modernos (4ª Edição) de Andrew S. Tanenbaum & Herbert Bos[cite: 1].
