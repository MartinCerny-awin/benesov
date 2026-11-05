# Kontrola 2: Prodej bytů (web 63) a Ostatní (web 279) – 5. 11. 2026

Hodnoty z webu podle zadání (real, bez nástavby, tis. Kč s DPH). Vstupy modelu čteno z `propocet/model.py` ř. 97–106, 157–161 (jen čtení). Ceny z internetu: vyhledávač dal jen málo ceníků, proto je u části řádků „ODHAD“ nebo převzato z dřívějších rešerší v `polozky/prodej-ostatni.md`, `podklady/marketing.md`.

## 1. Tabulka

| Položka | Web | Můj real | Pes–opt | Potřeba | Nejlevnější rozumná cesta (úspora) | Zdroj |
|---|---|---|---|---|---|---|
| Prodej: úschova kupní ceny, vaše polovina, 4 tis./byt | 24 | 27 | 36–15 | ano, kupující s hypotékou ji vyžaduje a chrání i vás před vkladem | bankovní jistotní účet nebo advokát; polovina z ~5,2 mil./byt: banka 0,2 % (min. 6 000, max. 20 000 Č. spořitelna) = ~5,2 tis. na vaši polovinu, advokát ~2,5–5 tis.; notář 15 600 bez DPH celé = ~9 tis. za polovinu (nejdražší). Úspora ~3 tis. s advokátem na dohodnutém ceníku | hyponamiru.cz „Úschova kupní ceny“ (říjen 2026, WebFetch 5. 11. 2026); ČSOB sazebník nedohledán (ODHAD) |
| Prodej: placená inzerce 4 měs., 6 500 Kč/byt | 39 | 32 | 40–20 | ano (bez RK je to jediný zdroj kupců) | Sreality soukromník balíček 90 dní 3 993 + prodloužení 30 dní 1 331 = 5 324 s DPH, jako plátce odečtete 21 % → čistě 4 400. Doplnit Bezrealitky (cena prodeje nenalezena, ODHAD 0–2 tis.) a bazar/FB zdarma. Úspora ~6–12 tis. | `podklady/marketing.md` ř. 88 (Sreality, ceník bez data platnosti; Seznam v 2026 mění ceník po zásahu ÚOHS, nový ceník nedohledán); model.py ř. 105 |
| Prodej: smlouvu připraví AI (náklad 0) | 0 | 0 (+18 jako pojistka) | +30 až 0 | ano | Rizikové: katastr vklad zamítne nebo přeruší za chybu v identifikaci jednotky, podílu na společných částech, věcném břemeni; banka kupce často chce advokáta nebo vlastní vzor. Nejlevnější bezpečné: AI návrh + kontrola advokátem 2–4 tis./byt (ODHAD). Do zadání to nepřidávám, viz bod 3 | ODHAD |
| Ostatní: energie a zabezpečení prázdného domu, 3 000 Kč/měs (24 měs.) | 72 | 55 | 72–35 | jen zabezpečení a minimum energie (pojišťovna a ochrana před vandaly, topení v zimě jen pro stavbu) | Dům je odpojený, po obnovení připojení (60 v položce Elektřina) platíte stálé platby ~400–600 Kč/měs + GSM kamera/zámky ~1 000–1 500 Kč/měs. 2 200 Kč × 24 = 53. Staveništní spotřeba se s tím nekryje: do položky Elektřina patří jen přípojka, spotřeba stavby se platí odtud, takže 3 000 je správně a nechává krýt spotřebu. Úspora ~0 | model.py ř. 97 (ODHAD); `polozky/prodej-ostatni.md` ř. 21–22 (ODHAD) |
| Ostatní: pojištění a daň z nem. věcí, 1 650 Kč/měs | 40 | 40 | 62–24 | ano (banka vyžaduje pojištění zástavy; daň ze zákona) | beze změny; pojištění stavby ~15 tis./rok, daň ~4,8 tis./rok | model.py ř. 98; hypox.cz 2026, `dane-financovani.md` ř. 93–97, 206 |
| Ostatní: PENB | 15 | 12 | 35–6 | ano při prodeji bytu v bytovém domě (stačí jeden PENB na dům; zák. 406/2000 § 7a), vystavuje ho jen energetický specialista | firma/specialista 7–15 tis. (relia.cz, realfree.cz, klik.cz 2026); svépomoc ne. Architekt zdarma PENB nevystaví, pokud není oprávněný energetický specialista. Úspora ~3 tis. | `polozky/prodej-ostatni.md` ř. 25 |
| Ostatní: s. r. o. založení 10 + účetnictví 3 000 Kč/měs (24 měs.) | 82 | 82 | 110–60 | jen pokud zůstane s. r. o. (viz bod 4 a 5) | viz odpověď 1 níže; FO místo s. r. o. ušetří ~35 tis. na účetní a založení, ale model počítá o 300–500 tis. vyšší daň | model.py ř. 157–161 (fintaxo.cz 17. 8. 2026, uctujeme-fm.cz); vlastní vyhledání ceníku účetních selhalo |
| Ostatní: prohlášení vlastníka (advokát) | 24 | 24 | 45–16 | ano (bez něj nevzniknou jednotky ani nejde převést byt) | prohlaseni-vlastnika.cz ceník 2024: 15 609 s DPH pro 6 jednotek, jiná kancelář 45 000 bez DPH. Svépomoc nedoporučuji (katastr formální náležitosti zamítá), šablona od advokáta ušetří ~8 tis. | `polozky/prodej-ostatni.md` ř. 26 |
| Ostatní: geodet | 28 | 30 | 45–15 | ano (plány jednotek jako příloha prohlášení) | geonovotny.cz ~5 000 Kč/byt bez DPH → 30–36 s DPH; plátce odečte DPH | `polozky/prodej-ostatni.md` ř. 27; `dane-financovani.md` ř. 124 |
| Ostatní: poplatky katastru | 6 | 6 | 9–3 | ano | beze změny (2 000 vklad prohlášení + sbírka listin 1 000 + rezerva) | `dane-financovani.md` ř. 106–107 |
| Ostatní: založení SVJ | 12 | 12 | 20–6 | ano, viz odpověď 2 | stanovy od stejného advokáta jako prohlášení, notář odpadá (jediný vlastník) | `dane-financovani.md` ř. 128 |

## 2. Součet

| | Prodej | Ostatní | Celkem |
|---|---|---|---|
| Web | 63 | 279 | **342** |
| Můj real (stávající firma/řemeslník) | 59 | 261 | **320** (−6 %) |
| Nejlevnější rozumná s „svépomocí“ | 48 | 235 | **283** (−17 %) |

Důvod nejlevnější varianty: bankovní/advokátní úschova, jeden hlavní inzerát na Sreality + zdarma portály, šablona prohlášení; energie a pojištění se nedají snížit. Svépomoc u PENB, prohlášení a geodeta nepřipadá v úvahu (oprávněná osoba). S. r. o. → FO by dalších ~−35 tis., ale přináší daňovou ztrátu. Rozdíl webu proti mému realistickému odhadu je pod 10 %, tedy bez změny.

## 3. Chybí / dvakrát / podhodnocené

- **Likvidace nebo zrušení s. r. o. po prodeji:** model dává jen založení a měsíční účetní. Likvidace/výmaz s. r. o. ~15–35 tis. (ODHAD, neověřeno). Nebo ji nechat a účtovat dál. Řád ~+25 tis., nad prahem 10 % u Ostatní není.
- **Poplatek za návrh na vklad kupní smlouvy 2 000 Kč/byt = 12 tis.:** obvykle platí kupující, ale záleží na smlouvě (ČÚZK sazebník). Zahrnuto v rozpětí pes, ne v realistickém.
- **Znalecký posudek pro banky kupců:** neplatí prodávající, banka kupce si objednává odhad sama (cca 3–5 tis., hradí kupec). Nechybí.
- **Kolaudace/změna užívání nebytové části → byty:** správní poplatky a doklady jsou v položce Projekt/Nebytová část, ne zde (nezkoumáno, ODHAD 5–15 tis., ověřit tam).
- **Pojištění stavebních rizik (CAR) a odpovědnosti při stavbě:** v Ostatní není; firmy ho často mají v ceně. ODHAD 15–40 tis., ověřit u zhotovitele.
- **Nic dvakrát:** energie v „Ostatní“ a obnovení elektřiny 60 v „Elektřina“ se nekryjí (připojení vs. spotřeba). Pozor jen na PENB: pokud je energetické hodnocení už v Projektu (293 tis.), překrývá se (nezjistil jsem).
- **Provize/RK:** neřeším, prodej je bez RK.

## 4. Odpovědi na zvláštní otázky

1. **S. r. o. vs. FO:** zadání říká, že kupuje FO, ale model od 5. 11. 2026 počítá `FORMA = "sro"` (rozhodnutí uživatele „navrhni nejlepší“; model.py ř. 157–159) a web popisuje podání nabídky ČD přes s. r. o. (výpis z OR do 16. 11.). S. r. o. není právně nutná: FO jako OSVČ (§ 7 ZDP) s daňovou evidencí/účetnictvím a registrací k DPH jde. Rozdíl je v datech: model tvrdí, že s. r. o. vychází o 0,3–0,5 mil. lépe (DPPO 21 % + 15 % z dividendy proti 15/23 % a odvody FO; úroky jako náklad). Účetní pro plátce DPH: model ř. 160 uvádí 1 820–4 000 Kč/měs. (fintaxo.cz 17. 8. 2026); FO bez DPPO a závěrky o ~1 000 Kč/měs. levnější, ověření ceníku jiným zdrojem se nepodařilo. Neměním, doporučuji ověřit u daňového poradce, zda rozdíl 0,3–0,5 mil. platí (zejména po výplatě dividendy a likvidaci).
2. **SVJ u 6 jednotek:** § 1198 OZ (povinnost při ≥ 5 jednotkách a ≥ 4 různých vlastnících) → po prodeji 4. bytu povinné (`prodej-ostatni.md` ř. 36, `dane-financovani.md` ř. 128). Prakticky založit před prvním prodejem; jediný vlastník = stanovy bez notáře (§ 1200 odst. 4). Znění zákona jsem znovu nečetl na zakonyprolidi.cz.
3. **Prohlášení vlastníka a geodet:** 15,6–45 tis. (prohlášení), ~5 tis./byt (geodet); 2026, viz tabulka.
4. **Úschova:** banka (Č. spořitelna) 0,2 %, min 6 000, max 20 000; Creditas od 14. 11. 2026 0,2 %, min 5 000; notář 15 600 bez DPH při 6 mil.; advokát smluvní, Garanční fond ČAK do 5 mil. (od 2026) – hyponamiru.cz říjen 2026. ČSOB sazebník nenalezen. Inzerce: Sreality 3 993 + 1 331 s DPH na byt; Bezrealitky samotné stačit nemusí (pro prodej ceník nenalezen, ODHAD levné/zdarma), nejlepší kombinace obou. Smlouva od AI: viz řádek v tabulce, riziko zamítnutí vkladu.
5. **Energie odpojeného domu:** nekryje se se staveništní elektřinou (viz tabulka). Svépomocí: fotky, inzerci a prohlídky už rozhodnutí uživatele řeší (marketing_byt = jen inzerce); PENB nelze.

## 5. Doporučení

**Beze změny** obou položek (Prodej 63, Ostatní 279). Rozdíl proti mému realistickému odhadu je −6 %, pod prahem 10 %. Poznámka k s. r. o. (82 tis.): rozhodnutí uživatele, jen ověřit daňově; do rozpočtu doplnit případnou likvidaci (~25 tis.), která Ostatní zhruba vyrovná (261 + 25 ≈ 286).
