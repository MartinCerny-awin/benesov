# Katastr, právní stav, okolí a podmínky prodeje – č.p. 1598, Benešov u Prahy

Zpracováno 4. 11. 2026. Všechny údaje „RÚIAN" a „ZABAGED" jsou stažené 4. 11. 2026 z veřejných REST služeb ČÚZK (stav dat k tomuto dni). Co je označeno **ODHAD**, nemá zdroj.

**Co se nepodařilo (důležité):** detail parcely/stavby na nahlizenidokn.cuzk.gov.cz (vlastníci, omezení vlastnického práva, věcná břemena, zástavy, předkupní práva, plomby/řízení) je za **CAPTCHA** (Radware). CAPTCHU jsem neobcházel. Z veřejné části jsem získal jen druh pozemku, LV a typ stavby (viz 2). Tyto údaje musí ověřit člověk (viz „Jak získat LV").

---

## 0. Nejdůležitější zjištění

1. **Lhůta pro nabídku končí 16. 11. 2026 v 12:00** (doručení do ČD, Praha 1, Nábřeží L. Svobody 1222, zalepená obálka v obálce). Min. cena = 8 326 000 Kč, hlavní kritérium = cena. Zdroj: Zadávací podmínky (viz 5).
2. **Dům nemá přímý kontakt s žádnou veřejnou komunikací.** Pozemek 2113/3 (239 m², jen půdorys domu) sousedí jedině s parcelou 2128/3 (zahrada, SPÚ). Od silnice (parc. 3501) ho dělí nejméně ~4,7 m pozemku 2128/3 (výpočet z RÚIAN geometrie). Inzerát říká jen, že přístup „je zajištěn" přes 2128/3, ale **věcné břemeno neuvádí; ČD v kartě nabídky uvádí „Věcné břemeno: Ne"**. Zákonné ani smluvní právo přístupu tedy není doloženo.
3. **ČD nemůže dát nemovitost do zástavy** (zadávací podmínky) – ovlivňuje hypotéku (viz 3).
4. **Dům je podle ZABAGED ~290 m od nejbližší koleje**, tedy mimo zákonné ochranné pásmo dráhy (60 m od osy krajní koleje). ČD přesto v podmínkách tvrdí, že je v ochranném pásmu, a chce po kupujícím závazky (stavby jen se souhrnným stanoviskem Správy železnic, strpění hluku). **Rozpor – nutno vyjasnit** (viz 4).
5. **Dům je odpojen od elektřiny** (zadávací podmínky). Karta nabídky navíc uvádí „Voda/Plyn/Kanalizace: Ne", RÚIAN uvádí vodovod i kanalizaci ano, plyn ne. Rozpor.

---

## 1. Identifikace, adresa, GPS, RÚIAN

Zdroj: ČÚZK ArcGIS REST, služba RÚIAN Vyhledávací, vrstva StavebniObjekt (kód 2924498), dotaz z 4. 11. 2026:
`https://ags.cuzk.gov.cz/arcgis/rest/services/RUIAN/Vyhledavaci_sluzba_nad_daty_RUIAN/MapServer/3/query?where=cisladomovni='1598'` (vyfiltrováno na Benešov, kód SO 2924498).
Doplněk: [regiony.kurzy.cz/katastr/o2924498](https://regiony.kurzy.cz/katastr/o2924498/) (zrcadlí RÚIAN, platí od 21. 12. 2023).

| Údaj | Hodnota | Zdroj / poznámka |
|---|---|---|
| Adresa | **Jana Nohy 1598, 256 01 Benešov** (adresní místo kód 2947048). Jen č.p., **číslo orientační není** | RÚIAN, vrstva AdresniMisto |
| GPS (WGS84) | **49,77892 N, 14,67884 E** (těžiště půdorysu) | RÚIAN geometrie |
| S-JTSK (def. bod) | X −1 079 502,89, Y −729 106,25 | kurzy.cz/RÚIAN |
| Typ stavebního objektu | budova s číslem popisným | RÚIAN |
| Způsob využití | **objekt k bydlení** (ne „bytový dům", kód 3) | RÚIAN i KN (nahlížení) |
| Identifikační parcela | st. 2113/3, k.ú. Benešov u Prahy (602191) | RÚIAN |
| **Zastavěná plocha** | **239 m²** | RÚIAN; shodně výměra parcely 2113/3 |
| Půdorys | cca 23,7 × 10,0 m (zdroj geometrie DKM) | výpočet z RÚIAN polygonu |
| **Podlahová plocha** | **v RÚIAN neuvedena** | RÚIAN |
| **Obestavěný prostor** | **v RÚIAN neuveden** | RÚIAN |
| Počet bytů | **4** | RÚIAN |
| Počet podlaží | **2** (nadzemních i podzemních dohromady) | RÚIAN; souhlasí s fotkami |
| Svislá nosná konstrukce | kámen, cihly, tvárnice vč. kombinací (zděný) | RÚIAN |
| Vytápění | centrální domovní (kotel ve stavbě) | RÚIAN; souhlasí s kotelnou z prohlídky |
| Vodovod | s vodovodem | RÚIAN |
| Kanalizace | přípoj na kanalizační síť | RÚIAN |
| Plyn | **bez plynu** | RÚIAN |
| Výtah | bez výtahu | RÚIAN |
| Datum dokončení | 31. 12. 1980 (v RÚIAN) | Pravděpodobně přibližný údaj: stejné datum mají řada okolních budov (č.p. 1627, 1628, 1463, 1720). Skutečně asi 1980–81 |
| Zdroj geometrie | DKM (digitální katastrální mapa) | RÚIAN |

### Co je „384,46 m² (budovy)" v inzerátu
- Není to zastavěná plocha (ta je 239 m²) a **RÚIAN ani katastr podlahovou plochu nevedou**. Číslo je tedy údaj z interní evidence ČD (nelze ověřit).
- Hrubá podlažní plocha = 239 m² × 2 NP = **478 m²**. 384,46 / 478 = **0,80**, což je typický poměr čistá užitná (podlahová) plocha / hrubá plocha u zděného domu s tl. obvodových zdí ~45 cm.
- Vychází to i na ~192 m² čisté plochy na podlaží, což sedí na dřívější odhad 190–200 m² v zadání.
- **ODHAD (bez zdroje): 384,46 m² = součet podlahových (užitných) ploch obou podlaží včetně společných prostor, dílny, kotelny a skladů.** Pro model brát jako celkovou podlahovou plochu, ne jako plochu bytů. Jistotu dá jen ČD (otázka 1).

### Sousední stavby (kontext, RÚIAN)
- **Č.p. 1597 (parc. 2113/2, 237 m², 4 byty, 2 NP, objekt k bydlení)** – zjevně dvojče. Majitel neznámý (v CAPTCHA). Ve stejné situaci s přístupem. Pokud je také ČD, může se prodávat zvlášť.
- Č.p. 1627, 1628 (po 235/239 m², 6 bytů, 3 NP, bytový dům, také 1980/81) – o ulici dál.
- Řada vilek/řadovek č.p. 749–755 podél Za Nádražím.

---

## 2. Katastr nemovitostí (nahlizenidokn.cuzk.gov.cz) – co šlo zjistit

Zdroj: [nahlizenidokn.cuzk.gov.cz/ZobrazObjekt.aspx?typ=parcela&id=2278418201](https://nahlizenidokn.cuzk.gov.cz/ZobrazObjekt.aspx?typ=parcela&id=2278418201), veřejná část, 4. 11. 2026 12:20 (poté mě bot-ochrana zablokovala).

| Parcela | Výměra | Druh pozemku | Využití | Vlastník / správce | Zdroj |
|---|---|---|---|---|---|
| **2113/3** | 239 m² | zastavěná plocha a nádvoří | – (je na ní č.p. 1598, objekt k bydlení) | **České dráhy a.s., LV 6313** (LV potvrzeno KN, vlastník dle inzerátu) | KN + inzerát NB503213 |
| **2128/3** | 1 942 m² (3 okruhy polygonu) | zahrada | neuvedeno | ČR, příslušnost hospodařit SPÚ (jen dle inzerátu, v KN neověřeno) | RÚIAN, inzerát |
| **3501** | 9 979 m² | ostatní plocha | ostatní komunikace | Město Benešov (jen dle inzerátu) | RÚIAN, inzerát |
| 2113/2 (č.p. 1597) | 237 m² | zastavěná plocha | – | neznámý | RÚIAN |

Poznámky ke geometrii (výpočet z RÚIAN polygonů, 4. 11. 2026):
- Parcela 2113/3 se dotýká **jen parcely 2128/3**. Nejbližší bod parcely 3501 je ~4,7 m od domu. Parcela 2128/3 má 3 okruhy (zřejmě „díry" pro 2113/2 a 2113/3), takže obklopuje obě budovy.
- Trávník a okolí domu tedy **nejsou součástí prodeje** (potvrzuje zadání).

### Co je v CAPTCHA a co z toho potřebujeme
Pro 2113/3, stavbu č.p. 1598 i 2128/3 a 3501 jsem **nemohl** zjistit: vlastníky a podíly, **omezení vlastnického práva**, **věcná břemena** (zejména chůze a jízdy ve prospěch 2113/3 na 2128/3), **zástavní práva**, **předkupní práva**, **plomby / probíhající řízení**, způsob ochrany nemovitosti, způsob využití stavby v LV. Jediný veřejný náznak je karta nabídky ČD: „Věcné břemeno: Ne".

**Jak získat (člověk, ne já):** na stránce parcely vyřešit CAPTCHA (nebo se přihlásit přes Identitu občana) – zobrazí se vlastník a „Omezení vlastnického práva", „Jiné zápisy" a „Řízení" (plomby). Totéž pro 2128/3 (její LV je LV Státního pozemkového úřadu) – tam hledat „věcné břemeno ... ve prospěch ... st. 2113/3". Úřední výpis LV je placený (Czech POINT/ČÚZK). To, že samotné nahlížení je bezplatné a LV ukáže, vychází z provozu aplikace, ne z citovaného dokumentu.

---

## 3. Přístup, věcné břemeno a důsledky

### Stav
- ČD tvrdí: přístup „zajištěn" z parc. 3501 (město) a „dále přes" 2128/3 (stát/SPÚ). **Neuvádí právní titul.** V kartě: „Věcné břemeno: Ne".
- **Pravděpodobný stav (ODHAD): jen faktické užívání bez zapsaného práva.** Ověří jedině LV 6313 a LV pozemku 2128/3 (viz 2).
- Pokud VB (chůze a jízdy) na 2128/3 zapsáno je, ČD by to musela uvést v nabídce – typicky se uvádí. Jeho absence u prodeje je silný, ale ne důkazní náznak, že VB není.

### Důsledky
| Oblast | Důsledek (zdroj: vlastní úvaha, kde není uvedeno jinak) |
|---|---|
| **Koupě** | Kupující získá dům bez zajištěného přístupu. Stát (SPÚ) může kdykoli omezit vstup, požadovat úplatu nebo pozemek oplotit/prodat třetí osobě. Riziko pro celou hodnotu domu. |
| **Hypotéka** | (a) **ČD nemůže dát majetek do zástavy** (zadávací podmínky) – takže banka nemůže mít zástavu před převodem; řeší se úschovou ceny (podmínky úschovu připouštějí: notářská/advokátní úschova, jistotní účet). Banka si zástavu zapíše po vkladu vlastnictví. (b) Banky v ocenění zkoumají právní přístup k veřejné komunikaci; nezajištěný přístup obvykle znamená nižší LTV nebo zamítnutí. Konkrétní banku nutno oslovit (ODHAD z praxe). |
| **Prodej po bytech** | Prohlášení vlastníka (§ 1166 a násl. občanského zákoníku) vytvoří jednotky se spoluvlastnictvím společných částí (pozemek 2113/3 jen pod domem). Kupující jednotek budou mít stejný problém s přístupem a hypotékou. Bez vyřešeného přístupu bude cena a prodejnost jednotek horší (ODHAD). Přístup je proto **předpoklad** záměru, ne detail. |
| **Změna ve vlastnictví 2128/3** | Pokud stát pozemek prodá/převede třetí osobě bez VB, kupující domu je zablokován. VB zapsané v katastru by přešlo na nového vlastníka (OZ). |

### Jak se to dá řešit (podle spolehlivosti)
1. **Před podáním nabídky:** zjistit LV 2128/3 (zda VB je). Požádat SPÚ (Krajský pozemkový úřad pro Středočeský kraj, pobočka Benešov) o písemné stanovisko k zřízení VB / pronájmu / prodeji pozemku a o to, zda je 2128/3 vůbec převoditelný (viz níže § 6 odst. 1). Nic nesmí odejít za mě; viz „Otázky".
2. **Koupě části 2128/3 podle zák. č. 503/2012 Sb. (o Státním pozemkovém úřadu):**
   - **§ 10 odst. 3 písm. b)** – na písemnou žádost SPÚ převede vlastníkovi stavby pozemek sousedící s pozemkem, na němž stavba stojí, je-li to **zemědělský pozemek funkčně spojený se stavbou** a vlastník stavby je jeho **oprávněným uživatelem**. Při splnění **není nutná veřejná nabídka** (ta je v § 12 a vyžaduje 3× marnou nabídku). Zahrada je zemědělský pozemek (zák. č. 334/1992 Sb. – z paměti, ověřit).
   - **§ 14 odst. 1**: převod je úplatný, **nejméně za cenu obvyklou** (nebo vyšší zjištěnou). **§ 14 odst. 3**: záloha ve výši ceny před smlouvou. **§ 16 odst. 1**: žadatel bez dluhů vůči státu; zaplatí náklady ocenění.
   - **Háček:** žadatel musí být **vlastníkem stavby** (tedy až po vkladu) a **„oprávněným uživatelem"** pozemku. Pokud ČD nemá nájemní/jinou smlouvu s SPÚ na 2128/3, kupující ji sám nemá (ODHAD, že ČD smlouvu nemá). Proto otázka na ČD a SPÚ, zda existuje nájemní/užívací smlouva na 2128/3 a zda ji lze převést.
   - **Zákaz převodu § 6 odst. 1** (mj. písm. b: pozemky určené územním plánem pro veřejně prospěšné stavby; písm. j: pozemky určené pro dopravní infrastrukturu). Nutno ověřit v územním plánu Benešova, zda 2128/3 není takto určen.
   - Znění zákona jsem četl přes shrnutí z [zakonyprolidi.cz/cs/2012-503](https://www.zakonyprolidi.cz/cs/2012-503) (stránka z 4. 11. 2026); **doporučuji přečíst § 6, 10, 12–16 přímo**, protože jde o strojový výtah.
3. **Zřízení věcného břemene (služebnosti) chůze a jízdy** za úplatu (znalecký posudek na hodnotu VB, geometrický plán pro vymezení trasy). Podle občanského zákoníku § 1257 a násl. Rychlejší a levnější než koupě, ale nechrání před novým vlastníkem tak dobře jako vlastnictví (VB ale zapsané v KN přechází). Ochota SPÚ neověřena.
4. **Nezbytná cesta (§ 1029 OZ)** – soudní zřízení za náhradu, když vlastník nemá dostatečný přístup. Záložní, pomalé (ODHAD 1–3 roky) a nejistý výsledek.
5. **Na straně nabídky:** do nabídky nelze přidat podmínku (rozhoduje jen cena; ČD si vyhrazuje zrušení kdykoli). Rizikové je vázat se na cenu bez jistoty přístupu. Lze ale **před nabídkou písemně položit otázky ČD** (viz otázky).

**ODHAD nákladů (bez zdroje; pro model, viz Shrnutí):** geometrický plán 10–30 tis. Kč; znalecký posudek 5–15 tis. Kč; cena VB nebo pruhu pozemku v zastavěném území Benešova zhruba 1 500–4 000 Kč/m² u koupě (plocha 30–300 m²), VB několik desítek tisíc Kč.

---

## 4. Okolí: železnice, ochranné pásmo, památky, záplavy

### Vzdálenost od kolejí
Zdroj: ZABAGED (ČÚZK ArcGIS REST, `ZABAGED_POLOHOPIS`, vrstvy Železniční trať, Kolejiště, Železniční stanice), 4. 11. 2026, výpočet vzdálenosti od středu domu.

| Objekt | Vzdálenost od domu |
|---|---|
| Nejbližší železniční trať (úsek s 9 kolejemi = staniční kolejiště, elektrifikovaná, státní železnice) | **~292 m** |
| Dvojkolejná trať (hlavní) | ~381 m |
| Polygon Kolejiště | ~259 m |
| Bod „Benešov u Prahy" (stanice) | ~290 m (východ-severovýchod) |
| Vlečka | v okolí nenalezena |

Ověření z druhého zdroje (OpenStreetMap/Overpass) se nepodařilo (server nedostupný). **Doporučuji pohledem v Mapy.cz / ČÚZK mapě ověřit** (je to ~4 minuty chůze od stanice).

### Ochranné pásmo dráhy (zák. č. 266/1994 Sb.)
- Zdroj: [zakonyprolidi.cz/cs/1994-266](https://www.zakonyprolidi.cz/cs/1994-266) (strojový výtah, ověřit). **§ 8 odst. 1 písm. a):** u celostátní a regionální dráhy **60 m od osy krajní koleje, nejméně však 30 m od hranice obvodu dráhy**; písm. b) 100 m pro celostátní dráhu na rychlost >160 km/h (není tento případ); c) vlečka a místní dráha 30 m.
- **§ 9 odst. 2:** v ochranném pásmu lze provádět stavby a nestavební záměry jen na základě povolení stavebního úřadu (drobné stavby výjimka); u drobných staveb do 15 m od obvodu dráhy zasahujících do ochranného pásma technické infrastruktury je nutný písemný souhlas vlastníka dráhy.
- **Závěr z geometrie:** dům je ~290 m od nejbližší koleje, **mimo zákonné ochranné pásmo**. Obvod dráhy je ještě blíže ke kolejím.
- **Rozpor s ČD:** zadávací podmínky říkají, že nemovitosti jsou „v ochranném pásmu dráhy", kupující „se zavazuje" postupovat podle zák. 266/1994 Sb., **bez souhrnného stanoviska Správy železnic nelze provádět jakékoliv stavební práce vč. oplocení, drobných staveb, terénních úprav a demolic**, a kupující „strpí" hluk, otřesy a nečistoty bez nároků. Stránka ČD „Nabídka vybraných objektů" tvrdí totéž plošně o komerčních objektech u tratí. Jde nejspíš o **vzorový text** (ODHAD).
- **Důsledky pro nástavbu / úpravy:**
  - Pokud je dům mimo ochranné pásmo (jak vychází z geometrie), **souhlas drážního úřadu ani Správy železnic ze zákona nepotřebuje**; vyřídí se běžně stavebním úřadem (Benešov).
  - Ale smluvní závazek v kupní smlouvě by kupujícího vázal **bez ohledu na skutečnost**, vč. požadavku na stanovisko Správy železnic ke každé stavbě. To znamená zdržení a závislost na SŽ.
  - **Požadavek:** před nabídkou získat od Správy železnic/ČD písemné potvrzení polohy vůči OP, nebo se pokusit o upravení textu smlouvy (ale ČD u výběru nejedná o textu předem).
- Hluk: nejbližší koleje ~290 m, ČD přesto zdůrazňuje hluk a otřesy – použít při posouzení bytů a ceně.

### Památková ochrana
- Zdroj: NPÚ geoportál ([geoportal.npu.cz/arcgis/rest/services](https://geoportal.npu.cz/arcgis/rest/services), vrstva INSPIRE/ProtectedSites + tematické vrstvy ochranných pásem a památkových zón), dotaz na bod domu, 4. 11. 2026. Žádná chráněná lokalita, památková zóna, rezervace ani ochranné pásmo památky neprotíná bod domu. Nejbližší památka v okruhu ~400 m: **železniční stanice** (národní/kulturní památka).
- Dům z ~1980 sám památkou není (zápis v Památkovém katalogu pamatkovykatalog.cz se přes web automaticky vyhledat nepodařilo – aplikace JS). **Vyhodnocení: NE (dle NPÚ geoportálu)**. Doporučeno zkontrolovat na pamatkovykatalog.cz ručně.
- Vrstva „Historická osada Benešov" (archeologická lokalita NPÚ) pokrývá město; v rámci územního řízení běžná povinnost oznámení Archeologickému ústavu (§ 22 zák. č. 20/1987 Sb., z paměti).

### Záplavové území
- Oficiální vrstvu Q100 (VÚV/Povodí Vltavy) jsem nenašel online přístupnou. Nejbližší vodní tok podle ZABAGED: **~470 m (Helenka)**, další >900 m (Mydlářka, Konopišťský a Benešovský potok).
- **Závěr: pravděpodobně NE (ODHAD)**; vzhledem ke vzdálenosti toků ≥470 m. Ověřit na [dibavod.cz / mapy.vuv.cz](https://www.dibavod.cz) nebo na MěÚ Benešov.

---

## 5. Podmínky prodeje ČD (NB503213)

Zdroje:
- Karta nabídky: [nemovitosti.ceskedrahy.cz/nemovitost/NB503213/...](https://nemovitosti.ceskedrahy.cz/nemovitost/NB503213/prodej-netypoveho-bytoveho-domu-c-p--1598-v-k-u--benesov-u-prahy) (4. 11. 2026). Poznámka: portál ČD je teď `nemovitosti.ceskedrahy.cz`; nabídka je v sekci „Prodej" po výběru Středočeského kraje.
- Příloha „Zadávací podmínky NB503213 VŘ_Benešov u Prahy č.p. 1598 konec 16.11.2026.pdf" (2 strany): `https://nemovitosti.ceskedrahy.cz/GetAttachment.ashx?docid=0050569EE6D61FD1B1D8DD09C93C0000` (staženo pouze ke čtení; lokální kopie v adresáři nástroje WebFetch `~/.claude/projects/-Users-martincerny-Documents-Benesov/…/tool-results/webfetch-1793792249235-sjkin9.pdf`, mimo složku Benesov).
- Web ČD – Otázky a odpovědi: [nemovitosti.ceskedrahy.cz/Otazky-a-odpovedi.aspx](https://nemovitosti.ceskedrahy.cz/Otazky-a-odpovedi.aspx).

| Téma | Obsah podmínek |
|---|---|
| Forma | **Výběrové řízení, písemné nabídky v zalepené obálce**; dvě do sebe vložené obálky, česky. Adresa: České dráhy, a.s., Generální ředitelství, **Odbor právní**, Praha 1, Nábřeží L. Svobody 1222, PSČ 110 15, označení „Výběr zájemce o koupi – NEOTVÍRAT – prodej nemovitých věcí v k.ú. Benešov u Prahy NB503213". Doručení datovou schránkou podmínky neřeší (ČD uvádějí jen fyzické doručení na adresu; ptát se). |
| **Termín** | Nabídka musí být **doručena do 12:00 dne 16. 11. 2026** (závazně). |
| Vnější obálka | Identifikace zájemce; prohlášení, že na něj není zahájeno insolvenční řízení a není insolvencí bezprostředně ohrožen; u právnických osob výpis z OR ne starší 30 dnů; u fyzické osoby v manželství, platí-li z SJM: **potvrzení manžela/ky**, že o koupi ví (i od bývalého manžela/ky při nevypořádaném SJM). |
| Vnitřní obálka | **Jen nabízená kupní cena v Kč.** |
| Hodnoticí kritérium | **Výše kupní ceny**; musí být **≥ 8 326 000 Kč**. Vybraný zájemce je vyzván k jednání o kupní smlouvě (výjimečně o smlouvě o smlouvě budoucí). |
| Kauce / jistota | **V podmínkách neuvedena** (žádná jistota při podání nabídky). Cena se platí před podpisem smlouvy (viz níže). |
| Další kola | ČD si vyhrazuje druhé a další kola, nabídka nesmí být nižší než v předchozím kole. Zákaz více nabídek propojených osob. |
| Výhrady ČD | Nereflektovat žádnou nabídku, vyhlásit záměr opakovaně, neprodat vůbec, **zrušit záměr kdykoli bez náhrady**. Žádný právní nárok ani **žádná forma předkupního práva** zájemců. Neveřejná komise. Listiny se nevracejí. |
| Platba | Kupní cena **před uzavřením kupní smlouvy**: bezhotovostně na účet ČD, nebo **notářská/advokátní úschova či jistotní účet** u tuzemské banky. |
| Financování úvěrem | „**České dráhy nemohou dát svůj majetek do zástavy.**" |
| Schválení | Prodej podmíněn **souhlasem představenstva a dozorčí rady ČD** před uzavřením smluv (interní, i proto trvá). |
| Elektřina | Objekt je **odpojen od elektřiny**; obnovení odběru u ČEZ Distribuce na náklady a odpovědnost kupujícího. |
| Ochranné pásmo | Viz 4 (závazky kupujícího). |
| Předkupní právo třetích | V podmínkách neuvedeno. Předkupní právo ani omezení z LV nelze ověřit (CAPTCHA). |
| Nájmy | **Neuvedeny.** Karta: „Volné od: Neuvedeno". Odpojení od elektřiny a stav z prohlídky naznačují, že je prázdný (ODHAD). |
| Prohlídka | V pracovní dny po dohodě s místním správcem. |
| Kontakt | Jana Pecinová, makléř, 602 710 214, pecinova@gr.cd.cz (nikam jsem nepsal). |
| Nevyřešeno | Kdo platí **správní poplatek za vklad** (2 000 Kč dle sazebníku, z paměti), náklady smlouvy a případně DPH – podmínky mlčí. Web ČD v Otázkách uvádí **daň z nabytí nemovitých věcí** (termín přiznání do konce 3. měsíce po vkladu) a bezplatnou právní asistenci ČD při smlouvě/vkladu. **Daň z nabytí byla zrušena zákonem č. 340/2020 Sb. (z paměti, ověřit)**, text na webu ČD je zřejmě zastaralý. Cena v inzerátu: 8 326 000 Kč – zda vč. DPH, nespecifikováno (prodej budovy staré >5 let je obvykle osvobozen dle § 56 ZDPH, z paměti). |
| Stěhování | Dle FAQ: nastěhování do 30 dnů od vkladu. |

Karta nabídky (ČD, 4. 11. 2026): Stav „Dobrý", Voda „Ne", Elektřina „Ne", Plyn „Ne", Kanalizace „Ne", Věcné břemeno „Ne". Údaje o Vodě/Kanalizaci jsou v **rozporu s RÚIAN** (vodovod ano, kanalizace přípoj ano) a „Stav: Dobrý" kontrastuje s trhlinami a plísní z prohlídky 3. 11. 2026.

Cena: 8 326 000 / 384,46 m² = **21 656 Kč/m²** (ČD plocha); / 478 m² hrubé plochy = 17 418 Kč/m²; na 4 byty = 2,08 mil. Kč/byt.

---

## 6. Proč ČD prodává, historie, nájmy

- **Důvod konkrétního prodeje nikde zveřejněn není.** Obecně: ČD prodává „nepotřebný majetek". Článek [e15 z 13. 6. 2014](https://www.e15.cz/byznys/reality-a-stavebnictvi/cd-stoply-prodej-realit-budou-s-nimi-podnikat-1092646) popisuje, že ČD tehdy plošný výprodej zastavily, ale pokračují prodeje nepotřebných budov a až ~3 000 podnikových bytů (většinou 4. kategorie) chtěly opravovat; prodeje schvaluje dozorčí rada. Současná strategie ČD (2026) nenalezena.
- **ODHAD (bez zdroje): dům postaven ~1980/81 jako podnikové byty pro zaměstnance ČSD** (RÚIAN datum 1980, 4 byty, vlastník ČD, okolní bloky Za Nádražím/J. Nohy, 290 m od nádraží, ČD má stejný typ ještě č.p. 1597). Doložit nelze – vyžádat u ČD.
- **Nájmy:** nejsou uvedeny. Podmínky zmiňují odpojení od elektřiny, karta nemá „Volné od". Pokud někdo bydlí, přechází nájem na kupujícího (OZ § 2221, z paměti). Vyžádat od ČD seznam nájemních smluv.
- Dostupný web ČD uvádí, že „veškeré prodeje podléhají schválení Představenstva a Dozorčí rady" (stránka [Nabídka vybraných objektů](https://nemovitosti.ceskedrahy.cz/Nabidka-vybranych-objektu.aspx)) – termín rozhodnutí o výběru po 16. 11. 2026 tedy není jistý (týdny).
- Stav ČD portálu: z krajského výpisu „Prodej – Středočeský kraj" (4. 11. 2026) je NB503213 jedním z 8 viditelných prodejních inzerátů; ostatní jsou jiné objekty (NB503215, NB503214, NB503211 …).

---

## Shrnutí pro model

### Plochy a parametry
| Položka | Pesimistické | Realistické | Optimistické | Zdroj |
|---|---|---|---|---|
| Zastavěná plocha | 239 m² | 239 m² | 239 m² | RÚIAN/KN |
| Počet podlaží | 2 | 2 | 2 | RÚIAN |
| Hrubá podlažní plocha | 478 m² | 478 m² | 478 m² | 239×2 |
| Podlahová/užitná plocha „budovy" | 384 m² | 384 m² | 384 m² | ČD inzerát; ODHAD, že jde o čistou plochu obou podlaží |
| Z toho plocha bytů (bez dílny, kotelny, skladů, chodby) | ~290 m² | ~310 m² | ~330 m² | **ODHAD** (80–85 % z 384 m²); upřesnit dispozicemi |
| Počet bytů | 4 | 4 | 4 | RÚIAN (a elektroměry 4×) |
| Pozemek v ceně | 239 m² (jen půdorys) | 239 m² | 239 m² | KN |
| Okolní pozemek 2128/3 | není součástí | není součástí | není součástí | inzerát |

### Cena a lhůty
- Minimální cena **8 326 000 Kč**; hlavní kritérium cena; termín nabídek **16. 11. 2026 12:00**; kauce nestanovena.
- Rozhodnutí vyhlašovatele: čekat na představenstvo a dozorčí radu (ODHAD 1–3 měsíce); dále vklad v KN (běžně do 20–30 dnů od podání).

### Zjištěná břemena a rizika
| Riziko | Stav | Dopad na model |
|---|---|---|
| **Přístup přes 2128/3 bez doloženého VB** | VB neověřeno, karta ČD „Ne" | Nutno přičíst náklady: pesimisticky koupě pruhu/okolí **0,3–1,2 mil. Kč** + GP/posudek 20–50 tis. + 12–24 měs. nejistoty; realisticky VB nebo koupa malého pruhu **0,1–0,4 mil. Kč** (ODHAD); optimisticky existující VB 0 Kč. |
| Hypotéka | ČD nedá zástavu, přístup nejistý | Kupní cena přes úschovu; zástava až po vkladu; LTV možná ≤ 60–70 % do vyřešení přístupu (ODHAD, ověřit v bance). |
| Prodej po bytech | Podmíněno přístupem | Do doby vyřešení přístupu nelze počítat s plnou cenou jednotek (ODHAD sleva 5–15 %). |
| Ochranné pásmo dráhy | ČD tvrdí ano, geometrie ~290 m = ne | Optimisticky OP neplatí (nástavba bez drážního souhlasu); pesimisticky smluvní závazek = stanovisko SŽ ke stavbám (+1–3 měs., poplatky). Ověřit u SŽ. |
| Elektřina odpojena | ano | Přípojka/obnovení u ČEZ Distribuce; náklady viz stav.md. |
| Rozpor sítí | RÚIAN vodovod + kanalizace ano, plyn ne; ČD voda/kanalizace „Ne" | Ověřit na místě a u dodavatelů. |
| Daň z nabytí | zrušena (ověřit), web ČD zastaralý | Do modelu 0 Kč; pesimisticky 4 % (332 tis. Kč), pokud by platila (ODHAD). |
| Památky / záplavy | NE (NPÚ geoportál, vzdálenost toků ≥470 m) | Bez dopadu. |
| Nájmy | neuvedeno, asi prázdné | Ověřit; nájem by přešel na kupujícího. |
| Nezjištěno (CAPTCHA) | zástavy, předkupní práva, plomby, VB na LV 6313 a 2128/3 | Nutné před odevzdáním nabídky. |

---

## Otázky k ověření

### Pro člověka (katastr, zdarma po CAPTCHA)
1. LV 6313: vlastník, **omezení vlastnického práva, věcná břemena, zástavy, předkupní práva, plomby/řízení**. Je tam zapsáno cokoli k přístupu?
2. LV 2128/3 (SPÚ): je zapsáno **věcné břemeno chůze a jízdy** ve prospěch st. 2113/3? Jiné nájmy, plomby, restituční nárok?
3. LV parcely 3501 (město) – status komunikace (veřejně přístupná).
4. Majitel č.p. 1597 (2113/2): ČD, či jiný? Případný společný zájem na VB.

### Pro ČD (jen písemně, makléřka Jana Pecinová)
1. Co přesně znamená 384,46 m² (čistá podlahová, užitná, jiná)? Podlahové plochy po bytech a společných prostorech; půdorysy.
2. **Na základě čeho je zajištěn přístup přes 2128/3** (zapsané VB, nájemní/užívací smlouva se SPÚ, jen faktické užívání)? Pošlete kopii.
3. Je cena 8 326 000 Kč vč. DPH? Kdo platí poplatek za vklad a náklady smlouvy? Je v ceně nábytek, kotel atd.?
4. Jsou v domě nájemci? Seznam smluv, volno od data.
5. Stav sítí: voda, kanalizace (ČD uvádí „Ne", RÚIAN „ano"), plyn, elektřina (od kdy odpojeno, proč, dluh?).
6. Na jakém podkladu tvrdíte, že dům leží v ochranném pásmu dráhy? Prosím vyjádření Správy železnic.
7. Zda lze doplnit kupní smlouvu o podmínku zajištění přístupu, nebo odložit převod do vyřešení VB.
8. Proč ČD prodává; vlastní prodej sousedního č.p. 1597?
9. Lhůta rozhodnutí představenstva/DR; přibližná doba do podpisu smlouvy.
10. Připojení domu k infrastruktuře a historie oprav (trhliny, vlhkost).

### Pro SPÚ (Krajský pozemkový úřad pro Středočeský kraj, pobočka Benešov)
1. Je parc. 2128/3 převoditelný (zákaz § 6 zák. 503/2012)? Je určen územním plánem pro veřejně prospěšnou stavbu?
2. Je zřízeno VB / existuje nájemní smlouva na 2128/3 (kdo je „oprávněný uživatel")?
3. Za jakých podmínek zřídí VB chůze a jízdy a za jakou úplatu (znalecký posudek)?
4. Podmínky převodu pruhu/okolí domu vlastníkovi stavby (§ 10 odst. 3 písm. b), zda lze žádat i před vkladem vlastnictví; odhad lhůty.

### Pro Správu železnic / stavební úřad Benešov / město
1. Potvrdit polohu domu vůči ochrannému pásmu dráhy a obvodu dráhy.
2. Územní plán: funkční využití 2128/3 a parc. 2113/3 (přípustnost nástavby), výšková regulace.
3. Záplavové území Q100 (MěÚ Benešov/Povodí Vltavy).

### Pro banku
1. Ochota financovat nákup s přístupem bez zapsaného VB; LTV; postup přes notářskou úschovu (ČD nedá zástavu před převodem).
