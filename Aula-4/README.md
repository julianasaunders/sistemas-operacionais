# 🛠️ Aula 04 — Estrutura do Sistema Operacional e Instalação do Windows

Os materiais desta pasta exploram a arquitetura interna do sistema por caminhos complementares: os componentes e modos de execução, o papel do **kernel** e o processo de formatação e instalação do **Windows**.

## 📂 Materiais disponíveis

| Arquivo | O que apresenta |
|---|---|
| [📝 resumoAula04.md](resumoAula04.md) | Componentes do SO, modos de execução, programas × processos × threads, sistema de arquivos, E/S e reuso de sistemas. |
| [🧠 o-que-e-Kernel.md](o-que-e-Kernel.md) | Explicação didática do kernel, a metáfora do restaurante, suas quatro funções e exemplos de kernels do mercado. |
| [💿 atividade01.md](atividade01.md) | Relatório técnico sobre a formatação e a instalação do Windows, ligando cada etapa aos conceitos de sistemas operacionais. |
| [🔍 atividade02.md](atividade02.md) | Pesquisa comparativa de cinco sistemas derivados: Android, macOS, Ubuntu, webOS e SteamOS. |

## 🧩 Conceitos centrais

- **Kernel:** núcleo do sistema, responsável por processos, memória, dispositivos e arquivos.
- **Modos de execução:** modo usuário (acesso restrito) e modo kernel (acesso total ao hardware), conectados pelas chamadas de sistema.
- **Programa, processo e thread:** arquivo estático, instância em execução e fluxo de execução dentro do processo.
- **Sistema de arquivos:** organização hierárquica de diretórios e arquivos.
- **Entrada e saída:** drivers que traduzem comandos genéricos para cada dispositivo.
- **Reuso de sistemas:** adoção de kernels consolidados, como Debian no Raspberry Pi OS e FreeBSD no Orbis OS.

## 📝 Atividades

A **Atividade 1** percorre pré-boot, Windows PE, particionamento, NTFS e OOBE, relacionando cada fase a kernel, processos, threads e drivers. A **Atividade 2** compara cinco sistemas derivados com suas bases e o foco de aplicação de cada um.

---

[← Aula 03](../Aula-3/README.md) · [📚 Índice da disciplina](../README.md) · [Aula 05 →](../Aula-5/README.md)
