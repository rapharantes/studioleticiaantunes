# Letícia Antunes Studio

Landing page do Letícia Antunes Studio — salão de beleza completo na Rua Guarujá, 19, Nova Suíça, Belo Horizonte.

## O que tem aqui

Uma página só, em HTML, CSS e JavaScript puros. Sem build, sem framework, sem dependência externa: as fontes ficam em `assets/fonts` e não há nenhuma chamada a servidor de terceiros. Para ver o site, abra `index.html` no navegador.

```
index.html          a página inteira, com o CSS e o JS embutidos
site.webmanifest     ícone e nome para "adicionar à tela inicial"
robots.txt           libera indexação e aponta o sitemap
sitemap.xml          mapa do site para os buscadores
assets/              vídeo, fotos, logotipos, favicon e fontes
assets/fonts/        Marcellus e DM Sans em woff2
```

## Publicar

O site é estático, então dá para servir direto do GitHub Pages: em Settings → Pages, escolha a branch `main` e a pasta `/ (root)`.

## Editar

**Mensagem do WhatsApp.** Cada botão leva para `wa.me/5531996471477` com um texto pré-escrito depois de `?text=`. As mensagens são diferentes por seção, o que ajuda a saber de onde veio o contato. Espaço vira `%20` e acento precisa ir codificado: `Olá!` vira `Ol%C3%A1%21`.

**Botão flutuante.** É o único elemento fora da paleta grafite/dourado, de propósito — verde do WhatsApp, para ser reconhecido na hora. Não é o `#25D366` puro: nesse tom o ícone branco tem contraste de 1.98:1 contra o fundo, abaixo do mínimo de 3:1 que a WCAG pede para ícone de interface. Usei `#28854E`, mesma matiz mais escura, contraste 4.6:1, ainda lido como "o botão do WhatsApp".

**Horário de funcionamento.** Ainda não foi definido. Tem um comentário na seção de contato marcando onde entra, e o mesmo dado precisa ir para o `openingHoursSpecification` do JSON-LD no fim do arquivo.

**Fotos.** Ficam em `assets/`, em WebP. Cards de serviço são 4:3 (760×570), fotos verticais são 3:4 (900×1200) e a faixa "Feito aqui" é quadrada (620×620). Mantenha as proporções ao trocar.

**Domínio.** `canonical`, `og:url`, `og:image`, `twitter:image` e a `url` do JSON-LD usam `https://leticiaantunesstudio.com.br/` como placeholder. Quando o domínio definitivo estiver decidido, essas 5 URLs (mais o `robots.txt` e o `sitemap.xml`) precisam ser atualizadas juntas.

**Prévia ao compartilhar o link.** A imagem que aparece quando o link é enviado no WhatsApp/Instagram/Facebook é `assets/og-image.jpg`, montada a partir da "Logo perfil". O favicon (aba do navegador, atalho no celular) usa o monograma dourado da pasta do projeto, em `assets/favicon.ico` e nos tamanhos do `site.webmanifest`. Redes sociais cacheiam a prévia por conta própria: se trocar a imagem depois de o link já ter circulado, pode levar um tempo para atualizar em quem já viu.

## Pendências

- Horário de funcionamento
- Depoimentos ou avaliações reais, se a cliente quiser exibir
- Fotos próprias de estética corporal e de cuidados de pele (esses dois cards são os únicos com imagem genérica)
- Domínio definitivo (ver seção "Domínio" acima)
- URL real da página do Facebook — o link antigo foi removido do rodapé e do JSON-LD por não ter sido confirmado pelo estúdio (o briefing só tinha o nome da página, não o endereço)
- Coordenadas de GPS exatas do endereço — não incluídas para não arriscar apontar o pino errado; hoje o mapa (`hasMap` no JSON-LD e o link de contato na página) resolve pelo endereço em texto, que o Google geocodifica com precisão sozinho

## Contato do estúdio

WhatsApp (31) 99647-1477 · leticiaantunesstudio@gmail.com · [@leticiaantunesstudio](https://www.instagram.com/leticiaantunesstudio/)
