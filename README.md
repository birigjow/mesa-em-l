# CaosTF — Ferramenta de escopo e apresentação de móveis

> Projeto piloto: **Mesa em L**. Site público: **https://birigjow.github.io/mesa-em-l/**
> Uso: Lucas, Murilo e Ygor (CaosTF). Não é open source; o código é do projeto CaosTF.

## O que é

Uma ferramenta de uma página para transformar o escopo de um móvel em uma **apresentação interativa para o cliente**, sem planilha e sem PDF pesado:

- **3D** do móvel (girar, aproximar, vista de baixo);
- **medidas** independentes (comprimento/profundidade de cada tampo, altura, lado);
- **resumo do projeto** (estrutura, pernas, base, tampos, acabamento, passagem de cabos, peso);
- **furos de cabo** que o cliente pode posicionar;
- **acabamento** em 9 cores;
- **orçamento** em 3 linhas: material, mão de obra e total;
- **condições** (sinal, cartão, prazo, validade) e o que não está incluso;
- **link do cliente** com a configuração atual.

O cliente não vê custo interno, margem, peças, plano de corte ou ferramentas de oficina.

## Link do cliente

`https://birigjow.github.io/mesa-em-l/`

O `index.html` redireciona para `mesa-em-l-ferro.html?modo=cliente&publico=1` e preserva os parâmetros (`cliente`, `projeto`, medidas, lado, acabamento, furos, peças removidas/avulsas).

No configurador, o botão **Copiar link do cliente** gera a URL com a configuração atual. O modo público esconde “Ver tudo”, “Sair” e o botão do dono.

## Estrutura

```
index.html                  redireciona para o modo cliente público
mesa-em-l-ferro.html        configurador (3D + medidas + furos + acabamento + orçamento)
mesa-em-l-ferro.pdf         PDF de 8 páginas (opcional)
logo.jpg                    favicon/marca
og-mesa-em-l.jpg            cartão 1200×630 para WhatsApp/redes
tools/make-og.py            gerador do cartão de prévia
LEIA-ME.md / PUSH-GITHUB.md manutenção e publicação
```

> Documentação interna (JORNADA, orçamento, padrão e handoff) fica no Drive CaosTF e **não** é versionada neste repo público.

## Como usar em um móvel novo

1. Copie a pasta para `PROJETOS/<novo-movel>/site/`.
2. Troque o HTML pelo build do novo móvel (mesmo contrato `?modo=cliente&publico=1` e `#orcamento-cliente`).
3. Preencha o bloco `#orcamento-cliente` com o preço fechado pelo marceneiro e auditado pelo `financeiro`.
4. Ajuste `PUBLIC_BASE`, `og:url` e `og:image` para o novo repositório.
5. Teste em **390 px** e **1440 px**: 3D, furos, orçamento, sem overflow; 0 erro de console.
6. No modo dono, preencha cliente/projeto, confira o preço e clique **Copiar link do cliente**.
7. Publique no GitHub Pages (`birigjow/<movel>`) e envie o link curto.

A documentação interna (JORNADA, orçamento, padrão e handoff) fica no Drive CaosTF; este repo público contém só o site e o README.

## Regras de ouro

- O preço vem do marceneiro + auditoria do `financeiro`; não é calculado no front.
- Mudou medida = preço **“a definir”** (“Projeto sob medida — orçamento a confirmar”). Furo e cor não mudam o preço.
- Não mostrar custo/margem/horas no modo cliente.
- Mobile é requisito: 390 px sem rolagem horizontal, botões ≥ 42 px, 3D dominante.
- Nada de segredo no repositório público. **Atenção:** o HTML público é o mesmo build do dono; o modo público esconde as ferramentas, mas o fonte contém o build completo. Se o custo interno for sigiloso, gere um build só-cliente antes de publicar.

## Publicação

- Repositório: `https://github.com/birigjow/mesa-em-l`
- Pages: `Settings → Pages → main / (root)`
- Link: `https://birigjow.github.io/mesa-em-l/`
- **Publicado em 23/10/2026** (commit `e2634b1`); o `gh` autenticado como `birigjow` está no PC do Lucas; o passo a passo de atualização está em `PUSH-GITHUB.md`.

## Créditos

Lucas (CaosTF), Murilo e Ygor. Projeto piloto: Mesa em L — 23/10/2026.
