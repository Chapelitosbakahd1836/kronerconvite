# PACOTE DE DESIGN — Convite Kroner
Uma tomada contínua de 15s · hero de 1800vh · 9 textos

## 1. A premissa da marca
**A palavra é PASSAGEM.** Um convite não é um anúncio, é uma porta. O site inteiro é a
travessia de uma porta: o leão abre a cortina, o visitante atravessa os palhaços, passa
sob o trapézio e chega no globo. Cada seção da página é um passo mais fundo para dentro
da lona. A chamada final não é "compre", é "atravesse". Se uma seção não faz o visitante
entrar mais fundo, ela não pertence à página.

## 2. O vídeo, como ficou de verdade
Uma geração única no Seedance 2.5, modo omni_reference, 15,04s, 720p, sem áudio.
Quatro imagens de referência entraram juntas, então nenhum artista foi improvisado
pelo modelo. Custo: 97,5 créditos.

**O fio que liga tudo é um facho de holofote dourado.** Ele nasce no leão, arrasta as
fitas de luz para a direita, entrega o palhaço, sobe com a câmera até a trapezista e
desce virando faísca no globo. Fundo azul-meia-noite com luzes douradas desfocadas
em toda a tomada, então os quatro leem como o mesmo lugar.

### Janelas medidas na filmagem (base do mapa de textos)
| Janela | Tempo | Progresso | O que tem na tela |
|---|---|---|---|
| Kroninho | 0,0 a 2,5s | 0,000 a 0,166 | mascote à esquerda |
| **Transição 1** | **2,5 a 4,0s** | **0,166 a 0,266** | **quadro limpo, só luz dourada** |
| Palhaço | 4,0 a 7,8s | 0,266 a 0,518 | ele à direita |
| **Transição 2** | **7,8 a 8,8s** | **0,518 a 0,585** | **câmera subindo, quase vazio** |
| Trapezista | 8,8 a 11,2s | 0,585 a 0,745 | ela ao centro, com reflexo |
| **Transição 3** | **11,2 a 12,2s** | **0,745 a 0,811** | **quadro limpo** |
| Moto e globo | 12,2 a 15,0s | 0,811 a 1,000 | salto sobre o globo |

**Regra de ouro do mapa:** as frases fortes vivem nas transições, centralizadas e
grandes. Sobre um artista, o texto sempre encosta no lado oposto ao corpo dele.
Nenhuma palavra cobre artista nenhum.

## 3. Paleta (amostrada do mundo da filmagem)
```css
:root{
  --canvas:#070B24;        /* azul-lona da noite, nunca preto puro */
  --panel:#0D1338;         /* superfícies elevadas */
  --accent:#F3C623;        /* o dourado Kroner: só o CTA e a ênfase rara */
  --accent-hover:#FFD84D;
  --accent-muted:#8B6B14;  /* bordas, brilhos, partículas em nível de sussurro */
  --ember:#D42030;         /* o vermelho do globo da morte, um momento só */
  --text-secondary:#A8B0D8;
  --text-primary:#F2EFE4;
}
```

## 4. O trio de fontes
- **Display: Bodoni Moda.** Desvio declarado: a skill avisa contra serifa de alto contraste
  em fundo quase-preto como reflexo padrão de IA. Aqui a exceção vale e é dita em voz alta —
  a didone de alto contraste É a tipografia histórica do cartaz de circo, e o logo do Kroner
  já é ouro em relevo sobre azul. É o mundo material do próprio assunto, não um reflexo.
  Ganhamos o direito amostrando os tons da filmagem e inventando a assinatura abaixo.
- **Texto: Manrope.** Quieta, moderna, some para o texto aparecer.
- **Mono: JetBrains Mono.** Rótulos pequenos, numeração de capítulo, o código do convite.

## 5. O elemento assinatura
**O trilho de lâmpadas de marquise.** Uma fileira de lâmpadas incandescentes desenhada em
SVG à mão, correndo pela borda da página. Cada lâmpada ACENDE conforme o visitante rola,
uma a uma, como a marquise de um circo ligando. No fim da jornada o trilho inteiro está
aceso. Teste de volume: sem ele a página vira um site escuro qualquer. Com ele, o visitante
está literalmente ligando as luzes do circo enquanto desce.

Segundo motivo, para a seção final: **a picotagem do ingresso.** Uma linha dourada
tracejada que separa o bloco do CTA como o canhoto de um ingresso de verdade.

## 6. Mapa de faixas: 9 textos, hero de 1800vh
Validado pelo teste de flick: cada texto fica legível por 6 a 10 flicks normais de
120px, e nenhum é pulável em flick agressivo de 360px.

| # | Intervalo | Lado | Momento | Texto (ao pé da letra) | Entrada |
|---|---|---|---|---|---|
| 1 | 0,000 a 0,078 | direita | leão à esquerda | INTERNACIONAL CIRCO KRONER · DESDE 1990 / Feche a porta. Isto é para você. | deriva para baixo |
| 2 | 0,150 a 0,262 | **centro** | **transição 1, vazio** | **VOCÊ FOI ESCOLHIDO.** / De todas as pessoas desta cidade, um punhado vai receber esta página. Você é uma delas. | metades se abrindo |
| 3 | 0,278 a 0,362 | esquerda | palhaço à direita | Não é publicidade. Não é permuta. Não é briefing. | dispersão |
| 4 | 0,378 a 0,472 | esquerda | palhaço à direita | **É um convite.** | soco de palavra |
| 5 | 0,522 a 0,604 | **centro** | **transição 2** | Sessenta artistas. Cinco países. Trinta e cinco anos de estrada. | deriva para baixo |
| 6 | 0,612 a 0,702 | direita | trapezista ao centro | **TRAPÉZIO TRIPLO** / Três corpos no ar. Nada entre a coragem e o chão. | subida palavra por palavra |
| 7 | 0,740 a 0,836 | **centro** | **transição 3, vazio** | **GLOBO DA MORTE** / Cinco motos. Uma esfera de aço. Zero margem de erro. | dispersão |
| 8 | 0,844 a 0,928 | esquerda | moto à direita | O som que você vai ouvir não passa em vídeo. | soco de palavra |
| 9 | 0,936 a 1,000 | esquerda | quadro final | **Você está dentro.** / Agora desce e fala com a produção. | subida em etapas |

## 7. O bloco do hero estático (celular e movimento reduzido)
Sobre o quadro final composto:
- **VOCÊ FOI ESCOLHIDO.**
- Um convite pessoal do Internacional Circo Kroner. Sessenta artistas, uma lona
  climatizada, e uma noite reservada para você.
- Botão: **Aceitar o convite**

## 8. Abaixo da dobra (enxugado a pedido do cliente)
O vídeo virou 87% da página. Só três seções sobraram depois dele, e não há cabeçalho
nem botão no topo, de propósito: o visitante precisa rolar até o fim para achar a
chamada.

1. **Como funciona na prática** — quatro passos, e nenhum é ficar na fila. Mata a
   objeção real encontrada na pesquisa (gente que chegou e não conseguiu entrar).
2. **Perguntas rápidas** — cinco objeções reais de influencer: se é obrigado a postar,
   se vem roteiro pronto, quantos acompanhantes, se pode gravar, e remarcação.
3. **O convite** — o canhoto de ingresso picotado, com o botão do WhatsApp e a
   mensagem já escrita.
4. **Rodapé** — Internacional Circo Kroner e o Instagram oficial.

**Saíram:** o cabeçalho fixo, o botão do topo, a seção do acordo, a galeria de
artistas, o que você recebe, e o lacre interativo. As imagens dos artistas foram
movidas para `review/imagens-fora-do-site/` e não embarcam.

**Destino do formulário:** não há formulário. A única chamada é o link do WhatsApp.

## 9. Plano da camada vetorial
- O trilho de lâmpadas SVG, acendendo por scroll (o elemento assinatura).
- A picotagem tracejada dourada do bloco de CTA.
- Poeira de picadeiro: partículas em nível de sussurro na camada de ambiente fixa.
- Um brilho de holofote lento atrás de tudo, ciclo de 60s.
- Tudo honra movimento reduzido: estados finais mostrados, motores parados.

## 10. Lista de engenharia
Busca por Blob com anel de carregamento (o vídeo de 15s passa de 8 MB), interpolação
normalizada por dt, seeks travados, escritas de DOM por delta, ritmo de faixas validado
pelo teste de flick, sistema de legibilidade de quatro camadas, os cinco portões do hero
estático com listeners de mudança, completo-sem-o-vídeo, e o padrão site-inteiro-animado.

## 11. Gate de texto
Cada linha acima embarca ao pé da letra. Zero travessões, zero palavras de estoque, mais a
varredura do corpo por sinais de IA, antes de qualquer pessoa ver a página.

---

## 12. O que foi verificado (Fase 9)

| Checagem | Resultado |
|---|---|
| Gate de texto | 0 travessões, 0 palavras de estoque, 0 sinais de IA |
| Scrub acompanha o scroll | vídeo vai de 0 a 14,44s, uma faixa acesa por vez |
| Teste de flick 120px | 6 a 10 flicks de leitura por texto (mínimo 5) |
| Teste de flick 360px | nenhum texto pulável, todos chegam a 100% |
| Contraste do pior pixel | pior faixa 5,22:1 (mínimo exigido 3,5:1) |
| Movimento reduzido ao vivo | fixa nos estados finais e re-arma nas duas direções |
| Celular 390x844 com toque | hero estático, vídeo nunca baixado |
| Vídeo bloqueado na rede | página completa, anel vira seta de scroll |
| Vazamento lateral | zero em 7 larguras de 375 a 1920 |
| Erros de console | nenhum |
| Animações de entrada | 35 de 35 disparam, 5 de 5 sequências assentam |
| Atraso escalonado aposentado | sim, 0s depois da entrada |
| Lâmpadas da marquise | 44 de 44 acendem ao longo do scroll |

## 13. Velocidade medida
Página carrega em **257ms** no desktop e **110ms** no celular. Peso sem o vídeo:
**126 KB**. O vídeo de 8,8 MB chega por streaming atrás do anel de progresso, com a
página já usável. Celular não baixa o vídeo.

## 14. Custo em créditos
| Item | Créditos |
|---|---|
| Quadro inicial do Kroninho | 2 |
| Vídeo Kling 15s (descartado) | 26,25 |
| 4 imagens de referência | 28,5 |
| Palhaço refeito pela descrição | 8,5 |
| Palhaço refeito com a foto real | 8,5 |
| 4 trechos Kling (descartados) | 28 |
| **Vídeo final Seedance 15s** | **97,5** |
| **Total** | **199,25 de 570** |

---

## 15. O celular deixou de ser estático

O convite chega por WhatsApp e DM, então o celular é a tela principal, não a secundária.
O padrão da skill entrega hero estático no celular; aqui isso estava otimizando para a
minoria.

**A solução:** uma segunda montagem da mesma tomada, cortada para 9:16 com a câmera
reenquadrada acompanhando cada artista. As três panorâmicas do corte caem dentro das
mesmas transições onde os textos moram, então a câmera se reposiciona quando não há
artista na tela. Feito com ffmpeg, custo zero em créditos.

| | Desktop | Celular e tablet em pé |
|---|---|---|
| Arquivo | `hero-scrub.mp4`, 1280x720, 8,8 MB | `hero-scrub-mobile.mp4`, 608x1080, 4,4 MB |
| Texto | ao lado do artista, lado oposto ao corpo | ancorado embaixo, com escurecimento em gradiente |
| Contraste do pior pixel | 5,22:1 | 3,58:1 |

**Hero estático agora só em dois casos:** movimento reduzido ligado, e celular deitado
com menos de 560px de altura, onde não existe altura para a jornada. Girar o aparelho
troca a montagem ao vivo, sem recarregar.
