# Como lançar o projeto no GitHub — passo a passo

Eu não consigo publicar no GitHub por você (não tenho acesso à sua conta). Use uma das opções abaixo.

---

## Opção A — GitHub Desktop (recomendado, sem terminal)

Não precisa usar o comando `git` no terminal.

### Passo 1 — Instalar o GitHub Desktop

1. Acesse: **https://desktop.github.com/**
2. Baixe e instale o programa.
3. Abra o **GitHub Desktop** e faça login na sua conta do GitHub (ou crie uma em github.com).

### Passo 2 — Adicionar a pasta do projeto

1. No GitHub Desktop: menu **File** → **Add local repository**.
2. Clique em **Choose...** e vá até a pasta:
   ```
   C:\Users\Pichau\Documents\Project Fin\pricing-site
   ```
   Selecione a pasta **pricing-site** e confirme.
3. Se aparecer a mensagem **"This directory does not appear to be a Git repository"**:
   - Clique no link **create a repository** (ou **Create Repository**).
   - **Name:** deixe `pricing-site`.
   - **Create Repository**.

### Passo 3 — Fazer o primeiro commit

1. Você verá a lista de arquivos à esquerda (calculadora-standalone.html, index.html, etc.).
2. Em **Summary (required)** embaixo, escreva: `Primeiro commit`.
3. Clique em **Commit to main** (botão azul).

### Passo 4 — Publicar no GitHub

1. No topo da janela, clique em **Publish repository**.
2. **Name:** `pricing-site` (ou outro nome).
3. **Description:** opcional (ex.: Calculadora de custos por kg).
4. Deixe **Keep this code private** desmarcado (repositório público).
5. Clique em **Publish Repository**.

Pronto. O projeto estará em **https://github.com/SEU_USUARIO/pricing-site**. Depois conecte esse repositório no Render.

---

## Opção B — Git no terminal (PowerShell / Git Bash)

Use só se o comando `git` já funcionar no seu terminal (depois de instalar o Git e reabrir o Cursor).

### Passo 1 — Instalar o Git

1. Baixe: **https://git-scm.com/download/win**
2. Durante a instalação, na tela **"Adjusting your PATH environment"**, escolha:
   - **Git from the command line and also from 3rd-party software**
3. Conclua a instalação.
4. **Feche o Cursor por completo** e abra de novo (para o terminal reconhecer o `git`).

### Passo 2 — Criar o repositório no site do GitHub

1. Acesse: **https://github.com/new**
2. **Repository name:** `pricing-site`
3. Deixe **Public**.
4. **Não** marque “Add a README” (o projeto já tem arquivos).
5. Clique em **Create repository**.

### Passo 3 — Abrir o terminal na pasta do projeto

1. No Cursor, abra o terminal (Terminal → New Terminal).
2. Digite e aperte Enter:
   ```powershell
   cd "C:\Users\Pichau\Documents\Project Fin\pricing-site"
   ```

### Passo 4 — Comandos (rode um por vez, apertando Enter após cada linha)

```powershell
git init
```

```powershell
git add .
```

```powershell
git commit -m "Primeiro commit: calculadora de preços"
```

```powershell
git branch -M main
```

```powershell
git remote add origin https://github.com/SEU_USUARIO/pricing-site.git
```
*(Troque **SEU_USUARIO** pelo seu usuário do GitHub.)*

```powershell
git push -u origin main
```

O navegador pode abrir para você fazer login no GitHub. Depois do `git push`, o código estará no GitHub.

---

## Depois que estiver no GitHub

1. Acesse **https://dashboard.render.com**
2. **New** → **Static Site**
3. Conecte o repositório **pricing-site**
4. **Build Command:** deixe em branco  
   **Publish Directory:** `.`
5. **Create Static Site**

Seu site ficará em uma URL como **https://pricing-site.onrender.com**.
