# Convite Kroner

Site-convite do **Internacional Circo Kroner** para influenciadores. Uma página só,
guiada por scroll: um vídeo de 15 segundos avança conforme o visitante rola e retrocede
quando ele sobe, com o texto do convite entrando por cima. No fim, a conversa vai para
o WhatsApp da produção.

## Como ver

O site é HTML, CSS e JavaScript puros. Sem build, sem dependências, sem servidor.

Dois cliques em `site/index.html` mostram o hero de imagem estática, que é a versão
que celulares com movimento reduzido recebem. Navegadores bloqueiam `fetch` em
endereços `file://`, então o vídeo não carrega por esse caminho, e isso é proposital.

Para ver a jornada completa, sirva a pasta:

```
npx http-server site -p 8899 -c-1
```

Depois abra `http://localhost:8899` num navegador de verdade.

> Se o scroll não animar, verifique se as animações do sistema estão ligadas. Com
> "reduzir movimento" ativo, o site entrega de propósito uma versão parada.

## Estrutura

```
site/
  index.html              a página inteira, com o CSS e o JS embutidos
  assets/
    hero-scrub.mp4        16:9, 1280x720, para desktop
    hero-scrub-mobile.mp4 9:16, 608x1080, corte vertical acompanhando cada artista
    hero-poster*.jpg      primeiro quadro de cada montagem
    hero-ending*.jpg      quadro final, usado no hero estático e no parallax
PACOTE-DE-DESIGN.md       todas as decisões criativas e o que foi verificado
IDENTIDADE-E-COPY.md      identidade visual do Kroner e a copy original
```

## Como funciona o hero

O vídeo é buscado como Blob e reproduzido por object URL, porque muitas hospedagens
não suportam download parcial e sem isso o scroll trava em qualquer posição. O
progresso do scroll comanda o tempo do vídeo por um loop `requestAnimationFrame` que
descansa quando converge. Os seeks são travados um a um para não se empilharem, e o
DOM só é tocado quando algum valor muda de verdade.

Nove faixas de texto acompanham a filmagem. As frases fortes moram nas transições, os
trechos em que nenhum artista está em cena. Sobre um artista, o texto sempre encosta
no lado oposto ao corpo dele.

Celular e tablet em pé recebem a montagem vertical com o texto ancorado embaixo. O hero
parado aparece só em dois casos: movimento reduzido ligado, e celular deitado, onde não
existe altura para a jornada.

## Publicar

É uma pasta de arquivos estáticos. Qualquer hospedagem serve, incluindo GitHub Pages
apontando para `site/`. Antes de publicar, troque as duas URLs marcadas com
`<!-- DEPLOY STEP -->` no `index.html` pelo endereço real do site, senão as
pré-visualizações de link saem quebradas.

## Alterar o WhatsApp

No `index.html`, procure por `WA_NUMBER` e `WA_TEXT`.
