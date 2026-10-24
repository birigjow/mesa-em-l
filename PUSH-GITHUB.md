# Publicar no GitHub — `birigjow/mesa-em-l`

> Este PC (Lucas) **não tem** `git`, `gh` nem credencial. O push precisa ser feito numa máquina com a conta `birigjow` autenticada.

## 1. Autenticar (uma vez)

```powershell
gh auth login --hostname github.com --git-protocol https --web
```

Se não tiver `gh`/`git`:

```powershell
winget install --id Git.Git -e --source winget
winget install --id GitHub.cli -e --source winget
```

O login abre o navegador; o código é de uso único e não deve ir para o Drive/chat.

## 2. Criar o repositório e subir a pasta `site/`

```powershell
cd C:\Users\lucas\workspace_maker\moveis\site
git init
git add .
git commit -m "mesa-em-l: site publico do cliente (3D, medidas, furos, orcamento)"
git branch -M main
gh repo create birigjow/mesa-em-l --public --source=. --remote=origin --push
```

Se o repo já existir:

```powershell
git remote add origin https://github.com/birigjow/mesa-em-l.git
git push -u origin main
```

## 3. Ligar o GitHub Pages

Pelo site: **Settings → Pages → Deploy from a branch → main / (root) → Save**.

Ou pela CLI:

```powershell
gh api -X POST repos/birigjow/mesa-em-l/pages -f "source[branch]=main" -f "source[path]=/"
```

Aguarde o deploy e abra:

`https://birigjow.github.io/mesa-em-l/`

## 4. Conferir

- Abrir no celular (390 px) e no desktop (1440 px).
- 3D, medidas, furos, acabamento e orçamento.
- O botão “Orçamento” rola até o valor.
- “Ver tudo”/“Sair” não aparecem no modo público.
- Copiar o link do cliente pelo configurador (botão **Copiar link do cliente**).

## 5. Se mudar o nome do repositório

Troque `PUBLIC_BASE` no `mesa-em-l-ferro.html` e as URLs `og:url`/`og:image` no `<head>` e no `index.html`. O padrão está em `30-produtos/marcenaria/PADRAO-APRESENTACAO-CLIENTE.md`.
