# 🐙 Guia Prático: Como Clonar e Commitar no GitHub

Este manual resume o fluxo essencial para baixar repositórios remotos para a sua máquina e enviar as suas alterações de volta para o GitHub.

---

## ⚙️ 1. Configuração Inicial do Git (Apenas na 1ª vez)

Antes de começar, identifique-se para que o Git registre a autoria dos seus commits:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu-email@exemplo.com"
```
Para testar se o Git está instalado corretamente, digite: git --version.

## 📥 2. Como Clonar um Repositório Remoto
Clonar serve para baixar uma cópia exata de um projeto do GitHub para a sua máquina local.

1. **Copie a URL: No GitHub, clique no botão verde <> Code e copie o endereço HTTPS (ex.: https://github.com/usuario/projeto.git).**

2. **Abra o terminal na pasta onde deseja guardar o projeto.**

3. **Execute o comando de clone:**

```bash
git clone [https://github.com/usuario/projeto.git](https://github.com/usuario/projeto.git)
```

4. **Entre na pasta baixada:**
```bash
cd projeto
```

## 🔄 3. Ciclo de Trabalho: Alterar, Commitar e Enviar (Push)
Sempre que fizer alterações no seu código (criar arquivos, editar, apagar), siga este fluxo de 3 passos:
```bash
[ Seus Arquivos Modificados ] 
             │
             ▼  git add .
[ Staging Area (Preparação) ]
             │
             ▼  git commit -m "mensagem"
[ Repositório Local (Salvo no PC) ]
             │
             ▼  git push
[ GitHub (Remoto na Nuvem) ]
```

### Passo 1: Preparar os arquivos (git add)
Adicione todos os arquivos modificados para a fila de envio:
```bash
git add .
```
### Passo 2: Registrar a versão (git commit)
Crie o ponto de restauração com uma mensagem clara sobre o que alterou:
```bash
git commit -m "Adiciona resumo da aula em markdown"
```
### Passo 3: Enviar para a nuvem (git push)
Envie os commits locais para o GitHub:
```bash
git push
```

## 💻 4. Fazendo pelo Visual Studio Code (Sem Terminal)
Se preferir usar interface gráfica:
1. **Abra a pasta do projeto no VS Code.**
2. **Acesse a aba de Controle de Código-Fonte (Ctrl + Shift + G).**
3. **Clique no ícone de + ao lado dos arquivos para prepará-los (Stage).**
4. **Escreva a mensagem de commit na caixa de texto superior e clique no botão azul Commit.**
5. **Clique em Sincronizar Alterações (Sync Changes) para enviar (push) para o GitHub.**

## 💡 Boas Práticas Rápidas⏱️

* **Commits pequenos e frequentes: Evite acumular muitas alterações em um commit só; isso facilita desfazer erros.**
* **📝 Mensagens descritivas: Prefira mensagens explicativas (ex.: "Corrige rota da API") a mensagens vagas (ex.: "ajustes" ou "teste").**
