# floudisc.cz

Nezávislý satirický a vzdělávací web o produktu Flow Disc (Centrum Serafín).
Statický jednosouborový web — žádný build, žádné závislosti, žádný backend.

## Soubory

- `index.html` — celý web (HTML + CSS + JS inline)
- `og.png` — obrázek pro sdílení na sociálních sítích (1200×630)

## Lokální náhled

```sh
python3 -m http.server 8123
# → http://localhost:8123
```

## Nasazení

Web běží na Vercelu (projekt `floudisc`, účet koutnydavid92), propojeno
s repem https://github.com/koutnydavid92/floudisc. Každý push na `main`
= automatický deploy. Produkce: https://floudisc.vercel.app

Ruční deploy: `vercel deploy --prod`

### DNS u registrátora (Websupport)

V administraci DNS domény floudisc.cz přidat:

```
A      @      76.76.21.21
CNAME  www    cname.vercel-dns.com
```

Vercel si pak sám ověří doménu a vystaví HTTPS certifikát
(stav: `vercel domains inspect floudisc.cz`).

### E-mail info@floudisc.cz

Adresa je jen forwarding, žádná schránka. Dvě cesty:

- **Registrátor**: většina českých registrátorů (Wedos, Forpsi…) nabízí
  e-mailové přesměrování zdarma v administraci domény — přesměrovat
  `info@floudisc.cz` na soukromý Gmail.
- **Cloudflare Email Routing** (zdarma): převést DNS domény na Cloudflare,
  pak Email → Email Routing → custom address `info@` → cíl Gmail.
  Cloudflare sám nastaví MX záznamy. (DNS pro Pages pak vede taky přes
  Cloudflare — A záznamy výše zůstávají stejné.)

## Pravidla hry (důležité — právní pozice webu)

Web je ubránitelný jako legitimní kritika/satira jen dokud platí:

1. **Nikdy nenabízet doménu k prodeji** — žádný banner, žádný e-mail majiteli
   Serafína, žádná zmínka o odkupu. Registrace „ve zlé víře" za účelem
   přeprodeje = prohraný doménový spor. Chtějí-li odkup, ať přijdou sami.
2. **Žádná monetizace** — žádná reklama, affiliate, ani prodej čehokoli.
3. **Fakta citovat doslova se zdrojem, hodnocení formulovat jako názor.**
   Nepoužívat slovo „podvod" jako tvrzení.
4. **Nekritizovat osobu majitele** — jen produkt a veřejná obchodní tvrzení.
   Žádné SPZ, jména, fotky osob.
5. Citovaná tvrzení jsou archivována ve Wayback Machine (uloženo 7. 7. 2026):
   - https://web.archive.org/web/2026/https://www.centrumserafin.cz/flow-disc/
   - https://web.archive.org/web/2026/https://www.centrumserafin.cz/flow-disc-slozeni/
   - https://web.archive.org/web/2026/https://www.centrumserafin.cz/flow-disc-order/
   - https://web.archive.org/web/2026/https://www.centrumserafin.cz/zkusenosti-s-flow-discem/
   Při změně jejich webu archivovat znovu (https://web.archive.org/save/...).

## Analytika

Vercel Web Analytics (bez cookies, není potřeba consent lišta) — zapnutá
na projektu `floudisc` (Hobby: 50 000 eventů/měsíc, 30 dní historie).
Skript `/_vercel/insights/script.js` je vložený v `index.html` v `<head>`.
Přehledy: vercel.com → projekt floudisc → Analytics.

Pozn.: GA4 property `floudisc.cz` (G-6VWPEN6GH2, properties/544633465)
existuje, ale tag byl z webu odstraněn 8. 7. 2026 — data od té doby
netečou; property lze případně smazat v GA administraci.

## Údržba obsahu

Ceny a citace odpovídají stavu webu výrobce k 7. 7. 2026. Při aktualizaci
změnit datum v sekci „Zdroje a metodika" a v patičce `index.html`.
