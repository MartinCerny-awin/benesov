# Kontrola 2: Projekt, dozor, statik (5. 11. 2026)

Web real bez nástavby: **390 tis.** = 201 + 45 + 111 + 25 + 8. Zaměření, projekt stavebních úprav a dozor dělá architekt zdarma a v položce nejsou (733 − 345 = 388, sedí). Veřejné sazby projektantů nejsou, většina čísel je ODHAD. Využil jsem `polozky/projekt-rezerva.md`, `polozky/strecha-statika.md` ř. 43–65, `polozky/nebyt-bytb.md` ř. 26, 42, `polozky/technika.md`.

## 1. Tabulka (tis. Kč s DPH 21 %, služby)

| Položka | Web | Můj real | Pes–opt | Potřeba | Nejlevnější rozumná cesta | Zdroj |
|---|---|---|---|---|---|---|
| Prováděcí projekt ÚT, ZTI, elektro | 201 | **160** | 230–100 | ÚT/elektro/ZTI částečně ano (viz 2a) | Zúžit na ÚT+elektro+hromosvod, TČ návrh v ceně dodavatele: ~120 (−40). Svépomoc nelze (autorizace) | ODHAD: 4–6 % z TZB částí 2,75 mil. (vytápění 1 230 + rozvody 810 + byty elektro/voda 707); vytápěcí projekt jen 5–15 tis. (vytapeni.tzb-info.cz, hledání 5. 11. 2026) |
| Požárně bezpečnostní řešení | 45 | **35** | 50–25 | Ano, jen jedno pro celý dům | Jedno PBŘ s nebytovou částí v jednom zadání, 30–35 | ODHAD; veřejný ceník bytového domu nenalezen (pbr.cz/cenik, daibau.cz/ceny/pozarni_ochrana, 5. 11. 2026: rekonstrukce „na nabídku“) |
| Statik: posudek trhlin, návrh sanace | 111 | **100** | 160–70 | Ano (aktivní trhliny, W05/W11; bez posudku neprodáte bezpečně ani nedostanete povolení sanace) | Jedna nabídka s pevnou cenou, terče a odečty dělá statik; 80 | rozpad v 2b; stav.md 5b/5c ř. 188, 219 |
| Koordinátor BOZP | 25 | **60** | 90–35 | Ano (více zhotovitelů, 3 a víc firem) | Požádat architekta Ondřeje, jestli má osvědčení koordinátora: 0–15; jinak 40 za minimum návštěv | 309/2006 Sb. § 14–15; ceny viz 2c |
| Poplatky, vyjádření správců sítí | 8 | **15** | 25–8 | Ano | – | ODHAD; geodet skutečného provedení + správní poplatky, viz 3 |
| **Součet** | **390** | **370** | 555–238 | | **~290 (−26 %)** | |

## 2. Zvlášť prověřeno

**a) Prováděcí projekt všech profesí, nebo stačí elektro a TČ?** Zákon prováděcí projekt (DPS) nevyžaduje, vyžaduje dokumentaci pro povolení záměru, a ta u nového společného zdroje tepla, nových rozvodů v 6 bytech a změny užívání nebytové části obsahuje části ÚT, ZTI a elektro. Revize elektro projekt nutně nepotřebuje, ale bez něj nemáte podklad pro 6 elektroměrových rozvaděčů, jističe a hromosvod (posouzení rizika, ČSN EN 62305). Výpočet tepelných ztrát a návrh TČ dělá dodavatel za 5–15 tis. (vytapeni.tzb-info.cz, 5. 11. 2026), což u 32 kW kaskády pro 6 bytů nenahradí hydrauliku rozvodů ani vyvážení. Rozumné je tedy zúžit na **ÚT+hydraulika, elektro+hromosvod, ZTI jen stoupačky** a TČ nechat v ceně dodavatele. Úspora ~40 tis., skoro celá nad hranicí „rozumné“ (hrozí vada kupcům bytů). Web 201 je proto lehce nad, ale ne o 10 %.

**b) Statik, ceny 2026 vč. monitoringu.** Veřejné ceny jsou pro jednoduché případy: posudek jedné poruchy ~6 tis. + DPH (staticke-posudky.cz, psds.cz), jednoduchý posudek 5–12 tis., komplexní RD 30–80 tis. (kalkulio.cz/blog/staticky-posudek-obsah-cena, 2026), od 24,9 tis. (estatika.cz). Sádrové terče: stovky Kč za kus, cena odečtů není veřejná. Zdola pro tento dům: ohledání 2 NP a soklu + posudek 35–50, návrh sanace s výkresem sešití a injektáže 20–30, monitoring (10 terčů + trhlinoměry, 6–8 odečtů × 2–4 tis.) 15–30, dohled nad sanací 10–20. Dohromady **80–130, střed 100**. Web 111 je v pořádku.

**Kryje se statik s „Statickým zajištěním“ (1 500, geologie)?** Ne. Zajištění obsahuje geologii, sondy k základům, táhla a ztužení (`strecha-statika.md` ř. 43–47); posudek a monitoring explicitně ne (ř. 50, 62: monitoring jen ve službách). Ale 1 500 je zadané pevně a jeho obsah mimo model pokrývá „rezervu na rozsah podle posudku“ 184 tis., takže je tam **zdvojení ~30–60 tis. se sanací trhlin (monitoring)** už jednou ošetřené v `strecha-statika.md`; neřeším.

**Kryje se s Nebytovou částí (450: projekt, zaměření, statik, PBŘ, průzkum vlhkosti)?** Částečně. Řádek v `nebyt-bytb.md` ř. 27 obsahuje **vlastní statik a PBŘ** a navíc je v rozpisu tamní „Nový vchod z chodby, statik“ 5 tis. (ř. 74). PBŘ pro dům a PBŘ pro změnu užívání nebytové části je jedna práce: jeden autorizovaný technik zpracuje jedno PBŘ celého objektu a nebytovou část do něj přidá za příplatek 5–10 tis. Dvojí započtení PBŘ ~**20–25 tis.**; statik ~**5–10 tis.** (posudek otvoru je součástí návrhu sanace). Dohromady ~30 tis. přebývá v Nebytové části, ne zde. Průzkum vlhkosti je jen tam, tady není.

**c) Koordinátor BOZP povinný?** Ano. § 14 zákona 309/2006 Sb. ukládá zadavateli zajistit koordinátora, když na staveništi pracuje více zhotovitelů současně nebo postupně; zde firma plus několik řemeslníků. Oznámení inspektorátu práce (§ 15) se podává, když stavba trvá > 30 pracovních dnů a pracuje na ní současně > 20 osob, **nebo** přesáhne 500 osobodnů (rulecalc.com/cs/zamestnavatel/bozp-koordinator-oznameni-stavby, businessinfo.cz, vše již v `projekt-rezerva.md`; znění jsem nově nepřečetl v zákoně). Při ~10 měsících a 3–6 lidech je to řádově 600–1 000 osobodnů, oznámení tedy asi nutné, pokuta až 2 mil. Ceny: plán BOZP od 8 tis. (30 a víc u rizikových), celá stavba RD 15–40 tis. (bezpecak.safetyfrog.cz, 5. 11. 2026); paušál 6–15 tis./měsíc podle návštěv (sohe.cz/blog/koordinator-bozp-na-stavbe; smlouvy.gov.cz 6 tis./měs.). Pro 10 měsíců s několika zhotoviteli tedy **plán 15 + 10 × 4–6 = 55–75 tis.**, web 25 je **podhodnocený o ~35 tis.** (platí zvlášť pro firma + řemeslníci, kde se zhotovitelé střídají).

**d) PBŘ jedno pro celý dům?** Ano, jedno pro objekt (nebytová část 2 byty + celé podlaží). Nedělat podruhé (viz b).

## 3. Co chybí / dvakrát / podhodnoceno

- **Podhodnoceno:** koordinátor BOZP +35 tis.
- **Chybí:** geodet pro skutečné provedení a zákres do katastru po změně užívání, správní poplatky za povolení a kolaudaci, vyjádření Správy železnic (každá práce potřebuje stanovisko, `index.html` data-tip) – celkem 15–25 tis., web má 8. Přidat +7 až +10.
- **Dvakrát:** PBŘ a statik v Nebytové části (~30 tis., viz 2b) a ~30–60 tis. monitoring ve Statickém zajištění / sanaci trhlin (zmíněno v `strecha-statika.md` ř. 62, vyřešeno tam).
- **Nechybí:** autorský dozor (architekt zdarma), PENB (jinde), stavbyvedoucí (u řemeslníků jinde v „Shánění a koordinace“).
- **Přebývá:** DPS rozsah (−40 až −50 při zúžení).

## 4. Součet

| Varianta | tis. | vs. web |
|---|---|---|
| Web | 390 | – |
| Můj real (firma + řemeslníci, služby se stejně platí 21 % DPH) | 370 | −5 % |
| Nejlevnější rozumná (zúžený DPS 120, PBŘ 35, statik 80, koordinátor 40, poplatky 12) | ~290 | −26 % |

Svépomoc u žádné položky: projekt, PBŘ, statik a koordinátor vyžadují autorizaci nebo osvědčení. Jediná legální úspora je architekt Ondřej jako koordinátor, pokud má osvědčení (−25 až −60).

## 5. Doporučení

**Beze změny (390).** Rozdíl −5 % je pod hranicí 10 % a plusy a minusy se vyrušují (koordinátor +35, poplatky +7, DPS −40, PBŘ −10). Poznámky: koordinátor BOZP je levný jen o ~35 tis., PBŘ a statik v Nebytové části (450) z velké části zdvojují tuto položku (~30 tis., jde o cizí položku, kterou by měl kontrolovat kolega). Pro nabídku: zadat jedno PBŘ pro celý dům a poptat tři statiky s pevnou cenou včetně monitoringu.
