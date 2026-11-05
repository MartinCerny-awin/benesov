# Kontrola 2: Rozvody domu (voda, kanalizace, elektro, společné části) – 5. 11. 2026

Web real: 810 tis. (8 dílčích řádků 812). Moje ceny: bez DPH zdola (množství × jednotka) × 1,3135 (DPH 12 % × režie 17 %, stejný koeficient jako `polozky/technika.md`), tedy srovnatelné s webem. Bez nástavby.

## 1. Tabulka

| Položka | Web | Můj real | Pes–opt | Potřeba | Nejlevnější rozumná cesta (úspora) | Zdroj |
|---|---:|---:|---|---|---|---|
| Stoupačky kanalizace 4 × 6 m, odvětrání | 173 | **172** | 250–60 | Jen když kamera/obhlídka ukáže vadnou litinu (viz níže). Odvětrání nad střechu ano. | Instalatér OSVČ + bourání a zapravení šachet svépomocí: ~125 (−47). Ponechání zdravých úseků po kameře: ~60–100 (−70 až −110) | Zdola: 24 m HT DN110 + odbočky 25, 4 střešní hlavice a prostupy 24, 8 požárních manžet 14, práce 60 h × 800 = 48, bourání/zapravení šachet 20 = 131 bez DPH. Nejremeslnici.cz (referenční výměna 2 stoupaček po 6 m ve 3 bytech 80 tis.), poptavky.cz/rekonstrukci-stoupacek (14 m litiny 125 tis.), 5. 11. 2026. ODHAD ±25 % |
| Stoupačky vody, hlavní vodoměr, napojení | 161 | **145** | 200–80 | Ano. Stoupačky 1981 neznámého stavu, nové byty = reklamace. | Instalatér OSVČ + drážky svépomocí: ~105 (−40) | Zdola: 4 × 6 m PPR + izolace 7, 8 uzávěrů po bytech 12, vodoměrná sestava 15 (`report.py` ř. 317), napojení 20, práce 50 h × 800 = 40, zapravení 15 = 109 bez DPH. ODHAD ±25 %. Jen studená, teplá je z el. bojlerů (`podklady/stav.md` ř. 50) |
| Kamera svodů, zapravení drážek, požární ucpávky | 80 | **75** | 120–45 | Kamera ano (R1, svody 1981 pod podlahou 1. NP, `stav.md` ř. 91). Ucpávky ano (kolaudace, PBŘ). | Kamera a ucpávky řemeslník s certifikátem; drážky svépomocí: ~50 (−25) | Kamera 8–15 (`stav.md` R1) = 12; ~14 prostupů × 2,5 tis. (Hilti/Promat sada) = 25; zapravení 20 = 57 bez DPH |
| Hlavní domovní + elektroměrový rozvaděč na 8 měření | 139 | **140** | 220–90 | Ano. Rozvaděč je z 90. let, bez elektroměrů (`stav.md` ř. 48, `rozpocet-2.md` ř. 54). Distributor bez něj nepřipojí. | Oprávněný elektrikář OSVČ (neplátce): ~120 (−20). Svépomoc ne (revize, ČEZ). | Skříň ER na 8 měření ČEZ 35 (pilíře na 1–2 měření stojí 7–19 tis. s DPH: elektrosms.cz, rozvadec.cz, 5. 11. 2026; na 8 měření odhad), HDV s jističi, SPD, chrániči 30, kabely 10, práce 30 h × 1 200 = 35 = 110 bez DPH. ODHAD |
| Stoupací el. vedení k bytům a na střechu | 93 | **92** | 140–55 | Ano, nynější jsou volné svazky jednožilových vodičů, Al/Cu neznámé (`stav.md` ř. 48). | Žlaby, drážky a zapravení svépomocí, kabeláž elektrikář: ~72 (−20) | 8 vedení CYKY 5×10 po ~12 m (96 m × 150 Kč) 14, žlaby 8, práce 40 h × 1 200 = 48 = 70 bez DPH. ODHAD |
| Společné osvětlení s čidly, zvonky, domovní telefon | 50 | **52** | 85–35 | Osvětlení a zvonky ano; domovní telefon „hezké mít“ (~6 tis.). | Svítidla koupit sám, montáž svépomocí, elektrikář jen zapojí: ~42 (−10) | Uživatel 5. 11. (8–10 svítidel, telefony 5,5 tis.): `report.py` ř. 321 = 43 bez DPH → 56 |
| Hromosvod: jímače zpět, revize | 31 | **38** | 60–25 | Ano, revize hromosvodu se chce ke kolaudaci/pojišťovně; stávající svody se ponechají (rozhodnutí uživatele). | Bez úspory (hromosvodář + revizní technik). | Zdola: drát FeZn + podpěry 7, práce 12 h 12, revize 8–12 = ~29 bez DPH. Když uzemnění neprojde revizí +20 (poznámka uživatele). ODHAD |
| Revize elektro a přívod k TČ na střeše | 85 | **60** | 100–40 | Revize ano (zákon, kolaudace, banka). Přívod k TČ ano. | Přívod: žlaby svépomocí, ~55 (−5). Revizi dělá jen revizní technik. | Revize společných částí 10–15; přívod 2 × 3×32 A: kabel 5×10 2 × 30 m 7, jističe a žlab 8, práce 20 h × 1 200 = 24 = ~45 bez DPH. ODHAD |

## 2. Součet

| | Tis. Kč s DPH |
|---|---:|
| Web (8 řádků / model) | 812 / 810 |
| Můj real (firma + řemeslník jako dnes) | **774** (−5 %) |
| Nejlevnější rozumná varianta (OSVČ + drážky, žlaby, bourání svépomocí) | **~607** (−22 % proti mému, −25 % proti webu) |
| Navíc, pokud kamera potvrdí litinu v pořádku a stoupačky se ponechají | ~−70 až −110 další |

Rozdíl 5 % je pod prahem 10 %. Rozdělení: kanalizace +/−0, voda −16, ucpávky −5, revize/přívod TČ −25 (web 85 je skoro dvojnásobek mé ceny zdola), hromosvod +7, ostatní ±3.

## 3. Stoupačky: musí se měnit? (zvláštní otázka)

- Obnova koupelen B, C, D (bez bourání jader) **výměnu stoupaček nevynucuje**. Stoupačka je v šachtě za koupelnou, kam se kvůli obnově nesahá. Výměna se ale vyplatí udělat **teď**, protože později by se rozbíjely nové obklady. Proto kamera a obhlídka stoupaček patří **před** obklady, ne po nich.
- Co je v domě vidět: oranžové PP odpady (novější úseky), HT stoupačka na chodbě, ale také litinové/ocelové svislé potrubí u umyvadla (`stav.md` ř. 49; materiál „nejde poznat“). Smíšený stav = někde výměna už proběhla. Litina z roku 1981 má 45 let, běžná životnost 50–80 let, hlavní problém je hluk, korozní hrdla a inkrustace, ne okamžité selhání.
- Alternativa k výměně: kamerová prohlídka stoupaček (revizní kusy), frézování inkrustací ~300 Kč/m (sosodpady.cz, 5. 11. 2026), případně relining. Pro 24 m to je řádově 10–100 tis. proti 172.
- **Doporučený postup:** nechat v ceně 172 (pes/real), do 14 dní od koupě udělat kameru + tlakovou zkoušku stoupaček. Pokud je litina celistvá a hrdla těsná, výměnu škrtnout a ušetřit ~70–110 tis. Úplně bez prověření neprodávat, vada v šachtě = reklamace u 6 kupců.

## 4. Chybí / dvakrát

- **Dvakrát (drobné):** (a) odvětrání stoupaček nad střechu je v řádku kanalizace (prostupy 24 tis.) i ve střeše „Prostupy, lemování komína a odvětrání“ (`report.py` ř. 299, 31 tis.): odhad překryvu ~10 tis. bez DPH, ~13 tis. s DPH. (b) Zapravení drážek je ve třech řádcích (stoupačky, kamera/drážky, „Byty: omítky a zapravení po nových rozvodech“ 111 tis. v `byty_povrch`). Překryv ~15–25 tis. (c) Kabeláž k TČ je i v řádku „Jeřáb, podstavce a propojení venkovních jednotek“ ve Vytápění (`technika.md`): ~10 tis. Celkem dvojí započtení ~35–50 tis. s DPH, už zahrnuté v mém nižším součtu u voda/revize.
- **Proti „Byty: elektro a voda“ a „Nebytová část“:** bytové rozvaděče a revize bytů jsou v bytech (390 tis.), společný rozvaděč a stoupací vedení tady. Nebytová část (390 tis.) má „přívod k elektroměrům“. Pokud ten přívod počítá i od HDV k rozvaděči, je to tady podruhé (k ověření u k-nebyt, ~10 tis.). Voda a odpady kuchyní (89 tis.) jsou jen v bytech, ne tady.
- **Chybí:** (1) Podíl na připojení a navýšení příkonu: Elektřina 60 tis. (50,4 podíl 3×63 A) je asi málo při TČ 2 × 16 kW + 6 bytů; ČEZ účtuje 800 Kč/A třífázově (modernistavitel.cz, 2026), při 3×100 A ~80 tis., plus R8 (0 / 150 / 400 tis., `stav.md` ř. 99). Není v této položce, patří k-elektrina. (2) Elektroměrový pilíř na hranici pozemku (ČEZ často vyžaduje měření přístupné z veřejné cesty; pozemek je jen půdorys, přístup přes SPÚ): ODHAD 15–30 tis., zjistit u ČEZ před objednáním rozvaděče. (3) Dočasné napájení stavby 10–35 tis. (`rozpocet-2.md` ř. 79) – ověřit, zda je v „Ostatní/Stavba“. (4) Revizní zpráva na stoupačky vody (tlaková zkouška) je v ceně.

## 5. Doporučení

**Beze změny (810).** Můj odhad 774 je −5 %, pod prahem. Jednotlivé řádky se vyvažují (revize/přívod TČ nadsazený o ~25, voda o ~16, hromosvod podhodnocen o ~7). Změnu rezervy v realistickém scénáři neprovádět. Upozornění pro rozhodnutí: za nejvýhodnější krok považuji kameru stoupaček před koupelnami (možná úspora 70–110 tis.) a ověřit u ČEZ polohu elektroměrů a příkon (možné navýšení +30 až +150 tis., mimo tuto položku).
