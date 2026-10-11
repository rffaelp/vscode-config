# Guia de Instalação das Minhas Configurações do VS Code

Este repositório contém o backup automatizado das minhas configurações do **Visual Studio Code** (`settings.json`, `keybindings.json`, `snippets/`) e a lista das minhas extensões (`extensions.txt`).

Siga o passo a passo abaixo para restaurar todo o ambiente de desenvolvimento em uma nova máquina com Windows.

---

## Pré-requisitos

Antes de executar os comandos, garanta que a nova máquina possui instalados:

- [Visual Studio Code](https://code.visualstudio.com/)
- [Git para Windows](https://git-scm.com/)

---

## 🛠️ Passo a Passo de Instalação

### Passo 1: Clonar as Configurações na Pasta do VS Code

Abra o **PowerShell** no Windows e execute os dois comandos abaixo:

```powershell
# 1. Navega até a pasta oficial de configurações do usuário no Windows
cd $env:APPDATA\Code\User

# 2. Clona o repositório diretamente dentro da pasta atual
git clone [https://github.com/rffaelp/vscode-config.git](https://github.com/rffaelp/vscode-config.git) .
```

### Passo 2: Instalar todas as extensões automaticamente

```powershell
# Lê o arquivo extensions.txt e instala cada extensão automaticamente no VS Code
Get-Content extensions.txt | ForEach-Object { code --install-extension $_ }
```
