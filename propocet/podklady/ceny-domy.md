# Ceny celých domů a nájmů – Benešov a okolí (stav k 4. 11. 2026)

Podklad pro propočet č.p. 1598 Benešov (viz `_spolecne.md`). Všechna čísla mají zdroj a datum zdroje. Odhady jsou označeny **ODHAD**.

## 0. Co se podařilo a co ne

- **Sreality činžovní filtr nefunguje.** URL `sreality.cz/hledani/prodej/domy/cinzovni-domy/...` vrací rodinné domy, API `api/cs/v2/estates` vrací 404. Filtr jsem proto obešel: vyhledávání přes agregátory (sousede.cz, ereality.cz) a fulltextem.
- **Bezrealitky** výpis Benešova přes URL nevrátila (404). **iDNES Reality** a **RealityMix** jsem neprošel přímo, jen přes výsledky vyhledávání.
- **Cíl 8 objektů v okruhu 25 km nebyl splněn.** Dohledáno 6 objektů v okrese Benešov, z toho 1 je projekt, 3 nemají cenu. Přidány 2 objekty mimo okruh/okres, jsou označeny a do mediánů nezahrnuty.
- **Výsledky výběrových řízení ČD/ÚZSVM pro Benešov nebyly nalezeny.** Viz oddíl 2.

---

## 1. Činžovní a vícebytové domy – nabídky

### 1a. V okruhu do ~25 km (okres Benešov, Vlašim)

| # | Lokalita | Byty | Užitná / podlahová plocha | Pozemek | Cena (Kč) | Kč/m² | Stav | Datum zdroje | URL |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Benešov, Na Chmelnici | 4 samostatné jednotky | 206 m² (typ plochy neuveden) | neuvedeno | 12 499 000 | 60 675 (na 206 m²) | neuvedeno, byl by „činžovní dům“ | vloženo 24. 9. 2026 | https://www.sousede.cz/prodej/rodinne-domy/cinzovni-domy/benesov/prodej-cinzovniho-domu-206-m2-na-chmelnici-3902500.html (výpis sousede.cz 4. 11. 2026; detail vrátil 404) |
| 2 | Benešov u Prahy (256 01) | 2 identické bytové jednotky (dům 151 m²) | 151 m² (dům celkem) | neuvedeno | 11 500 000 | 76 159 (na 151 m²) | neuvedeno | neuvedeno | https://reality.hn.cz/detail/benesov/prodej-rodinneho-domu-151-m2-benesov-8580337.html (ověřit, zda totéž jako inzerát 8115151) |
| 3 | Bukovany, okr. Benešov (novostavba) | 3 samostatné obytné jednotky | 308 m² | 2 113 m² | cena na dotaz | n/a | novostavba, „kompletní celek“ | neuvedeno | https://reality.hn.cz/detail/bukovany/moderni-novostavba-bukovany-okres-benesov-8603339.html (detail vrátil 404, údaje ze snippetu vyhledávání) |
| 4 | Vlašim, Jana Očka (rozestavěný) | 11 (4× 1+kk, 4× 2+kk, 3× 3+kk) | bytů 592,79 m² (podlahová), navržená užitná celého domu 653,28 m² | 1 416 m² | **nebyla uvedena** (expats fetch 4. 11. 2026); search snippet uvádí 21 000 000 | 35 421 při 21 M (na 592,79 m²), jinak n/a | rozestavěno, nezkolaudováno, základy, zastřešení a okna hotové; nastěhování předpoklad 1. 7. 2027 | poslední aktualizace 13. 10. 2026 (expats), vloženo 8. 10. 2026 (sousede) | https://www.expats.cz/praguerealestate/for-sale/commercial/333436-apartment-building-in-vlasim ; https://www.sousede.cz/prodej/rodinne-domy/cinzovni-domy/vlasim/prodej-cinzovniho-domu-592-m2-jana-ocka-3916879.html |
| 5 | Netvořice, Hrubínova | neuvedeno | 322 m² (typ plochy neuveden) | neuvedeno | cena na dotaz | n/a | dle popisu kompletně dokončená investiční nemovitost | vloženo 29. 10. 2026 | https://www.sousede.cz/prodej/rodinne-domy/cinzovni-domy/netvorice/prodej-cinzovniho-domu-322-m2-hrubinova-3751634.html (detail vrátil 404) |
| 6 | Bystřice (Nesvačily) – **projekt, ne existující dům** | 8 plánovaných bytových jednotek | 182 m² (uvedeno) | neuvedeno | 9 680 000 | 53 187 (na 182 m²) | developerský záměr, stavební povolení neověřeno | vloženo 1. 7. 2026 | https://www.sousede.cz/prodej/rodinne-domy/cinzovni-domy/bystrice-benesov/prodej-cinzovniho-domu-182-m2-3443263.html (detail 404) |

Pozn.: Benešov, Na Chmelnici a Vlašim – oba údaje o ceně pocházejí z různých agregátorů a nejsou ověřeny v detailu.

### 1b. Mimo okruh – pro srovnání (nezahrnuto do mediánů)

| # | Lokalita | Byty | Plocha | Pozemek | Cena (Kč) | Kč/m² | Stav | Datum zdroje | URL |
|---|---|---|---|---|---|---|---|---|---|
| 7 | Beroun-Závodí (okr. Beroun, cca 45–50 km) | 3 jednotky | 228 m² | 678 m² | 9 999 000 | 43 855 | určeno k rekonstrukci | neuvedeno | https://www.ereality.cz/presmeruj/sreality/5a7d4ceac4f30306 |
| 8 | Horní Benešov (okr. Bruntál, Moravskoslezský kraj) | 12 bytů | 930 m² | neuvedeno | 24 000 000 | 25 806 (2,0 mil. Kč/byt) | částečně vybaveno, s parkováním; prodává vlastník | dostupnost 1. 7. 2026 | https://www.bezrealitky.com/properties-flats-houses/1035830-nabidka-prodej-domu-horni-benesov |

Vyřazeno: Heřmaničky, 550 m² „nájemní dům“ bez ceny a počtu bytů (ve skutečnosti penzion s restaurací a čerpací stanicí, ereality.cz); Bojanovice 260 m² za 29,8 mil. (Praha-západ, mimo okruh); Staré Křečany a Štětí (ČD, jiný kraj).

### 1c. Referenční: ČD č.p. 1598 (vyvolávací cena)

| Položka | Hodnota | Kč/m² |
|---|---|---|
| Cena | 8 326 000 Kč (výběrové řízení, zdroj: inzerát ČD NB503213, viz _spolecne.md) | |
| Budovy 384,46 m² (typ plochy nejasný) | | **21 660** |
| Užitná plocha **ODHAD** cca 320 m² (2 NP × ~190 m² bez společných částí cca 15 %) | | **26 020** |
| Pozemek parc. č. 2113/3, 239 m² | | 34 840 (na m² pozemku) |
| Byty: ODHAD 4 (A 4+1, B 2+1, C 3+1, D 1+1), cena na byt | | cca 2 080 000 Kč/byt |

Stav: zdevastovaný, svislé a šikmé trhliny, vlhkost a plíseň, starý kotel. Datum inzerátu z podkladů ČD (prohlídka 3. 11. 2026).

### Srovnání nabídek (okres Benešov, bez projektu a bez ceny)

- Nabídky s cenou v okrese (včetně projektu): Kč/m² **53 000 – 76 000**, medián **57 000** (n = 4: 53 187; 60 675; 76 159; a rozestavěný Vlašim 35 421 při 21 M → při n = 4 medián 56 900).
- Vzorek je malý, a navíc jde o nabídkové ceny.

---

## 2. Výsledky prodejů ČD / Správa železnic / ÚZSVM

**Výsledek výběrového řízení na podobný bytový dům v Benešově nebyl dohledán.** Nic nenašlo ani vyhledávání v médiích (ČT24, e15, TN, Property Forum) ani registr NNM.

| Objekt | Prodávající | Stav / typ | Cena | Datum | Výsledek | Zdroj |
|---|---|---|---|---|---|---|
| Benešov, Pražská ul. (bývalá šatlava 1815 + polyfunkční dům + stavební pozemek) | Naxos (realitka), vlastník neuveden | prodej v centru, územní plán počítá s bytovým domem | doporučená 14 900 000 | vyhlášeno 2017 (článek 20. 8. 2017) | **neznámý** (I. kolo končilo 27. 9. 2017) | https://www.estav.cz/cz/5436.domy-v-centru-benesova-vcetne-byvale-satlavy-jsou-na-prodej |
| Benešov u Prahy, pozemek 60 m² (NNM) | SŽ, zakladatel MD | nabízen pouze pozemek | 47 000 (měna neuvedena) | platnost do 9. 4. 2021 | neaktivní, výsledek neznámý | https://portal.gov.cz/nepotrebny-nemovity-majetek/94694 |
| Staré Křečany, bytový dům 2 jednotky | ČD | nabídka | 580 000 | neuvedeno | neznámý | výsledek vyhledávání (bez URL) |
| Štětí, bytový dům | ČD | nabídka | 885 000 | neuvedeno | neznámý | výsledek vyhledávání (bez URL) |
| Milín, bývalá železniční budova s bytem 3+1 | ČD, výběrové řízení | nejnižší nabídka min. 415 000 | neuvedeno | neuvedeno | neznámý | výsledek vyhledávání (bez URL) |
| Jičín, řadový dům (3 NP + 1 PP), v původním stavu | ÚZSVM, dražba | výchozí 13 500 000 | neuvedeno | neuvedeno | neznámý | výsledek vyhledávání (repost na webu s recenzemi, nízká důvěryhodnost) |
| Harrachov, 2 bytové domy s nájemníky | neuvedeno (snad stát/ČD) | veřejná soutěž | neuvedeno | neuvedeno | neúspěšné, ani po 7. pokusu nebyl zájemce | newstream.cz (výsledek vyhledávání, **neověřeno**) |

Obecný kontext: ČD podle dostupných zpráv opakovaně neúspěšně prodávalo bytové domy (historicky cca 470 domů k prodeji, tři neúspěšné dražby, bez zájemce ani při minimální nabídce 300 mil. Kč; zdroj výsledek vyhledávání, bez URL, **neověřeno**). Prodeje rozprodávají ČD i SŽ nejčastěji přes výběrové řízení; výsledky se obvykle nezveřejňují. Ceny u malých objektů jsou pod 1 mil. Kč, což neodpovídá ceně 1598.

---

## 3. Nájmy bytů v Benešově

### 3a. Nabídky pronájmu, Benešov (město), 15 kusů

Zdroj: sreality.cz (výpis hledání „pronájem bytů – Benešov“, stažen 4. 11. 2026, celkem 58 výsledků včetně okolí). Poplatky a služby výpis neuvádí, u všech je „neuvedeno“ – ověřit v detailu. Všechny nabídky aktivní k 4. 11. 2026 dle výpisu.

| # | Dispozice | Ulice | Plocha m² | Nájem Kč/měs. | Kč/m²/měs. | URL |
|---|---|---|---|---|---|---|
| 1 | 1+kk | Hodějovského | 28 | 12 500 | 446 | https://www.sreality.cz/detail/pronajem/byt/1+kk/benesov-benesov-hodejovskeho/2001076300 |
| 2 | 3+kk | Pražského povstání | 74 | 23 000 | 311 | https://www.sreality.cz/detail/pronajem/byt/3+kk/benesov-benesov-prazskeho-povstani/1501364300 |
| 3 | 2+kk | Dukelská | 53 | 15 490 | 292 | https://www.sreality.cz/detail/pronajem/byt/2+kk/benesov-benesov-dukelska/988553292 |
| 4 | 1+1 | Jana Švermy | 44 | 11 990 | 273 | https://www.sreality.cz/detail/pronajem/byt/1+1/benesov-benesov-jana-svermy/1932263500 |
| 5 | 2+kk | Konopišťská | 40 | 15 000 | 375 | https://www.sreality.cz/detail/pronajem/byt/2+kk/benesov-benesov-konopistska/498348108 |
| 6 | 2+1 | Vlašimská | 67 | 12 500 | 187 | https://www.sreality.cz/detail/pronajem/byt/2+1/benesov-benesov-vlasimska/3028025420 |
| 7 | 2+kk | Tyršova | 40 | 16 300 | 408 | https://www.sreality.cz/detail/pronajem/byt/2+kk/benesov-benesov-tyrsova/1188757580 |
| 8 | 2+kk | Benešov (ulice neuvedena) | 40 | 10 500 | 263 | https://www.sreality.cz/detail/pronajem/byt/2+kk/benesov-benesov-/63438924 |
| 9 | 1+kk | 102. pluku | 32 | 13 000 | 406 | https://www.sreality.cz/detail/pronajem/byt/1+kk/benesov-benesov-102-pluku/4217962572 |
| 10 | 1+1 | Nová Pražská | 46 | 8 500 | 185 | https://www.sreality.cz/detail/pronajem/byt/1+1/benesov-benesov-nova-prazska/2129264716 |
| 11 | 3+kk | Tyršova | 72 | 23 000 | 319 | https://www.sreality.cz/detail/pronajem/byt/3+kk/benesov-benesov-tyrsova/193658956 |
| 12 | 2+kk | Jiráskova | 42 | 16 000 | 381 | https://www.sreality.cz/detail/pronajem/byt/2+kk/benesov-benesov-jiraskova/1772490828 |
| 13 | 1+kk | Vnoučkova | 51 | 14 900 | 292 | https://www.sreality.cz/detail/pronajem/byt/1+kk/benesov-benesov-vnouckova/658706508 |
| 14 | 2+kk | Vnoučkova | 50 | 14 000 | 280 | https://www.sreality.cz/detail/pronajem/byt/2+kk/benesov-benesov-vnouckova/3885707340 |
| 15 | 1+kk | Tyršova | 44 | 13 900 | 316 | https://www.sreality.cz/detail/pronajem/byt/1+kk/benesov-benesov-tyrsova/404295756 |

**Mediány (Benešov, n = 15):**

| Skupina | n | Kč/m²/měs. medián | Rozpětí (Q1–Q3 přibližně) | Nájem Kč/měs. medián |
|---|---|---|---|---|
| Malé (1+kk až 2+1) | 13 | **292** | cca 270–385 | 13 900 |
| Velké (3+kk a větší) | 2 | **315** (311; 319) | málo dat | 23 000 |

Pozn.: malé byty jsou v rozptylu, 1+kk 28 m² vychází nejvýš; poplatky nejsou započteny.

### 3b. Statistiky nájmů

- **Realiťák roku + CEMAP + Reality.iDNES (okres Benešov):** 285 Kč/m² v březnu 2026, proti 228 Kč/m² v březnu 2025 (+25 %), nejvyšší meziroční růst z okresů. Článek ze 4. 5. 2026. Zdroj: https://www.fxstreet.cz/zpravodajstvi-200593.html (přetištěno z Realiťák roku, ověřeno v textu). Pozor: jde o průměr všech bytů v okrese, ne o medián typu.
- **Deloitte Rent Index Q2 2026:** ČR 343 Kč/m²/měs. (+1,2 % q/q). Zdroj: https://www.deloitte.com/cz-sk/en/Industries/real-estate/collections/rent-index.html (stav k 4. 11. 2026). Středočeský kraj 328 Kč/m² (+0,6 % q/q, sekundární zdroj, bez URL, tedy neověřeno). Okres Benešov samostatně v Rent Indexu nevykázán; je součástí středočeského průměru. Praha 2026 Q2: Praha 7 493, Praha 9 468 Kč/m².
- **Nabídkové vs. skutečné nájmy:** Deloitte i Realiťák pracují s nabídkami z portálů. Výsledky za smlouvy nejsou dostupné.
- **MMR cenová mapa nájemného:** nenalezena jako otevřený výpis pro okres Benešov.

---

## 4. Výnosnost

Prodejní Kč/m² bytů v Benešově (pro srovnání): **89 394 Kč/m²** (median, Housi.cz, aktualizace 4. 11. 2026, 65 aktivních nabídek; z Housi.cz 90 625 Kč/m², září 2026, 44 nabídek). Zdroj: https://www.housi.cz/prodej/byty/stredocesky-kraj/benesov/benesov

| Výpočet | Cena | Roční nájem | Hrubý výnos |
|---|---|---|---|
| Typický byt 2+kk, 41 m² (medián plochy), cena 89 394 × 41 m² | 3 665 000 | 15 245 × 12 = 182 940 (medián nájmů 2+kk, n = 6) | **5,0 %** |
| Typický byt 1+kk, 38 m² (medián), cena 3 397 000 | 3 397 000 | 13 450 × 12 = 161 400 (medián 1+kk, n = 4) | **4,8 %** |
| Byt 2+kk, 50 m² | 4 470 000 | 15 245 × 12 | 4,1 % |
| Celý dům, 4 jednotky, 206 m² (č. 1 výše), nájem ODHAD 290 Kč/m²×200 m² | 12 499 000 | 58 000 × 12 = 696 000 | **5,6 %** (ODHAD) |
| Celý dům, ČD 1598, užitná ODHAD 320 m², nájem ODHAD 290 Kč/m² | 8 326 000 | 1 114 000 | **13,4 %** (ODHAD, před rekonstrukcí a neobsazeností) |

Závěr: u jednotlivých bytů hrubý výnos **4–5 %**, po neobsazenosti a nákladech (ODHAD cca 25–30 % z hrubého) netto cca 3 %. U celých domů z nabídek cca 5,5–6 % hrubého (ODHAD, při ceně 53–76 tis. Kč/m²), při realistické ceně 40 tis. Kč/m² cca 8–9 %. U ČD 1598 výrazně vyšší, ale vyžaduje rekonstrukci.

Neobsazenost: **ODHAD**, žádný zdroj v podkladech.

---

## Shrnutí pro model

Všechna čísla v Kč/m² jsou nabídková (asking) nebo ODHAD, pokud není uvedeno jinak.

| Veličina | Pesimistické | Realistické | Optimistické | Zdroj / poznámka |
|---|---|---|---|---|
| Cena celého domu Kč/m² (užitná, existující 2–8 bytů, okres Benešov) | **22 000** | **40 000** | **57 000** | pes.: ČD vyvolávací 8 326 000 / 384 m² = 21 660; real.: ODHAD cca 45 % cen bytů (89 394); opt.: medián nabídek v okrese (53–76k, n = 4) |
| Nájem malé byty (1+kk–2+1) Kč/m²/měs. | **265** | **292** | **315** | medián 292 (n = 13, sreality, 4. 11. 2026); pes. dolní kvartil |
| Nájem velké byty (3+kk+) Kč/m²/měs. | **285** | **315** | **330** | n = 2 (311; 319), okres 285 (Realiťák, březen 2026); ODHAD horní mez |
| Neobsazenost | **12 %** | **8 %** | **5 %** | ODHAD, žádný zdroj |
| Hrubý výnos bytů | 4 % | 5 % | 5,5 % | výpočet z oddílu 4 |
| Hrubý výnos celého domu (nájem Kč/m² × 12 / cena Kč/m², před neobsazeností) | 15,9 % (při ceně 22 000; nereálně nízká cena) | 8,8 % (při ceně 40 000) | 6,1 % (při ceně 57 000) | ODHAD, dopočet z řádků výše; sloupce jsou vázány na cenu, ne na scénář výnosu |
| Prodejní Kč/m² bytů v Benešově (pro kontrolu) | 85 000 | 89 400 | 91 000 | Housi.cz, 4. 11. 2026 |
| Deloitte Středočeský kraj nájem Kč/m²/měs. (Q2 2026) | – | 328 | – | sekundární zdroj, neověřeno |

---

## Otázky k ověření

1. **Vlašim, Jana Očka (č. 4):** expats.cz v detailu uvádí „cena nebyla uvedena“, ale v search snippetu je 21 000 000 Kč. Který údaj je aktuální? Potvrdit přímo na inzerátu nebo u RK Broker Consulting / REALITYSPOLU.
2. **Benešov u Prahy 151 m² (č. 2):** je to totéž co inzerát 8115151 (reality.hn.cz)? Počet bytů a dispozice, datum.
3. **Na Chmelnici 206 m² (č. 1) a Netvořice (č. 5):** detailní stránky sousede.cz vrátily 404. Ověřit plochu (užitná, podlahová, zastavěná), počet bytů, stav a cenu.
4. **Bukovany (č. 3):** cena na dotaz, 3 jednotky. Ověřit, zda se prodává celek a jestli je možné oddělení.
5. **ČD 1598:** kolik bytů a jaké jejich plochy (ČD prohlídka nebo prospekt NB503213), zda je užitná plocha blíže 320 než 384 m². Jaké jsou požadavky výběrového řízení (min. nabídka, ceny za m²) a zda ČD zveřejní výsledek.
6. **Výsledek ČD/SŽ/ÚZSVM výběrového řízení pro podobné bytové domy v okrese Benešov:** nebylo dohledáno. Zkusit nemovitosti.ceskedrahy.cz a nabidkamajetku.gov.cz s filtrem okres Benešov, případně NEN.
7. **Nájmy:** poplatky (služby, kauce, energie) nejsou ve výpisu sreality. Potřeba ověřit alespoň u 5 nabídek, aby se dal přepočítat Kč/m² včetně poplatků.
8. **Realiťák 285 Kč/m² (březen 2026):** definice (nabídky, medián, průměr) a plocha. Potvrdit v originálním článku Reality.iDNES.
9. **Deloitte Q2 2026 Středočeský kraj 328 Kč/m²:** potvrdit v PDF Rent Indexu, zda je okres Benešov zahrnut a jak je počítán.
10. **Neobsazenost** v Benešově: chybí zdroj. Doporučuji zjistit u RK nebo z ČSÚ (sčítání 2021, podíl neobydlených bytů v okrese).
11. **Vlašim, Jana Očka:** předpokládaný termín 1. 7. 2027 a stav rozestavěnosti – jak ovlivní cenu a riziko kolaudace?
12. **Vynechané zdroje:** RealityMix a iDNES Reality přímo neprošly (pouze přes vyhledávání). Pro úplnost doplnit.
