# Nezávislý odhad cen – Jana Nohy 1598, Benešov (ceny-2)

Datum odhadu: 4. 11. 2026. Nečetl jsem nic ze složky Benesov/ kromě tohoto výstupu; nic jsem nikam neodeslal ani nevyplnil, CAPTCHA se neobjevila.
Vše označené **ODHAD** je můj úsudek z uvedených srovnatelných; ostatní čísla jsou citovaná z uvedených zdrojů.

## 0. Metodika a omezení (čtěte první)

- Všechny inzeráty z Sreality jsem stáhl 4. 11. 2026 přes JSON API (`/api/v1/estates/search?...locality_district_id=48` = okres Benešov, 77 bytů k prodeji, 58 k pronájmu, a detail `/api/v1/estates/<id>`). Jsou to **nabídkové** ceny aktivních inzerátů. Prodané inzeráty Sreality nezveřejňuje. Skutečné realizované ceny po bytech (katastr) pro Benešov jsem veřejně nenašel; Cenová mapa (cenovamapa.org) vyžaduje registraci – tu jsem nevytvářel.
- Proto realizovanou cenu odvozuji: nabídková cena minus typická sleva (viz bod 0.1) a u dlouho inzerovaných bytů (viz sloupec „na trhu od“) ještě opatrněji.
- Rekonstrukční náklady a výnosová požadavky nemají v dostupných zdrojích přesné benchmarky pro Benešov; označeno ODHAD.
- Plochy bytů jsou podle zadání odhad; ceny tedy přepočítávejte podle skutečné užitné plochy (Kč/m² jsou přenosnější než celkové částky).
- Plus/minus specifika objektu (vše zahrnuto v pesimistickém a realistickém scénáři): zdivo 1980 s plochou střechou (riziko vlhkosti/hydroizolace), u silnice (hluk), bez parkování a zahrady (v Benešově je u centrálních bytů parkování často součástí nabídky, např. Rubešova 551, Scheinerova 2474), bez výtahu (2. NP).
- Prodej jednotlivých bytů předpokládá vznik jednotek (prohlášení vlastníka, vklad do katastru). Tento proces a čas nejsou v cenách zahrnuty.

### 0.1 Zdroje pro rozdíl nabídková → realizovaná cena

| Zdroj | Údaj | Datum |
|---|---|---|
| Newstream.cz (cituje Valuo) https://www.newstream.cz/reality/prodavajici-ustupuji-kupujici-si-znovu-rikaji-o-slevy-a-rok-2027-muze-byt-jejich | Kupující dnes vyjednávají v průměru cca 5–6 % z nabídky (v roce 2023 cca 11,5 %, v 2024–25 jen cca 2 %); každý třetí inzerovaný byt už zlevnil (před rokem každý čtvrtý); průměrná doba prodeje cca 60 dní | 8. 10. 2026 |
| Banky.cz https://www.banky.cz/clanky/rekordni-median-43-milionu-kc-ceny-starsich-bytu-rostou-nerovnomerne/ | Medián realizované ceny staršího bytu v ČR (katastr, Maxima Reality) v červenci 2026 rekordních 4,3 mil. Kč; v části regionů prodávající ustupují o 200–300 tis. Kč | 21. 9. 2026 |
| Banky.cz https://www.banky.cz/clanky/rozdil-mezi-inzertni-a-realnou-cenou-nemovitosti-2025/ (Valuo) | Průměrný rozdíl inzertní × reálná cena v ČR „cca 21 %“, Praha/Brno/Plzeň 10–15 %, Středočeský kraj v článku neuveden; metodika nejasná, **beru s nízkou vahou** (nesouhlasí s údajem Valua výše) | akt. 3. 2. 2026 |
| Newstream/REALIndex https://www.newstream.cz/reality/rozdil-mezi-nabidkovymi-a-prodejnimi-cenami-nemovitosti-se-prohlubuje | Největší rozdíl nabídka × prodej měl Středočeský kraj, ~12 % (datum období v mém výtahu neuvedeno, starší údaj) | neověřeno |
| Vlastní měření: historie sleva inzerátů (Sreality `price_summary_old_czk` a gohome.cz historie cen) | Benešov Bezručova 2+1 družstevní 52 m²: 5 650 000 → 5 200 000 → 5 090 000 Kč (−9,9 % za 7 měs.); J. Franka 4+kk 75 m²: 7 890 000 → 7 490 000 (−5,1 %, 1. 10. 2026); Dukelská 3+kk 83 m²: 8 300 000 → 8 000 000 (−3,6 %); Týnec Pod Hradištěm 3+kk 87 m²: 7 300 000 → 6 990 000 (−4,2 %); Čerčany Havlíčkova 2+kk 48 m²: 4 500 000 → 4 300 000 (−4,4 %); Vlašim Družstevní 3+1 58 m²: 4 576 000 → 4 360 000 (−4,7 %) | 4. 11. 2026 |

**ODHAD sleva nabídka → realizace pro Benešov:** typicky 5–8 % z aktuální nabídkové ceny (u dlouho visících bytů i 10 % a více). V tabulkách níže počítám realizovanou cenu ≈ 0,92–0,94 × typická nabídka srovnatelného bytu.
Orientace trhu: průměrná nabídka okres Benešov 85 985 Kč/m² (realitymix, říjen 2026), medián města Benešov 89 394 Kč/m² (housi.cz, 4. 11. 2026) / 90 625 Kč/m² (housi.cz 8. 9. 2026), 93 229 Kč/m² (gohome.cz, 67 inzerátů) – všechno nabídky.

## 1. Srovnatelné byty (nabídky, Sreality, stav 4. 11. 2026, doplněno gohome.cz)

URL ve tvaru `https://www.sreality.cz/detail/prodej/byt/<dispozice>/benesov-benesov-<ulice>/<ID>` (rozhoduje ID; API ověření: `https://www.sreality.cz/api/v1/estates/<ID>`).

### 1A. Benešov – po rekonstrukci / velmi dobrý stav (cíl pro scénář b)

| # | Ulice | Dispozice | m² | Stav / typ | Nabídka Kč | Kč/m² | Na trhu od | ID |
|---|---|---|---|---|---|---|---|---|
| 1 | Vlašimská | 4+kk | 85 | po starší kvalitní rekonstrukci, panel, výtah | 8 300 000 | 97 647 | 30. 9. 2026 | 4061536332 |
| 2 | Jiřího Franka | 4+kk | 75 | po kompletní rekonstrukci, panel | 7 490 000 (z 7 890 000) | 99 867 | 25. 6. 2026 | 3487625292 |
| 3 | Vlašimská 1560 | 3+1 | 76 | kompletní rekonstrukce, cihla, sdílená zahrada | 7 500 000 | 98 684 | 30. 10. 2026 | 2898395212 |
| 4 | F. V. Mareše 491 | 2+kk | 76 (vnitřní 68,7) | rekonstrukce 2021, cihla, terasa | 6 990 000 | 91 974 | 28. 8. 2026 | 4158046284 |
| 5 | Rubešova 551 | 2+kk | 45 | cihla, generální rekonstrukce domu 2017, parking. stání | 4 990 000 | 110 889 | 11. 8. 2026 | 2861879372 |
| 6 | Nová Pražská | 2+kk | 43 | kompletní rekonstrukce, panel | 5 650 000 | 131 395 | **11. 10. 2025 (13 měs., neprodáno)** | 1693434700 |
| 7 | Na Bezděkově 1780 | 2+kk | 61 | revitalizovaný panel, výtah, 7. NP | 5 700 000 | 93 443 | 22. 7. 2026 | 2654720076 |

### 1B. Benešov – běžný/udržovaný stav bez rekonstrukce (cena dnešního stavu po „obnově“; horní mez pro scénář a)

| # | Ulice | Dispozice | m² | Stav / typ | Nabídka Kč | Kč/m² | Na trhu od | ID |
|---|---|---|---|---|---|---|---|---|
| 8 | Dukelská 1586 | 2+1 | 62 | velmi dobrý, panel | 5 250 000 | 84 677 | 18. 4. 2026 (6,5 měs.) | 3060183116 |
| 9 | Zapova 1286 | 2+1 | 62 (70,3 vč. příslušenství) | dobrý, panel, sklep | 5 397 000 | 87 048 | 29. 7. 2026 | 1971179596 |
| 10 | Jiřího Horáka 1557 | 3+1 | 57 | dobrý, panel, výtah | 5 490 000 | 96 316 | 20. 10. 2026 | 1642790988 |
| 11 | Na Tržišti | 3+1 | 88 | dobrý, cihla, centrum | 6 500 000 | 73 864 | 28. 9. 2026 | 114368588 |
| 12 | (bez ulice) | 2+kk | 52 | velmi dobrý, panel, 5. NP | 4 950 000 | 95 192 | 16. 3. 2026 (7,5 měs.) | 3603256140 |
| 13 | Rubešova | 2+kk | 38 | velmi dobrý, cihla, nová podlaha | 4 390 000 | 115 526 | **3. 10. 2025 (13 měs., neprodáno)** | 2659636044 |
| 14 | Bezručova (gohome.cz/vitio.cz) | 2+1 družstevní | 52 | lodžie, bez rekonstrukce | 5 090 000 (z 5 650 000) | 97 885 | 11. 3. 2026 | zdroj https://www.gohome.cz/byty+BENE%C5%A0OV/ |

### 1C. Okres Benešov – opravdu původní stav / „před rekonstrukcí“ (cíl pro scénář a)

| # | Lokalita | Dispozice | m² | Stav / typ | Nabídka Kč | Kč/m² | Na trhu od | ID |
|---|---|---|---|---|---|---|---|---|
| 15 | Vlašim, Severní | 2+1 | 55 | „určen k rekonstrukci“, el. akumulační kamna, cihla | 3 900 000 | 70 909 | 5. 7. 2026 (4 měs.) | 1305075788 |
| 16 | Týnec n. S., Družstevní | 2+1 | 49 | „určen spíše k rekonstrukci“, cihla, zateplený dům | 4 200 000 | 85 714 | 9. 9. 2026 | 2728538188 |
| 17 | Sázava, Sídliště 9. května | 2+1 | 57 | částečná rekonstrukce, zbytek původní, cihla | 3 450 000 | 60 526 | 12. 7. 2026 (4 měs.) | 2468143180 |
| 18 | Vlašim, Obora | 2+1/3+kk | 88 | před rekonstrukcí, revitalizovaný dům | 5 199 000 | 59 080 | 26. 9. 2026 | 2268143692 |

Poznámka: Vlašim je cenově cca 10–15 % pod Benešovem (realitymix: 77 115 Kč/m² vs. 85 985 okres); Týnec je cenově blíž Benešovu. Pro Benešov (centrum, 6 min od nádraží) proto beru srovnatelné „před rekonstrukcí“ nabídky ≈ 70–86 tis. Kč/m², **realizace ≈ 60–75 tis. Kč/m²**.

### 1D. Nové byty (nástavba) – Benešov

| # | Ulice | Dispozice | m² | Stav | Nabídka Kč | Kč/m² | Na trhu od | ID |
|---|---|---|---|---|---|---|---|---|
| 19 | Dukelská 2460 | 3+kk | 83 | novostavba, výtah, 3. NP | 8 000 000 (z 8 300 000) | 96 386 | **27. 3. 2026 (7 měs., sleva 3,6 %)** | 3395437388 |
| 20 | Scheinerova 2474 | 3+kk | 94 | novostavba 2026, 5. NP, vč. parkování, lodžie 11 m² | 10 990 000 | 116 915 | 21. 8. 2026 | 3617833036 |
| 21 | 102. pluku 2452 | 1+kk | 42 | novostavba, bezbariérový | 5 800 000 | 138 095 | 20. 9. 2026 | 2809077836 |
| 22 | Tyršova 2077 | 1+kk (ateliér) | 33 | novostavba, centrum, strop 3 m | 4 400 000 | 133 333 | 7. 9. 2026 | 1759326284 |

## 2. Odpovědi na bod 1 – jednotlivé byty (realizované ceny, ODHAD)

Plocha: dle zadání (A 95, B 56, C 70, D 38 m²). Realizovaná cena ≈ nabídka srovnatelného bytu − 5–8 % − korekce na vlastnosti objektu (plochá střecha, silnice, bez parkování, bez výtahu).

### 2a. Dnešní stav (zdevastovaný/původní), prodej bytu samostatně – ODHAD

| Byt | m² | Pesimist. Kč/m² | Realist. Kč/m² | Optimist. Kč/m² | Pesimist. Kč | Realist. Kč | Optimist. Kč |
|---|---|---|---|---|---|---|---|
| A 4+1 (1. NP) | 95 | 51 000 | 60 000 | 69 000 | 4,84 mil. | **5,70 mil.** | 6,55 mil. |
| B 2+1 | 56 | 54 000 | 64 000 | 74 000 | 3,02 mil. | **3,58 mil.** | 4,14 mil. |
| C 3+1 | 70 | 53 000 | 62 000 | 71 000 | 3,71 mil. | **4,34 mil.** | 4,97 mil. |
| D 1+1 (2. NP) | 38 | 61 000 | 72 000 | 83 000 | 2,32 mil. | **2,74 mil.** | 3,15 mil. |
| **Součet (259 m²)** | | | | | 13,89 mil. | **16,36 mil.** | 18,81 mil. |

Odůvodnění: srovnatelné 15–18 (Vlašim Severní 70,9 tis., Týnec 85,7 tis., Sázava 60,5 tis., Vlašim Obora 59,1 tis. Kč/m² nabídky) plus nákladový test: realizovaná cena po rekonstrukci (2b) minus rekonstrukce (ODHAD 15–22 tis. Kč/m² vč. nového topení, rozvodů, jader; jediný veřejně nalezený benchmark: ~1 mil. Kč za 65 m² panelový byt v Praze, novinky.cz – slabý zdroj) minus riziko/marže kupce. Menší byt má vyšší Kč/m². Byty „zdevastované“ jsou na spodní hraně až pod ní. Součet bytů je nad cenou celého domu (bod 3) – rozdíl je náklad dělení, času a rizika.

### 2b. Po kvalitní rekonstrukci vč. nového topení – ODHAD

**Původní dispozice**

| Byt | m² | Pesim. Kč/m² | Real. Kč/m² | Optim. Kč/m² | Pesim. Kč | Real. Kč | Optim. Kč |
|---|---|---|---|---|---|---|---|
| A 4+1→4+kk | 95 | 76 000 | 86 000 | 94 000 | 7,22 mil. | **8,17 mil.** | 8,93 mil. |
| B 2+1 | 56 | 80 000 | 89 000 | 98 000 | 4,48 mil. | **4,98 mil.** | 5,49 mil. |
| C 3+1 | 70 | 82 000 | 90 000 | 98 000 | 5,74 mil. | **6,30 mil.** | 6,86 mil. |
| D 1+1 | 38 | 95 000 | 105 000 | 118 000 | 3,61 mil. | **3,99 mil.** | 4,48 mil. |
| **Součet (259 m²)** | | | | | 21,05 mil. (81 tis./m²) | **23,44 mil. (91 tis./m²)** | 25,76 mil. (99 tis./m²) |

**Alternativní dispozice (5 jednotek, 256 m²)**

| Byt | m² | Pesim. Kč/m² | Real. Kč/m² | Optim. Kč/m² | Pesim. Kč | Real. Kč | Optim. Kč |
|---|---|---|---|---|---|---|---|
| 2+kk | 52 | 82 000 | 92 000 | 102 000 | 4,26 mil. | **4,78 mil.** | 5,30 mil. |
| 2+kk | 40 | 95 000 | 105 000 | 118 000 | 3,80 mil. | **4,20 mil.** | 4,72 mil. |
| 2+kk | 56 | 82 000 | 92 000 | 100 000 | 4,59 mil. | **5,15 mil.** | 5,60 mil. |
| 3+kk | 70 | 82 000 | 90 000 | 98 000 | 5,74 mil. | **6,30 mil.** | 6,86 mil. |
| 1+kk | 38 | 95 000 | 105 000 | 118 000 | 3,61 mil. | **3,99 mil.** | 4,48 mil. |
| **Součet (256 m²)** | | | | | 22,00 mil. (86 tis./m²) | **24,42 mil. (95 tis./m²)** | 26,96 mil. (105 tis./m²) |

Odůvodnění: srovnatelné 1–7 (nabídky rekonstruovaných bytů v Benešově 92–100 tis. Kč/m² pro 45–85 m², po slevě 6–8 %); malé byty 38–45 m² mají prémii (nabídky 111–131 tis. Kč/m², ale 6 a 13 stále neprodáno po 13 měsících, proto realizace jen 95–118 tis. Kč/m²); velký byt A (95 m²) má nižší Kč/m². Nemovitost nemá parkování, výtah ani zahradu, a je u silnice – proto realistický střed leží uvnitř, ne na špičce nabídek.

## 3. Celý dům investorovi – ODHAD

Použitelný rozsah užitné plochy 256–259 m² (součet bytů, bez společných prostor).

### Srovnatelné činžovní domy (Sreality, 4. 11. 2026, nabídky; střední Čechy)

| Lokalita | Plocha | Jednotky / stav | Nabídka Kč | Kč/m² | Výnos z inzerátu | ID / URL |
|---|---|---|---|---|---|---|
| **Benešov, Na Chmelnici** | 206 m² | 4 byty, cihla, dobrý stav, od 24. 9. 2026 | 12 499 000 | 60 675 | nájmy 55 000 Kč/měs. = 660 000/rok → **hrubý 5,3 %** z nabídky | 2905808972 |
| Petroupim (10 min od Benešova) | 306 m² | 5 bytů, po rekonstrukci, obsazené, od 1. 10. 2026 | 13 490 000 („k jednání“) | 44 085 | potenciál 70 000 Kč/měs. = 840 000/rok → **hrubý 6,2 %** | 1381310540 |
| Kutná Hora, Husova | 365 m² | 3 byty + podkroví k vestavbě, centrum UNESCO, od 20. 10. 2025 (stále neprodáno) | 13 999 000 | 38 353 | „čistý roční výnos 6 %“ (údaj prodejce); bankovní odhad 2022 15 mil. | 37798732 |
| Dobrovice, Václavská | 230 m² | rekonstruovaný nájemní dům, 5 vstupů | 11 330 000 | 49 261 | – | 2762199116 |
| Dublovice-Líchovy | 319 m² | RD se 3 jednotkami + chata, rekreační lokalita | 16 999 000 | 53 288 | – | 2677272652 |
| Slaný, Vinařického | 200 m² | bytový dům v centru, velmi dobrý, od 30. 5. 2025 (stále neprodáno) | 15 670 000 | 78 350 | – | 2760880972 |
| Mladá Boleslav, Pražská brána | 300 m² | nájemní dům **před rekonstrukcí**, historické centrum | 14 990 000 | 49 967 | – | 1782514508 |
| Nové Strašecí, Žižkovo nám. | 471 m² | 2 domy, obytná část + komerce | 20 990 000 | 44 565 | – | 1236238412 |
| Kladno, Váňova | 416 m² | 2 byty + obchody, dobrý, od 6. 10. 2023 (!) neprodáno | 12 500 000 | 30 048 | – | 2420868428 |

Pozn. k nabídkám: u domu 3 (Kutná Hora), 6 (Slaný) a 9 (Kladno) dlouhá doba na trhu potvrzuje, že nabídkové ceny investorských domů nejsou realizovatelné; **realizace ODHAD −8 až −15 %**.
Požadovaný výnos: z inzerátů hrubě 5,3–6,2 % u rekonstruovaných domů; prime rezidenční yield v ČR (Knight Frank, institucionální/Praha) 4,25 % https://www.property-forum.eu/news/czech-investment-market-tops-eur1-billion-in-q2-2026/21754 (Q2 2026) – pro malý dům v Benešově nepoužitelný. **ODHAD požadovaný hrubý výnos pro soukromého investora v Benešově: 5,5–6,5 % po rekonstrukci, 8–10 % z celkových nákladů (nákup+rekonstrukce) u domu k rekonstrukci.**

### Odhad nájmů po rekonstrukci (podrobně v bodě 5)
Roční hrubé nájemné (bez záloh) ODHAD: původní dispozice 745 / 852 / 962 tis. Kč; alternativní dispozice 808 / 923 / 1 048 tis. Kč (pesim. / real. / optim.).

### (c) Dům v dnešním stavu – ODHAD

| | Pesimisticky | Realisticky | Optimisticky |
|---|---|---|---|
| Cena celého domu | 9,0 mil. Kč (35 tis./m²) | **11,5 mil. Kč (44 tis./m²)** | 14,0 mil. Kč (54 tis./m²) |

Odvození: (i) Benešov Na Chmelnici (dobrý stav) nabídka 60,7 tis. Kč/m² → přepočet na 259 m² 15,7 mil. nabídka, −8 % realizace, −25–30 % za zdevastovaný stav ≈ 10–11 mil.; (ii) metoda „rozdělit a prodat“: součet rekonstruovaných bytů 24,4 mil. − rekonstrukce ~5,2 mil. (20 tis. Kč/m², ODHAD) − náklady prodeje/financování/dělení ~2,0 mil. − marže developera 15 % ≈ 3,7 mil. = ~13,5 mil. (horní mez); (iii) Mladá Boleslav Pražská brána před rekonstrukcí 50 tis. Kč/m² nabídka. Realistický střed 11,5 mil. Kč.

### (d) Dům po rekonstrukci, prodej investorovi – ODHAD

| | Pesimisticky | Realisticky | Optimisticky |
|---|---|---|---|
| Cena celého domu | 13,5 mil. Kč (52 tis./m²) | **16,5 mil. Kč (64 tis./m²)** | 19,5 mil. Kč (75 tis./m²) |

Odvození: výnosově – roční nájem 923 tis. (alt. dispozice, real.) / 5,75 % = 16,0 mil.; při 6,5 % z 808 tis. = 12,4 mil.; při 5 % z 1 048 tis. = 21,0 mil.; původní dispozice při 5,75 % = 14,8 mil. Srovnání: Na Chmelnici 60,7 tis. Kč/m² nabídka. Poznámka: součet cen jednotlivých bytů (23–24 mil.) je výrazně nad cenou celého domu → pokud je cílem maximalizovat výnos, vyplatí se po rekonstrukci prodávat byty zvlášť (po odečtu nákladů a času, ODHAD +4–6 mil. oproti prodeji bloku), prodej bloku investorovi je rychlejší, ale s diskontem cca 25–30 % oproti součtu bytů.

## 4. Nové byty v nástavbě (e), 2 × 60 m² – ODHAD

| | Pesimisticky | Realisticky | Optimisticky |
|---|---|---|---|
| Kč/m² | 82 000 | **92 000** | 105 000 |
| 1 byt (60 m²) | 4,92 mil. | **5,52 mil.** | 6,30 mil. |
| 2 byty | 9,84 mil. | **11,04 mil.** | 12,60 mil. |

Odvození: srovnatelné 19–22: nejbližší parametry (nové, 3. NP, výtah) Dukelská 3+kk 83 m² nabídka 96 386 Kč/m², sedm měsíců neprodáno, již −3,6 %; menší jednotky mají prémii (+5 %), bez výtahu a parkování −5–10 %; nabídky nových 1+kk 133–138 tis. Kč/m² a Scheinerova 117 tis. (s parkováním) jsou prémiové projekty v centru. Pozn.: stavební náklady nástavby nejsou součástí; projekt Postupice (Blanická 81) nabízí nové byty 72–85 tis. Kč/m² (ID např. 4082352204) – ukazuje, že mimo centrum je pevná konkurence.

## 5. Měsíční nájem po rekonstrukci (Kč/m², bez záloh na služby/energie) – ODHAD

### Srovnatelné pronájmy v Benešově (Sreality, 4. 11. 2026, nabídky)

| Ulice | Dispozice | m² | Stav | Nájem Kč (bez záloh) | Kč/m² | Od | ID |
|---|---|---|---|---|---|---|---|
| Dukelská 2190 | 2+kk | 53 | velmi dobrý | 15 490 (+761/os) | 292 | 23. 9. 2026 | 988553292 |
| Vnoučkova 476 | 2+kk | 50 | po rekonstrukci | 14 000 | 280 | 1. 9. 2026 | 3885707340 |
| Černoleská 584 | 2+kk | 47 | rekonstrukce 2022, cihla | 15 000 (+4 500) | 319 | 29. 9. 2026 | 3062898764 |
| Konopišťská 1652 | 2+kk | 40 | zrekonstruovaný, panel | 15 000 | 375 | 15. 9. 2026 | 498348108 |
| Pražská 124 | 3+kk | 82 | po rekonstrukci, podkroví | 21 000 | 256 | 21. 9. 2026 | 2554273868 |
| Pražského povstání 2059 | 3+kk | 74 | velmi dobrý, zařízený | 23 000 | 311 | 26. 10. 2026 | 1501364300 |
| Mariánovice | 3+kk | 72 | novostavba | 19 500 | 271 | 6. 9. 2026 | 228470860 |
| Tyršova 2260 | 1+kk | 38 | velmi dobrý | 12 900 | 339 | 1. 11. 2026 | 1602289740 |
| Tyršova 181 | 1+kk | 44 | velmi dobrý, cihla, výtah | 13 900 (+2 700) | 316 | 6. 10. 2026 | 404295756 |
| Jana Švermy 1709 | 1+1 | 44 | velmi dobrý, panel | 11 990 (+2 796) | 272 | 27. 10. 2026 | 1932263500 |
| Nová Pražská 1716 | 1+1 | 46 | dobrý, původní kuchyň | 8 500 | 185 | 21. 10. 2026 | 2129264716 |
| Jiráskova 2342 | 2+kk | 42 | novostavba | 16 000 (+3 000) | 381 | 17. 10. 2026 | 1772490828 |
| Tyršova 2077 | 3+kk | 72 | nový | 23 000 | 319 | 20. 10. 2026 | 193658956 |
| 102. pluku 2452 | 1+kk | 32 | novostavba 2024 | 13 000 (+2 000) | 406 | 21. 10. 2026 | 4217962572 |

Kontext: průměrné nabídkové nájemné Středočeský kraj 325 Kč/m² (Q1 2026, Reality iDNES/CEMAP, Estav uvádí ~315 Kč/m² k jaru 2026) https://zpravy.kurzy.cz/856904-pronajem-bytu-v-cr-za-poslednich-8-kvartalu-cena-vzrostla-na-323-kc-m2-a-trh-se-v-q1-2026-zrychlil/ (22. 4. 2026), https://www.estav.cz/cz/14532.najemni-bydleni-v-cesku-v-2026-se-stava-standardem (21. 4. 2026); doba pronájmu ve středních Čechách 26 dní.

### Odhad nájmu po rekonstrukci (netto, bez záloh) – ODHAD

**Původní dispozice**

| Byt | m² | Pesim. Kč/m² | Real. Kč/m² | Optim. Kč/m² | Real. Kč/měs. |
|---|---|---|---|---|---|
| A 4+kk | 95 | 220 | 250 | 280 | 23 800 |
| B 2+1 | 56 | 240 | 275 | 310 | 15 400 |
| C 3+1 | 70 | 235 | 270 | 305 | 18 900 |
| D 1+1 | 38 | 300 | 340 | 390 | 12 900 |
| **Součet** | 259 | 240 | **274** | 310 | **71 000** (pesim. 62 100 / optim. 80 200) |

**Alternativní dispozice**

| Byt | m² | Pesim. | Real. | Optim. | Real. Kč/měs. |
|---|---|---|---|---|---|
| 2+kk | 52 | 250 | 290 | 330 | 15 100 |
| 2+kk | 40 | 310 | 350 | 400 | 14 000 |
| 2+kk | 56 | 245 | 280 | 315 | 15 700 |
| 3+kk | 70 | 240 | 275 | 310 | 19 200 |
| 1+kk | 38 | 300 | 340 | 390 | 12 900 |
| **Součet** | 256 | 263 | **300** | 341 | **76 900** (pesim. 67 300 / optim. 87 300) |

**Nástavba 2 × 60 m² (nová)**: 280 / **320** / 360 Kč/m² → 16 800 / **19 200** / 21 600 Kč za byt (celkem 38 400 Kč/měs. realisticky).
Čistý příjem ODHAD: hrubé nájemné × ~0,80–0,85 (neobsazenost, fond oprav, daň z nemovitosti, pojištění, správa).

## 6. Souhrnná tabulka (ODHAD, realizované ceny, 4. 11. 2026)

| Položka | Pesimisticky | Realisticky | Optimisticky |
|---|---|---|---|
| (a) A 4+1 95 m², dnešní stav | 4,84 mil. (51 tis./m²) | 5,70 mil. (60 tis.) | 6,55 mil. (69 tis.) |
| (a) B 2+1 56 m², dnešní stav | 3,02 mil. (54 tis.) | 3,58 mil. (64 tis.) | 4,14 mil. (74 tis.) |
| (a) C 3+1 70 m², dnešní stav | 3,71 mil. (53 tis.) | 4,34 mil. (62 tis.) | 4,97 mil. (71 tis.) |
| (a) D 1+1 38 m², dnešní stav | 2,32 mil. (61 tis.) | 2,74 mil. (72 tis.) | 3,15 mil. (83 tis.) |
| (a) součet bytů, dnešní stav | 13,89 mil. | 16,36 mil. | 18,81 mil. |
| (b) A po rekonstrukci | 7,22 mil. (76 tis.) | 8,17 mil. (86 tis.) | 8,93 mil. (94 tis.) |
| (b) B po rekonstrukci | 4,48 mil. (80 tis.) | 4,98 mil. (89 tis.) | 5,49 mil. (98 tis.) |
| (b) C po rekonstrukci | 5,74 mil. (82 tis.) | 6,30 mil. (90 tis.) | 6,86 mil. (98 tis.) |
| (b) D po rekonstrukci | 3,61 mil. (95 tis.) | 3,99 mil. (105 tis.) | 4,48 mil. (118 tis.) |
| (b) součet bytů po rekonstrukci | 21,05 mil. | 23,44 mil. | 25,76 mil. |
| (b-alt) součet 5 bytů alt. dispozic | 22,00 mil. | 24,42 mil. | 26,96 mil. |
| (c) celý dům dnes, investor | 9,0 mil. | 11,5 mil. | 14,0 mil. |
| (d) celý dům po rekonstrukci, investor | 13,5 mil. | 16,5 mil. | 19,5 mil. |
| (e) nástavba, 2 nové byty po 60 m² | 9,84 mil. (82 tis./m²) | 11,04 mil. (92 tis.) | 12,60 mil. (105 tis.) |
| Nájem po rekonstrukci, 4 byty orig. | 62,1 tis./měs. (240 Kč/m²) | 71,0 tis. (274) | 80,2 tis. (310) |
| Nájem po rekonstrukci, 5 bytů alt. | 67,3 tis. (263) | 76,9 tis. (300) | 87,3 tis. (341) |
| Nájem nástavba, 2 × 60 m² | 33,6 tis. (280) | 38,4 tis. (320) | 43,2 tis. (360) |

## 7. Nejistoty, které by měly největší dopad

1. Skutečná užitná plocha a vybavení bytů (plochy jsou odhad) a zda je dům právně rozdělitelný na jednotky.
2. Nepodařilo se získat realizované ceny z katastru pro Benešov (odhady slev jsou z národních zdrojů 5–6 % a z historie slev inzerátů 4–10 %).
3. Rekonstrukční náklady (15–22 tis. Kč/m², ODHAD) a stav konstrukcí (plochá střecha, hydroizolace, rozvody po 1980) – mění výsledky (a) a (c) o ±1–2 mil.
4. Trh se podle zdrojů z října 2026 otevírá směrem k vyšším slevám (Valuo, MECH), horizont 2027 neutrální až mírně negativní pro ceny starších bytů; mírně pozitivní pro nájmy (+4–6 % meziročně, Estav 21. 4. 2026).
