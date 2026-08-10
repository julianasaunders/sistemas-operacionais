## 📌 SUMÁRIO EXECUTIVO & VISÃO GERAL
* **Obra original:** *Sistemas Operacionais Modernos* (4ª Edição) — Andrew S. Tanenbaum & Herbert Bos.
* **Recorte textual:** Capítulo 1, Seção 1.2 — *História dos Sistemas Operacionais* (Páginas 5 a 13).
* **Objetivo:** Mapear e detalhar a evolução histórica dos Sistemas Operacionais (SO), desde a era das válvulas termiônicas e painéis de ligações até a revolução dos dispositivos móveis e da computação em nuvem.

---

## 🗺️ MAPA MENTAL DA EVOLUÇÃO DOS SISTEMAS OPERACIONAIS

                   EVOLUÇÃO DOS SISTEMAS OPERACIONAIS
                                   │
┌───────────────────┬───────────────┼───────────────┬───────────────────┐
▼                   ▼               ▼               ▼                   ▼
1ª GERAÇÃO          2ª GERAÇÃO      3ª GERAÇÃO      4ª GERAÇÃO          5ª GERAÇÃO
(1945 - 1955)       (1955 - 1965)   (1965 - 1980)   (1980 - PRESENTE)   (1990 - PRESENTE)
│                   │               │               │                   │
├─ Válvulas         ├─ Transistores ├─ CIs (360)    ├─ LSI/VLSI (PC)    ├─ Dispositivos Móveis
├─ Painéis de fios  ├─ Batch        ├─ Multiprog.   ├─ GUIs & UNIX      ├─ Smartphones
└─ Sem SO           └─ FMS / IBSYS  └─ MULTICS/UNIX └─ MS-DOS/Win/Linux └─ Android / iOS


---

## ⏳ LINHA DO TEMPO DA COMPUTAÇÃO E DOS SOs (1945–PRESENTE)

1945 ─── 1ª Geração: Válvulas, ENIAC, Z3, Colossus (Programação por painéis/fios)
│
1955 ─── 2ª Geração: Transistores e Sistemas em Lote (IBM 7094, FMS, Cartões Perfurados)
│
1961 ─── Lançamento do DEC PDP-1 (Início da era dos minicomputadores)
│
1964 ─── Lançamento do IBM System/360 (Unificação da arquitetura comercial e científica)
│
1965 ─── Projeto MULTICS (MIT, Bell Labs, GE) — Conceito de serviço utilitário de computação
│
1969 ─── Criação do UNIX (Ken Thompson / Bell Labs no PDP-7)
│
1974 ─── Lançamento do Intel 8080 (CPU de 8 bits) & CP/M (Gary Kildall)
│
1981 ─── Lançamento do IBM PC com o MS-DOS (Microsoft / Tim Paterson / Bill Gates)
│
1984 ─── Lançamento do Apple Macintosh (Popularização da Interface Gráfica - GUI)
│
1987 ─── Lançamento do MINIX (Andrew S. Tanenbaum, para fins educacionais)
│
1991 ─── Linus Torvalds lança o Linux (Inspirado no MINIX)
│
1995 ─── Lançamento do Windows 95 e do Nokia N9000 (Primeiro Smartphone)
│
2008 ─── Lançamento do Android pela Google (Baseado no Linux)
│
PRESENTE ─ Predomínio de processadores multinúcleo, virtualização, nuvem e SOs móveis.


---

## ⌛ 1.2 HISTÓRIA DOS SISTEMAS OPERACIONAIS

A evolução dos sistemas operacionais está umbilicalmente ligada às mudanças na **arquitetura do hardware**. Cada avanço tecnológico nos componentes físicos reduziu custos e tamanho, exigindo novas abstrações de software.

┌─────────────────────────────────────────────────────────────────────────┐
│              Relação Ciclica: Hardware vs. Software                    │
│                                                                         │
│   Evolução do Hardware  ───►  Aumento de Capacidade                     │
│           ▲                                │                            │
│           │                                ▼                            │
│   Novas Exigências      ◄───  Gargalos de Software / Paradigmas         │
└─────────────────────────────────────────────────────────────────────────┘


---

## 🔌 1.2.1 A Primeira Geração (1945–1955): Válvulas

| Parâmetro | Detalhes Técnicos / Históricos |
| :--- | :--- |
| **Tecnologia Base** | Válvulas termiônicas e relés eletromagnéticos. 💡 |
| **Pioneiros** | John Atanasoff & Clifford Berry (ABC), Konrad Zuse (Z3), Alan Turing (Colossus), Howard Aiken (Mark I), Eckert & Mauchly (ENIAC). |
| **Modo de Operação** | Inserção direta de cabos em painéis de ligações (*plugboards*). |
| **Linguagem** | Código de máquina absoluto (sem assembly, sem linguagens de alto nível). 🔣 |
| **Sistema Operacional** | **Inexistente.** O usuário agendava tempo de máquina na parede. |
| **Tipo de Problema** | Cálculos numéricos e matemáticos diretos (tabelas trigonométricas, trajetórias balísticas). |

### 🛠️ Dinâmica de Trabalho na Era das Válvulas
1. O programador reservava um bloco de tempo em uma folha na parede. 📝
2. Descia até a sala de máquinas.
3. Conectava milhares de cabos aos painéis de ligação para definir a lógica do programa.
4. Torcia para que nenhuma das ~20.000 válvulas queimasse durante a execução. 🔥
5. No início da década de 1950, introduziram-se os **cartões perfurados**, eliminando a necessidade dos painéis de fios.

---

## 🔲 1.2.2 A Segunda Geração (1955–1965): Transistores e Sistemas em Lote (*Batch*)

Com a introdução do transistor em meados dos anos 1950, a confiabilidade dos computadores aumentou drasticamente. Pela primeira vez, surgiram papéis profissionais bem definidos: **projetistas, operadores, programadores e equipe de manutenção**.

┌───────────────────────────────────────────────────────────────────────────┐
│                    FLUXO DE UM SISTEMA EM LOTE (BATCH)                    │
│                                                                           │
│  [Programador] ──► Cartões ──► [IBM 1401] ──► Fita Entr. ──► [IBM 7094]   │
│                                                                    │      │
│  [Relatório]  ◄── Impressão ◄── [IBM 1401] ◄── Fita Saída ◄────────┘      │
└───────────────────────────────────────────────────────────────────────────┘


### 💻 Equipamentos Emblemáticos
* **IBM 1401:** Computador menor e barato, excelente para leitura de cartões, cópia de fitas e impressão de relatórios (E/S).
* **IBM 7094:** Mainframe caro e veloz, voltado exclusivamente para cálculos numéricos científicos pesados.

### 📜 Estrutura de uma Tarefa em FMS (Fortran Monitor System)

+-------------------------------------------------------+
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


| Componente | Função |
| :--- | :--- |
| **`$JOB`** | Especifica tempo máximo de CPU, conta bancária/devedora e nome do usuário. |
| **`$FORTRAN`** | Orienta o sistema operacional a carregar o compilador FORTRAN da fita do sistema. |
| **`$LOAD`** | Determina o carregamento do código-objeto recém-compilado na memória. |
| **`$RUN`** | Executa o programa com os dados que seguem no lote. |
| **`$END`** | Marca o término definitivo da tarefa no lote. |

---

## 🔲 1.2.3 A Terceira Geração (1965–1980): CIs e Multiprogramação

A terceira geração foi marcada pelo surgimento dos **Circuitos Integrados (CIs)** e pelo lançamento do histórico **IBM System/360**.

                       IBM SYSTEM/360
                             │
     ┌───────────────────────┴───────────────────────┐
     ▼                                               ▼
Cálculo Científico (7094)                       Processamento Comercial (1401)
Orientado a Palavras                             Orientado a Caracteres
│                                               │
└───────────────────────┬───────────────────────┘
▼
LINHA ÚNICA COMPATÍVEL


### 📊 Comparativo: Uniprogramação vs. Multiprogramação

UNIPROGRAMAÇÃO (2ª Geração):
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


### 🚀 Conceitos Fundamentais Introduzidos na 3ª Geração

1. **Multiprogramação:** Divisão da memória em várias partições. Enquanto uma tarefa espera pela conclusão de uma operação de Entrada/Saída (E/S), a CPU é alocada para outra tarefa.
2. **Spooling (*Simultaneous Peripheral Operation On Line*):** Capacidade de ler tarefas dos cartões diretamente para o disco assim que chegavam, eliminando a necessidade de máquinas intermediárias como o IBM 1401.
3. **Compartilhamento de Tempo (*Timesharing*):** Variante da multiprogramação onde cada usuário possui um terminal interativo on-line, permitindo respostas rápidas a comandos curtos.
4. **MULTICS (*MULTiplexed Information and Computing Service*):** Projeto ambicioso de um "computador utilitário", concebido pelo MIT, Bell Labs e General Electric. Embora comercialmente limitado, introduziu conceitos fundamentais para o UNIX.

                              MULTICS
                                 │
                         (Ken Thompson)
                                 ▼
                            UNIX (1969)
                                 │
             ┌───────────────────┴───────────────────┐
             ▼                                       ▼
        System V (AT&T)                        BSD (Berkeley)
             │                                       │
             └───────────────────┬───────────────────┘
                                 ▼
                            POSIX Standard
                                 │
             ┌───────────────────┴───────────────────┐
             ▼                                       ▼
        MINIX (1987)                           Linux (1991)

---

## 💻 1.2.4 A Quarta Geração (1980–Presente): Computadores Pessoais

Com a tecnologia LSI (*Large Scale Integration*) e VLSI, milhares e depois milhões de transistores foram integrados em um único chip microprocessador, tornando o computador um bem individual.

                              EVOLUÇÃO DOS SOs DE PC
                                         │
  ┌──────────────────────────────────────┼──────────────────────────────────────┐
  ▼                                      ▼                                      ▼
DIGITAL RESEARCH                         MICROSOFT                                APPLE
(CP/M)                                 (MS-DOS)                               (Macintosh)
│                                      │                                      │
Criado por                             Comprado da                            Inspirado no
Gary Kildall                          Seattle Computer                          Xerox PARC
para o 8080.                            (QDOS/Paterson).                          (GUI, Mouse,
│                                      │                                     Janelas).
Dominou a era                            Evoluiu para:                             │
de 8 bits (1977-1982).                  • Win 95/98/ME                            Evoluiu para
• Win NT/2000/XP                          Mac OS X (Mach/
• Win 7/8/10/11                           FreeBSD).


### 📑 Comparativo Técnico: Principais Famílias de SOs Pessoais

| Característica | CP/M | MS-DOS | Windows (Linha NT) | UNIX / Linux / Mac OS X |
| :--- | :--- | :--- | :--- | :--- |
| **Origem** | Digital Research (1974) | Microsoft (1981) | Microsoft (1993 - NT 3.1) | AT&T / BSD / Torvalds / Apple |
| **Arquitetura Base** | 8 bits (Intel 8080/Z80) | 16 bits (Intel 8086/8088) | 32/64 bits híbrido | 32/64 bits modular / monolítico |
| **Interface Padrão** | Linha de Comando (CLI) | Linha de Comando (CLI) | Interface Gráfica (GUI) | Shell / GUI (X11, Wayland, Aqua) |
| **Multiprogramação** | Inexistente | Não (Monotarefa) | Sim (Preemptiva) | Sim (Preemptiva) |
| **Segurança/Proteção** | Nenhuma | Nenhuma | Elevada (Acessos, ACLs) | Elevada (Permissões, POSIX) |

---

## 📱 1.2.5 A Quinta Geração (1990–Presente): Computadores Móveis

A miniaturização extrema e a integração de componentes permitiram o surgimento de smartphones e tablets, transformando a telefonia móvel em uma plataforma de computação de propósito geral.

                     EVOLUÇÃO DOS SOs MÓVEIS
                                │
┌───────────────────┬────────────┴───────┬───────────────────┐
▼                   ▼                    ▼                   ▼
Symbian OS         BlackBerry OS         Apple iOS        Google Android
(Dominante até     (Foco em              (Lançado em      (Lançado em 2008,
2010 - Nokia)      Negócios)             2007 - iPhone)   Código Aberto/Linux)


| Parâmetro | Android | iOS |
| :--- | :--- | :--- |
| **Núcleo (Kernel)** | Linux | Mach / XNU (Derivado do FreeBSD) |
| **Licenciamento** | Aberto (Open Source / Licença Apache) | Proprietário (Fechado) |
| **Linguagem Primária** | Java / Kotlin (Executado em Dalvik/ART) | Objective-C / Swift |
| **Participação de Mercado** | Liderança global no mercado móvel | Segunda posição global |

---

## ⚙️ 1.3 REVISÃO SOBRE HARDWARE DE COMPUTADORES

Para gerenciar recursos de forma eficiente, um sistema operacional precisa interagir diretamente com os componentes físicos subjacentes.

┌─────────────────────────────────────────────────────────────────────────┐
│                    ARQUITETURA DE UM HARDWARE SIMPLES                   │
│                                                                         │
│  ┌──────┐     ┌────────┐     ┌───────────┐     ┌─────────────────────┐  │
│  │ CPU  │     │Memória │     │Controlador│     │ Controlador Disco   │  │
│  │ +MMU │     │   RAM  │     │ de Vídeo  │     │      SATA           │  │
│  └──┬───┘     └───┬────┘     └─────┬─────┘     └──────────┬──────────┘  │
│     │             │                │                      │             │
│ ════╧═════════════╧════════════════╧══════════════════════╧═══════════  │
│                            BARRAMENTO DO SISTEMA                        │
└─────────────────────────────────────────────────────────────────────────┘


---

## 🧠 1.3.1 Processadores (CPUs)

A CPU é o cérebro do sistema. Seu ciclo básico é: **Buscar (*Fetch*) $\rightarrow$ Decodificar (*Decode*) $\rightarrow$ Executar (*Execute*)**.

PIPELINE DE INSTRUÇÕES (3 Estágios):
Instrução 1: [ Busca ] ──► [ Decodifica ] ──► [ Executa ]
Instrução 2:             [ Busca ]      ──► [ Decodifica ] ──► [ Executa ]
Instrução 3:                            [ Busca ]      ──► [ Decodifica ] ──► ...

ARQUITETURA SUPERESCALAR:
┌──► Unidade Inteira (ALU)
[ Buffer de Instruções ] ─┼──► Unidade Ponto Flutuante (FPU)
└──► Unidade Booleana


### 📋 Registradores Principais da CPU

| Registrador | Nome / Função |
| :--- | :--- |
| **PC** (*Program Counter*) | Aponta para o endereço da próxima instrução a ser buscada na memória. |
| **SP** (*Stack Pointer*) | Aponta para o topo da pilha de execução (parâmetros, variáveis locais, endereços de retorno). |
| **PSW** (*Program Status Word*) | Contém os bits de estado da CPU: modo de execução (núcleo/usuário), prioridade, códigos de condição. |

### 🔒 Modos de Operação
* **Modo Núcleo (*Kernel Mode* / Supervisor):** A CPU pode executar todas as instruções do seu conjunto de instruções e acessar qualquer recurso de hardware. O SO opera neste modo.
* **Modo Usuário (*User Mode*):** Apenas um subconjunto de instruções é permitido. Instruções de E/S e manipulação direta de memória/proteção são estritamente proibidas.

---

## 💾 1.3.2 Memória e Hierarquia de Armazenamento

A memória é organizada em uma hierarquia estrita: quanto mais rápida e próxima da CPU, menor a sua capacidade e maior o seu custo por bit.

                       HIERARQUIA DE MEMÓRIA

                              /\
                             /  \       Registradores (< 1 KB) | ~1 ns
                            /----\
                           / Cache\     Cache L1 / L2 / L3 (MB) | ~2-5 ns
                          /--------\
                         /  Memória \   RAM Principal (GB) | ~10-100 ns
                        /  Principal \
                       /--------------\
                      / Discos Magnét. \ Discos Magnéticos / SSDs (TB) | ~10 ms
                     /__________________\

### 📊 Especificações da Hierarquia de Memória

| Nível | Tempo de Acesso Típico | Capacidade Típica | Gerenciado por |
| :--- | :--- | :--- | :--- |
| **Registradores** | $\le 1 \text{ ns}$ | $< 1 \text{ KB}$ | Compilador / Hardware |
| **Cache (L1/L2/L3)** | $1 \text{ a } 5 \text{ ns}$ | $4 \text{ a } 64 \text{ MB}$ | Hardware |
| **Memória Principal (RAM)**| $10 \text{ a } 100 \text{ ns}$ | $1 \text{ a } 64 \text{ GB}$ | Sistema Operacional |
| **Disco Magnético / SSD** | $5 \text{ a } 10 \text{ ms}$ (Disco) | $1 \text{ a } 16 \text{ TB}$ | Sistema Operacional |

---

## 💽 1.3.3 Discos e Estrutura Física

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

### ⏱️ Tempos Envolvidos na Leitura de Disco
1. **Tempo de Busca (*Seek Time*):** Tempo para mover o braço mecânico até o cilindro correto ($\approx 5 \text{ a } 10 \text{ ms}$).
2. **Atraso Rotacional (*Rotational Latency*):** Tempo até o setor desejado girar para baixo da cabeça de leitura ($\approx 5 \text{ a } 10 \text{ ms}$ em discos de 5.400–10.800 RPM).
3. **Taxa de Transferência:** Velocidade de leitura real dos dados ($\approx 50 \text{ a } 160 \text{ MB/s}$).

---

## 🔌 1.3.4 Dispositivos de Entrada/Saída e Interrupções

Dispositivos de Entrada/Saída (E/S) são divididos em duas partes primordiais: o **controlador físico** (chip de controle) e o **dispositivo em si**.

               MECANISMO DE TRATAMENTO DE INTERRUPÇÃO
[1. Driver grava registradores] ──► [Controlador inicia E/S]
│
[4. CPU executa Tratador]     ◄── [3. Sinaliza CPU] ◄── [2. Conclusão E/S]


### ⚡ Formas de Realizar Entrada e Saída

┌───────────────────────────────────────────────────────────────────────────┐
│                       MÉTODOS DE MANEJO DE E/S                            │
│                                                                           │
│ 1. ESPERA OCUPADA (Polling):                                            │
│    CPU interroga o registrador do controlador em um laço infinito até terminar. │
│    ↳ Desvantagem: Desperdício massivo de tempo de CPU.                     │
│                                                                           │
│ 2. E/S ORIENTADA A INTERRUPÇÃO:                                           │
│    CPU inicia o dispositivo e passa a executar outro processo.            │
│    O controlador emite uma interrupção de hardware ao concluir.          │
│    ↳ Vantagem: Libera a CPU durante a operação de E/S.                   │
│                                                                           │
│ 3. DMA (Direct Memory Access):                                          │
│    Um chip dedicado controla a transferência direta de dados entre o      │
│    dispositivo e a RAM sem intervenção contínua da CPU.                 │
│    ↳ Vantagem: Altíssima eficiência para grandes volumes de dados.        │
└───────────────────────────────────────────────────────────────────────────┘


---

## 🚏 1.3.5 Barramentos e Estrutura dos Sistemas Modernos

Os sistemas x86 modernos utilizam uma estrutura hierárquica complexa de barramentos seriais ponto a ponto para suportar altas taxas de transferência.

┌─────────────────────────────────────────────────────────────────────────┐
│                     ESTRUTURA DE BARRAMENTOS MODERNA                    │
│                                                                         │
│    ┌──────────────────────────────────────────────────────────────┐     │
│    │ CPU (Núcleos + Caches + GPU + Controlador de Memória RAM)     │     │
│    └──────────────────────────────┬───────────────────────────────┘     │
│                                   │ DMI                                 │
│    ┌──────────────────────────────┴───────────────────────────────┐     │
│    │ CENTRO CONTROLADOR DA PLATAFORMA (Platform Controller Hub)   │     │
│    └────┬─────────────────┬────────────────┬───────────────┬──────┘     │
│         │ PCIe            │ SATA           │ USB 3.0       │ Ethernet   │
│         ▼                 ▼                ▼               ▼            │
│  [Placas Gráficas]   [Discos Rígidos]  [Periféricos]   [Conexão Rede]   │
└─────────────────────────────────────────────────────────────────────────┘


---

## 🔄 1.3.6 O Processo de Inicialização do Computador (*Booting*)

+-------------------------------------------------------------------------+
| 1. ENERGIA LIGADA: A CPU executa o BIOS/UEFI localizado na Flash ROM.   |
+-------------------------------------------------------------------------+
│
▼
+-------------------------------------------------------------------------+
| 2. POST (Power-On Self-Test): Verifica a quantidade de RAM e os         |
|    dispositivos básicos (teclado, discos, barramentos PCIe).            |
+-------------------------------------------------------------------------+
│
▼
+-------------------------------------------------------------------------+
| 3. DISPOSITIVO DE BOOT: O BIOS lê a lista de boot gravada na CMOS      |
|    (CD-ROM, USB ou Disco Rígido).                                       |
+-------------------------------------------------------------------------+
│
▼
+-------------------------------------------------------------------------+
| 4. SECTOR DE BOOT: O primeiro setor do disco ativo (MBR/GPT) é lido     |
|    para a memória e executado.                                           |
+-------------------------------------------------------------------------+
│
▼
+-------------------------------------------------------------------------+
| 5. CARREGADOR SECUNDÁRIO: Lê o núcleo do Sistema Operacional da        |
|    partição ativa e inicia sua execução.                               |
+-------------------------------------------------------------------------+
│
▼
+-------------------------------------------------------------------------+
| 6. INICIALIZAÇÃO DO SO: O SO consulta o BIOS para obter configurações,  |
|    carrega os drivers de dispositivos no núcleo e inicia a tela de login.|
+-------------------------------------------------------------------------+


---

## 🦁 1.4 O ZOOLÓGICO DOS SISTEMAS OPERACIONAIS

A diversidade de hardware e de cenários de uso resultou no surgimento de várias categorias especializadas de SOs.

                       ZOOLÓGICO DOS SOs
                               │
┌─────────────┬───────────┬─────┴─────┬─────────────┬─────────────┐
▼             ▼           ▼           ▼             ▼             ▼
Mainframes   Servidores   Móveis    Embarcados   Tempo Real    Smartcards
(OS/390)     (Linux/Win) (Android)  (VxWorks)      (eCos)       (JavaCard)


### 🐾 Matriz Comparativa do Zoo de Sistemas Operacionais

| Tipo de SO | Hardware Alvo | Aplicação Principal | Exemplos Notáveis |
| :--- | :--- | :--- | :--- |
| **Computadores de Grande Porte** | Mainframes (centenas de discos, TBs de RAM) | Processamento em lote, transações maciças (bancos, reservas). | OS/390, z/OS, Linux |
| **Servidores** | PCs grandes, estações de trabalho | Servir páginas web, impressão, arquivos e banco de dados. | Solaris, FreeBSD, Linux, Windows Server |
| **Multiprocessadores** | Chips multinúcleo / Computadores paralelos | Computação científica de alto desempenho, servidores de grande porte. | Linux, Windows, macOS |
| **Computadores Pessoais** | Desktops e Laptops | Uso pessoal, navegação, edição de texto, jogos. | Windows 7/8/10/11, macOS, Linux |
| **Computadores Portáteis** | Smartphones e Tablets | Comunicação móvel, consumo de mídia, aplicativos diversos. | Android, iOS |
| **Embarcados** | Eletrodomésticos, carros, TVs | Controle de dispositivos físicos fechados (sem software de usuário). | Embedded Linux, QNX, VxWorks |
| **Nós Sensores** | Microprocessadores com rádio e bateria | Monitoramento ambiental, defesa, medição de dados em rede. | TinyOS |
| **Tempo Real (*Real-Time*)** | Processadores de controle industrial | Sistemas críticos com prazos rígidos de resposta (*deadlines*). | eCos, QNX, RTLinux |
| **Cartões Inteligentes** | Chips em cartões de crédito (*smartcards*) | Pagamentos eletrônicos, autenticação segura. | JavaCard, SOs proprietários |

---

## 🎯 RESUMO FINAL & RECAPITULAÇÃO DAS PÁGINAS 5 A 13

* **Evolução Histórica:** Passou de sistemas sem SO programados por painéis de fios (válvulas) para os sistemas em lote (*batch* - transistores), evoluindo para a multiprogramação e compartilhamento de tempo (CIs), consolidando-se nos computadores pessoais (LSI) e explodindo nos dispositivos móveis (VLSI).
* **Fundamentos de Hardware:** O SO precisa entender o funcionamento de CPUs (registradores, pipelines, modos núcleo/usuário), memórias (hierarquia RAM/Cache/Disco), controladores de E/S e arquiteturas de barramento (PCIe, SATA, USB).
* **Aplicações Práticas:** A escolha da arquitetura do SO depende diretamente das limitações de hardware e dos requisitos do ambiente — desde um sistema de *Smartcard* baseado em Java de recursos mínimos até mainframes capazes de processar milhões de transações por segundo.

---
*Documento gerado com base no conteúdo das páginas 5 a 13 da obra **Sistemas Operacionais Modernos (4ª Edição)** de Andrew S. Tanenbaum & Herbert Bos.*
"""

# Executa o salvamento e conversão em HTML/PDF
os.makedirs('/tmp/md_output', exist_ok=True)
md_file_path = '/tmp/md_output/sistemas_operacionais_p5_13.md'

with open(md_file_path, 'w', encoding='utf-8') as f:
    f.write(md_content)

print(f"Markdown gerado com sucesso em: {md_file_path}")
print(f"Total de linhas geradas: {len(md_content.splitlines())}")
