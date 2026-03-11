# 🚌 Excel BR — Controle de Atualização de Frota

Sistema web para controle e registro das atualizações do sistema de abastecimento **Excel BR** instalado na frota de ônibus da **Rápido D'Oeste / Ribe Transporte**.

Hospedado via **GitHub Pages**. Os dados são salvos diretamente neste repositório no arquivo `dados.json`, usando a GitHub API — sem banco de dados externo.

---

## 📋 Funcionalidades

- Cadastro de atualizações por prefixo de frota
- Registro de odômetro do painel e do tacógrafo
- Suporte a tacógrafo **digital** e **analógico** (com Constante K e validade)
- Número RAVO e status do sistema (OK / Sem leitura / KM trava)
- Data e hora de atualização gerada automaticamente
- Consulta com filtros por prefixo, status, tipo e período de data
- Edição e exclusão de registros com salvamento direto no GitHub
- Exportação para planilha `.xlsx`
- **Dados salvos no próprio repositório** via GitHub API (`dados.json`)

---

## 🚀 Como configurar

### 1. Criar o Personal Access Token (PAT)

1. Acesse seu GitHub → **Settings → Developer settings → Personal access tokens → Tokens (classic)**
2. Clique em **Generate new token (classic)**
3. Dê um nome, selecione a permissão **`repo`** (acesso completo)
4. Clique em **Generate token** e **copie o token** — ele aparece apenas uma vez

### 2. Criar o arquivo de dados no repositório

Crie um arquivo chamado **`dados.json`** na raiz do repositório com o conteúdo:

```json
[]
```

### 3. Configurar o sistema

1. Acesse a página no GitHub Pages
2. Clique em **"Configurar GitHub"** na faixa superior
3. Preencha:
   - **Usuário GitHub** — seu nome de usuário
   - **Nome do Repositório** — nome exato do repositório
   - **Personal Access Token** — o token gerado no passo 1
4. Clique em **Conectar**

As credenciais ficam salvas no navegador — configure uma vez por dispositivo.

### 4. Publicar no GitHub Pages

1. No repositório, vá em **Settings → Pages**
2. Em **Source**, selecione a branch `main` e pasta `/ (root)`
3. Clique em **Save**
4. Acesse em: `https://<usuario>.github.io/<repositorio>/`

---

## 🗂 Estrutura do Repositório

```
/
├── index.html     # Sistema principal
├── dados.json     # Banco de dados (conteúdo inicial: [])
├── README.md      # Este arquivo
├── LICENSE        # Licença de uso
└── .gitignore     # Arquivos ignorados pelo Git
```

---

## ⚠️ Observações

- O **Personal Access Token** fica salvo apenas no navegador local, nunca no repositório
- O `dados.json` é atualizado automaticamente a cada cadastro, edição ou exclusão
- Cada dispositivo precisa ser configurado uma vez com o token
- Mantenha o token seguro

---

## 🛠 Tecnologias

| Tecnologia | Uso |
|---|---|
| HTML / CSS / JavaScript | Interface do sistema |
| GitHub API (REST) | Leitura e escrita no `dados.json` |
| GitHub Pages | Hospedagem gratuita |
| [SheetJS](https://sheetjs.com) | Exportação para Excel |
| [Google Fonts](https://fonts.google.com) | Tipografia |

---

## 📄 Licença

MIT — consulte o arquivo [LICENSE](LICENSE).

> Desenvolvido para uso interno — Rápido D'Oeste / Ribe Transporte
