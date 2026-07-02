# ExplAInerCodigo

# 🚀 ExplAIner - Backend

Instruções para configuração do ambiente virtual e execução da API Flask.

## 🛠️ Pré-requisitos

Antes de começar, certifique-se de ter instalado em sua máquina:
* **Python 3.x**
* **Git** (opcional)

---

## 💻 Passo a Passo para Rodar o Projeto

Siga os comandos abaixo no seu terminal (Prompt de Comando ou PowerShell):

### 1. Acessar a pasta do backend
```bash
cd backend
```

### 2. Criar o Ambiente Virtual (.venv)
Cria um ambiente isolado para evitar conflitos de bibliotecas globais:
```bash
python -m venv .venv
```

### 3. Ativar o Ambiente Virtual
* **No Windows (PowerShell):**
  ```powershell
  .\.venv\Scripts\activate
  ```
* **No Windows (Prompt de Comando - CMD):**
  ```cmd
  .\.venv\Scripts\activate.bat
  ```

### 4. Configurar as Variáveis de Ambiente
Crie o arquivo `.env` copiando as configurações de exemplo:
```bash
cp .env.example .env
```
*(Se o comando `cp` não funcionar no CMD do Windows, use: `copy .env.example .env`)*

### 5. Instalar as Dependências
Para evitar erros de scripts corrompidos (`Fatal error in launcher`), instale as dependências chamando diretamente o executável do Python do ambiente:

```powershell
# Instalar pacotes do arquivo de requerimentos
.\.venv\Scripts\python.exe -m pip install -r requirements.txt

# Garantir a instalação dos pacotes principais e drivers de banco
.\.venv\Scripts\python.exe -m pip install flask flask-sqlalchemy pymysql
```

### 6. Executar a Aplicação
Inicie o servidor Flask utilizando o Python do ambiente virtual:
```bash
.\.venv\Scripts\python.exe app.py
```

---

## 🐛 Resolução de Problemas Comuns

### Erro: "Fatal error in launcher: Unable to create process..."
Esse erro ocorre no Windows quando a pasta do projeto é movida de lugar ou sincronizada no OneDrive. 
* **Solução:** Nunca use o comando `pip install` diretamente se o erro persistir. Use sempre o prefixo `.\.venv\Scripts\python.exe -m pip install <pacote>`.

