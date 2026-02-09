# Calculadora de Preços — Pequenos Empreendedores

Calculadora simples para definir o preço de venda por unidade, considerando custo do produto, embalagem e custos operacionais do mês (salários, água, luz, aluguel, reparos, embalagens, telefone, seguros, marketing, etc.), com rateio por quantidade de itens vendidos e margem de lucro desejada. Frete não entra no cálculo (pago pelo cliente).

## Como usar

1. Abra o arquivo **`calculadora-standalone.html`** no navegador (duplo clique ou arraste para o Chrome/Edge/Firefox).
2. Preencha o custo do produto por unidade e a embalagem por unidade.
3. Informe os custos operacionais do mês (salários, água, luz, aluguel, etc.).
4. Digite a quantidade de itens que você vende no mês (total de todos os produtos) para o rateio.
5. Escolha a margem de lucro desejada.
6. O preço de venda sugerido aparece automaticamente.

Não é necessário instalar nada nem rodar servidor.

## Lançar no GitHub

Antes do deploy no Render, envie o projeto para o GitHub. **Passo a passo completo:** **[COMO-LANCAR-NO-GITHUB.md](COMO-LANCAR-NO-GITHUB.md)** (Opção A = GitHub Desktop, Opção B = terminal).

## Deploy no Render

Para publicar o site no [Render](https://render.com) (gratuito para sites estáticos):

1. **Repositório no GitHub** já criado e com o código enviado (veja acima).
2. Acesse [dashboard.render.com](https://dashboard.render.com) e faça login.
3. Clique em **New** → **Static Site**.
4. Conecte o repositório (GitHub/GitLab/Bitbucket) e selecione este repositório.
5. Configure:
   - **Name:** `calculadora-pricing` (ou outro nome).
   - **Branch:** `main` (ou a branch que você usa).
   - **Build Command:** deixe em branco.
   - **Publish Directory:** `.` (ponto = raiz do repositório).
6. Clique em **Create Static Site**.

O Render vai gerar uma URL como `https://calculadora-pricing.onrender.com`. A raiz do site redireciona para a calculadora.

Se o repositório tiver um arquivo **`render.yaml`** na raiz, você pode usar **New** → **Blueprint** e conectar o repositório; o Render aplica a configuração automaticamente.

## Licença

MIT.
