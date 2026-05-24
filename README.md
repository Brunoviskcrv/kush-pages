# kush-pages

Hosting público de apresentações HTML geradas pelo [Kush-Dev](https://github.com/Brunoviskcrv/Kush-Dev).

Os repositórios dos projetos apresentados aqui permanecem privados. Este repo serve apenas como *static page host* via GitHub Pages — só HTML, CSS e JS estáticos.

## Como funciona

A cada execução de `/apresentar` no bot Telegram, o pipeline:

1. Lê o repositório do projeto (privado)
2. Extrai metadados estruturados via IA
3. Renderiza um HTML auto-contido
4. Sobe aqui no branch `gh-pages` em `<slug>/v<N>.html`

Cada projeto ocupa uma subpasta. Cada execução cria uma nova versão snapshot.

## Estrutura

```
<slug-projeto>/
  v1.html              ← snapshot da fase 1
  v1-leigo.html        ← mesma fase, tom para leigo iniciante
  v2.html              ← snapshot da fase 2
  ...
  index.html           ← alias estável (sempre aponta pra última versão)
  mindmap.html         ← mapa mental fullscreen, atualizado a cada execução
```

## URLs

`https://brunoviskcrv.github.io/kush-pages/<slug>/<arquivo>.html`
