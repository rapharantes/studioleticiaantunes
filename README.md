# Letícia Antunes Studio

Landing page do Letícia Antunes Studio — salão de beleza completo na Rua Guarujá, 19, Nova Suíça, Belo Horizonte.

## O que tem aqui

Uma página só, em HTML, CSS e JavaScript puros. Sem build, sem framework, sem dependência externa: as fontes ficam em `assets/fonts` e não há nenhuma chamada a servidor de terceiros. Para ver o site, abra `index.html` no navegador.

```
index.html          a página inteira, com o CSS e o JS embutidos
assets/             vídeo, fotos, logotipos e fontes
assets/fonts/       Marcellus e DM Sans em woff2
```

## Publicar

O site é estático, então dá para servir direto do GitHub Pages: em Settings → Pages, escolha a branch `main` e a pasta `/ (root)`.

## Editar

**Mensagem do WhatsApp.** Cada botão leva para `wa.me/5531996471477` com um texto pré-escrito depois de `?text=`. As mensagens são diferentes por seção, o que ajuda a saber de onde veio o contato. Espaço vira `%20` e acento precisa ir codificado: `Olá!` vira `Ol%C3%A1%21`.

**Horário de funcionamento.** Ainda não foi definido. Tem um comentário na seção de contato marcando onde entra, e o mesmo dado precisa ir para o `openingHours` do JSON-LD no fim do arquivo.

**Fotos.** Ficam em `assets/`, em WebP. Cards de serviço são 4:3 (760x570), fotos verticais são 3:4 (900x1200) e a faixa "Feito aqui" é quadrada (620x620). Mantenha as proporções ao trocar.

## Pendências

- Horário de funcionamento
- Depoimentos ou avaliações reais, se a cliente quiser exibir
- Fotos próprias de estética corporal e de cuidados de pele (esses dois cards são os únicos com imagem genérica)
- Domínio definitivo, hoje marcado como `leticiaantunesstudio.com.br` no canonical e no og:url
- URL da página do Facebook

## Contato do estúdio

WhatsApp (31) 99647-1477 · leticiaantunesstudio@gmail.com · [@leticiaantunesstudio](https://www.instagram.com/leticiaantunesstudio/)
