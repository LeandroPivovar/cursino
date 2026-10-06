# Cursino Ferro e Aço

Site institucional da Cursino Ferro e Aço (WhatsApp: "Cursino Vendas"), venda de ferro e aço.
HTML/CSS/JS estático, sem build. Mesma estrutura dos sites da Mecânica JR e IA Tech, mas em **tema claro**,
como a logo (preto e vermelho sobre branco). O foco é levar o cliente a mandar a lista de materiais pelo WhatsApp.

```bash
npx --yes serve . -l 6330
```

## Estrutura

```
index.html
assets/
  css/styles.css
  js/main.js              menu mobile, formulário (lista de materiais) -> WhatsApp, FAQ, reveal, ano do rodapé
  fonts/phosphor/         ícones Phosphor (woff2 local, licença MIT)
  img/icon.svg            ícone da logo redesenhado em SVG (também é o favicon)
```

Sem fotos: o hero tem uma ilustração em CSS de um feixe de vergalhões e as seções usam ícones.

## Dados usados (fonte: perfil do WhatsApp Business)

| Campo | Valor |
|---|---|
| Nome | Cursino Ferro e Aço (perfil: "Cursino Vendas") |
| WhatsApp / telefone | (11) 91143-4405 (`wa.me/5511911434405`, constante `WA` no `main.js`) |
| Horário | Aberto até as 18:00 (só isso aparece no perfil) |

## Confirmar com o cliente

- **Endereço:** o perfil não tem. O site não mostra endereço nem mapa. Se tiver loja/depósito para retirada,
  passar o endereço para incluir a seção de localização (como nos outros sites) e o `address` no JSON-LD.
- **Horário:** só se sabe que fecha às 18h. Pegar dias e horário de abertura.
- **Produtos:** o perfil não lista produtos. Os 7 cards (vergalhões, telas soldadas, treliças e colunas, tubos,
  chapas, perfis e cantoneiras, barras) são o mix comum de loja de ferro e aço. Ajustar ao que a Cursino vende.
- **Público:** a seção "Para quem vendemos" cita quem está construindo, pedreiros, construtoras e serralherias.
  Confirmar (vende para pessoa física? atende serralheria?).
- **Entrega, frete e pagamento:** o site não promete nada, só manda combinar pelo WhatsApp. Se houver entrega
  (região, frete grátis acima de X, etc.), vale destacar.
- **Corte e dobra:** muitas lojas do ramo oferecem. Se a Cursino faz, dá para criar um card próprio.

## Logo

A logo do perfil tem resolução muito baixa (~170 px). O ícone (casa dentro do balão vermelho) foi **redesenhado em
SVG** e o nome "CURSINO / FERRO E AÇO" é texto com a fonte Michroma, parecida com a original. Pedir a logo em
arquivo (SVG ou PNG grande) e trocar `assets/img/icon.svg` e o `.brand` no header e no footer.

## Depoimentos

Não foram incluídos depoimentos. Se o cliente tiver avaliações no Google, dá para adicionar a seção.

Fontes: Archivo e Michroma (Google Fonts, OFL).

## Deploy

Sem build: publicar a pasta na Vercel, GitHub Pages ou hospedagem comum.
Depois do deploy, adicionar `og:image` (URL absoluta) e `<link rel="canonical">`.
