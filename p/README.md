# Links por cliente (presets)

Cada pasta `p/<cliente>/index.html` é um **link fixo** de uma proposta: abre o configurador no modo público com as medidas, furos, acabamento e peças daquele cliente.

## Link

`https://birigjow.github.io/mesa-em-l/p/<cliente>/`

Exemplo: `https://birigjow.github.io/mesa-em-l/p/ygor/`

## Criar um novo

1. Copie `p/ygor/` para `p/<cliente>/`.
2. Troque os valores do `URLSearchParams` (l1, l2, p1, p2, h, lado, acabamento, cliente, projeto, h1e/h1y/h2e/h2y, rem).
3. Ajuste `<title>` e as metas `og:title`/`og:description`/`og:url`.
4. Teste no celular e no desktop.
5. Commit + push; o Pages publica.

O preset é um **snapshot**: se o cliente alterar as medidas na página, a URL do configurador muda, mas o link enviado continua o mesmo. Para uma nova proposta, crie outro preset.
