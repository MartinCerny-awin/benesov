# Prodej (provize, právník, marketing) a Ostatní (držení, PENB, jednotky) – V1 firma, realisticky

Stav: 4. 11. 2026. Model spuštěn dnes: `m.run('V1','real')` dává **prodej 1 563 665**, tržby 31 255 374 (6 bytů, 344 m²), **držení 106 950, PENB 15 000, rozdělení 70 000** (součet Ostatní 191 950). Číslo „prodej 1 496 501 / tržby ~29 mil.“ ze zadání je starší běh. Dnešní kód: 31,26 mil. × 3,5 % × 1,21 = 1 323 665 plus 6 × (15 000 + 25 000) = 240 000. Rozpis níže sedí na dnešní běh. Ceny jsou s DPH (model počítá vstupy hrubě, odpočet DPH řeší jen u provize a stavby).

## 1. Rozpis

### A) Prodej – 1 563 665 Kč

| Položka | Množství | Jedn. cena | **Real. Kč s DPH** | Pes / opt | Zdroj |
|---|---|---|---|---|---|
| Provize RK 3,5 % z cen 6 bytů (bez DPH) | 31 255 374 Kč tržeb | 3,5 % | **1 093 938** | 5 % / 2,5 % | `model.py` `IN["provize"]`; `podklady/dane-financovani.md` ř. 111, `marketing.md` ř. 89 (trh 3–5 %, nad 10 mil. 3–4 %); explicitreality.cz „Provize 2026“ (4 % pro 6–8 mil., 3,5 % pro 8–10 mil.; 4. 11. 2026) |
| DPH 21 % z provize (RK je plátce) | 1 093 938 Kč | 21 % | **229 727** | stejně | zák. 235/2004; model ji dává do odpočtu DPH (`dph_in += provize*21/121`), čistý náklad tedy 1 093 938 |
| Marketing bytů: foto 3 000, 3D prohlídka 3 500, půdorys 1 200, video/dron 2 500, inzerce Sreality + další portály 4 800 | 6 bytů | 15 000 / byt | **90 000** | 150 000 / 48 000 | `marketing.md` ř. 75–80 (foto 2 200–3 500, 3D 2 300–5 000, půdorys 690–1 500, video 2 400–5 000), Sreality balíček 3 993 s DPH za 90 dní; rozdělení na pět částí je ODHAD |
| Právník na prodej bytu: kupní smlouva, advokátní úschova, návrh na vklad | 6 bytů | 25 000 / byt | **150 000** | 240 000 / 60 000 | `dane-financovani.md` ř. 201 (ODHAD); trh: úschova 3 500–10 000 + smlouva 5 000–15 000 (dostupnyadvokat.cz, muj-pravnik.cz, bricks.legal, 2026) |
| **Součet** | | | **1 563 665** | | |

### B) Ostatní – 191 950 Kč

| Položka | Množství | Jedn. cena | **Real. Kč s DPH** | Pes / opt | Zdroj |
|---|---|---|---|---|---|
| Energie prázdného domu (staveništní elektřina a voda, odpojený dům) | 23 měs. | 1 800 | **41 400** | 76 000 / 20 000 | `IN["drzeni_mes"]` 3 000 – ODHAD, rozdělení ODHAD |
| Zabezpečení prázdného domu (kamera s GSM, kontroly, zámky) | 23 měs. | 1 200 | **27 600** | viz výše | ODHAD |
| Pojištění domu (stavba + odpovědnost, v rekonstrukci) | 23 měs. | 1 250 (15 000/rok) | **28 750** | 48 000 / 15 000 | `dane-financovani.md` ř. 206; hypox.cz 2026: 0,5–1 ‰ z pojistné hodnoty, tj. 2,5–5 tis. při 5 mil., bytový dům 8–15 tis. při 12–20 mil.; Allianz: rekonstrukci nelze zvýhodnit |
| Daň z nemovitých věcí (celý dům, 2 splátky k 1. 1. 2027 a 2028) | 23 měs. | 400 (4 800/rok) | **9 200** | 11 500 / 7 000 | `dane-financovani.md` ř. 93–97, 196; koeficient obce 2 × místní koeficient Benešova 2 se pro 2026 nemění (podnikatel.cz, přehled okresních měst 2026) |
| PENB pro bytový dům do 10 bytů | 1 ks | 15 000 | **15 000** | 25 000 / 7 000 | relia.cz 7–15 tis. (bytový dům do 10 bytů), realfree.cz 8–18 tis., klik.cz 10–20 tis. (všechny 2026) |
| Prohlášení vlastníka – advokát (6 jednotek, ověření podpisů) | 1 | 25 000 | **25 000** | 45 000 / 16 000 | prohlaseni-vlastnika.cz ceník od 1. 1. 2024: 15 609 s DPH pro 6 jednotek; jiná kancelář 45 000 bez DPH za 6–15 jednotek (prohlasenivlastnika.cz) |
| Geodet: zaměření skutečného stavu a schémata 6 jednotek + společné prostory | 6 jednotek | 5 000 | **30 000** | 45 000 / 15 000 | geonovotny.cz 5 000 Kč za byt bez DPH; `dane-financovani.md` ř. 124 (15–40 tis.). Přestavba 1. NP bude hotová, plány musí odpovídat |
| Poplatky katastru: uložení prohlášení do sbírky listin 1 000, vklad 2 000, rezerva na zápis jednotek | 1 prohlášení | 6 000 | **6 000** | 9 000 / 3 000 | ČÚZK sazebník, položka 120 (`dane-financovani.md` ř. 106–107); „za každou jednotku“ zdroje nepotvrdily, platí 2 000 za návrh, ODHAD rezerva |
| Založení SVJ: stanovy (advokát) 8 000, zápis do rejstříku + rezerva na notáře 5 000 | 1 | 13 000 | **13 000** | 20 000 / 6 000 | viz bod C; notář za zápis 3 000 + DPH (notarskesluzby.cz) jen pokud by SVJ zakládali až noví vlastníci |
| **Součet** | | | **195 950** | | |

Mezisoučty: držení 106 950 (41 400 + 27 600 + 28 750 + 9 200), jednotky 74 000, PENB 15 000.

### C) Odpovědi na otázky ze zadání

- **SVJ je povinné?** Ano, ale až později. § 1198 OZ: povinné při alespoň 5 jednotkách, z nichž alespoň 4 mají 4 různí vlastníci (podnikatel.cz, `dane-financovani.md` ř. 14). V1 má 6 jednotek, takže po prodeji 4. bytu. Podle § 1198 odst. 2 se navíc další převod nezapíše, dokud nevznikne společenství. Prakticky ho založit před prvním prodejem.
- **Notář?** Při založení jediným vlastníkem všech jednotek nemusí být stanovy veřejnou listinou (výklad k § 1200, pravniprostor.cz a Stanovisko KANCL č. 11). Notářský zápis (3 000 Kč + DPH) by byl potřeba, kdyby SVJ zakládali až noví vlastníci na ustavující schůzi. Doporučení: založit před prvním prodejem, notář odpadne. Právní znění k 1. 1. 2026 ověřit ve Sbírce zákonů, zdroje měly odlišná data účinnosti.
- **Bez RK?** Úspora provize je 1,32 mil. s DPH (čistě 1,09 mil. po odpočtu). Měsíc držení stojí ~35 tis. (úrok 705 tis./23 měs. ≈ 30 tis. + provoz 4,7 tis.), takže RK se zaplatí jen když zkrátí prodej o víc než ~30 měsíců, což nehrozí (`IN["t_prodej_byty"]` 6 měs.). Proti: 6 prodejů fyzickým osobám s hypotékou, nutná komunikace a prohlídky v Benešově. Střední cesta: prodej bez RK s advokátem (úschova + smlouva) a vlastním inzerátem, nebo RK s pevnou provizí kolem 2,5 %. Jen poznámka, model neměnit.

## 2. Kontrola proti modelu

| | Model | Můj součet | Rozdíl |
|---|---|---|---|
| Prodej | 1 563 665 (dnešní běh; zadání uvádělo 1 496 501) | 1 563 665 | 0 % |
| Držení | 106 950 | 106 950 | 0 % |
| PENB | 15 000 | 15 000 | 0 % |
| Rozdělení na jednotky | 70 000 | 74 000 | +5,7 % |
| **Ostatní celkem** | **191 950** | **195 950** | **+2,1 %** |

- Provize je v modelu počítána z každé tržby (nikoli z nájmu), 4,235 % s DPH. Sazba 3,5 % je na spodní hranici komerčního ceníku (explicitreality.cz uvádí pro byt za 6–8 mil. 4 %), ale 6 prodejů najednou dává prostor k vyjednání. Beze změny.
- **Možné dvojí započtení:** RK běžně v provizi nabízí foto, 3D, půdorys, inzerci, smlouvu a advokátní úschovu (explicitreality.cz: „v provizi je profesionální fotky, video, 3D, půdorys … advokátní úschova“). Model platí marketing (90 000) a právníka (150 000) navíc. Pokud RK tyto služby zahrne, je v modelu rezerva až 240 000 (0,8 % tržeb). Ověřit v exkluzivní smlouvě; bez RK jsou obě částky potřebné.
- DPH z marketingu, právníka, geodeta a SVJ je v modelu nezapočtena jako odpočet (jen provize a stavba). Pokud jsou dodavatelé plátci, jde o ~21/121 z ~490 000 = ~85 000 odpočet. Konzervativní, nerozlišuji.
- PENB: model platí 15 000 na začátku (`t_start`). PENB musí odpovídat stavu po rekonstrukci a platí 10 let. Před stavbou pořízený štítek při prodeji nestačí. Může jít o platbu ve špatnou chvíli, ne o dvojí cenu. Jestli už je energetické hodnocení v položce Projekt (293 tis.), tak se částky překrývají. Ověřit.
- Daň z nemovitých věcí se platí jen k 1. 1. (dva termíny), takže 9 200 sedí; po vzniku jednotek ji platí vlastníci jednotek k 1. 1.
- Rozdělení: rozdíl +4 000 (model 60 tis. + 10 tis. SVJ; já geodet a KN o něco výš), pod 10 %.

## 3. Doporučení

**Beze změny** všech vstupů (`provize`, `marketing_byt`, `advokat_prodej`, `drzeni_mes`, `pojisteni_dan_mes`, `penb`, `rozdeleni`). Rozdíl 2 % je pod prahem 10 %. Poznámka: `advokat_prodej` 25 000 je horní část trhu (reálně 8–20 tis. s úschovou), tedy konzervativní. Neměnit.

## 4. Pro report

```python
# Prodej (součet 1 563 665)
[
 ("Provize realitní kanceláře 3,5 % z cen 6 bytů (tržby 31,3 mil.), bez DPH", 1_093_938),
 ("DPH 21 % z provize (odpočitatelná, v modelu v odpočtu DPH)", 229_727),
 ("Marketing: foto, 3D prohlídka, půdorys, video, inzerce – 6 bytů po 15 tis.", 90_000),
 ("Právník: kupní smlouva, advokátní úschova, vklad – 6 bytů po 25 tis.", 150_000),
]

# Ostatní (součet v modelu 191 950; po rozpisu 195 950)
[
 ("Držení: energie prázdného domu, 23 měsíců po 1 800", 41_400),
 ("Držení: zabezpečení domu (kamera, kontroly), 23 měsíců po 1 200", 27_600),
 ("Držení: pojištění domu v rekonstrukci, 15 tis. ročně × 23 měsíců", 28_750),
 ("Držení: daň z nemovitých věcí, 4,8 tis. ročně (2 termíny k 1. 1.)", 9_200),
 ("Průkaz energetické náročnosti budovy (PENB), celý dům", 15_000),
 ("Rozdělení: prohlášení vlastníka (advokát), 6 jednotek", 25_000),
 ("Rozdělení: geodet – zaměření 6 jednotek a společných částí", 30_000),
 ("Rozdělení: poplatky katastru za prohlášení, vklad a zápis jednotek", 6_000),
 ("Rozdělení: založení společenství vlastníků (stanovy, zápis do rejstříku)", 13_000),
]
```

Poznámka k součtu: u Ostatních dává tento seznam 195 950, tedy o 4 000 víc než `drzeni + penb + rozdeleni` v modelu (191 950). Chce-li report přesně modelový součet, sníží se řádek „geodet“ na 26 000. Jinak beze změny, protože rozdíl je 2 %.
