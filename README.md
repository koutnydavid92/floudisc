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

## Nasazení (Cloudflare Pages, zdarma)

1. Nahraj repo na GitHub (nebo použij přímý upload v Cloudflare dashboardu).
2. Cloudflare Pages → Create project → připoj repo, žádný build command, output = kořen.
3. Custom domain → `floudisc.cz` → uprav DNS záznamy dle instrukcí (CNAME/A na Pages).

Alternativy: GitHub Pages (repo → Settings → Pages), Netlify (drag & drop).

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

## Údržba obsahu

Ceny a citace odpovídají stavu webu výrobce k 7. 7. 2026. Při aktualizaci
změnit datum v sekci „Zdroje a metodika" a v patičce `index.html`.
