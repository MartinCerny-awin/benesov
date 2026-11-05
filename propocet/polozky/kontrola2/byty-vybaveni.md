# Kontrola 2: Byty – koupelny, kuchyně, okna, dveře (5. 11. 2026)

Web real 1 471 tis. (rozpis 231 + 22 + 370 + 56 + 428 + 364). Vlastní rozpis v `report.py` (`byty_vyb`, ř. 285–291) dává jen 1 055 tis., web je tedy o 39 % výš kvůli dopočtu na součet z modelu (viz bod 2). Tabulka porovnává s webem; všechny ceny s DPH, listopad 2026.

## 1. Tabulka

| Položka | Web | Můj real | pes–opt | Potřeba | Nejlevnější rozumná cesta (úspora) | Zdroj |
|---|---|---|---|---|---|---|
| Koupelny s WC B, C, D – obnova | 231 | **170** (3 × 57) | 230–130 | ano (prodejnost, plíseň; ze zákona ne) | řemeslník + svépomoc nátěr obkladu, výměna sanity, podlaha: ~140 (−30) | rozpis uživatele 50 tis. bez DPH/byt (`model.py` ř. 50): materiál ~25 × 1,21 + práce ~25. Sanita, obklad, nátěr: ODHAD 45–65 tis./byt. Kontrola proti S2/S8 (60–120 tis. menší zásah, `stav.md` ř. 116, 122) |
| Byt A – obnova koupelny a WC | 22 | **22** (20–30) | 30–15 | ano (nové WC, baterie, spáry) | řemeslník/svépomoc ~20 (−2) | A_okna.jpg a F/085808012: koupelna s obkladem a vanou je v pořádku; user 20–30 tis. |
| Kuchyňské linky B, C, D | 370 | **270** (3 × 90) | 330–200 | jen když chceš prodat „na klíč“; kolaudace ji nevyžaduje | řemeslník + svépomoc montáž linky: ~230 (−40); bez spotřebičů 150 | IKEA Knoxhult 240 cm 7 900 Kč od 1. 9. 2026 (https://www.ikea.com/cz/cs/cat/kuchynske-linky-ka003/, 5. 11. 2026); Metod 270 cm s dvířky ODHAD 25–35 tis.; spotřebiče (deska 4, trouba 6, digestoř 2,5, dřez s baterií 4, lednice 7) ODHAD 24 tis.; obklad zástěry 6 tis.; montáž truhlář 8–15 tis. (https://truhlarijedou.cz/blog-cena-montaze-kuchyne.html, 5. 11. 2026); linka z bazaru 17–27 tis. (bazos.cz, 5. 11. 2026) |
| Byt A – stávající linka, obklad, spotřebiče | 56 | **40** | 55–30 | ano, ale menší (linka „dá se použít“) | svépomoc ~35 (−5) | `rozpocet-2.md` ř. 22; foto F/085756949; ODHAD: spotřebiče 15 + obklad 5 + deska a dřez 8 + drobnosti |
| Okna A, B, D (21 ks) + seřízení plastových v C | 428 | **305** | 380–240 | ano (dřevěná z 1981, plíseň, kupci čekají plast) | firma 12 % (vč. montáže a záruky), poptat 3 firmy: ~290 (−15). Svépomoc ne | Velké 150×150 = 2,25 m² × 4 500 Kč/m² vč. montáže ≈ 10 + parapety 2 + špalety 2,5 + odvoz 0,5 = ~15 tis. bez DPH; malé ~8; 14 × 15 + 7 × 8 + C 3 = 269 × 1,12. Zdroje: https://www.daibau.cz/ceny/plastova_okna (4 000–5 000 Kč/m², montáž 1 500–4 000/ks), https://kolikmaterialu.cz/kolik-stoji-vymena-oken/ (5. 11. 2026); `stav.md` S1, S5, S17 |
| Dveře: 16 vnitřních + 4 vstupní bezpečnostní | 364 | **208** (vnitřní 88 + vstupní 120) | 260–170 | vnitřní ano (prodejnost); vstupní RC2/RC3 ne ze zákona, EI/EW podle PBŘ | nová křídla do stávajících ocelových zárubní, pověšení svépomocí: ~192 (−16); vstupní viz níže | křídlo CPL s kováním ~4 tis. (ODHAD, `kontrola.md` ř. 26: 3–4 tis.); truhlář za pověšení 0,6–1 tis./ks ODHAD; bezpečnostní RC3 + EI 30 vč. montáže 25–45 tis., EI 30 DP3 bez RC 8–11 tis. + zárubeň (https://www.htdvere.cz/sortiment/protipozarni-dvere/, https://laminatyprotruhlare.cz/vstupni-dvere-do-bytu-jak-vybrat-bezpecnost-a-design-podle-norem, 5. 11. 2026) |

## 2. Součet

| | tis. Kč |
|---|---|
| Web | 1 471 |
| Můj real (současné rozdělení firma/řemeslník) | **1 015** (−31 %) |
| Nejlevnější rozumná varianta se svépomocí | **~905** (−38 %) |

Hlavní důvod rozdílu: web není nadsazený po cenách, ale je dopočtený na model (rozpis v `report.py` je 1 055, tj. na úrovni mého odhadu); přes 400 tis. je tedy plošná přirážka, ne věcný náklad. Okna jsou ~−125, kuchyně ~−116, dveře ~−156, koupelny ~−61 proti webu. Svépomoc přidává jen ~110 tis. (montáž linek, pověšení dveří, sanita), protože u řemeslníka-neplátce se z práce DPH neodečítá a okna, vstupní dveře ani revize laik dělat nemá.

## 3. Zvláštní otázky

- **Okna v A:** stav.md je bere za dřevěná (F/085748234), rozpocet-2 za plastová. Na A_okna.jpg mají tenký světlý rám s vnitřní žaluzií, spíš dřevěná/zdvojená z doby stavby. Z fotek nejde rozhodnout jistě; zbylá riziko ±45 tis. (A má ~8 oken). Ověřit na místě (plastová mají viditelné komory a těsnění). Počet 21 ks: dispozice dávají A 8–9, B 5, D 5 + malá (kuchyň, koupelna, WC) → blíž 21–26; ±3 ks = ±45 tis.
- **Kuchyně IKEA/Sconto vs. studio:** studio 100–150 tis./byt (rozpocet-2 ř. 98: 60–130 tis. + obklad), IKEA/Sconto linka 25–40 + spotřebiče ~24 + montáž je 80–90 tis. Studio je zbytečné, kupci bytů z druhé ruky kuchyň předělají. Nejlevnější: linka bez spotřebičů (kupec si vybere) = ~50 tis./byt; prodejnost trochu klesá, riziko menší dopad na cenu.
- **Dveře:** nová křídla do stávajících ocelových zárubní stačí, pokud jsou zárubně rovné a standardního rozměru (80×197); jinak zárubně 3–4 tis./ks navíc. Vstupní: bezpečnostní třída není zákonná povinnost ani podmínka pojišťovny (jen u vyšších limitů pojištění domácnosti, ODHAD). Požární odolnost dveří bytů do chodby závisí na PBŘ (2 NP, nechráněná úniková cesta: nejspíš nanejvýš EW 15–30 DP3, ODHAD, nutno ověřit v PBŘ, který je v položce projekt). Levnější: EI 30 DP3 bez RC3 (~15 tis. vč. montáže) místo 30 tis. → −60 tis.; já ponechávám RC2/RC3 kvůli prodejnosti.
- **Koupelny 77 tis./byt (web):** dle rozpisu uživatele 57 tis./byt s DPH stačí; 77 je plíseň a rozvody ve zdi (jsou v jiné položce), proto 60–65 reálné s rezervou.

## 4. Chybí / dvakrát

- **Chybí:** nový el. bojler (80–100 l) v koupelnách B, C, D ~7 tis. × 3 = 21 tis., pokud „nová sanita“ stávající nezahrnuje (ODHAD); demontáž starých kuchyní, sanity a bojlerů 32 tis. bez DPH (`rozpocet-2.md` ř. 99) – ověřit, že je v položce bourání/vyklizení (128 tis.); žaluzie a sítě (kupci čekají; ~1 tis./okno = 21 tis., ODHAD).
- **Dvakrát:** nic zjevného. Voda a odpady pro kuchyně (89) a rozvody koupelen jsou jinde, v této položce nesmí být.
- **Podhodnoceno:** nic, jen okna v A (viz výše).

## 5. Doporučení

Změnit: real **1 190** (můj 1 015 × 1,17 přirážka jako rezerva), pes beze změny (1 471), opt ~910 (svépomoc). Důvod: web je o 31 % výš než zdola spočítané ceny a hlavní rozdíl je plošná přirážka; položka je dobře doložená (okna, kuchyně, dveře). Rozhodnutí uživatele (koupelny jen obnova) nerušeno.
