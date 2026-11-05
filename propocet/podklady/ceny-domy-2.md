# Ceny celých malých bytových domů – střední Čechy (stav k 4. 11. 2026)

Doplněk k `ceny-domy.md`. Cíl: za kolik se reálně prodávají celé domy se 3–8 byty, a z toho cena č.p. 1598 Benešov ve stavech (a) současný, (b) standardní rekonstrukce bytů, (c) kompletní rekonstrukce. Zdroj + datum u každého čísla, odhady jsou označeny **ODHAD**.

## 0. Metodika a co se nepovedlo

- **Sreality filtr funguje přes JSON API.** `https://www.sreality.cz/api/v1/estates/search?category_main_cb=4&category_type_cb=1&category_sub_cb=38&locality_region_id=11&limit=100` (Komerční → Činžovní dům, Středočeský kraj, 79 inzerátů, staženo 4. 11. 2026). Detail: `https://www.sreality.cz/api/v1/estates/<ID>`. Starý endpoint `api/cs/v2` je 404, `ceny-domy.md` proto filtr nenašel. Okres Tábor (Jihočeský kraj, region 6) v kategorii neměl žádný inzerát.
- **Kategorie je znečištěná** (komerční objekty, vily, penziony, nedokončené domy). Proto níže 36 inzerátů z cílových okresů prošlo ručním výběrem a do srovnání jsou zařazeny jen skutečné bytové domy.
- **Ceny jsou nabídkové (asking).** Sreality neukazuje prodané ceny. Skutečné prodejní ceny mám jen z ÚZSVM aukcí (výroční zprávy) a jedné soutěže (Libenice). Pro převod nabídka → prodej: viz oddíl 4.
- **Plocha.** U srovnatelných inzerátů je „užitná plocha“ prakticky vždy součet ploch bytů (Mokrovraty 2×65+2×80 = 290; Kolín 314; Křivsoudov 4×67,5 = 270). Pro č.p. 1598 je proto správná srovnávací báze **plocha bytů 260–310 m² (střed 285)**, ne 384 m². Přepočet: Kč/m² podlahové (384) = Kč/m² bytů × 285 / 384 = × 0,742.
- **Nedostupné.** reality.idnes.cz (WebFetch blokuje), realitymix.cz (404), bezrealitky (bez výpisu). Výsledky dražeb na exdrazby/okdrazby/edrazby: archiv ukončených s vydraženou cenou nenalezen (jen aktuální nabídky). ČD nezveřejňuje výsledky výběrových řízení (viz oddíl 2). CAPTCHA se neobjevila.

## 1. Srovnatelné domy – nabídky (Sreality, staženo 4. 11. 2026)

Sloupec „Zdroj“ = ID inzerátu na Sreality (detail přes API URL výše; `since` = vloženo, `edited` = poslední úprava).

### 1a. Jádro srovnání (cenově známé, skutečné bytové domy, ne novostavby, ne památky)

| # | Lokalita (okres) | Byty | Plocha bytů/užitná m² | Stav | Cena Kč | Kč/m² | Vloženo / upraveno | ID |
|---|---|---|---|---|---|---|---|---|
| 1 | Benešov, Na Chmelnici (Benešov) | 4 | 206 | dobrý, 2 NP, nájem 4 bytů 55 000 Kč/měs. | 12 499 000 | **60 675** | 24. 9. / 24. 10. 2026 | 2905808972 |
| 2 | Petroupim (Benešov) | 5 (2×1+1 37 m², 2×3+kk 73 m², 4+kk 100 m²), obsazené | 306 | po rekonstrukci (zateplení, trojskla, el. kotle) | 13 490 000 | **44 085** | 1. 10. / 1. 10. 2026 | 1381310540 |
| 3 | Zaječov-Kvaň (Beroun) | 4× 3+1, tuhá paliva ve sklepě, **pozemek jen pod budovou 132 m² + garáž; okolí a příjezd obecní** | 200 (ODHAD podlahová bytů spíš 240–260) | k celkové rekonstrukci | 10 950 000 | **54 750** (při 250 m² ≈ 43 800) | 24. 3. / 23. 10. 2026 | 3265151820 |
| 4 | Mokrovraty (Příbram) | 4 (2×2+kk 65, 2×3+kk 80), 3 pronajaty, projekt 2 podkrovních bytů | 290 | dobrý | 13 500 000 | **46 552** | 25. 5. / 4. 10. 2026 | 238391372 |
| 5 | Kutná Hora, Husova 140 (Kutná Hora) | 3 (120, 72, 108 m²) + podkroví k dostavbě, historické centrum | 365 (byty 300) | dobrý, bankovní odhad 2022 15 M | 13 999 000 | **38 353** (na bytech 46 700) | 20. 10. 2025 / 2. 11. 2026 (**inzerováno 12 měsíců**) | 37798732 |

Medián jádra (n = 5): **46 552 Kč/m²**, průměr 48 900, rozpětí 38 400–60 700.

### 1b. Rozšířený vzorek (pro rozpětí; slabší srovnatelnost)

| # | Lokalita (okres) | Popis | Plocha | Stav | Cena Kč | Kč/m² | Vloženo | ID |
|---|---|---|---|---|---|---|---|---|
| 6 | Dublovice-Líchovy (Příbram) | dům se 3 jednotkami (64+90+100 m²) + chata, rekreační lokalita | 319 | dobrý | 16 999 000 | 53 288 | 23. 6. 2026 | 2677272652 |
| 7 | Zeleneč-Mstětice (Praha-východ) | atypický dům k přestavbě na byty, pozemek 2 104 m² | 390 | před rekonstrukcí | 14 880 000 | 38 154 | 6. 10. 2026 | 369692748 |
| 8 | Černošice, Pod Horkou (Praha-západ) | 3podlažní dům, lze 1–3 byty | 260 | velmi dobrý | 13 800 000 | 53 077 | 13. 10. 2026 | 2729578572 |
| 9 | Krásná Hora n. Vlt. (Příbram) | 2 domy na náměstí, komerce + až 5 bytů | 350 | dobrý | 9 975 000 | 28 500 | 4. 8. 2026 | 3436302412 |
| 10 | Čáslav, Hluboká cesta (Kutná Hora) | RD + sklad 220 m², „až 9 bytů“ | 420 | před rekonstrukcí | 9 999 000 | 23 807 | 18. 8. 2026 | 4195270732 |
| 11 | Zásmuky, Havlíčkova 364 (Kolín) | 3 byty + 2 obchody + podkroví, rok 1932 | 540 | dobrý | 9 500 000 | 17 593 | 9. 7. 2026 | 3280920652 |

Medián všech 11 (jádro + rozšířený): **44 085 Kč/m²**.

### 1c. Mimo medián (odlehlé nebo bez ceny)

| Lokalita | Popis | Cena / Kč/m² | Poznámka | ID |
|---|---|---|---|---|
| Nehvizdy, Pražská (Praha-východ) | 7 bytů 1+kk/2+kk, novostavba 2019, TČ, hotové prohlášení vlastníka | 40 000 000; **141 074** na 283,5 m² | vloženo 30. 10. 2026; novostavba v Praze-východ, horní mez (cena ≈ cena bytů) | 622919756 |
| Konojedy (Praha-východ) | 3 bytové části, kolaudace 2020 | 12 990 000; 67 306 | novostavba | 1115340876 |
| Čáslav-Filipov (Kutná Hora) | 5 pronajatých bytů + špýchar, kulturní památka, zahrada 3 000 m² | 20 998 000; 55 550 | stav „špatný“, památka | 2647445580 |
| Černolice (Praha-západ) | nedokončený dům 375 m², 7+kk, nutná investice | 14 990 000; 39 973 | scénář nájmu 70 000 Kč/měs. | 1133326412 |
| Čáslav, Čermáka (Kutná Hora) | komerce + ordinace + kanceláře | 12 970 000; 39 543 | ne bytový dům | 2990280780 |
| Kolín, Pražská 177 | 5 bytů 42–117 m² (314 m²), **tržní nájem celkem 92 000 Kč/měs. (293 Kč/m²)** | cena v RK | jen nájem využit níže | 4186526540 |
| Pečky, Barákova (Kolín) | 6 pronajímaných jednotek, 336 m² | cena v RK | | 2865430604 |
| Křivsoudov (Benešov) | 4× 3+1 po 67,5 m² (270 m²), zateplení, TČ, majitel | cena na dotaz | vloženo 29. 9. 2026 | 1399857228 |
| Benešov, Pod Hřbitovem 2261 | novostavba 8 bytů | cena v RK | vloženo 14. 11. 2025 | 3803784012 |
| Vlašim, Jana Očka | rozestavěno, 11 bytů | cena nezveřejněna | viz `ceny-domy.md` | 3119386700 |
| Tábor, náměstí č.p. 13 | historický činžovní dům z r. 1703 | 27 900 000 | RE/MAX One, 28. 4. 2026; plocha neznámá, nesrovnatelné; zdroj: https://rk.realitnieso.cz/PDF_detail/nabidka/K-prodeji-Cinzovni-dum/4400794 | – |

**Nejbližší analogie k č.p. 1598:** Zaječov-Kvaň (#3): 4 byty, tuhá paliva, k rekonstrukci, **pozemek jen pod domem a okolí obecní**. Nabídka 10,95 M (asking, od 3/2026, tedy pravděpodobně nad trhem).

### 1d. Prodané / vysoutěžené (skutečné ceny)

| Objekt | Prodejce / forma | Výchozí | Konečná | Navýšení | Datum | Zdroj |
|---|---|---|---|---|---|---|
| Libenice 102 (Kolín), RD se 2 byty, 299 m², pozemek 593 m², interiéry zanedbané | výběrové řízení (insolvence/soukromé), cena snížená na 60 % posudku | 3 990 000 (asking 25. 6. 2026) | 4 311 111 (nejvyšší nabídka 3. kola; 2. kolo 4 177 777) | **+8,0 %** (+4,7 % ve 2. kole) = 14 418 Kč/m² | léto 2026 | https://www.edrazby.cz/detail/vyberove-rizeni-na-prodej-rd-2-bytove-jednotky-podlahova-plocha-299-m2-pozemky-c/b940a1bb5d15e638 (4. 11. 2026) |
| Tábor, rodinný (nárožní) dům z odúmrti, 2 pozemky 552 m² | ÚZSVM e-aukce, 100 příhozů | 9 000 000 | **14 750 000** | **+63,9 %** | 2025 | ÚZSVM výroční zpráva 2025, s. 26 a 32: https://www3.uzsvm.gov.cz/2026/04/01/vyrocni_zprava_uzsvm_2025.pdf |
| Náchod, dům | ÚZSVM e-aukce | 15 000 000 | 17 550 000 | +17,0 % | 2025 | tamtéž, s. 26 |
| Harrachov, chata Koruna | ÚZSVM e-aukce | 9 000 000 | 11 500 050 | +27,8 % | 2025 | tamtéž |
| Staré Sedlo, pozemky | ÚZSVM e-aukce | 10 887 000 | 13 887 000 | +27,6 % | 2025 | tamtéž |
| Žižkov, budova s pozemky | ÚZSVM e-aukce, 243 příhozů | 79 120 000 | 387 000 000 | ×4,9 | 2025 | tamtéž (extrém, nepoužívat) |
| Ústí n. Orlicí, rodinný dům | ÚZSVM e-aukce | 625 000 | 3 660 000 | ×5,9 | 2024 | https://www3.uzsvm.gov.cz/2025/08/29/vyrocni_zprava_uzsvm_2024.pdf, s. 22 (extrém) |
| Praha-Lipence, rekreační chata | ÚZSVM e-aukce | 5 643 000 | 8 500 000 | +50,6 % | 2024 | tamtéž |
| Kobylisy, byt 2+kk (odúmrť) | ÚZSVM e-aukce, 50 příhozů | 3 800 000 | >4 500 000 | >+18 % | 2024 | tamtéž |

Výsledky Správy železnic, ÚZSVM ani ČD pro **bytový dům** ve střední Čechách jsem nenašel (ÚZSVM prodává bytové domy zřídka, částky u jednotlivých aukcí jsou v detailu na nabidkamajetku.gov.cz, který neindexuje vyhledávání).

## 2. Jak se prodává u ČD / ÚZSVM a o kolik nad vyvolávací cenu

**ČD – výběrové řízení (písemné nabídky v zalepené obálce):**
- Podmínky ČD z oznámení pro Kladno-Kročehlavy (NB502936, bývalá administrativní budova, 4. 10.–10. 11. 2023, min. cena 4 400 000 Kč): https://nemovitosti.ceskedrahy.cz/GetAttachment.ashx?docid=0050569E8BD71EEE97A6BDBC7C9CB53A. Hlavním kritériem je **nabízená kupní cena, která musí být ≥ minimální stanovená**. Vyhlašovatel může vyhlásit **2. (i další) kolo**, ve kterém nabídka nesmí být nižší než v 1. kole; k jednání o smlouvě vyzve vybraného zájemce; má právo žádnou nabídku nepřijmout; prodej podléhá **souhlasu představenstva a dozorčí rady**. Kupní cena se platí před podpisem (převod/úschova).
- Jiné oznámení ČD (min. 175 000 Kč, nabídky do 30. 11. 2025 12:00) má stejný text (zdroj z vyhledávání: https://nemovitosti.ceskedrahy.cz/GetAttachment.ashx?docid=0050569E5C8B1FD081A909F3EA5E2000).
- **Inference (neověřeno u č.p. 1598):** uvedená cena 8 326 000 Kč je s velkou pravděpodobností **minimální kupní cena**. Přílohu k NB503213 (podmínky) jsem nenašel (stránka `/nemovitost/NB503213` vrací 404). Ověřit v příloze.
- **Výsledky ČD nezveřejňuje.** Stránka https://nemovitosti.ceskedrahy.cz/Results.aspx?fgroup=S (151 nabídek) neobsahuje příznak „prodáno“ ani vítěznou cenu; https://nemovitosti.ceskedrahy.cz/Nabidka-vybranych-objektu.aspx (4. 11. 2026) uvádí jen, že prodeje jdou výběrovým řízením a podléhají schválení představenstva a dozorčí rady. Výroční zpráva ČD 2025 (https://www.ceskedrahy.cz/sites/default/files/soubory-ke-stazeni/financni-zpravy/vyrocni-zprava_2025.pdf) výnos z prodeje po objektech nerozlišuje (nečteno do hloubky). Žádné médium, které by uvádělo výsledek ČD výběrového řízení u bytového domu, jsem nenašel. Neověřené zprávy o neúspěšných pokusech (Harrachov, 7 pokusů bez zájemce – newstream.cz, převzato z `ceny-domy.md`) naznačují, že u defektních domů bývá zájemců málo.

**ÚZSVM – elektronická aukce (otevřené příhozy):** zveřejněné výsledky 2024–2025 (tabulka 1d) ukazují **+17 % až +64 %** nad výchozí cenou u domů a chat (medián z 6 běžných případů ≈ +28 %), u extrémů ×5. Výchozí cena je ale u ÚZSVM často záměrně nízká (u Žižkova a Ústí n. O. startovní cena byla jen 17–20 % konečné), takže **poměr k tržní hodnotě je mnohem menší než poměr k výchozí**. Starší údaj MF: nemovitosti v následných aukcích +16 % (2018–2019, zdroj z vyhledávání: https://mf.gov.cz/cs/aktualne/tiskove-zpravy/2019/nabidky-nepotrebneho-statniho-majetku-no-35564, neověřeno ve zdroji).

**Soukromé soutěže:** Libenice +8,0 % nad cenou snížené na 60 % posudku (3 kola). Kutná Hora (město), dům U Tří pávů: 11,111 M, 2 zájemci, jeden vyřazen pro nesplnění minima (Kutnohorský deník, https://kutnohorsky.denik.cz/zpravy-region/konec-letiteho-chatrani-historicky-dum-u-tri-pavu-v-centru-kutne-zmeni-majitele/, bez data v mém výtahu).

**Závěr pro soutěž ČD (ODHAD, nízká jistota):** protože ČD 8,326 M ≈ tržní hodnota „as-is“ (viz oddíl 5a), na rozdíl od ÚZSVM (nízký start) se čeká jen mírné navýšení: **0 až +25 %, realisticky +5 až +10 %** (9,0 M ≈ 23 400 Kč/m² podlahové). Čím víc zájemců (zdevastovaný dům, přístup přes SPÚ, odpojená elektřina nižší zájem), tím blíž minimu. Nabídka pod 8 326 000 Kč nemá smysl (musí být ≥ min.).

## 3. Požadovaná hrubá výnosnost (yield) u malých činžáků 2026

| Údaj | Hodnota | Zdroj / datum |
|---|---|---|
| Nabídka Na Chmelnici, Benešov: nájem 55 000/měs. při ceně 12 499 000 | **5,3 %** hrubých | výpočet z inzerátu 2905808972 (24. 10. 2026) |
| Petroupim: „až 70 000 Kč/měs.“ při ceně 13 490 000 | 6,2 % (potenciální nájem) | inzerát 1381310540 (1. 10. 2026) |
| Černolice: 70 000/měs. po dokončení při 14 990 000 | 5,6 % (scénář) | inzerát 1133326412 (5. 10. 2026) |
| Kutná Hora Husova: „čistý roční výnos 6 %“ | netto 6 % (hrubých cca 7,5–8 % ODHAD) | inzerát 37798732 (2. 11. 2026) |
| Byty Benešov (jednotlivě) | 4,8–5,0 % | `ceny-domy.md`, oddíl 4 |
| ČR průměr hrubá výnosnost investičního bytu | 3,65 % (leden 2026) | UniCredit, přes https://ekonom.cz/c1-67848870-vynosy-investicnich-bytu-padaji-terno-uz-nejsou-ani-drive-vynosne-lokality-v-regionech (24. 2. 2026) |
| Nejvyšší regionální: Ústí n. L. 5,7 %, Karlovy Vary ~6 %, Ostrava < 5 % | | tamtéž |
| Prime rental housing yield ČR | 4,50 % (Q1 2026), 4,25 % (Q2 2026) | Knight Frank přes https://www.property-forum.eu/news/czech-investors-shift-focus-to-rental-housing-and-hotels/21451 (30. 4. 2026) a přehled v WebSearch (Q2) |
| Regiony a menší města, bytový investor | 5–7 % hrubých | roiestate.cz, https://roiestate.cz/jak-vybrat-investicni-byt-a-neslapnout-vedle/ (2026, blogový zdroj, nízká váha) |

**Interpretace:** nabídkové ceny dobře udržovaných malých domů v okolí Benešova znamenají **hrubý výnos 5,3–6,2 %** (z deklarovaných nájmů). Po slevě nabídka → prodej 8 % je to **5,8–6,8 %**. Za dům vyžadující rekonstrukci investoři požadují nominálně 7–9 % z nájmu po rekonstrukci (ODHAD, žádný publikovaný zdroj pro tento segment); z toho plyne, že hodnota „as-is“ je hodnota hotového domu minus náklady rekonstrukce minus riziková marže.

**Nájmy do výpočtu (Kč/m²/měs., hrubé, bez služeb):** Na Chmelnici 267 (55 000/206), Kolín Pražská 293 (92 000/314), Petroupim 229 („až“), Benešov malé byty 292, velké 315 (`ceny-domy.md`). Pro velké byty (4+1, 3+1 67–100 m²) v domě 1980 s TP topením: **ODHAD 245 (b) až 270 (c) Kč/m²** → nájem celého domu při 285 m²: (b) 838 000, (c) 923 000 Kč/rok.

## 4. Portfoliová sleva (celek vs. součet bytů) a nabídka → realizace

**Výpočet ze srovnávacích dat** (nabídková cena domu Kč/m² vs. medián nabídek bytů v téže oblasti, Sreality API, staženo 4. 11. 2026):

| Dům | Kč/m² dům | Kč/m² byty (medián okresu) | Rozdíl |
|---|---|---|---|
| Na Chmelnici, Benešov | 60 675 | 97 017 (město Benešov, n = 18) / 84 603 (okres Benešov, n = 77) | −37 % / −28 % |
| Petroupim | 44 085 | 84 603 | −48 % |
| Mokrovraty | 46 552 | 82 296 (okres Příbram, n = 130) | −43 % |
| Dublovice | 53 288 | 82 296 | −35 % |
| Zaječov (k rekonstrukci) | 54 750 | 106 531 (okres Beroun, n = 166) | −49 % |
| Kutná Hora Husova | 38 353 | 86 036 (okres Kutná Hora, n = 56) | −55 % |
| Konojedy (nové) | 67 306 | 122 679 (okres Praha-východ, n = 306) | −45 % |
| Černošice | 53 077 | 127 105 (okres Praha-západ, n = 267) | −58 % |

Medián hrubého rozdílu **−46 %** (n = 8). Je přeceněný: medián bytů v okrese zahrnuje novostavby a lepší stav a dům se prodává hůř. Při srovnání se starším bytem (cca −20 % pod okresní medián, ODHAD) vychází **srovnatelný rozdíl cca −30 %** (rozpětí −20 až −40 %). Jediná nezávislá kvantifikace, kterou jsem našel, je nepodložené tvrzení makléře, že prodej po bytech vynese asi o 30 % víc než celek (https://www.najemnidomybrno.cz/jak-prodat-najemni-dum/) ⇒ celek ≈ −23 %. Reálné odhady pro č.p. 1598: součet renovovaných bytů ≈ 68 000 Kč/m² (ODHAD: 80 % okresního mediánu 84 600) × 285 = 19,4 M vs. celek (c) 14,25 M ⇒ −27 %. **Pozn.:** prodej po bytech vyžaduje prohlášení vlastníka a zápis jednotek, u č.p. 1598 to je další náklad a čas; navíc vlastník pozemku musí být vyřešen (pozemek pod domem je ČD, kupující koupí jen pozemek 239 m²).

**Nabídka → skutečná cena (domy):**
- Valuo: průměrná vyjednaná sleva byla začátkem 2023 asi 11,5 %, 2024–2025 asi 2 %, nyní (říjen 2026) 5–6 % (byty). Zdroj: https://www.newstream.cz/reality/prodavajici-ustupuji-kupujici-si-znovu-rikaji-o-slevy-a-rok-2027-muze-byt-jejich (8. 10. 2026).
- Valuo 2023: u domů rozdíl průměrně 11,4 %, u bytů nižší (zdroj z vyhledávání, neověřeno ve zdroji). Plošných 21 % z banky.cz (3. 2. 2026) je zkreslených extrémy v ústeckém a moravskoslezském kraji; Praha/Brno/Plzeň 10–15 %. Středočeský kraj v obou zdrojích není.
- Použito: **−8 % (rozpětí −3 až −12 %)** z nabídky na realizaci.
- Signál: Kutná Hora Husova se prodává 12 měsíců a bankovní odhad 2022 byl 15 M, takže asking 14 M zjevně neprošel.

## 5. Odvození ceny č.p. 1598

Báze: plocha bytů **285 m² (260–310)**, podlahová plocha 384 m². Tabulky v Kč/m² bytů i podlahové. Ve všech řádcích jde o **tržní hodnotu celého domu v daném stavu** (ne čistý zisk; náklady rekonstrukce odečítá model zvlášť).

### (a) Současný stav
Východiska: nerekonstruované domy v nabídkách 17–55 tis. Kč/m² (Zásmuky 17,6; Čáslav 23,8; Krásná Hora 28,5; Zeleneč 38,2; Zaječov 43,8–54,8 včetně možného nadhodnocení); prodané zchátralé RD 14,4 tis. (Libenice). Rizika č.p. 1598: odpojený od elektřiny, trhliny (statika neověřena), plíseň, tuhá paliva, plochá střecha, přístup přes cizí (SPÚ) pozemek, pozemek jen pod domem. Výchozí cena ČD odpovídá **29 200 Kč/m² bytů**, tj. mému realistickému odhadu.

### (b) Standardní rekonstrukce bytů
Byty hotové, obálka a technika jen částečně (tuhá paliva, stará střecha a fasáda). Hodnota ≈ 82 % hotového (c) domu (ODHAD, poměr z nabídek „dobrý stav“ 38–47 tis. vs. „po rekonstrukci/nový“ 44–61 tis.); výnos při nájmu 245 Kč/m² = 7,2 % hrubých z hodnoty.

### (c) Kompletní rekonstrukce
Hotový dům s novou technikou. Medián jádra srovnání 46,6 tis., po slevě nabídka → prodej −8 % 42,8 tis., s prémií Benešova (nájmy 292–315) a srážkou za pozemek/přístup. Výnos při nájmu 270 Kč/m²: pes. 7,7 %, real. 6,5 %, opt. 5,6 % hrubých (srovnej s 5,3–6,8 % z oddílu 3).

---

## Shrnutí pro model

**Konvence:** „pes.“ = nízká hodnota domu, „opt.“ = vysoká (tj. pro výstupní/zástavní hodnotu). Pro **nákupní cenu v soutěži** platí opak: pes. = nejvyšší cena, kterou musíte dát, opt. = minimum.

### Cena celého domu (hodnota ve stavu)

| Stav | | Pesimistické | Realistické | Optimistické | Kč celkem (260–310 m² bytů) |
|---|---|---|---|---|---|
| **(a) současný** | Kč/m² podlahové (384) | **14 800** | **21 500** | **28 200** | pes. 5,7 M; real. 8,3 M; opt. 10,8 M |
| | Kč/m² bytů (285) | 20 000 | 29 000 | 38 000 | |
| **(b) standardní rekonstrukce bytů** | Kč/m² podlahové | **25 200** | **30 400** | **35 600** | pes. 9,7 M; real. 11,7 M; opt. 13,7 M |
| | Kč/m² bytů | 34 000 | 41 000 | 48 000 | |
| **(c) kompletní rekonstrukce** | Kč/m² podlahové | **31 200** | **37 100** | **43 000** | pes. 12,0 M; real. 14,25 M; opt. 16,5 M |
| | Kč/m² bytů | 42 000 | 50 000 | 58 000 | |

Rozpětí v Kč při jiné ploše bytů (260 / 310 m²): (a) real. 7,5 / 9,0 M; (b) real. 10,7 / 12,7 M; (c) real. 13,0 / 15,5 M.

Kontrola proti `ceny-domy.md`: tam „realistických 40 000 Kč/m² užitné“ (ODHAD, užitná cca 320 m²) dává dům za 12,8 M. Moje (c) real. 14,25 M je o ~10 % výš a (b) real. 11,7 M o ~9 % níž, tedy stejný řád. Rozdíl: medián skutečných nabídek bytových domů 44–47 tis. Kč/m² bytů je teď podložený daty (n = 5–11), kdežto tehdejších „45 % ceny bytů“ ne.

### Nákupní cena v soutěži ČD (stav a)

| | Pesimistické (pro kupujícího) | Realistické | Optimistické |
|---|---|---|---|
| Navýšení nad vyvolávací 8 326 000 Kč | **+25 %** (10,4 M; 27 100 Kč/m² podl.) | **+8 %** (9,0 M; 23 400 Kč/m² podl.) | **0 %** (8,326 M; 21 700 Kč/m² podl.) |

Podklad: výběrové řízení ČD v zalepené obálce, cena = hlavní kritérium, min. cena závazná (podmínky ČD 2023); Libenice +8 %; ÚZSVM e-aukce +17 až +64 % (jiný mechanismus, nízký start). Výsledky ČD se nezveřejňují, jistota **nízká**. Strop rozumné nabídky = tržní hodnota (a) opt. 10,8 M, nad ní by se koupě nevyplatila ani při nulové ceně rekonstrukce.

### Portfoliová sleva (celek vs. součet bytů)

| Pesimistické (celek nejlevnější) | Realistické | Optimistické |
|---|---|---|
| **−40 %** | **−30 %** | **−20 %** |

Surový rozdíl proti okresním mediánům nabídek bytů −46 % (n = 8), srovnatelný po úpravě na starší stav ODHAD −30 %.

### Doplňkové vstupy

| Veličina | Pes. | Real. | Opt. | Poznámka |
|---|---|---|---|---|
| Sleva nabídka → prodej (domy) | −12 % | −8 % | −3 % | Valuo (newstream 8. 10. 2026), Libenice |
| Hrubý výnos požadovaný u hotového malého činžáku | 7,0 % | 6,3 % | 5,5 % | nabídky 5,3–6,2 % (Na Chmelnici, Petroupim), po slevě 5,8–6,8 % |
| Hrubý výnos požadovaný u domu k rekonstrukci (z nájmu po rekonstrukci) | 9 % | 8 % | 7 % | ODHAD, bez publikovaného zdroje |
| Nájem velké byty v domě Kč/m²/měs. | 230 | 270 (c) / 245 (b) | 293 | Kolín Pražská 293; Na Chmelnici 267; Petroupim 229; Benešov velké 315 (n = 2) |
| Kč/m² nabídkové ceny nových bytů v Benešově (kontrola) | 84 600 (okres) | 97 000 (město, n = 18) | 89 394 (Housi) | Sreality API 4. 11. 2026 |

---

## Otázky k ověření

1. **Je 8 326 000 Kč minimální kupní cena?** Příloha „podmínky výběrového řízení“ k NB503213 (stránka `/nemovitost/NB503213` vrátila 404). Pokud je to jen orientační cena, může se vejít i pod ni.
2. **Přístup přes SPÚ a pozemek pod domem:** Zaječov (#3) má stejný problém (okolí obecní) a v nabídce o něm kupující ví, ale bez ocenění. Potřeba ocenit služebnost (znalec) a srážku z hodnoty (v tabulce zahrnuta jen v (c) jako ~10 %, ODHAD).
3. **Zaječov-Kvaň, Mokrovraty, Petroupim, Na Chmelnici:** zjistit skutečné nájmy a po prodeji dosaženou cenu (kontakt na RK, katastr/listina po kolaudaci; nelze ze Sreality).
4. **Skutečná plocha bytů č.p. 1598** (260–310 m² vs. 384 m²): ovlivní všechny výsledné Kč částky; jednotkové ceny v tabulce jsou na plochu bytů.
5. **Statika (trhliny):** pokud posudek ukáže vadu základů, hodnota (a) klesne pod pesimistickou (5,7 M).
6. **Výsledky ČD a Správy železnic:** zkusit požádat o poskytnutí informace podle zákona č. 106/1999 Sb. (ČD je akciová společnost ve vlastnictví státu, povinnost je diskutabilní); Správa železnic je povinný subjekt. Neodesíláno, jen návrh.
7. **Portfoliová sleva:** chybí transakční data; ověřit u realitního znalce (cena celku vs. jednotek podle prohlášení vlastníka) a na Valuo/Deloitte Real Index, zda existují data pro domy.
8. **Yield požadovaný investory u domů k rekonstrukci (7–9 %)** je ODHAD bez zdroje.
9. **iDNES Reality, RealityMix, Bezrealitky, Bidli:** neprošly (blokace/404). Pro úplnost doplnit ručně nebo přes prohlížeč.
10. **Okres Tábor:** v kategorii Činžovní dům na Sreality není žádný inzerát (Jihočeský kraj). Použit jen ÚZSVM prodej z r. 2025 (14,75 M, plocha budovy neznámá) a nabídka náměstí č.p. 13 (27,9 M).
