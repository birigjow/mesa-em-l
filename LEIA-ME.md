# Site público — Mesa em L (CaosTF)

> Este é o link que vai para o cliente. Ele abre no celular e no computador.
> **Não coloque custo interno, margem ou segredo aqui.** O site é público.

## Link curto

`https://birigjow.github.io/mesa-em-l/`

O `index.html` redireciona para `mesa-em-l-ferro.html?modo=cliente&publico=1` e mantém os parâmetros (`cliente`, `projeto`, medidas, acabamento, furos).

Link com um cliente específico (exemplo):

`https://birigjow.github.io/mesa-em-l/?cliente=Ageu&projeto=Mesa+em+L+%E2%80%94+escrit%C3%B3rio`

O botão **Copiar link do cliente** no configurador gera esse link automaticamente, com as medidas/furos/acabamento atuais.

## Arquivos

- `index.html` — redireciona para o modo cliente público
- `mesa-em-l-ferro.html` — configurador (3D, medidas, furos, acabamento, orçamento)
- `logo.jpg` — favicon e imagem de marca
- `og-mesa-em-l.jpg` — cartão de prévia (WhatsApp/redes)
- `mesa-em-l-ferro.pdf` — PDF de 8 páginas (opcional; link direto)

## Como publicar (GitHub Pages)

1. Repositório: `https://github.com/birigjow/mesa-em-l` (público).
2. Suba o conteúdo desta pasta na raiz do repositório (branch `main`).
3. Settings → Pages → Deploy from a branch → `main` / `(root)` → Save.
4. Aguarde o deploy e abra `https://birigjow.github.io/mesa-em-l/`.

**Publicado em 23/10/2026:** repo `https://github.com/birigjow/mesa-em-l` (commit `e2634b1`) e Pages ativo em `https://birigjow.github.io/mesa-em-l/`. Para atualizar, use `git`/`gh` autenticado como `birigjow` (ver `PUSH-GITHUB.md`).

## Como atualizar

- Substitua `mesa-em-l-ferro.html` pelo novo build.
- Rode os testes em 390 px e 1440 px: 3D, furos, orçamento, sem overflow.
- Se o nome do repositório mudar, troque `PUBLIC_BASE` no HTML e as URLs `og:image`/`og:url`.

## Cuidado

O HTML é o mesmo build do dono; o modo público esconde as ferramentas internas, mas o código-fonte ainda contém o build completo. Se o custo interno for sigiloso, o próximo passo é gerar um build só-cliente (sem tabela de custo) antes de publicar. Hoje a interface esconde; o fonte não.
