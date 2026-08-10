import re

pdf_source = """
[source: 1]ANDREW S.
TANENBAUM
HERBERT
BOS
SISTEMAS
OPERACIONAIS
MODERNOS
4ª EDIÇÃO
Thread
Cliente
mogro
Fat
32
Transbordamento
de buffer
Região
crítica
Sistemas
operacionais
móveis
Problema do
confinamento
Remoção
de paginas Interface de troca Windows 8
de mensagem
Segurança
(10)
Balanceamento
de cargo
Caractere
de escape
Espiando
Intruso
Jantar dos filósofos
Servidor
Algoritmo
do avestruz
Fila de execução
Bit-sujo
Cavalo de Troia
Grande trava
de núcleo
Corrida
Interrupção
Entrada
Escalonamento
de processadores
Virtualização
Nuvem
Pipe
Recusa
de serviço
Farejador
de pacotes
Interferências
Pearson
SISTEMAS
OPERACIONAIS
MODERNOS
4ª EDIÇÃO
Pearson Education
EMPRESA CIDADÃ
TANENBAUM_BOOK.indb 2 20/01/16 14:28 SISTEMAS
OPERACIONAIS
MODERNOS
ANDREW S. TANENBAUM
HERBERT BOS
Vrije Universiteit
Amsterda, Países Baixos
4ª EDIÇÃO
Tradutores:
Daniel Vieira e Jorge Ritter
Revisão técnica:
Prof. Dr. Raphael Y. de Camargo
Centro de Matemática, Computação e Cognição -
Universidade Federal do ABC
PEARSON
abdr
Respeite o direito autoral
BRASILEMA
DE CEREITOS
HERBOOBARCO
 2016 by Pearson Education do Brasil Lida.
Copyright  2015, 2008 by Pearson, Inc.
Todos os direitos reservados. Nerihuma parte desta publicação poderá ser reproduzida ou
transmitida de qualquer modo ou por qualquer outro meio, eletrônico ou mecânico, incluindo
fotocópia, gravação ou qualquer outro tipo de sistema de armazenatnento e transmissão de
informação, sem prévia autorização, por escrito, da Pearson Education do Brasil,
GERENTE EDITORIAL
 | Thiago Anacleto

SUPERVISORA DE PRODUÇÃO EDITORIAL
 | Silvana Afonso

COORDENADOR DE PRODUÇÃO EDITORIAL
 | Jean Xavier

EDITOR DE AQUISIÇÕES
 | Vinícius Souza

EDITORA DE TEXTO
 | Sabrina Levensteinas

EDITORES ASSISTENTES
 | Marcos Guimarães e Karina Ono

PREPARAÇÃO
 | Christiane Gradvoll Colas

REVISÃO
 | Maria Aiko

CAPA
 | Solange Rennó

PROJETO GRÁFICO E DIAGRAMAÇÃO
 | Casa de Ideias

Dados Internacionais de Catalogação na Publicação (CIP)
(Câmara Brasileira do Livro, SP, Brasil)
Tanenbaum, Andrew S.
Sistemas operacionais modernos/Andrew S. Tanenbaum, Herbert
Bos; tradução Jorge Ritter, revisão técnica Raphael Y. de Camargo. -
4, ed. São Paulo: Pearson Education do Brasil, 2016.
Titulo original: Modern operating systems. Bibliografia.
ISBN 978-85-4301-818-8
1. Sistemas operacionais (Computadores) 1. Bos, Herbert. II. Titulo.
15-10681
Indice para catálogo sistemático:
1. Sistemas operacionais: Computadores:
Processamento de dados 005.43
CDD-005.43
2016
Direitos exclusivos para a língua portuguesa cedidos à
Pearson Education do Brasil Ltda.,
uma empresa do grupo Pearson Education
Avenida Santa Marina, 1193
CEP 05036-001 - São Paulo - SP - Brasil
Fone: 11 3821-3542
vendas@pearson.com
A Suzanne, Barbara, Daniel, Aron, Nathan, Marvin, Matilde e Olivia. A lista continua crescendo. (AST)
A Marieke, Duko, Jip e Spot. Incrivel Jedi, todos. (HB)
TANENBAUM_BOOK.indb 6 20/01/16 14:28 SUMÁRIO
Prefácio
XV
 | 1.4.2
 | Sistemas operacionais de servidores
 | 25

 | 1.4.3
1.4.4
 | Sistemas operacionais de
multiprocessadores
Sistemas operacionais de computadores
pessoais
 | 25
25

 | 1.4.5
 | Sistemas operacionais de computadores
 | 
 |  | portáteis.
 | 25

 | 1.4.6
 | Sistemas operacionais embarcados.
 | 26

 | 1.4.7
 | Sistemas operacionais de nós
sensores (sensor-node).
 | 26

 | 1.4.8
 | Sistemas operacionais de tempo real
 | 26

 | 1.4.9
 | Sistemas operacionais de cartões
 | 
 |  | inteligentes (smartcard)
 | 27

 | 1.5
 | Conceitos de sistemas operacionais.......
 | 27

 | 1.5.1
 | Processos..
 | 27

 | 1.5.2
 | Espaços de endereçamento.
 | 28

 | 1.5.3
 | Arquivos.
 | 29

 | 1.5.4
 | Entrada/Saída
 | 31

 | 1.5.5
 | Proteção.
 | 31

 | 1.5.6
 | O interpretador de comandos (shell).
 | 32

 | 1.5.7
 | A ontogenia recapitula a filogenia
 | 32

 | 1.6
 | Chamadas de sistema
 | 35

 | 1.6.1
 | Chamadas de sistema para
 | 
 | 1.6.2
 | gerenciamento de processos.
Chamadas de sistema para
 | 37

 | 1.6.3
 | gerenciamento de arquivos.
Chamadas de sistema para
gerenciamento de diretórios.
 | 39
40

 | 1.6.4
 | Chamadas de sistema diversas
 | 41

 | 1.6.5
 | A API Win32 do Windows
 | 42

1
 | Introdução...
1

1.1
 | O que é um sistema operacional?
3

1.1.1
 | O sistema operacional como uma máquina
estendida..
3

1.1.2
 | O sistema operacional como um gerenciador

 | de recursos..
4

1.2
 | História dos sistemas operacionais.
5

1.2.1
 | A primeira geração (1945-1955): válvulas.... 5

1.2.2
 | A segunda geração (1955-1965): transistores
e sistemas em lote (batch)
5

1.2.3
 | A terceira geração (1965-1980): CIs e
multiprogramação
7

1.2.4
 | A quarta geração (1980-presente):

 | computadores pessoais.
10

1.2.5
 | A quinta geração (1990-presente):
computadores móveis.
13

1.3
1.3.1
1.3.2
1.3.3
1.3.4
1.3.5
1.3.6
1.4
 | Revisão sobre hardware de
computadores
14
15
Processadores
17
Memória
Discos
19
Dispositivos de E/S
20
22
Barramentos
Inicializando o computador.
24
O zoológico dos sistemas operacionais..24
"""

# Let's generate a full Markdown file with 500+ lines covering the requested elements based on pages 5-13 of the PDF (History of OS, Hardware Review, OS Zoo).
# The user specified:
# - pages 5 to 13 (History of OS 1.2, Hardware Review 1.3, OS Zoo 1.4)
# - emojis, gifs, Text, Lists, Links, Images, Tables, Checklists, Quotes, Mermaid Diagrams, Advanced Media, Advanced Tables, Extra Diagrams, Alert Blocks, Folder Structure
# - minimum 500 lines

md_content = """# 📚 Estudo de Sistemas Operacionais Modernos (Páginas 5 a 13)
> **Baseado na obra:** *Sistemas Operacionais Modernos (4ª Edição)* — Andrew S. Tanenbaum & Herbert Bos 📖

---

## 📋 Sumário Interativo
- [📜 1. História dos Sistemas Operacionais](#-1-história-dos-sistemas-operacionais)
  - [⚡ 1.2.1 A Primeira Geração (1945-1955): Válvulas](#-121-a-primeira-geração-1945-1955-válvulas)
  - [📠 1.2.2 A Segunda Geração (1955-1965): Transistores e Sistemas em Lote](#-122-a-segunda-geração-1955-1965-transistores-e-sistemas-em-lote)
  - [🔲 1.2.3 A Terceira Geração (1965-1980): CIs e Multiprogramação](#-123-a-terceira-geração-1965-1980-cis-e-multiprogramação)
  - [💻 1.2.4 A Quarta Geração (1980-Presente): Computadores Pessoais](#-124-a-quarta-geração-1980-presente-computadores-pessoais)
  - [📱 1.2.5 A Quinta Geração (1990-Presente): Computadores Móveis](#-125-a-quinta-geração-1990-presente-computadores-móveis)
- [🖥️ 2. Revisão sobre Hardware de Computadores](#-2-revisão-sobre-hardware-de-computadores)
  - [⚙️ 1.3.1 Processadores (CPUs, Pipelines, Multicore)](#-131-processadores)
  - [🧠 1.3.2 Memória e Hierarquia](#-132-memória)
  - [💽 1.3.3 Discos e Armazenamento](#-133-discos)
  - [🔌 1.3.4 Dispositivos de Entrada/Saída (E/S)](#-134-dispositivos-de-entradasaída)
  - [🚌 1.3.5 Barramentos](#-135-barramentos)
  - [🚀 1.3.6 Inicializando o Computador (Boot)](#-136-inicializando-o-computador)
- [🦁 3. O Zoológico dos Sistemas Operacionais](#-3-o-zoológico-dos-sistemas-operacionais)
- [📂 4. Estrutura do Projeto de Estudo](#-4-estrutura-do-projeto-de-estudo)
- [✅ 5. Checklist de Aprendizado](#-5-checklist-de-aprendizado)

---

## 📂 4. Estrutura do Projeto de Estudo

```text
meu-projeto-so/
├── 📁 docs/
│   ├── 📄 historia_so.md
│   ├── 📄 hardware_review.md
│   └── 📄 zoologico_so.md
├── 📁 diagramas/
│   ├── 📊 geracoes_so.mermaid
│   ├── 📊 hierarquia_memoria.mermaid
│   └── 📊 fluxo_boot.mermaid
├── 📁 midia/
│   ├── 🖼️ arquitetura_hardware.png
│   └── 🎞️ batch_system.gif
├── 📁 exemplos_c/
│   ├── 📜 sys_call_demo.c
│   └── 📜 registers.h
└── 📄 README.md
