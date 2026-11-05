# Kontrola 2: Vytápění, tepelné čerpadlo místo kotlů (5. 11. 2026)

Web real **1 230 tis.** (dílčí řádky jsou dopočtené na součet z modelu). Pozor: `report.py` ř. 308–316 už řádek rozvodů přepsal na indikátory místo měřičů (komentář „měřiče po bytech nejdou, svislé stoupačky“), ale web ještě ukazuje „6 měřičů tepla“ za 259 tis. Po příštím `deploy-web.sh` se rozpis přeškáluje. Můj odhad je proto porovnán s celou položkou.

Všechny moje částky jsou tis. Kč s DPH, firma = 12 % na bytový dům včetně režie firmy ~10 %. Zdroje: S1 = `podklady/stav.md` ř. 115, S15 = ř. 129, R2 = `overeni/rozpocet-2.md`, T = `polozky/technika.md`, KR = https://obchod.klimarapid.cz/tepelna-cerpadla-vzduch-voda/ (vyhledáno 5. 11. 2026, 16 kW Midea/Panasonic s montáží 134–237 tis. s DPH), WT = https://eshop.wterm.cz/tepelna-cerpadla-16-kw/ (monoblok 16 kW 249 990 Kč bez montáže), CHKT = https://chkt.cz/poradna/kolik-stoji-tepelne-cerpadlo/ (14–16 kW pro nezateplený dům od 184 tis., T-CAP od 343 tis.).

## 1. Tabulka po dílčích položkách

| Položka | Web | Můj real | Pes–opt | Potřeba | Nejlevnější rozumná cesta | Zdroj |
|---|---:|---:|---|---|---|---|
| TČ vzduch–voda 2 × 16 kW vč. montáže | 552 | **480** | 620–380 | ano (bez zdroje tepla nejde kolaudace bytů ani prodej, kotle na tuhá paliva nikdo nechce) | firma. Řemeslník na hydrauliku a elektro + uvedení do provozu autorizovaným servisem (jinak propadne záruka): −40 | 2 × 150 tis. jednotka (střední značka) + 2 × 25 montáž + 15 kaskádní regulace = 365 bez DPH × 1,12 × 1,10 ≈ 450–500; KR, WT, S1, S15. Montáž a F-plyny: monoblok se na chladivu neotevírá, split ano (oprávnění nutné) |
| Jeřáb, podstavce, propojení na střeše | 46 | **45** | 65–30 | ano (pozemek je jen půdorys, jednotky jdou na střechu) | firma. Jeřáb ve stejný den jako střecha: −10. Podstavce s tlumiči vibrací a hluku jsou nutné nad bytem 2. NP | ODHAD: autojeřáb 3–4 h ~15, 2 podstavce ~12, preizolované potrubí 15 m + kabel ~12 |
| Akumulace 1 000 l, rozdělovač, čerpadla, regulace, patrona | 90 | **110** | 150–80 | ano (kaskáda + bivalence při −12 °C) | firma. Elektro část s revizí smí jen oprávněná osoba. Žádná svépomoc | nádrž 25–35, hydroskupina + rozdělovač 20, čerpadla 10, patrona 9 kW 5, pojistky a expanze 8, rozvaděč MaR 15, práce 25 = 116 bez DPH → ~130. ODHAD (T ř. 14 dává 131) |
| Rozvody topení, izolace, vyvážení, měření spotřeby | 259 | **170** | 330–110 | ano (vyvážení a tlaková zkouška po 0 provozu; vadné úseky) | řemeslník, izolaci potrubí svépomocí −15. Měření: **poměrové indikátory, ne měřiče** (viz bod 2). Indikátory si pronajmout od rozúčtovací firmy a neinvestovat | rozvody v kotelně 70, vyvážení 6 stoupaček 21, proplach + filtr 12, izolace 15, indikátory 30 × 0,7 = 21 → ~140 bez DPH → ~170. R2 ř. 126 (100–300) |
| Demontáž 2 kotlů a rozvodů v kotelně | 62 | **28** | 60–12 | ano (místnost pro nádrž, ať nejsou kotle bez provozu) | svépomoc: 2 lidi 1 den (~16 h), kontejner + sběr kovů ~6. Úspora ~22. Nejdřív odběr vzorku na azbest (R4 v `stav.md` ř. 94, mimo tuto položku) | R2 ř. 124 (kotle jsou v ceně 650–1 100 kaskády), T ř. 18: 59 tis. s DPH je nadsazené |
| Odstranění komínového nástavce, zapravení střechy | 83 | **50** | 110–25 | ano (nástavec by překážel nové střeše a nesmí zůstat bez funkce) | řemeslník + lešení/plošina už stojí na fasádě pro trhliny. Svépomoc nedoporučuji (výška, prostup střechy, záruka střechy kupcům): úspora max. −15 | R2 ř. 121 (30/60/120 tis. bez DPH). Průduch uvnitř domu využít na odvětrání stoupaček (viz dvakrát) |
| Topení ve 4 bytech (hlavice, proplach, vadná tělesa) | 138 | **115** | 170–80 | ano (hlavice povinné vybavení těles, bez nich nejde rozúčtovat) | svépomoc hlavic (nasazení na stávající ventily, ~10 h): −12. Výměnu ventilových vložek a těles řemeslník | 30 hlavic × 0,55 + 30 vložek × 0,35 + proplach/plnění 4 × 3 + práce 27 + 3–4 deskové těleso 24 + zkouška 4 = ~100 bez DPH → ~115 |
| **Součet** | **1 230** | **998** | **1 505–717** | | s řemeslníky a svépomocí **~880** | |

Pes–opt je součet řádkových rozpětí, jsou to krajní hodnoty, nikoli pravděpodobný rozsah.

## 2. Zvlášť prověřeno

### Je centrální TČ nejlepší pro byty na prodej?

Kapitál s DPH, 6 bytů, 344 m²; provoz = potřeba tepla ~38 MWh/rok (344 m² × ~110 kWh/m², ODHAD), elektřina ~5 Kč/kWh. Provozní čísla jsou orientační.

| Varianta | Investice (tis.) | Provoz celý dům za rok | PENB / prodejnost | Verdikt |
|---|---:|---|---|---|
| **Centrální TČ v–v 2 × 16 kW** | ~1 000 | SCOP 2,8 → 13,5 MWh ≈ 65–70 tis. (~11 tis./byt) | třída B–C (ODHAD), REAS cenu bytu počítá „s TČ“ (`model.py` ř. 143) | **nejlepší poměr**, využije radiátory a stoupačky |
| TČ v–v pro každý byt (6 ks) | 1 500–1 900 | podobný, o něco lepší SCOP | dobré, ale 6 jednotek na střeše/fasádě, hluk, každá jednotka jiný servis | dražší o 50 %: stoupačky jsou společné, tedy nové vedení do každého bytu (4 × 60–120 tis., S: `stav.md` ř. 227) a 6 příkonů. Dotace to nepodpoří (výměna centrálního zdroje za individuální v BD není podporovaná, TZB-info) |
| Elektrokotel 2 × 20 kW + stávající rozvody | 150–250 | 38 MWh × 5 = ~190 tis. (**~2,8× víc**, ~31 tis./byt) | D–E, banky a kupci to vidí; chybí „TČ“ v ocenění | investice nižší o ~800 tis., ale příkon 3 × 63 A navíc a prodejní cena bytů klesne víc, než ušetříš (≥ 3 % z ceny bytů, ODHAD). Přímotopy + bojler stejně |
| Klimatizace split v–v v bytech (multisplit) | 350–600 | SCOP 4 → ~50 tis. | PENB dobrý, ale radiátory nevyužity | kupec odmítne byt bez ústředního topení, hluk vnějších jednotek na fasádě 6 ×, F-plyny. Nižší cena, horší prodejnost |
| Ponechat kotle na tuhá paliva | 0 | levné palivo, ale ruční práce | PENB G, banka kupce | **ne**. Kotle jsou pravděpodobně 1.–2. emisní třída (ověřit štítky), jejich provoz zakazuje zákon o ovzduší od 9/2022. Plyn v domě není, přípojka + 4 kotle 1,0–1,9 mil. (`stav.md` ř. 227) |

Slabé místo centrálního řešení není cena, ale **správa po prodeji**: společné TČ a rozúčtování zajišťuje SVJ. Doporučuji připsat do prodejního materiálu servisní smlouvu na TČ a rozúčtování (zdarma od firmy, která indikátory pronajme).

### Je 2 × 16 kW předimenzované?

Ne, spíš těsné. Pro Benešov (návrhová teplota −12 °C) a dům z roku 1981 s novou střechou a novými okny (postup.md: okna všechna 28 ks) odhaduji měrnou ztrátu 50–65 W/m² (T uvádí 70–90 W/m² pro stav bez oken i střechy, `stav.md` ř. 228 23–35 kW). Vytápěných ~385 m² (344 + společné) → **19–25 kW**. Jmenovitý výkon 16 kW platí při +7/35 °C. Při −12 °C a teplotě vody 45–55 °C (litinové radiátory) dává jednotka jen ~10–11 kW, kaskáda tedy ~21 kW a dotopná patrona 9 kW pokryje špičky. 2 × 12–14 kW by ušetřilo jen 30–50 tis., ale ubralo by rezervu. Nechat 2 × 16. Rozhodne výpočet tepelných ztrát v projektu (v položce Projekt, ověřit, že je v ceně).

### Měřiče tepla po bytech u svislých stoupaček?

Nejdou. Byt je napojen na více svislých větví, kalorimetrický měřič na vstupu do bytu není možný, a to je přesně případ, pro který vyhláška 269/2015 Sb. počítá s **poměrovými indikátory na radiátorech** (výklad v metodickém pokynu MMR: https://mmr.gov.cz/getmedia/fe4516cd-c1fc-4e04-91e6-378d691349b2/Metodicky-pokyn_teplo_vyhl-c-269_2015-Sb-_15_12_17.pdf, vyhledáno 5. 11. 2026; od října 2020 musí být dálkově odečitatelné, TZB-info). Povinnost má dodavatel služby, tedy až SVJ po prodeji. Nové byty 2+kk s podlahovým topením mají vlastní rozdělovač, kde jde kalorimetr osadit za ~8 tis. (T). **Doporučení: vypustit „6 měřičů“ z popisu, pronajmout indikátory (kapitál 0, ODHAD 300–500 Kč/ks/rok) nebo koupit ~30 ks za ~21 tis.** Výsledek už `report.py` obsahuje (150 tis.), web ještě ne.

### Ceny TČ 2026 s montáží

Jednotka 16 kW s montáží 134–237 tis. s DPH (KR, 5. 11. 2026), monoblok 16 kW bez montáže ~250 tis. (WT), nezateplený dům od 184 tis., T-CAP od 343 tis. (CHKT), RD „na klíč“ 270–450 tis. (https://freshtechnology.cz/radce/kolik-stoji-tepelne-cerpadlo, 5. 11. 2026). Web: 276 tis./jednotku vč. kaskádových nákladů je v horní třetině rozpětí, ale neodporuje. Kaskádu pro bytový dům jsem nedohledal, je to ODHAD, nutné poptat u 3 firem.

### Dotace NZÚ

**Nic nezapočítávat.** Od 2026 NZÚ nedává běžným žadatelům přímou dotaci na TČ, jen bezúročný úvěr; přímá dotace 150 tis. je jen pro nízkopříjmové domácnosti (NZÚ Light) a podle TZB-info neplatí pro výměnu centrálního zdroje za individuální. Bytové domy dostávají úvěry při komplexní renovaci (úspora ≥ 30 %, renovační pas), tady bez zateplení fasády nesplnitelné a investor, který byty prodává, o ně nežádá (E.ON, TZB-info, Revizit, vyhledáno 5. 11. 2026: https://www.eon.cz/radce/blog/jake-dotace-lze-ziskat-na-tepelne-cerpadlo/ , https://stavba.tzb-info.cz/zelena-usporam-na-tzb-info/29942-nova-zelena-usporam-2026-zvyhodnene-uvery-pro-bytove-domy). Zdroje se v částkách rozcházejí, ověřit na novazelenausporam.cz. Pro kupce bytů to naopak může být prodejní argument.

### Svépomoc

| Činnost | Hodiny | Úspora | Zvládne laik? | Riziko |
|---|---:|---:|---|---|
| Demontáž kotlů a rozvodů v kotelně | ~16 (2 lidé) | ~22 tis. | ano | azbest v izolaci potrubí a těsnění (vzorek před zahájením), vypuštění soustavy |
| Nasazení hlavic na stávající ventily | ~10 | ~12 tis. | ano | netěsné staré ventily, ty vymění řemeslník |
| Izolace ležatého potrubí | ~6 | ~15 tis. | ano | nízké |
| Komín | – | max. 15 tis. | ne | výška, prostup střechy, záruka střechy |
| TČ, hydraulika, elektro | – | – | ne | F-plyny, revize, záruka výrobce |

## 3. Chybí / dvakrát / podhodnocené

- **Chybí: stav stoupaček a ležatých rozvodů.** Soustava 1981 byla odstavená; tlaková zkouška může odhalit netěsné úseky. R2 ř. 126 dává 100–300 tis., ve mé ceně je ~30 tis. Rezerva ve výši rozdílu mezi webem a mým součtem (232 tis.) to z velké části kryje. Radiátory jsou litinové, nízkoteplotní provoz ověřit v projektu (R2 ř. 189 riziko výměny těles +150–300 tis.).
- **Chybí: hluková studie a ověření hluku TČ nad bytem 2. NP** (~10 tis., ODHAD, vyhl. o hluku; podstavce s tlumením jsou ve mně započteny).
- **Chybí (patří do Elektřiny): příkon pro TČ + patrona.** 2 × ~5,5 kW + patrona 9 kW, hlavní jistič 3 × 63–80 A. Položka „Elektřina obnovení připojení 60 tis.“ je nízká, R8 v `stav.md` ř. 99 uvádí 0/150/400 tis. Není v této položce, jen upozorňuji.
- **Chybí (dispozice): technická místnost** pro nádrž 1 000 l, rozdělovač a rozvaděč (~6–8 m²) v nebytové části 86 m² (T ř. 31, `postup.md` ř. 195). Není to náklad, ale ztráta plochy bytů N1/N2.
- **Dvakrát: komín vs. Střecha.** Nová střecha (1 063 tis.) musí řešit prostupy a oplechování; „zapravení střechy“ po nástavci tam nesmí být podruhé. Vyjasnit rozsah s firmou na střechu.
- **Dvakrát možné: vytápění nových bytů 2+kk** (T ř. 18: 105 tis.) není v mé položce. Ověřit, že je v Nebytové části, jinak chybí.
- **Dvakrát: jeřáb** pro TČ a pro střechu v jednom dni (−10 tis.).
- Ohřev teplé vody zůstává elektrickými bojlery v bytech (`stav.md` ř. 50), není to chyba, ale provozní náklad kupců a důvod, proč PENB nebude lepší než B–C.

## 4. Doporučení

**Beze změny, real 1 230 tis.** Můj bottom-up součet je 998 tis. (−19 %), s řemeslníky a svépomocí ~880 tis. (−28 %), ale rozdíl ~230 tis. odpovídá nenaceněnému riziku stoupaček, příkonu a hluku (viz kap. 3), které tady jinak nikdo nehlídá. Pes 1 500 tis., opt 720 tis. (odhad). Změnit rozpis: web má nadsazený komín (83 vs. ~50) a demontáž kotlů (62 vs. ~28), podhodnocenou akumulaci (90 vs. ~110) a stále „6 měřičů tepla“ místo indikátorů. Svépomocí lze uspořit ~120 tis. (demontáž kotlů, hlavice, izolace), TČ nechat firmě. Při redeployi `report.py` zkontrolovat, že se rozpis neškáluje na samé drobné řádky.
