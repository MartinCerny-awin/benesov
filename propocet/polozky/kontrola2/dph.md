# Kontrola 2: DPH z prodeje po odpočtu (real, bez nástavby), 5. 11. 2026

Web: 1 792 tis. (= 3 095 − 1 132 − 103 − 69). Pozn.: aktuální `model.py` (V1 real, mix firma+řemeslníci, spuštěno 5. 11. odpoledne) dává **3 095 − 988 = 2 108 tis.**; rozpis odpočtu na webu (1 399/127/86 tis.) je jen proporcionálně škálovaný starý rozpis (`report.py` ř. 190–192), skutečné složky jsou: statické zajištění 1 500 × 12/112 = **161 tis.** (web 69), služby ~21/121 × ~300 tis. = ~52 (web 103), stavba zbytek. Součet odpočtu na webu je tedy rozpadnutý špatně a posunul se i celkově (web 1 304 vs. model 988); hodnotu položky je třeba po přegenerování ověřit.

## 1. Je DPH nutná? (zákon)
- Zdroj znění: `podklady/dane-financovani.md` ř. 63–67 (§ 56 ZDPH verze 2026 na zakonyprolidi.cz + Informace GFŘ č.j. 1127/26/7100-30116-051722); samotný text § 56/56a/79 jsem tentokrát nedočetl (stránka zakonyprolidi 616 tis. znaků, WebFetch ukázal jen začátek) → § 79 a § 76 označeno „ověřit“.
- První dodání dokončené věci / po podstatné změně do konce 23. měsíce po měsíci dokončení (po kolaudaci) = zdanitelné, jinak osvobozeno bez nároku na odpočet. „5 let / 2 roky“ jsou staré lhůty (do 6/2025), dnes **23 měsíců**.
- Podstatná změna (§ 56 odst. 5): cíl změnit využití / podmínky obývání **a** náklady bez DPH nesené prodávajícím > **30 % základu daně** dodání. Úroky se nepočítají, náklady předchozího vlastníka také ne, vlastní práce ano. **U jednotky se test dělá za každou jednotku zvlášť: přímé náklady přímo, společné podle podlahových ploch** (dane-financovani.md ř. 66).
- Pronájem je osvobozený (§ 56a), nic se nezdaňuje.

**Model ale test dělá souhrnně za dům** (`model.py` ř. 436–438, komentář „ponytail“) a vychází 31,2 % (RV, real; RF 32,3 %; pes 85 %, opt 25 %). To je těsně nad hranicí, takže celý dům je zdanitelný.

## 2. Test po jednotkách (moje přepočtení, ODHAD ±3 p. b.)
Data: `r["byty"]` z `model.run("V1","real")` (ceny bytů s DPH × idx, tržby 28,89 mil.), náklady bez DPH 8,05 mil. (31,2 % × 25,79 mil. bez DPH), z toho přímé N1+N2 ≈ 2,24 mil. (nebytová část 2,51 s DPH), zbytek 5,81 mil. společné (střecha, TČ, rozvody, statika 1,5 mil., byty).

| Skupina | cena bez DPH | náklady bez DPH (přímé + podíl podle m²) | podíl | výsledek |
|---|---|---|---|---|
| Staré byty A, B, C, D (264 m², 77 % hodnoty) | ~19,9 mil. | 4,46 mil. | **~22 %** | **osvobozeno** |
| Nové 2+kk N1, N2 (80 m², 23 % hodnoty) | ~5,8 mil. | 2,24 + 1,35 = 3,59 mil. | **~61 %** | zdanitelné 12 % |

Tzn. při správném (po jednotkách) výkladu GFŘ by staré byty už **nebyly** podstatnou změnou. Hranici by sice mohlo posunout, že rozdělení společných nákladů podle ploch dává novým bytům větší podíl než 23 %, ale i při 100 % přenesení společných nákladů na staré byty (8,05 − 2,24 = 5,81 mil.) je to 29 % → pořád < 30 %. Nutné ověřit s daňovým poradcem a případně závazným posouzením (GFŘ), ne spoléhat na můj výpočet.

Dopad (ODHAD): DPH na výstupu jen z N1+N2 ≈ 5,8 × 12 % = 0,70 mil.; odpočet z jejich nákladů (3,59 mil. × ~12 %) ≈ 0,43 mil. (a krácení společných vstupů koeficientem § 76) → čisté DPH ≈ **0,25–0,35 mil. místo 2,1 mil. → úspora ~1,8 mil. Kč (≈ 7 % všech nákladů)**. Tím ztratíte odpočet z části nákladů starých bytů (~0,5 mil.), ale to už je v čisté úspoře započteno.

## 3. Musí být kupující plátce už při nákupu? Odpočet
- Registrace není povinná při koupi ani rekonstrukci. Plátcem se FO stane povinně až při překročení obratu (2 mil. k 1. 1. dalšího roku, 2 536 500 Kč dnem následujícím), do obratu se počítá i osvobozené dodání nemovitosti, pokud není jen doplňková příležitostná činnost (§ 4a, dane-financovani.md ř. 13, 83). Registrace dobrovolná (§ 6 odst. 2 písm. a): v přihlášce lze uvést, že se chce stát plátcem určitým dnem; potvrzeno zakonyprolidi 5. 11. 2026).
- Odpočet z vstupů před registrací: model předpokládá registraci **před** první fakturou (ř. 441). Odpočet po pozdní registraci podle § 79 se týká jen zásob/majetku (ne služeb a prací, ODHAD – nedočteno), proto: **registrovat před první zakázkou**. Pokud ale zvolíte osvobozený prodej starých bytů (bod 2), registrace je potřeba jen kvůli novým bytům N1, N2 (a ty jsou v domě i dále společné vstupy).

## 4. Varianty
| Varianta | efekt na DPH | cena | verdikt |
|---|---|---|---|
| A) beze změny: souhrnný test | 2,1 mil. | 0 | model nyní |
| B) **test po jednotkách**, staré byty osvobozeny, N1/N2 zdaněny | ~0,3 mil. (−1,8 mil.) | prostě výklad GFŘ; riziko dodatečného vyměření, nutný poradce | nejlevnější, ale je to výklad, ne jistota |
| C) držet 24 měsíců po kolaudaci (pronajmout), prodat osvobozeně vše | 0 (−2,1 mil.) | +17 měs. úroků ~15,3 mil. × 6,2 %/12 = ~77 tis./měs. = ~1,3 mil. + držení ~0,08 mil.; nájem ~78 tis./měs. ≈ +1,3 mil. (ODHAD, dane-financovani.md ř. 82; model má B2h) → čistě ~0,1 mil. | vyrovnané až mírně výhodné, ale vyšší riziko trhu a banky; nové byty z nebytové části jsou „první dodání nové věci“ → osvobození až po 23 měs. |
| D) snížit náklady pod 30 % souhrnně | musí klesnout z 8,05 na ~7,7 mil. bez DPH (−0,35 mil., −4 %) | nutné ubrat ~0,4 mil. s DPH ze stavby | cesta k úspoře 2,1 mil. pouhou úpravou rozsahu (např. statika nebo část společných prací nesmí ale hnát „nutné“; svépomoc práce, lze ji počítat jako náklad, takže nepomůže) |
| E) prodat část bytů nerekonstruovaných | – | rekonstrukce všech bytů je zadání; nové byty z nebytové části nejdou bez stavby | nedoporučuji |
| F) svépomoc | práce „zdarma“ nesnižuje náklady testu (do nákladů se počítá i vlastní práce, GFŘ) | – | na test nemá vliv, kromě materiálové části |

Pozn. k D: je to jen 4 %, takže i „ušetřená“ věc u firmy/řemeslníka (levnější jádra, okna) hranici překročí. Ale pozor – nedělejte to uměle bez přepočtu po jednotkách; stačí B.

## 5. Kontrola výpočtu
- 12/112 z ceny **vč.** DPH: ano (`model.py` ř. 440 `trzby_prodej * 12 / 112`). Ceny bytů vycházejí z trhu s ojetými byty (osvobozeno) → DPH se vyřezává z ceny, nepřidává. Konzervativní: na trhu kupující FO nemá odpočet, takže může být těžké přidat 12 % navíc.
- Dává 3 095 smysl? Tržby (V1 real) 28,89 mil. s DPH × 12/112 = 3,095 mil. (zadání mělo ~29,7 – pro mix 28,89, pro RF stejně). Ano, vychází.
- Odpočet: stavba 12/112 u firmy; u řemeslníků jen materiál 21 % a podíl plátců; služby 21/121; statika 12/112 z 1,5 mil.; viz ř. 355–367. **Neobsahuje** provizi RK (nulová), ani DPH z drobných služeb prodeje (inzerce 6 × 6,5 tis. × 21/121 ≈ 7 tis.; advokát/úschova 4 tis. na byt ≈ 25 tis., PENB, dělení domu ~12 tis., energie ~12 tis.) → +50–70 tis. odpočtu, pokud je fakturují plátci (ODHAD, pod 3 %).
- Rozpad odpočtu na webu je neodpovídající (viz úvod).
- Svépomoc: práce bez DPH, ale bez odpočtu; do testu 30 % se počítá (GFŘ) → dává stejný podíl jako práce firmy, jen nižší hotové náklady.

## 6. Součet a doporučení
- Web 1 792 tis. · aktuální model 2 108 tis. (+18 %, jiná složka odpočtu, ověřit po deploy) · po jednotkách (varianta B) ~300 tis. (−86 %), držet 24 měs. (C) ~0 DPH, ale +1,4 mil. úrok/držení −1,3 mil. nájem.
- **Doporučení:** v modelu hodnotu neměnit (konzervativní, souhrnný test), ale **přidat poznámku**: pokud finanční správa přijme test po jednotkách, staré byty A–D jsou pod 30 % (~22 %) a DPH klesne na ~0,3 mil.; úspora ~1,8 mil. je největší jednotlivá páka v celém rozpočtu → nechat si od daňového poradce zpracovat výpočet po jednotkách a případně požádat o závazné posouzení (§ 38nb? – číslo ověřit) **před** začátkem stavby. Před přegenerováním webu opravit rozpad odpočtu v `report.py` ř. 190–192 (statika ~161 tis., služby ~52 tis., zbytek stavba).
- Vedlejší efekt mé práce: při ověřování jsem importoval `report.py`, což přepsalo `propocet/report.html` a `propocet/srovnani.html` (generované soubory, obsah = aktuální model).

---

## Kolo 2 (5. 11. 2026, doplněno na pokyn koordinátora)

### 1. Zákon (zakonyprolidi.cz/cs/2004-235, znění 2026, čteno 5. 11. 2026; e-sbirka nezkoušena)
- **§ 56 odst. 5** (podle výtahu z WebFetch, doslovně jen části): podstatná změna = změna dokončené věci s cílem změnit její využití nebo podmínky obývání, „pokud skutečné náklady vynaložené na tuto změnu bez daně osobou, která uskutečňuje bezprostředně následující dodání“ „přesáhnou 30 % základu daně při tomto bezprostředně následujícím dodání“. Dělí se tedy **základem daně z toho následujícího dodání** (cena dodání bez DPH), ne tržbou celého domu.
- **Po jednotkách:** zákon mluví o „bezprostředně následujícím dodání“ a § 56 odst. 7 řadí mezi vybrané nemovité věci i **jednotku**; test se tedy vztahuje na dodání té které jednotky už ze zákona (základ daně = cena jednotky). **Jak se na jednotku přiřadí společné náklady (podle podlahových ploch), zákon neříká; to je jen Informace GFŘ č.j. 1127/26/7100-30116-051722** (dauc.cz/predpisy/6393; obsah převzat z `podklady/dane-financovani.md` ř. 64–67, samotnou informaci jsem znovu nečetl, datum nevím).
- **Vlastní (nefakturovaná) práce:** zákon říká „skutečné náklady vynaložené … bez daně“; výslovně o vlastní práci nic nevím. Dokument `dane-financovani.md` ř. 66 uvádí, že GFŘ počítá i svépomoc, ale to jsem neověřil v originále. Berte jako **nejisté**.
- § 6 odst. 3 ZDPH a § 79, § 76: znění jsem nedočetl (§ 6 odst. 3 viz výše, § 76/79 jen ze znalosti).

### 2. Test po jednotkách s aktuálními čísly (ODHAD, nic nezapsáno, spuštěno jen `model.run("V1","real")` a aritmetika)
Aktuální stav sedí na web: DPH výstup 3 095, odpočet 988 (857+78+52), čisté 2 108 tis. Podíl souhrnně **31,2 %**, tržby 28,89 mil. s DPH, náklady bez DPH 8,05 mil. (z toho přímé N1+N2 ≈ 2,24 mil., společné 5,81 mil.). Ceny: model × 1,0532 (růst do prodeje). Společné náklady dle podlahových ploch (344 m²), 0,01689 mil./m².

| Jednotka | m² | cena s DPH | základ bez DPH | náklady bez DPH | test | režim |
|---|---|---|---|---|---|---|
| A 4+1 | 80 | 6,33 | 5,65 | 1,35 | 23,9 % | osvobozeno |
| B 2+1 | 67 | 5,70 | 5,09 | 1,13 | 22,2 % | osvobozeno |
| C 3+1 | 75 | 6,38 | 5,70 | 1,27 | 22,2 % | osvobozeno |
| D 1+1 | 42 | 3,91 | 3,49 | 0,71 | 20,3 % | osvobozeno |
| N1 2+kk | 40 | 3,29 | 2,94 | 1,12 + 0,68 = 1,80 | 61,2 % | 12 % |
| N2 2+kk | 40 | 3,29 | 2,94 | 1,80 | 61,2 % | 12 % |

(mil. Kč.) Přímé náklady bytů A–D jsem nerozlišoval (koupelny, okna apod. jsou v modelu společně); kdyby v nich byly přímé náklady rozložené nerovnoměrně, vyjde u dražšího bytu víc. Rezerva do 30 %: i při 100 % přenesení společných nákladů na A–D je podíl 29 % → mezi 20–29 %.

Čisté DPH:
- Výstup N1+N2: 2 × 3,288 × 12/112 = **0,705 mil.**
- Odpočet přímých nákladů N: 2,24 × 12,3 % (průměrné DPH ve vstupech: 0,988/8,05) = 0,275 mil.
- Odpočet společných vstupů 5,81 × 12,3 % = 0,713 mil., krácený koeficientem § 76 (podíl zdanitelných plnění: 5,87 / (5,87 + 22,31) ≈ **20,8 %**, ODHAD; podle ploch 23,3 %) → 0,15–0,17 mil.
- Odpočet celkem ≈ **0,43 mil.** → **čisté DPH ≈ 0,27–0,30 mil.** (místo 2,108) → **úspora ≈ 1,8 mil.** Nezapočteno: úprava odpočtu (§ 78 a násl.) a že koeficient § 76 u osvobozených dodání nemovitostí může mít speciální pravidla – ověřit.

### 3. Citlivost
- Souhrnný test: 31,2 % → pod 30 % by náklady bez DPH musely klesnout o 3,8 %, tedy o **~0,31 mil. bez DPH (~0,34 mil. s DPH)**. Web od 13:52 už toto snížení obsahuje (DPH 2 108 odpovídá mému běhu), podíl je pořád 31,2 %; rezerva jen 1,2 p. b. Změna cen bytů o −4 % (tržby) test překlopí také z druhé strany (podíl roste).
- Svépomoc, pokud se vlastní práce do testu nepočítá: každý 1 mil. bez DPH, který se udělá vlastníma rukama (práce ~45–50 % ceny stavby, materiál ne), sníží čitatele o práci; kdyby šlo svépomocí ~0,6 mil. práce, souhrnný test klesne ~29,7 % a dům by byl osvobozen. Pokud se naopak počítá (GFŘ?), svépomoc test neovlivní. Nutno ověřit; nespoléhat na to.
- Pozn.: souhrnný práh nepřekročit „náhodou“: při osvobození celého domu zmizí i odpočet (~0,99 mil.), ale také výstup 3,1 mil. (úspora ~2,1 mil.).

### 4. Ověřit u poradce
Přiřazení společných nákladů na jednotky (GFŘ, plochy), zda se počítá vlastní práce, § 76 koeficient u osvobozených dodání nemovitostí, úprava odpočtu, a zda by GFŘ nepovažovalo A–D za „bez změny obývání“ vůbec (pak se test nedělá, výsledek stejný).
