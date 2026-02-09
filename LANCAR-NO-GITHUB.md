# Como lançar o projeto no GitHub

Siga estes passos no seu computador (no PowerShell ou no Git Bash).

---

## 1. Instalar o Git (se ainda não tiver)

- Baixe em: https://git-scm.com/download/win  
- Instale e **reabra o terminal** depois.

---

## 2. Criar o repositório no GitHub

1. Acesse https://github.com/new  
2. **Repository name:** `pricing-site` (ou outro nome)  
3. Deixe **Public**.  
4. **Não** marque “Add a README” (o projeto já tem um).  
5. Clique em **Create repository**.

---

## 3. No terminal, na pasta do projeto

Abra o PowerShell ou Git Bash, vá até a pasta do projeto e rode:

```powershell
cd "C:\Users\Pichau\Documents\Project Fin\pricing-site"
```

Depois execute, **um por vez**:

```powershell
git init
```

```powershell
git add .
```

```powershell
git commit -m "Primeiro commit: calculadora de preços + deploy Render"
```

```powershell
git branch -M main
```

```powershell
git remote add origin https://github.com/SEU_USUARIO/pricing-site.git
```

**Troque `SEU_USUARIO`** pelo seu usuário do GitHub e **`pricing-site`** pelo nome do repositório que você criou.

Por fim:

```powershell
git push -u origin main
```

O GitHub vai pedir login (ou usar o GitHub Desktop / token, se configurou). Depois do `git push`, o código estará no GitHub e você poderá conectar o repositório no Render.

---

## Resumo dos arquivos que vão subir

- `calculadora-standalone.html` – calculadora  
- `index.html` – redireciona para a calculadora  
- `render.yaml` – configuração do Render  
- `README.md` – documentação  
- `.gitignore` – arquivos ignorados pelo Git  
