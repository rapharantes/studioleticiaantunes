# Subir a LP no Hostinger — Letícia Antunes Studio

Domínio: **leticiaantunesstudio.com.br** (sem www)
Pacote: `leticia-antunes-studio-hostinger.zip` — 44 arquivos, 3,3 MB

---

## 1. Domínio

No hPanel, em **Domínios → Meus domínios**, confirme se `leticiaantunesstudio.com.br` já está apontando para a hospedagem.

Se o domínio foi registrado fora da Hostinger (Registro.br, por exemplo), troque os DNS no painel do registrador para os nameservers que a Hostinger mostra em **Hospedagem → Detalhes do plano**:

```
ns1.dns-parking.com
ns2.dns-parking.com
```

Propagação leva de 15 minutos a algumas horas. O site só responde depois disso.

## 2. Limpar o public_html

**Arquivos → Gerenciador de arquivos → public_html**

Se o Hostinger criou uma página de "em construção" ou instalou WordPress, apague tudo que estiver dentro de `public_html` antes de subir. A pasta precisa ficar vazia.

Ative o **"Mostrar arquivos ocultos"** no menu de configurações do gerenciador — sem isso o `.htaccess` fica invisível e você não confere se subiu.

## 3. Subir os arquivos

Com o `public_html` aberto:

1. Botão **Upload** → envie o `leticia-antunes-studio-hostinger.zip`
2. Clique com o botão direito no zip → **Extrair**
3. Confirme que ficou assim, com o `index.html` na raiz (não dentro de uma subpasta):

```
public_html/
├── .htaccess
├── 404.html
├── index.html
├── robots.txt
├── sitemap.xml
├── site.webmanifest
└── assets/
    ├── (32 imagens, ícones e o vídeo do hero)
    └── fonts/  (4 arquivos .woff2)
```

4. Apague o zip do servidor

Se preferir FTP: mesma estrutura, host/usuário/senha em **Arquivos → Contas FTP**. FileZilla em modo binário.

## 4. SSL

**Segurança → SSL → Instalar SSL** (gratuito, Let's Encrypt). Costuma sair em poucos minutos.

⚠️ O `.htaccess` já força HTTPS. **Se o site der `ERR_TOO_MANY_REDIRECTS` logo depois de subir**, é porque o SSL ainda não foi emitido. Abra o `.htaccess` no editor do gerenciador, coloque `#` no início destas quatro linhas, salve, espere o SSL sair e tire os `#`:

```apache
  RewriteCond %{HTTPS} !=on
  RewriteCond %{HTTP:X-Forwarded-Proto} !https
  RewriteRule ^ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
```

## 5. Conferir depois que subir

- [ ] `leticiaantunesstudio.com.br` abre com cadeado (HTTPS)
- [ ] `www.leticiaantunesstudio.com.br` redireciona para a versão sem www
- [ ] `http://` redireciona para `https://`
- [ ] O vídeo do hero toca no celular (iPhone e Android)
- [ ] Os botões de WhatsApp abrem a conversa com a mensagem já escrita
- [ ] `leticiaantunesstudio.com.br/qualquer-coisa` cai na página 404 da marca
- [ ] Colar o link no WhatsApp mostra a prévia com a foto (og-image)

Prévia de compartilhamento: se a foto não aparecer de primeira, force a releitura em [developers.facebook.com/tools/debug](https://developers.facebook.com/tools/debug/).

## 6. Depois do site no ar

**Google Search Console** — adicione a propriedade em [search.google.com/search-console](https://search.google.com/search-console/), valide pelo DNS (registro TXT) ou pelo arquivo HTML na raiz, e envie o sitemap:

```
https://leticiaantunesstudio.com.br/sitemap.xml
```

**Google Meu Negócio** — coloque o site no perfil do salão. Para busca local isso pesa mais que o site em si.

---

## Trocar uma foto depois

O `.htaccess` deixa imagem e vídeo no cache do navegador por 30 dias. Quem já visitou o site pode continuar vendo a foto antiga por até um mês se você substituir o arquivo com o mesmo nome.

Para a troca aparecer na hora: suba com nome novo (`srv-pele-2.webp`) e troque a referência no `index.html`.

## Ainda pendente da Letícia

Anotado desde o briefing, não bloqueia o site no ar:

- Horário de funcionamento (tem um comentário HTML marcando o lugar no `index.html`)
- Depoimentos/avaliações reais
- Faixa de preço
- URL do Facebook
- Fotos próprias de **estética corporal** e **cuidados de pele** — esses dois cards ainda usam imagem genérica
