# Kontrola 2: Byty, elektro a voda (A, B, C, D, 264 m²), 5. 11. 2026

Web (nasazená verze) ukazuje 488 + 219 = **707 tis.** `report.py` (ř. 277–278, lokální, ještě nenasazeno) už má 390 + 89 = **479 tis.** (kontrola kolo 1, `polozky/_kontrola.md` ř. 14–15). Porovnávám s oběma.

## 1. Tabulka

| Položka | web | lokální report | můj real (s DPH) | pes–opt | potřeba | nejlevnější rozumná cesta | zdroj |
|---|---:|---:|---:|---|---|---|---|
| Nové elektro v bytech (264 m², rozvaděče, revize) | 488 | 390 | **400** | 520–320 | ano (viz 3.1) | svépomoc drážky/krabice + elektrikář OSVČ: ~350 (−50) | níže, výpočet A |
| Voda a odpady v bytech mimo koupelny | 219 | 89 | **95** | 130–65 | ano, ale jen kuchyně + uzávěry/vodoměry | instalatér OSVČ ~75; svépomoc PPR ~50 (−45) | výpočet B |
| **Součet** | **707** | **479** | **495** | 650–385 | | **~400** | |

### Výpočet A, elektro (tis. Kč, s DPH)
- **Materiál**: kabely CYKY 5–10 m na m² podlahy, 3×1,5 = 23, 3×2,5 = 36 Kč/m, tj. 100–250 Kč/m² jen kabely (kolikmaterialu.cz, 5. 11. 2026). Krabice, zásuvky a vypínače (~190 kusů, 4+1 ~50, 1+1 ~20), bytový rozvaděč 24 modulů s jističi, proudovými chrániči a svodičem (10–14 tis./byt) ODHAD: celkem ~450 Kč/m² bez DPH, tj. 264 × 450 × 1,21 = **144**.
- **Práce elektrikáře OSVČ** (400–700 Kč/h; montáž zásuvky/vypínače 150–450 Kč/ks, kolikmaterialu.cz): 264 m² × ~950 Kč/m² vč. sekání = **251** (neplátce, bez DPH); bez sekání drážek (~25 %) **188**.
- **Revize** 4 byty × 3,5 tis. (1 850–4 200 Kč/byt, revizit.cz; průměr 2 500, kolikmaterialu.cz) = **14**. Svítidla jen základní (žárovky/přisazená) ~5 tis./byt = **20**; zatím nikde.
- Řemeslník vč. sekání: 144 + 251 + 14 + 20 = **429**. Řemeslník bez sekání (sekání svépomocí): 144 + 188 + 14 + 20 + pronájem drážkovačky s odsáváním 5 = **371**. Realistický mix (část prací dělá firma, byt A větší): **~400**.
- **Firma** (plátce, 12 %): trh 1 500–3 000 Kč/m² (stavimbydlim.cz), od 1 950 Kč/m² bez DPH u elektromistrů (xxlcredit.cz), 80–180 tis./byt (koky-stavby.cz), stav-garant 700–1 800 Kč/m² (stav.md S1). Střed ~1 650 × 264 × 1,12 = **488**. Tedy web = cena firmy; řemeslník je o ~15–20 % levnější, hlavně bez marže a režie.
- Svépomoc: sekání drážek a krabic + zapravení: ~0,6 h/m² = ~160 h na 4 byty (2 lidé 2 týdny). Laik to zvládne (hlavní práce je prach a fyzická síla), riziko: trasy podle ČSN 73 4301 (vodorovně/svisle od zásuvek), nenarušit nosné zdivo; **při trhlinách 2–3 mm nesekat do nosných stěn horizontálně bez schválení statika**. Zapravení drážek je už v položce „Omítky a zapravení“ (111 tis.), nezapočítávat dvakrát. Tahání kabelů, zapojení a revize musí dělat osoba s oprávněním (vyhl. 50/1978 Sb.).

### Výpočet B, voda a odpady mimo koupelny
Jádra B, C, D mají „rozvody“ v ceně koupelny (`byty.md` ř. 9), A je hotová, kuchyně mají „montáž linky“ zvlášť. Zbývá jen: v každé kuchyni přívod SV/TV (~6 m PPR), odpad HT (~4 m), vývody pro dřez a myčku, rohové ventily, napojení na stoupačku = ~8 h instalatér × 700 + materiál 4 tis. = **~10 tis. bez DPH řemeslník, 15–25 tis. firma**. Ceny: PPR od 80 Kč/bm práce, spoj 50 Kč, HT 50 Kč/bm (daibau.cz/megastroj.cz, 5. 11. 2026); „rozvody celého bytu 45–100 tis.“ jen reklamní odhad (pujckasnadne.cz).
- 4 kuchyně × 22 = **88**
- Uzávěry a **bytové podružné vodoměry** (2 ks/byt SV+TV, ~1,5 tis. + montáž) 4 × 5 = **20**, nikde nezapočteno (stoupačky v „Rozvody domu“ mají jen „uzávěry po bytech“ a hlavní vodoměr)
- Celkem ~108 firma, **~95 mix**, **~75 řemeslník**, **~50 svépomoc** (PPR sváření laik zvládne po zácviku, ale zatékání do prodaných bytů = záruční riziko, vodoměry a tlaková zkouška ať dělá instalatér).

## 2. Součet
- Web 707 vs můj real **495**: **−30 %**. Důvod: web počítá 600 Kč/m² vody na celé ploše, ale koupelny jsou v jádrech a stoupačky v Rozvodech domu (zčásti dvakrát), a elektro firmou místo řemeslníkem.
- Lokální report 479 vs 495: +3 %, v pořádku.
- Nejlevnější rozumná varianta (svépomocí drážky a krabice, elektrikář OSVČ jen tahá/zapojuje/reviduje, instalatér OSVČ): **~400 tis.** (−43 % proti webu, −19 % proti reportu). Neodpočítaná DPH 21 % z materiálu (~30 tis.) se vrací investorovi jako plátci, takže čistě ještě ~30 tis. méně.

## 3. Zvláštní otázky

**3.1 Hliník a výměna celého rozvodu.** Zákon výměnu hliníku nevyžaduje; hliník není zakázaný, ale patří pod revizního technika (revizelektro.cz „Staré hliníkové rozvody“, spp.cz; i revize při prodeji není povinná, jen ji může chtít kupec nebo banka: revizelektro.cz, portalsvj.cz). Z fotek (stav.md ř. 48) materiál vodičů **nejde poznat**; barevné jednožilové vodiče v elektroměrovém rozvaděči spíš značí novější úpravu, bytové rozvody v A, B, C, D neprohlédnuty. Doporučení: **měnit celé na měď**, ne jen rozvaděče, protože (a) se stejně vysekávají koupelny, kuchyně, podlahy a malují se stěny (omítky 264 m² jsou v rozpočtu), takže mezní cena kabelů je malá; (b) dům z roku 1981 má pravděpodobně dvouvodič TN-C bez PE, nový stoupací rozvod TN-S (100 + 80 tis. v Rozvodech domu) vyžaduje nové okruhy s ochranou a chrániči; (c) prodáváte „rekonstruované byty“ s DPH 12 %, kupec nebo banka s hliníkem a staršími okruhy bude smlouvat nebo odmítne; (d) výměna později po prodeji je pro vás nemožná. **Úspora při „jen rozvaděče + chrániče + revize + oprava poškozených okruhů“**: ~4 × (12 rozvaděč + 3,5 revize + oprava 20) ≈ 140 tis. místo 400, tj. −260 tis., ale jen když revize ukáže měď v dobrém stavu. Možnost: **byt A** (koupelna 2000–2010, nejnovější) otevřít rozvaděč a nechat posoudit; když je měď s PE, ušetří až 50–60 tis. (ODHAD). Do té doby počítat s plnou výměnou. Pojišťovna (jediný zdroj spp.cz-typ článků, neověřeno): bez revize může krátit plnění.

**3.2 „Voda a odpady mimo koupelny“.** Reálný obsah jsou jen 4 kuchyně + uzávěry/vodoměry. Dvakrát: web 219 tis. odpovídá 264 m² × 600 Kč (S1 stav-garant „vody + odpady 120 m² 95–240 tis.“ vč. jádra, `stav.md` ř. 115, 175), tedy zahrnuje i rozvody v koupelnách, které jsou v ceně jader (473 tis. v `byty.md`), a stoupačky jsou v „Rozvody domu“ (133 + 111 tis.). Kolo 1 to už opravilo na 89.

**3.3 Chybí / dvakrát.**
- Chybí **bytové vodoměry** ~20 tis. (v mém výpočtu B), a základní **svítidla** ~20 tis. (v A). Datové/TV rozvody, zvonek a domovní telefon: telefon v „Rozvody domu“ (92 tis.), v bytech 4 × ~3 tis. (UTP, anténní zásuvka) ODHAD **~12**; není v ničem. Zásuvky pro kuchyňské spotřebiče, indukce 3F a přípojka bojleru jsou součást elektro (v mém materiálu).
- Dvakrát: zapravení drážek (elektro ×omítky 111 tis.) – svépomoc sekání je odečtena z práce elektrikáře, zapravení zůstává jen v Omítkách; rozvody v jádrech (viz 3.2).

## 4. Doporučení
- **Elektro: nová hodnota real ~400 tis.** (pes 520, opt 320); report.py má 390, tedy beze změny proti lokálnímu reportu (rozdíl 3 %). Web 488 je cena firmy při svépomoci nulové; nasadit lokální hodnotu.
- **Voda: real ~95 tis.** (pes 130, opt 65); report.py 89 je v pořádku, doplnit do popisku „vč. bytových vodoměrů a uzávěrů“ (+ ~20 tis., nikde není).
- Celkem **~495 (real)**, nasadit `deploy-web.sh`, až doběhnou souběžná sezení. Web 707 je zastaralý, ne chyba modelu. Před koupí dohodnout prohlídku rozvaděčů A–D s revizním technikem (zjistit Al/Cu, TN-C): 2–3 tis. za prohlídku rozhodne, zda je v hlavním scénáři 400 nebo ~140 tis.

Zdroje (vše staženo 5. 11. 2026): https://kolikmaterialu.cz/cena-elektroinstalace/ · https://www.revizit.cz/blog/revize-elektroinstalace/cena · https://stavimbydlim.cz/cena-elektroinstalace-byt-2-1/ · https://www.xxlcredit.cz/pujcka-na-elektroinstalaci/ · https://www.koky-stavby.cz/rady/kolik-stoji-rekonstrukce-bytu-a-domu/ · https://www.revizelektro.cz/aktuality/stare-hlinikove-rozvody/ · https://www.revizelektro.cz/aktuality/revize-elektroinstalace-pri-prodeji-nemovitosti/ · https://www.daibau.cz/ceny/instalater · https://www.megastroj.cz/cenik-remesel · `propocet/podklady/stav.md` ř. 48–49, 115, 174–175 · `propocet/polozky/byty.md` · `propocet/overeni/rozpocet-2.md` ř. 100–101, 127–128.
