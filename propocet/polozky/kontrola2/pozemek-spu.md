# Kontrola 2: Pozemek SPÚ, přístup a stání (5. 11. 2026)

Web (real, bez nástavby): **236 tis.** = `pristup` 125,5 + `parkovani_1_poz` 110 (`model.py` ř. 88, 93; `report.py` ř. 262–274). Dílčí položky na webu jsou dopočtené na tento součet. Rozpis a zdroje: `polozky/pristup-parkovani.md`, `podklady/katastr.md` ř. 100–106, 217, `podklady/uzemni-plan.md` ř. 103, 183–197.

## 1. Tabulka po dílčích položkách (tis. Kč s DPH)

| Položka | Web | Můj odhad real | pes–opt | Potřeba | Nejlevnější rozumná cesta | Zdroj |
|---|---|---|---|---|---|---|
| Koupě pruhu SPÚ od ulice k domu, 25 m² × 3 500 | 88 | 88 | 500–0 (web pes 500 = 100 m² × 5 000; opt 0 = VB už zapsané) | **Ano.** Bez právního přístupu banka kupci neposkytne hypotéku a ČD v kartě nabídky uvádí „Věcné břemeno: Ne“ (`katastr.md` ř. 12, 73, 217). | Služebnost místo koupě ušetří ~35–45 tis. (viz bod 2). Rozloha: 4,7 m × ~5 m, na pruh stačí i 3,5 m (−7 tis.), ale rezerva na šířku je rozumná. | cena 3 500: ODHAD; inzerce okres Benešov 3 286–3 403 Kč/m² (reas.cz, ceskereality.cz, 5. 11. 2026), konkrétní nabídky Benešov 2 600 a Mariánovice 3 830 Kč/m² |
| Geometrický plán (pruh + stání) | 18 | **11** (GP 10 + příplatek za 2. část 4 → celkem ~14 včetně obou) | 8–25 | **Ano.** Oddělení z 2128/3 nejde bez GP. | Geodet je dnes OSVČ nebo s. r. o. za 4 500–11 400 Kč bez DPH za oddělení (vytyčení +2 000–3 000). Dvě části + vytyčení + DPH = 12–16. Nic dalšího se ušetřit nedá. | Geodézie Vysočina 8 300 / 11 400 s vytyčením bez DPH, Geodezie Bohemia 4 500–7 000, Geodezie UO 7 000–8 000 + vytyčení 2 000 (jejich ceníky, 5. 11. 2026) |
| Znalecký posudek na cenu | 15 | **8** | 5–15 | **Ano.** SPÚ prodává jen za cenu obvyklou podle posudku (§ 14 zák. 503/2012). | Platí kupující. Nejlevnější je soudní znalec – OSVČ neplátce DPH, 6–10 tis. | ceníky znalců: pozemek 3 000–12 000 Kč (posudekpraha.cz, trznicena.com, deluxreality.cz, 5. 11. 2026); malý pozemek bez budovy je levnější než dům, web 15 je spíš horní hranice |
| Vklad do KN | 2 | 2 | 2 | Ano (vlastnictví vzniká vkladem). | Elektronicky 1 600 Kč (sleva 20 %), v praxi 2 | správní poplatek 2 000 Kč, položka 120 sazebníku 634/2004 Sb. (hyponamiru.cz, drbacon.cz, 5. 11. 2026) |
| Nájem části pozemku do převodu | 3 | 2 | 0–10 | **Ano.** § 10 odst. 3/4 chce „oprávněného uživatele“ sousedního pozemku: žadatel musí být nájemce či pachtýř podle smlouvy se SPÚ (spu.gov.cz, 5. 11. 2026). | Roční nájem malé části zahrady je v řádu stovek až tisíců Kč, minimální. Smlouva na ~1 rok. | ODHAD (SPÚ sazby nenalezeny); `katastr.md` ř. 103 |
| Koupě pozemku pro 1 stání a vjezd (25 m² × 3 500) | 106 (110 s GP) | **100** | 600–30 | **Jen když** úřad stání po změně užití chce. 86 m² nebytové části / 120 = 0,72 → 1 stání (zaokrouhlení ≥ 0,5 nahoru); 2 byty 2+kk po ~38 m² = 76 m² → 0,63 → 1 stání (vyhl. 146/2024, příl. 1, `uzemni-plan.md` ř. 103). Úřad může chtít i celý dům, 344/120 = 2,9 → 3. | Služebnost k parkování (viz bod 2). Nebo stání na pruhu: pruh 4,7 m dlouhý se dá využít jako 1. stání (5 × 2,5 m), pak se pozemek pro stání ušetří úplně (−88). Úřad to ale nemusí přijmout bez vjezdu. | vážený odhad: 15 % 0 stání, 65 % 1, 20 % 3 stání → 0,65 × 87,5 + 0,2 × 262 = 109 (ODHAD, model ř. 88) |
| GP příplatek za druhou část | 4 | (zahrnuto výše) | 3–12 | Ano | Jedna GP pro obě části | viz GP |
| **Součet** | **236** | **~214** (211 + DPH riziko) | pes 600+500 · opt 30 | | | |

Pozn.: 214 = 88 + 14 (GP obě části) + 8 + 2 + 2 + 100. K tomu přistupuje riziko DPH 21 % (viz bod 2), které je v očekávané hodnotě asi +8, takže **~222**.

## 2. Zvlášť prověřeno

**Cena za m².** Cenová mapa stavebních pozemků: obec Benešov **nemá** platnou CMSP (v přehledu MF k 23. 3. 2026 je v okrese Benešov jen Vlašim, vyhláška z roku 1994; mf.gov.cz/assets/attachments/2026-03-23_Prehled-cenovych-map-stavebnich-pozemku-obci-CMSP.pdf, přečteno 5. 11. 2026). Znalec tedy ocení srovnáním. Inzertní ceny stavebních pozemků okres Benešov 3 286–3 403 Kč/m² (reas.cz, ceskereality.cz), město Benešov 2 600–3 830 Kč/m² (`pristup-parkovani.md`). Skutečné ceny bývají pod inzercí. Naopak malý pruh k domu vedle nádraží znalec může ocenit i na 4 000–5 000. Prodejní ceny SPÚ jsou v registru smluv (smlouvy.gov.cz), konkrétní srovnatelný prodej v Benešově jsem nenašel. **3 500 Kč/m² nechávám** (rozpětí 2 000–6 000 platí).

**DPH 21 % u prodeje SPÚ.** Od 1. 7. 2025 je v § 55a ZDPH osvobozen jen pozemek, který **není stavební**. Stavební pozemek je ten, na kterém lze podle územního plánu nebo vymezeného zastavěného území umístit stavbu, i když je v katastru „zahrada“ (dauc.cz/clanky/15121, 5. 11. 2026). Ulice u nádraží je v ploše BI, takže pruh i stání jsou s vysokou pravděpodobností stavební pozemek = **21 %** (pokud je SPÚ plátce; v registru smluv jsou ceny SPÚ uváděny „bez DPH“, takže DPH se k ceně přičítá). Dopad: 21 % z ~175 tis. = **37 tis.** Jako kupující plátce DPH (§ 56 prodej bytů s DPH 12 %) si ji ale **odečteš**, pokud pozemek skončí u prodaných bytů (jako podíl na společných částech nebo jako příslušenství), takže je to jen cash-flow, ne náklad. Jen když pozemek v prodeji nezůstane (zůstane u tebe), odpočet nejspíš nebude. Pravděpodobnost ~25 % × 37 = **+9 tis.** Doporučení: do rozpočtu nedávat, ale **zeptat se SPÚ**, zda k ceně přičte DPH, a pozemek zahrnout do prohlášení vlastníka.

**Služebnost místo koupě.** Cena věcného práva za jednorázovou úplatu určenou posudkem, zhruba 30–50 % ceny pozemku (ODHAD, `pristup-parkovani.md`; vzorová smlouva o služebnosti stezky a cesty na smlouvy.gov.cz, úplata podle posudku). Pro pruh ~26–44 tis. místo 88, GP a posudek zůstávají, vklad zůstává. Úspora **~45 tis.**, pro stání o něco méně, ale:
- není rychlejší: SPÚ musí tak či tak schválit, posudek i GP jsou potřeba. Jediné, co odpadá, je nájem „oprávněného uživatele“ (§ 10 odst. 4), takže cca 3 tis. a hlavně **čekání**;
- je slabší ochrana (banka kupce a kupci bytů uvidí cizí pozemek, SPÚ může pozemek později prodat třetí osobě s břemenem), zhoršuje to prodejnost 6 bytů. Doporučuji **koupi** a služebnost mít jako záložní variantu, kdyby SPÚ koupi odmítlo (§ 6 zák. 503/2012: pozemky pro dopravní infrastrukturu a veřejně prospěšné stavby nelze převést; podnět na změnu ÚP BI → BH, `uzemni-plan.md`).

**Víc stání než 1.** V1 (bez nástavby) = jen přírůstek 86 m² → 1 stání. Praxe MěÚ Benešov žádala jen rozdíl a stání povolila i na cizím pozemku (MUBN/189104/2023/VÝST, `pristup-parkovani.md`). Hrozba 3 stání (celý dům) je zahrnuta váženě (~+20 tis.). Výjimka podle § 95 vyhl. 146/2024 s poplatkem +5 000 Kč existuje, ale není jistá. Stání do 300 m od domu jinde nejsou prověřená.

**Doba SPÚ.** Oficiální lhůta na webu SPÚ ani portálu občana není (spu.gov.cz, portal.gov.cz, 5. 11. 2026). Postup: nájem → žádost o převod → posudek → záloha na cenu → smlouva → vklad. Model: 12 měs. real, 24 pes, 6 opt (`model.py` ř. 94). To odpovídá `uzemni-plan.md` ř. 197 (12–24 měs.), **drží**. Riziko: nájem pozemku od ČD/SPÚ vůbec neexistuje a musí se nejdřív uzavřít.

**Bez právníka.** Právník (24,5 tis.) je z modelu pryč a rozumím tomu: žádost, nájem a kupní smlouva se SPÚ jsou standardní vzory (smlouvy.gov.cz), zvládne to laik. Vklad podává kupující sám přes ČÚZK. Riziko: chyba v textu smlouvy (např. chybějící VB k jiným částem). Rozumná pojistka: **jednohodinová konzultace u advokáta nad hotovým návrhem smlouvy za 2–4 tis.** (ODHAD), není v ceně.

## 3. Součet

| | tis. Kč |
|---|---|
| Web | 236 |
| Můj odhad real (stejné rozdělení, kupující sám) | ~214, s rizikem DPH ~222 |
| Nejlevnější rozumná varianta (stání na pruhu místo samostatného pozemku, GP/posudek nejlevnější, vklad online) | ~125–150 (pruh 88 + GP 10 + posudek 6 + vklad 2 + nájem 2 + malé stání/vjezd); riziko zamítnutí úřadem |
| Služebnost místo koupě | ~170–185 |

Rozdíl webu a mého real: **−6 až −9 %**, hlavně GP (18 → 14) a posudek (15 → 8) jsou nadsazené; cena pozemku dopadla stejně. Pod hranicí 10 %.

## 4. Chybí / dvakrát

- **Chybí: DPH 21 % u kupní ceny SPÚ** (+37 tis. na pozemek, zpravidla odpočitatelné; riziko +9 tis. očekávaně). Neřešit v položce, ale vyřešit v dotazu na SPÚ a v textu prohlášení vlastníka.
- **Chybí: záloha na kupní cenu před podpisem** (§ 14 odst. 3 zák. 503/2012) – nevadí, jen cash-flow, v modelu je pozemek už v měsíci 0.
- **Chybí: konzultace s advokátem** nad smlouvou 2–4 tis. (volitelné).
- **Dvakrát: nic.** GP, posudek a vklad jsou jen zde; dlažba a vjezd jsou v „Parkovací stání: stavba“ (90), ne zde. Ověřit, že „Ostatní (rozdělení)“ nezahrnuje GP pozemku.
- Podhodnocené: vážení 3 stání (20 %) je ODHAD; kdyby úřad chtěl 3 stání jistě, +175 tis. (pes 600 to kryje).

## 5. Doporučení

**Beze změny** (236 tis. real; pes/opt beze změny). Rozdíl proti mému odhadu je −6 až −9 %, tedy pod 10 %, a vyrovná ho riziko DPH a váhy za stání. Před koupí se zeptat SPÚ (1) zda k ceně přičtou DPH, (2) zda lze 2128/3 převést (§ 6), (3) zda stačí nájem + služebnost na stání.
