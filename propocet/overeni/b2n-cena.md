# Nezávislý odhad ceny: byt 2+kk ~55 m², 1. NP, Jana Nohy 1598, Benešov

Datum zpracování: 4. 11. 2026. Vše mimo označení **ODHAD** je dohledaný údaj se zdrojem a datem.
Do složky /Users/martincerny/Documents/Benesov/ jsem nic nečetl; zapsán je jen tento soubor.

## 0. Shrnutí

- **ODHAD realizované ceny (po rekonstrukci, 1. NP, kolaudovaný byt): ~83 000 Kč/m², tj. ~4,6 mil. Kč** (pesimisticky 67 000 Kč/m² = 3,7 mil.; optimisticky 97 000 Kč/m² = 5,3 mil.).
- **ODHAD srovnávací základ (stejný byt ve vyšším patře, po rekonstrukci, Benešov): ~92 000 Kč/m², tj. ~5,06 mil. Kč** (85 000–100 000 Kč/m² = 4,7–5,5 mil.).
- Sleva za přízemí v Benešově: z vlastních dat (Sreality, nabídky 4. 11. 2026) 7 % (Benešov město, n=3 vs 6) až 9 % (okres) až 13 % (okres, byty 35–75 m²). Studie: 7 % (RE/MAX), 2,5 % (VŠE, Praha), cca 7–8 % (Seznam Zprávy, Praha).
- Sleva za bývalý nebytový prostor: pokud bude byt zkolaudovaný a v katastru veden jako **byt**, právní sleva je malá nebo žádná. Pokud se prodává jako **nebytová jednotka / ateliér**, publikovaná sleva je 10–30 % a hypotéka je problém.
- Největší riziko pro cenu není přízemí, ale **prokazatelný stav kolaudace a katastru + výsledek bankovního odhadu** u kupujícího na hypotéku.
- Nabídka → prodej: aktuálně cca 5–6 % (Valuo, říjen 2026); na vzorku REAS v okrese Benešov medián 8 %, ale s velkým rozptylem (3–26 %).

## 1. Srovnatelné přízemní byty (1. NP / zvýšené přízemí)

Zdroj: Sreality JSON API `https://www.sreality.cz/api/v1/estates/search?category_main_cb=1&category_type_cb=1&locality_district_id=48&limit=100` (77 nabídek v okrese, staženo 4. 11. 2026) a detail `https://www.sreality.cz/api/v1/estates/<id>`. Pole `floor_number`=1 znamená 1. NP (přízemí / zvýšené přízemí); u Benešova potvrzeno v textech inzerátů ("1.NP", "přízemí"). Všechno jsou **nabídkové ceny** (ne realizované). Sloupec "od" = datum vložení inzerátu (`since`).

| # | Lokalita, ulice | Dispozice, plocha | Stav | Nabídková cena | Kč/m² | Od | ID / URL detailu |
|---|---|---|---|---|---|---|---|
| 1 | Benešov, Vlašimská | 3+1, 76 m² | po precizní rekonstrukci, cihla, společná uzavřená zahrada, sklep 6,5 m² | 7 500 000 | 98 684 | 30. 10. 2026 | 2898395212 |
| 2 | Benešov, F. V. Mareše | 2+kk, 68,7 m² vnitřní (Sreality 76 m²) | rekonstrukce 2021, terasa 12,5 m² | 6 990 000 | 91 974 (na 68,7 m²: 101 748) | 28. 8. 2026 | 4158046284 |
| 3 | Benešov, Na Tržišti | 3+1, 88 m² | dobrý, udržovaný, částečně vybavený | 6 435 000 | 73 125 | 28. 9. 2026 | 114368588 |
| 4 | Vlašim, Žižkovo nám. | 2+kk, 39,7 m² | velmi dobrý, revitalizace domu 2003, elektrické topení | 3 499 000 | 87 475 | 18. 9. 2026 | 2366120012 |
| 5 | Vlašim, B. Martinů | 2+1, 52 m² | zvýšené přízemí, dům po zateplení a výměně oken, byt k rekonstrukci | 3 990 000 | 76 731 | 2. 11. 2026 | 2521825356 |
| 6 | Vlašim, Ppor. Příhody | 2+1, 60 m² | velmi dobrý, 1. NP, 2 sklepy 15 m² | 4 500 000 | 75 000 | 18. 8. 2026 | 3154034764 |
| 7 | Vlašim, Severní | 2+1, 55 m² | před rekonstrukcí | 3 900 000 | 70 909 | 5. 7. 2026 (4 měsíce bez prodeje) | 1305075788 |
| 8 | Vlašim, U Lesa | 3+1, 73 m² | přízemí, právě v kompletní rekonstrukci, terasa 26 m², zahrada 431 m², parkování 2 auta | 5 890 000 | 80 685 | 8. 10. 2026 | 57544780 |
| 9 | Vlašim, V. Hálka | 3+1, 75 m² (Sreality uvádí 150 m² včetně zahrady) | po kompletní rekonstrukci, zahrada 75 m², parkování, sklep | 5 540 000 | 73 867 (na 75 m²) | 1. 11. 2026 | 129040460 |
| 10 | Domašín u Vlašimi | 2+1, 55 m² | po kompletní rekonstrukci, 2 sklepy; patro jen z pole API, v textu neověřeno | 4 499 000 | 81 800 | 19. 10. 2026 | 141230156 |
| 11 | Netvořice, Pod Strání | 4+kk, 78 m² | po rekonstrukci, zahrada 60 m² | 6 599 000 | 84 603 | 26. 9. 2026 | 4168163404 |
| 12 | Postupice, Blanická (novostavba/projekt) | 2+kk, 68 m² | projekt, předzahrádka | 5 779 800 | 84 997 | 1. 2. 2026 | 2086433612 |

Poznámky:
- V samotném Benešově jsou k 4. 11. 2026 jen 3 přízemní nabídky (řádky 1–3). Bezrealitky (nelze filtrovat podle patra, výpis nevrátil Benešov) a iDNES (nedostupné pro fetch) jsem využít nemohl; REAS "prodané" patro neuvádí. Přímo srovnatelný (malý, přízemní, po rekonstrukci, Benešov) byt k dispozici není, nejbližší je řádek 2 (2+kk, 1. NP, rekonstrukce 2021, ale s terasou).
- Realizované ceny přízemních bytů v Benešově nejsou veřejně dohledatelné (REAS neuvádí patro). Proto vše níže u přízemí vychází z nabídkových cen a z tržního odečtu nabídka → prodej.

## 2. Sleva za přízemí

### 2a. Vlastní data (Sreality, nabídkové ceny, 4. 11. 2026)

Vyloučeny stavy Novostavba / Projekt / Ve výstavbě / V rekonstrukci a byty > 110 m². Medián Kč/m².

| Výběr | Přízemí (1. NP) | 2.–3. NP | 4. NP a výš | Přízemí vs 2.–3. NP |
|---|---|---|---|---|
| Celý okres, všechny velikosti | 78 708 (n=14) | 86 366 (n=30) | 84 762 (n=12) | **−8,9 %** |
| Okres, 35–75 m² | 75 866 (n=8) | 87 034 (n=24) | 84 677 (n=11) | **−12,8 %** |
| Města Benešov, Vlašim, Votice, Týnec, Sázava, Čerčany | 81 242 (n=10) | 87 019 (n=21) | 84 848 (n=11) | **−6,6 %** |
| Benešov město | 91 974 (n=3) | 98 757 (n=6) | 94 318 (n=4) | **−6,9 %** (velmi malý vzorek) |
| Vlašim | 78 708 (n=6) | 76 319 (n=5) | 84 848 (n=3) | **+3 %** (žádná sleva; směs stavů) |

Párování ve stejném domě / projektu:
- Netvořice, Pod Strání (všechny "po rekonstrukci", cihla): 1. NP 4+kk 78 m² 84 603 Kč/m² (se zahradou 60 m²) vs 2. NP 3+kk 60 m² 89 167 a 3. NP 4+kk 58 m² 92 241 → přízemí −5 až −8 %, ale větší byt a zahrada (velikost sama tlačí Kč/m² dolů).
- Postupice, Blanická (novostavba): 1. NP 2+kk 68 m² 84 997 vs 2. NP 2+kk 67 m² 83 999 a 83 126 → přízemí +1 % (developer cenu nesnižuje; přízemí má předzahrádku).

Závěr vlastních dat: **sleva přízemí ≈ 7–9 % (rozptyl 0–13 %)**. Vzorky jsou malé, stavy nejsou plně sjednocené, jde o nabídky.

### 2b. Studie a články (ČR)

| Zdroj | Údaj | Datum / poznámka |
|---|---|---|
| EnergoZrouti.cz, citace analýzy RE/MAX (~100 000 prodaných a pronajatých bytů) | přízemní byty v průměru o **7 %** levnější než ve vyšších patrech; obecný nezdrojovaný rozsah "20–40 %" a nájem −10 až −20 % | článek 8. 4. 2026; období analýzy RE/MAX neuvedeno; rozsah 20–40 % bez zdroje, nepoužít |
| Seznam Zprávy (K. Štuková), data Sreality a Bezrealitky | Praha: podzemní/přízemní jednotky nabízeny cca 132 000 Kč/m², vyšší patra jen cca +10 000 Kč/m² (cca 7–8 %, můj přepočet); Sreality: "už to není automaticky výrazně levnější nabídka"; doba prodeje ~64 dní vs ~40 dní u běžného bytu | 18. 7. 2025; Praha, nabídkové ceny |
| Diplomová práce M. Vinterová, VŠE (hedonická metoda, 1 185 prodaných 3+1/3+kk, Praha 2007–2012) | přízemí **−2,5 %** | obhájeno 8. 9. 2014, https://vskp.vse.cz/english/43494 |
| Diplomová práce M. Pokorný, VŠE (1 100 bytů, 8 měst ČR) | přízemní byty "výrazně levnější", procento nezjištěno | 2016, https://vskp.vse.cz/english/50313 |

Závěr: **sleva 7 % je podložená (RE/MAX + vlastní data), 2,5–13 % je rozumný rozptyl.** Malé město s nízkou poptávkou po bytech a dobrou přízemní dispozicí (zahrada) sleva klesá; byt bez výhledu, bez soukromí a s okny do cizí zahrady spíš nahoru.

## 3. Sleva za byt vzniklý z nebytového prostoru

Rozhodující je právní stav v okamžiku prodeje.

| Stav | Sleva / dopad | Zdroj |
|---|---|---|
| Prodává se jako nebytová jednotka / ateliér (před rekolaudací) | ateliéry zpravidla **10–30 % levnější** než srovnatelné byty; banky často nepůjčí vůbec, jinde LTV cca 60–70 %, úvěr může být strukturován jako podnikatelský; nižší odhad pro hypotéku | Finance.cz, rozhovor s M. Kovářem (Explicit Reality), 23. 5. 2025, https://www.finance.cz/clanky/553082-vypada-jako-byt-ale-neni-makler-varuje-pred-nastrahami-atelieru/ |
| Dtto | "Banky na nebytový prostor hypotéku neposkytnou"; u přestaveb na byt LTV klidně 60–70 %; odhadní cena ateliéru bývá nižší než u srovnatelného bytu, odhadce použije snižující koeficient (procento neuvedeno) | hyponamiru.cz, 3. 9. 2025, https://www.hyponamiru.cz/?p=15820 |
| Koupě nebytového prostoru | klasická účelová hypotéka nelze; možná americká hypotéka s jinou zástavou, nebo spotřebitelský úvěr (vyšší úrok, kratší splatnost) | hyponamiru.cz, aktualizace 11. 7. 2025, https://www.hyponamiru.cz/hypoteka-na-nebytovy-prostor/ |
| Přestavba na byt financovaná hypotékou | banky chtějí doložit možnost rekolaudace; typicky 100 % prostředků na rekonstrukci z banky | tamtéž |
| Banky 2017 (historicky) | mBank: do 100 m², LTV 80 %, individuálně; ČSOB: nutno zajistit rekolaudaci; Raiffeisenbank: jen se zástavou druhé nemovitosti; ČS: ano, pokud vznikne bytová jednotka; Sberbank: individuálně | e15.cz, 28. 11. 2017, https://www.e15.cz/finexpert/bydlime/hypoteka-na-nebytove-prostory-jen-u-nekterych-bank-1340300 (zastaralé) |
| Kolaudovaný byt vs ubytovací jednotka | při vyšším technickém standardu je rozdíl "spíše právní povahy", ne technické | Právní prostor (Grygar, Petřek), 17. 1. 2024 |
| Problémové vlastnosti přestaveb | typické důvody, proč jednotka nebyla byt: nedostatek denního světla, nevhodná orientace, přízemí/suterén, orientace do světlíku; horší osvětlení, větrání, akustika | Finance.cz 23. 5. 2025 (výše) |

Dopad na tento byt (ODHAD):
- **Pokud bude pravomocná kolaudace změny účelu užívání na byt a zápis v katastru "byt": ODHAD sleva 0–5 % (realisticky 3 %)**, za stigma bývalé dílny/kotelny, nižší světlou výšku, okna do cizího pozemku (soukromí, stín), chybějící parking, sklep a balkon. Přímý dohledatelný benešovský příklad ceny takto vzniklého bytu jsem nenašel.
- **Pokud se bude prodávat před rekolaudací / jako nebytová jednotka: ODHAD sleva 15–30 %** a okruh kupců jen za hotové/americkou hypotéku. Pesimistický scénář níže počítá s horní mezí kolaudovaného stavu, ne s tímto; je to samostatné riziko k odstranění přípravou prodeje.
- Doporučení pro cenotvorbu: nabízet až po právní moci kolaudace, zápisu do katastru a s bankovním odhadem (kupující s hypotékou je rozhodující segment u bytu 4–5 mil.).
- Ze Seznam Zpráv: bytům s nedostatky se majitelé snaží držet ceny na úrovni bytů bez nedostatku, ale doba prodeje je delší (~64 vs ~40 dní). To podporuje počítat spíš s delším prodejem než s hlubokou slevou.

## 4. Nabídkové vs realizované ceny

| Zdroj | Sleva nabídka → prodej | Datum / rozsah |
|---|---|---|
| Valuo (R. Šitera) přes Newstream | **5–6 % aktuálně**; 2024–2025 cca 2 %; začátek 2023 cca 11,5 % | Newstream 8. 10. 2026, ČR, bez regionů |
| Valuo / Seznam Zprávy (data z katastru) | byty v průměru **−2,3 %** od první ceny; celkový rozdíl všech nemovitostí 1,4 %; 46 % prodáno pod nabídkou | 8. 12. 2020, ČR (starší, klidnější trh) |
| Valuo / Banky.cz | průměr "cca 21 %" napříč ČR; Praha/Brno/Plzeň 10–15 %; Středočeský kraj neuveden | aktualizace 3. 2. 2026; metodika nejasná, výrazně vyšší než ostatní zdroje; **nepoužívám** |
| REAS prodané, okres Benešov (ručně spočteno z 8 záznamů s oběma cenami) | rozsah 2,7–25,8 %, **medián 8,2 %, průměr 11,5 %**; Benešov město: Jiráskova −19,1 %, Antuškova −5,8 %, Kpt. Nálepky −5,7 %, Bezručova −5,6 %, Zapova −25,8 % | prodeje 16. 4. 2025 – 23. 4. 2026, https://www.reas.cz/prodane/byty/okres-benesov |

Upozornění k REAS: u záznamů jsou ceny převzaté z inzerce (u Rubešovy je uvedeno, že cena zahrnuje provizi RK a právní servis); nemusí odpovídat kupní smlouvě. Patro REAS neuvádí; u ověřených záznamů zjištěno ručně: Jiráskova 4. NP, Rubešova 2. NP, Na Chmelnici 3. NP.

Pro odhad používám: **realizovaná cena ≈ nabídková −6 % (rozsah −3 % až −12 %)**. U přízemního bytu s delší dobou prodeje je spodní polovina rozsahu pravděpodobnější. Dlouho neprodané nabídky v Benešově: Nová Pražská 43 m² 5,65 mil. (od 11. 10. 2025, 13 měsíců), Rubešova 38 m² 4,39 mil. (od 3. 10. 2025), 2+kk 52 m² 4,95 mil. (od 16. 3. 2026) – jejich nabídkové ceny tedy zjevně nejsou realizovatelné.

## 5. Srovnávací základ: malý byt 2+kk po rekonstrukci ve vyšším patře, Benešov

Realizované (REAS, ověřeno na detailu):

| Byt | Plocha | Patro | Stav | Cena | Kč/m² | Prodáno |
|---|---|---|---|---|---|---|
| Rubešova 551, 2+kk | 37,7 m² | 2. NP | modernizace 2022, částečně vybaveno vč. kuchyně | 4 297 000 | 114 000 (REAS: 116 135 na 37 m²) | 12. 9. 2025 |
| Na Chmelnici 1998, 1+kk | 30 m² | 3. NP | dům 2016, zánovní | 3 450 000 | 115 000 | 9. 9. 2026 |

Aktuální nabídky (Sreality, 4. 11. 2026), malé byty ve vyšším patře v Benešově:

| Byt | Patro | Nabídka | Kč/m² | Od |
|---|---|---|---|---|
| Rubešova 2+kk 45 m², rekonstrukce domu 2017, parking. stání, sklep (2861879372) | 2. NP | 4 990 000 | 110 889 | 11. 8. 2026 |
| Rubešova 2+kk 38 m² (2659636044) | 2. NP | 4 390 000 | 115 526 | 3. 10. 2025 |
| Nová Pražská 2+kk 43 m², kompletní rekonstrukce, panel (1693434700) | 4. NP | 5 650 000 | 131 395 | 11. 10. 2025 |
| Benešov 2+kk 52 m², velmi dobrý, panel (3603256140) | 5. NP | 4 950 000 | 95 192 | 16. 3. 2026 |
| Na Bezděkově 2+kk 61 m², panel s výtahem, revitalizovaný (2654720076) | 7. NP | 5 700 000 | 93 443 | 22. 7. 2026 |

Pozorování: Kč/m² klesá s velikostí (37 m² ≈ 114 000; 52–61 m² ≈ 93–95 000 v nabídkách). Byt ~55 m² leží mezi 52 m² a 61 m² nabídkami.

**ODHAD základu pro 55 m², 2+kk, rekonstruovaný, vyšší patro, Benešov (realizovaná cena):**

| Scénář | Kč/m² | Celkem (55 m²) | Odůvodnění |
|---|---|---|---|
| Pesimisticky | 85 000 | 4,68 mil. | nabídky 93–95 tis. −9 až −10 % |
| Realisticky | 92 000 | 5,06 mil. | nabídky ~97–100 tis. (interpolace 52–61 m² a prémie za stav) −6 % |
| Optimisticky | 100 000 | 5,50 mil. | nabídky ~105 tis. −5 %; blíž k realizovaným malým bytům 114 tis. |

## 6. ODHAD ceny bytu na Jana Nohy 1598 (1. NP, 2+kk ~55 m², po rekonstrukci)

Výpočet (ODHAD): základ × (1 − sleva za přízemí) × (1 − sleva za původ z nebytového prostoru a nevýhody lokality/vybavení).

| Scénář | Základ Kč/m² | Přízemí | Nebyt. původ + nevýhody* | Kč/m² | Celkem (55 m²) |
|---|---|---|---|---|---|
| Pesimisticky | 85 000 | −12 % | −10 % | **≈ 67 000** | **≈ 3,7 mil. Kč** |
| Realisticky | 92 000 | −7 % | −3 % | **≈ 83 000** | **≈ 4,6 mil. Kč** |
| Optimisticky | 100 000 | −3 % | 0 % | **≈ 97 000** | **≈ 5,3 mil. Kč** |

\* Okna do dvora/cizího pozemku, bez parkování, sklepa a balkonu, ex-dílna/kotelna, nižší světlá výška (neznámá). Pesimistický scénář −10 % předpokládá kolaudovaný byt s horšími reálnými parametry; **při prodeji jako nebytová jednotka by cena byla ještě o dalších cca 15–30 % nižší (ODHAD, pásmo 2,6–3,3 mil.)**.

Křížová kontrola (nabídky přízemních bytů v Benešově): Vlašimská 3+1 98,7 tis., F. V. Mareše 2+kk 92–102 tis. (obojí s výhodami: sklep, zahrada/terasa), Na Tržišti 73 tis. (nižší stav). Po odpočtu 6 % za realizaci a chybějícího sklepa/terasy/parkingu vychází 80–88 tis. Kč/m², tedy konzistentní s realistickým scénářem. Nabídková cena pro inzerci při realistickém scénáři: ODHAD ~4,9 mil. Kč (≈ 89 000 Kč/m²), aby po slevě 6 % vyšlo ~4,6 mil.

Faktory, které mohou posunout nahoru: nová okna, nové rozvody, tepelné čerpadlo (nízké náklady na bydlení), nový dům/byt po kompletní rekonstrukci bez rizika fondu oprav; poloha 6 min od nádraží; malý byt = malá celková částka, širší okruh kupců. Faktory dolů: soukromí okna, bez parkování (u konkurenčního Rubešova je parking. stání v ceně), široká nabídka starších bytů a vysoké hypoteční sazby (průměrná nabízená sazba 5,19 % v květnu a 5,30 % v červnu 2026; Banky.cz, 17. 7. 2026), delší doba prodeje přízemních a atypických bytů.

## 7. Souhrnná tabulka

| Položka | Hodnota | Typ | Zdroj / datum |
|---|---|---|---|
| Přízemní nabídky v okrese Benešov, medián | 78 708 Kč/m² (n=14) | data | Sreality API, 4. 11. 2026 |
| 2.–3. NP v okrese, medián | 86 366 Kč/m² (n=30) | data | totéž |
| Sleva přízemí, vlastní data | 7–13 % (Benešov 6,9 %, okres 8,9 %, 35–75 m² 12,8 %) | data | totéž |
| Sleva přízemí, RE/MAX | 7 % | studie | EnergoZrouti.cz, 8. 4. 2026 |
| Sleva přízemí, VŠE Praha | 2,5 % | studie | Vinterová, 2014 |
| Sleva přízemí, Praha nabídky | ~7–8 % | data | Seznam Zprávy, 18. 7. 2025 |
| Sleva ateliér / nebytový prostor | 10–30 % | broker | Finance.cz, 23. 5. 2025 |
| LTV pro přestavby nebyt → byt | 60–70 % (banky mohou snížit) | článek | hyponamiru.cz, 3. 9. 2025 |
| Sleva nabídka → prodej, ČR | 5–6 % aktuálně | data | Newstream/Valuo, 8. 10. 2026 |
| Sleva nabídka → prodej, REAS okres Benešov | medián 8,2 %, rozsah 2,7–25,8 % (n=8) | data | reas.cz, prodeje 4/2025–4/2026 |
| Realizovaný malý 2+kk, vyšší patro, Benešov | 114 000 Kč/m² (37,7 m², 4,297 mil.) | data | REAS, prodáno 12. 9. 2025 |
| Základ 55 m², vyšší patro, po rekonstrukci | 85 / 92 / 100 tis. Kč/m² = 4,7 / 5,1 / 5,5 mil. | **ODHAD** | tento dokument |
| Byt J. Nohy 1598, realizovaná cena | **67 / 83 / 97 tis. Kč/m² = 3,7 / 4,6 / 5,3 mil.** (pes. / real. / opt.) | **ODHAD** | tento dokument |
| Doporučená nabídková cena | ~4,9 mil. Kč (≈ 89 tis. Kč/m²) | **ODHAD** | tento dokument |
| Pokud nebytová jednotka | dalších −15 až −30 % (cca 2,6–3,3 mil.) | **ODHAD** | tento dokument, podle Finance.cz 2025 |

## 8. Omezení

- Žádný přímý realizovaný prodej přízemního bytu v Benešově dohledán nebyl; REAS patro nezobrazuje. Přízemní sleva vychází z nabídek (n=3 v Benešově, n=14 v okrese).
- REAS "prodané" ceny jsou převzaté z inzerce a mohou být poslední nabídkou, ne kupní smlouvou.
- Bezrealitky, iDNES a realitní kanceláře nelze strojově filtrovat podle patra; Sreality je jediný úplný zdroj. Údaj 21 % (Banky.cz/Valuo) a rozsah 20–40 % (EnergoZrouti.cz) nepoužívám pro slabou metodiku.
- Nevím skutečnou plochu (užitná vs podlahová), světlou výšku, orientaci oken, stav kolaudace ani cenovou politiku vlastníka; změna kteréhokoli posune odhad více než ± 5 %.
- Odhad není znalecký posudek.
