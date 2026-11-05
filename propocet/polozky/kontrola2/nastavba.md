# Kontrola 2: Ustupující podlaží (2 byty), jen V2 s nástavbou (5. 11. 2026)

Web real (`rozpis["nástavba"]` z `model.py`, ověřeno spuštěním): **9 861 tis.** (stavba 6 671 + statika 2 000 + projekt 1 200 v modelu; v reportu dopočteno na 12 řádků). Moje čísla jsou rozpis zdola z `polozky/nastavba.md` přepočtený na aktuální vstupy modelu (TČ 230, schodiště 450, střecha 3 200 Kč/m²), s DPH, listopad 2026. Zdroje cen: viz poslední sloupec; ostatní ODHAD.

## 1. Tabulka po dílčích položkách (tis. Kč s DPH)

| Položka | Web | Můj real | Pes–opt | Potřeba | Nejlevnější rozumná cesta (úspora) | Zdroj |
|---|---:|---:|---|---|---|---|
| Nosná dřevěná konstrukce 150 m² + demontáž staré střechy | 2 606 | 2 600 | 3 300–2 000 | jen když nástavba | firma, 3 nabídky prefabrikovaných panelů; tesařská parta −10 % (−250), riziko záruk a montáže jeřábem | `nastavba.md` ř. 1 (150 × 14 000 + demontáž 0,12 mil. bez DPH × 1,045 × 1,12); RD dřevostavba na klíč 39–52 tis./m², rámová 35–50 tis. (nejremeslnici.cz, megastroj.cz, biodomy.cz, WebSearch 5. 11. 2026) |
| Střecha nástavby | 564 | 560 | 760–400 | ano (nová střecha je tak jako tak) | firma; svépomoc ne (hydroizolace, záruka) | `model.py` `strecha_v_rekonstrukci` 3 200 Kč/m² × 150 |
| Okna 14 ks + balkonové dveře 4 ks | 446 | 420 | 550–330 | ano | řemeslník −8 % (−35); balkonové dveře 35 tis. jsou nadsazené (běžné dvoukřídlé 15–25 tis.), −60; montáž okny svépomocí ne (těsnost, záruka) | `stav.md` S1 (okno 11–23 tis.); dveře ODHAD |
| Terasa 89 m²: dlažba na terčích + zábradlí | 399 | 390 | 500–250 | ne pro kolaudaci, ano pro prodej (cena bytu) | pokládka dlažby svépomocí (~65 h) −70; zábradlí firma (pád, ČSN 74 3305) | ODHAD: 89 × 1 800 + 40 bm × 4 500 |
| Prodloužení schodiště do 3. NP | 529 | 540 | 1 000–350 | ano (jediná cesta do bytů, evakuace) | firma (ocel + statik); nic svépomocí; největší nejistota: vejde se 2. rameno do haly? | `nastavba.md` ř. 5, `model.py` `nastavba_m2` poznámka (450 tis. bez DPH) |
| Rozvody ZTI, elektro, topení + další TČ | 892 | 880 | 1 100–650 | ano | řemeslník s oprávněním −10 % (−90); TČ 8 kW stačí (dřevostavba A/B, ~4 kW/byt); revize elektro a TČ ze zákona firma | `stav.md` ř. 115, 204; ODHAD |
| 2 koupelny + 2 kuchyně | 504 | 500 | 650–330 | ano (byt bez koupelny nelze prodat) | řemeslník −70; svépomocí jen sestavení linky (−30), obklady raději ne (hydroizolace, vodní škody) | `stav.md` 5b ř. 172–173 |
| Vnitřní dokončení 120 m² | 646 | 640 | 800–420 | ano | **svépomoc**: materiál ~45 % práce → net −290 (cca 600–800 člověkohodin, 3 lidé ≈ 3 měsíce víkendů); laik zvládne SDK, podlahy, malbu; riziko: požární dělení bytů EI 30, kročejová neprůzvučnost, záruka kupcům 5 let u nového bytu | ODHAD: příčky 160 m² × 1 100, podlahy 120 × 1 800, strop SDK 72, dveře 64, malba 36 (bez DPH) |
| Lešení, autojeřáb, zařízení staveniště | 411 | 450 | 570–300 | ano | firma; lešení společně se sanací trhlin (−50 možné); výše odpovídá lešení 4 měsíce, ne 1 | ODHAD: 600 m² × (250 montáž + 3 × 80 nájem) + jeřáb 5 dní ~0,12 mil. |
| Požární úpravy, elektroměrový rozvaděč, příkon | 317 | 320 | 450–200 | ano (PBŘ, stavební úřad, distributor) | firma/autorizovaná osoba; svépomoc ne | `uzemni-plan.md` ř. 110–112 |
| Podchycení mikropilotami + věnec nad 2. NP | 2 006 | 2 000 | 2 500–500 | **jen když to řekne statik** (viz bod 4) | podchycení jen firma se statikem; bez posudku nepočítat jako jistotu | mikropiloty24.cz 1 800–4 500 Kč/bm, nejstav.cz 1 500–3 000 Kč/bm (WebSearch 5. 11. 2026); 480 bm × 2 800 + věnec 68 bm × 5 000 = ODHAD |
| Statika, průzkumy, PBŘ, projekt rozvodů, poplatky | 542 | 540 | 700–360 | ano (bez toho není povolení) | firma/projektant; viz překryv níže (−100) | `uzemni-plan.md` ř. 177–182 |
| **Součet** | **9 861** | **9 840** | | | | |

## 2. Součet

| | tis. Kč |
|---|---:|
| Web real | 9 861 |
| Můj real (rozpis výše) | 9 840 (−0,2 %) |
| + chybějící položky (bod 3) | +380 → **10 220 (+3,6 %)** |
| − překryv s jinými položkami | −100 → 10 120 (+2,6 %) |
| Nejlevnější rozumná varianta (řemeslníci + svépomoc dokončení a dlažba, balk. dveře, TČ) | ≈ **9 400 (−5 % proti webu)**; úspora hlavně z dokončení (−290) |

Rozdíl proti webu je pod 10 %, položka je v mezích rozumného odhadu. **Cena konstrukce 2,6 mil. je přiměřená**: 17,3 tis. Kč/m² hrubé s DPH za nosnou konstrukci a obálku bez základů, což je spodní až střední část trhu (rámová dřevostavba RD na klíč 35–52 tis./m² včetně základů, instalací a povrchů). Celá stavba bez statiky a projektu je 7 313 tis. = 48,8 tis./m² hrubé (61 tis./m² čisté) s DPH, tedy horní polovina RD na klíč, ale obsahuje terasu, schodiště, TČ, lešení a statiku mimo RD standard. Ceny nástavby bytového domu v Kč/m² 2026 jsem veřejně nenašel (WebSearch 5. 11. 2026 vrací jen rodinné domy), takže jde pořád o ODHAD bez nabídky dodavatele.

## 3. Chybí / dvakrát

**Chybí (ODHAD, tis. s DPH):**
- Rekuperace / nucené větrání 2 bytů (dřevostavba v energetické třídě A–B, vlhkost): **130**
- Provizorní zastřešení a ochrana 2. NP při výměně střechy (zatečení do hotových bytů): **120**
- Pojištění stavby (CAR, 0,5–1 % stavby): **60**
- Hromosvod, uzemnění nástavby, kolaudační revize: **40**
- Kročejová a vzduchová neprůzvučnost stropu nad 2. NP (plovoucí podlaha na dřevěném stropě je dražší než na ŽB): **30** (částečně už v dokončení)
- Celkem **≈ +380**.

**Podhodnocené:** schodiště (nutná zaměřená haly; pes 1 000) a doba lešení; cena prodeje 3. NP bez výtahu (viz bod 5), není v nákladech ale ve výnosu.

**Dvakrát / překryv (≈ −100 až −250):**
- Řádek „Statika, průzkumy, PBŘ, projekt rozvodů“ (542) vs. základ: PBŘ 83, statik 203 a prováděcí projekt rozvodů 110–369 už jsou v „Projekt, dozor, statik“ a „Prováděcí projekt“. Překryv ~100.
- Mikropiloty vs. statické zajištění 1 500 (pevné): base obsahuje „lokální zesílení základů ~10 m“ (105) a geologii s monitoringem. Překryv 100–250 (`nastavba.md` kap. 2 odhaduje 200–300).
- V pesimistickém scénáři se podchycení počítá dvakrát (statické zajištění 3 500 + nástavba 2 500), poznámka v `nastavba.md` – rozhodnutí uživatele, neměním.
- Dobře vyřešeno: střecha rekonstrukce se z V2 odečítá (V2 má rekonstrukci o 453 tis. levnější než V1), terasa nemá hydroizolaci.

## 4. Mikropiloty 2 mil.: nutné?

Nejsou nutné automaticky. Lehká dřevěná nástavba přidá +4–6 kN/m² (`uzemni-plan.md` ř. ~125), ale odebere stávající plochou střechu, čisté přitížení je asi 2–4 kN/m², tedy zhruba +40–60 t na dům. To zdravý dům unese. Důvod, proč je v modelu podchycení, jsou **aktivní trhliny** (sedání pokračuje, vyplněná trhlina se znovu otevřela, `stav-nove-fotky.md` ř. 25–26, 37). Rozhodnout musí statik po 6–12 měsících sádrových terčů, sondě k základům a geologii. Možnosti od nejlevnější: nic + věnec (0,35), lokální podbetonování a injektáž (0,5–0,9), mikropiloty jen pod nejvíc zatíženými zdmi (1,0–1,4), plné podchycení (2,0–2,5). Reálný očekávaný náklad po vážení je zhruba 1,3–1,6 mil. místo 2,0, ale uživatel rozhodl o 2,0 (podmíněná stopka z 4. 11.), nechávám a připisuji poznámku. Množství (60 ks × 8 m) odpovídá obvodu 68 bm + vnitřním nosným zdem, jednotková cena 2 800 je střed rozpětí 1 800–4 500 Kč/bm.

## 5. Vyplatí se nástavba vůbec? (model, `model.run`, 5. 11. 2026)

| Scénář | Čistý zisk V1 (bez) | Čistý zisk V2 (s) | Rozdíl | Měsíců V1 / V2 | Náklady celkem V1 / V2 | ROI V1 / V2 |
|---|---:|---:|---:|---|---|---|
| Pes | −8,41 mil. | −12,87 mil. | **−4,46 mil.** | 41 / 47 | 31,2 / 44,1 mil. | −27 % / −29 % |
| **Real** | **2,96 mil.** | **3,19 mil.** | **+0,23 mil.** | 23 / 27 | 24,3 / 35,0 mil. | 13,1 % / 9,6 % |
| Opt | 9,95 mil. | 12,55 mil. | +2,59 mil. | 13 / 16 | 18,2 / 28,9 mil. | 54,7 % / 49,4 % |

Tržby 2 bytů v modelu: 2 × 60 m² × 84,8 tis. Kč/m² s DPH = 2 × 5,09 mil. (cena za m² z realizovaných prodejů, `ceny-byty-realizovane.md` kap. 3: Benešov, byty nad 60 m² 65,7–84,4 tis., medián 77,5 tis.; Kpt. Nálepky 3+kk 71 m² 84,4 tis. s klimatizací a garáží; okres 2025 ČSÚ 61,4 tis.). Náklady na čistý m²: 9 861 / 120 = **82 tis. Kč/m² s DPH, prodejní cena 84,8 tis.** Po odpočtu 12 % DPH na vstupu (73 tis.) a prodeji s 12 % DPH (75,7 tis.) zůstává hrubá marže ~3 tis./m² před úroky (v modelu +1,0 mil. úroků a poplatků navíc).

- Rozdíl V2−V1 před daní je +0,35 mil., po dani +0,23 mil. na dodatečných 10,7 mil. nákladů a 4 měsíce. To je ~2 % výnos na vázaný kapitál, úvěr stojí 9–10,5 %. ROI klesá z 13,1 na 9,6 %.
- **Bod zvratu:** náklady nástavby +4 % (+0,35 mil.) nebo ceny dvou bytů −4 % zisk z nástavby smažou. Rozptyl odhadu ceny konstrukce je ±25 %, ceny statiky −75 až +25 %.
- Cenová rizika nad rámec modelu: 3. NP bez výtahu (běžně −5 až −10 % na m²; model dává naopak prémii +5 % za novost), 1 parkovací stání na 6 bytů, silnice II/110. Podmíněná stopka: bez posudku statika nástavbu neplánovat.
- Pesimistický scénář je navíc zkreslený překryvem statiky, ale i bez něj je nástavba ztrátová.

**Závěr:** v realistickém scénáři se nástavba nevyplatí (+0,23 mil. za riziko ±4 mil. a 4 měsíce navíc). Dává smysl jen v optimistickém scénáři (+2,6 mil.), tedy když statik potvrdí, že podchycení netřeba (úspora ~1,5 mil. = +1,5 mil. realisticky), nebo když dodavatel nabídne konstrukci pod ~2,0 mil. Do rozhodnutí o koupi ji nezapočítávat; po koupi a 6 měsících monitoringu trhlin ji znovu prověřit s nabídkami 2–3 dodavatelů dřevostaveb. Svépomocí (dokončení −290, dlažba −70, linka −30) se zisk zvedne na ~+0,6 mil., pořád jde o nízký výnos.

## 6. Doporučení

**Beze změny** (9 861 tis., rozdíl +2,6 až +3,6 % proti mému odhadu, pod prahem 10 %). Poznámka k rozhodnutí: statika 2,0 mil. je horní polovina věrohodného rozpětí; pokud statik nepožaduje mikropiloty, hodnota klesne o 0,5–1,5 mil. a nástavba se z „nerentabilní“ změní na „rentabilní“. Nezměněné rozhodnutí uživatele: statické zajištění 1,5 mil. pevně, rezerva zrušená, architekt zdarma.
