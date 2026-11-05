# Postup – dispozice bytů, č.p. 1598 Benešov

## Podklady
- `photos/`: 37 fotek a 5 videí z prohlídky 3. 11. 2026 (9:56–10:25), videa bez zvuku k přepisu (whisper není nainstalovaný)
- `NB503213.pdf`: inzerát ČD – netypový bytový dům č.p. 1598, Benešov u Prahy, 2 nadzemní podlaží, 384,46 m² budovy, 239 m² pozemku, 8 326 000 Kč. Bez půdorysů a bez počtu bytů.

## Hotovo
- 2026-11-04: snímky z videí (každé 2 s) → `prace/soubory.csv`, 125 obrázků
- 2026-11-04: spuštěno 9 popisovačů (Haiku) → `prace/popisy/davka-01..09.jsonl`

## Předběžná časová osa (z přehledových náhledů, ověřit podle popisů)
- 09:56–09:58 fotky: zrekonstruovaný byt (laminát, dlouhá chodba, kuchyň s bílou prosklenou linkou, samostatné WC, koupelna s vanou a bojlerem, pokoj s kobercem s autíčky); pravděpodobně totéž co video 10:18:54
- 09:58–10:01 fotky: společná chodba (oranžový sokl), DÍLNA, kotelna, sklepní/technické prostory – nebytové
- 10:01–10:03 fotky: byt se žlutou kuchyní, oranžovým linoleem a modrým pokojem; pravděpodobně totéž co videa 10:12:05 a 10:12:27
- 10:10:24 video: zdevastovaný byt s růžovými pokoji a parketami
- 10:11:25 video: byt s modro-žlutými stěnami a parketami, končí na schodišti (zábradlí dolů → patro)
- 10:13–10:15 fotky: elektro – rozvaděč s elektroměry označenými „byt 3“, „2.“, „4.“, „HDO 3“, „HDO 4“, dole „3“, „2 ŠACH“, „4“
- 10:22–10:25 fotky: exteriér, vstup se 3 schránkami (možná víc mimo záběr)

## Návrh po kroku 2 (před ověřením)
- A (1. NP, zrekonstruovaný): 4+1 – obývák se 3 okny průchozí do kuchyně, lila pokoj, pokoj s šedým kobercem, pokoj s holou podlahou
- B (2. NP, růžový, video 10:10): 2+1 – růžový pokoj, šedomodrý pokoj s vestavěnou skříní, kuchyň mezi růžovým pokojem a chodbou
- C (2. NP, žlutá kuchyň, „4“ na dveřích): 3+1 – pokoj s oranžovým linem, modrý pokoj, pokoj se zeleným kobercem
- D (2. NP, modro-žlutý, video 10:11): 1+1 – pokoj s parketami a 2 okny, kuchyň s odstraněnou linkou
- Tvrzení: `prace/overeni/kolo1-tvrzeni.md`; hustší snímky z videí B a D v `prace/husto/`

## Otevřené otázky

## Ověření
- Kolo 1 (2026-11-04, po bytech, Sonnet):
  - A sedí (4+1). Upřesnění: P4 má světlý kobercový povrch; 1. NP plyne z návaznosti fotek.
  - B: chyba – zelenkavá místnost bez okna je komora, kuchyň je vedlejší místnost; 2+1 platí.
  - C: zelený pokoj nebyl potvrzen videem → dohledán vstup dveřmi s kulatou klikou v předsíni (časová návaznost 090252 → 090321 → 090328); kuchyň má dveře do P1 i do chodby; výhled „shora“ vypuštěn.
  - D sedí (1+1). Pokoj má 3 okna, nika v předsíni je šatní skříň.
  - Celkový ověřovatel se zasekl a druhý byl zastaven – nahrazeno ověřováním po bytech.
- Kolo 2: `prace/overeni/kolo2-tvrzeni.md`, 4 ověřovatelé s úkolem dispozici vyvrátit – nikomu se to nepodařilo.
  - A 4+1 drží: P3 a P4 se liší oknem, radiátorem i podlahou.
  - B 2+1 drží: komora nemá okno, panel v chodbě nejsou dveře do nového pokoje.
  - C 3+1 drží: zelený pokoj patří do C podle časů, zárubní a oken; vstup do něj je spíš přes tmavé dveře s koštětem, ne přes dveře s koulí.
  - D 1+1 drží. B, C, D jsou v patře, A v přízemí.
  - Na rozvaděči je možná „byl 3“, ne „byt 3“.
- 2026-11-04: **hotovo**, výsledek v `dispozice.md`.
- 2026-11-04 (dotaz uživatele „není B 3+1?“ a „chci plnou dispozici“):
  - B znovu prošel: zelenkavá „komora“ je roh kuchyně, B zůstává 2+1.
  - Rozložení všech bytů zrekonstruováno naslepo (4 agenti), pak ověřeno (4 agenti).
  - Upřesnění: A – obývák blíž ke vstupu, kuchyň dál, WC a 4. pokoj z koncové předsíňky. B – v čele chodby koupelna a WC, šedomodrý pokoj naproti kuchyni. C – vpravo pokoj, kuchyň, koupelna, WC; vlevo zelený pokoj; v čele modrý pokoj. D – vstup a dveře pokoje vedle sebe, na podélné stěně WC, koupelna, kuchyň.
  - Výstup: `dispozice.html` (artifact).
- 2026-11-04 (uživatel: „půdorysy nedávají smysl“): přechod na půdorysy podlaží v měřítku.
  - Obrys z RÚIAN (SO kód 2924498): 23,79 × 10,05 m, 4 byty, 2 podlaží, zastavěná plocha 239 m².
  - Okna změřená na fotkách fasád (uliční zpříma ±0,3 m, zahradní šikmo ±1 m) a přiřazená k místnostem podle tvaru, rámů, žaluzií a výhledů. Ověřeno dvěma agenty (přízemí a patro), opravené polohy jsou zapracované.
  - Výsledek: A = levá polovina přízemí; C = levý konec patra nad A; D = uliční strana patra nad vstupem; B = pravá část patra; pravá polovina přízemí je nebytová; schodiště uprostřed proti vstupu.
  - Generátor: `prace/pudorys.py` → `prace/pudorys-*.svg`, šablona `prace/dispozice.tpl.html` → `dispozice.html`. Tvrzení: `prace/overeni/fasady-tvrzeni.md`.
  - Nejisté: vnitřní příčky (±0,5–1 m), pravý štít (není vyfocený), zahradní fasáda za modřínem a borovicí (x 10,5–15 a 17–23,8).
- 2026-11-04 (nové fotky z WhatsAppu: 36 fotek, 3 videa; bez času pořízení):
  - `snimky.py` opraven pro WhatsApp názvy (tečky v čase přepisovaly soubory do jednoho). Popisy jsou v davka-10…14.
  - Tři analytici po částech domu a jeden ověřovatel. Hlavní změny:
    - Levý štít: WC a koupelna uprostřed štítu (okna y 3,45–4,1 a 5,0–6,2).
    - Pravý štít: žebřík, v 1. NP dveře do nebytové chodby; ve 2. NP WC a koupelna B (y 3,8–4,4 a 5,1–6,4).
    - Schodiště: dvouramenné, x ~11,2–13,8, mezipodesta u zahrady. D má dveře v uliční stěně podesty.
    - B: kuchyň u štítu, růžový pokoj se 2 okny, roh bez oken je nejspíš spíž.
    - C: kuchyň v zahradním rohu u štítu; dveře vpravo na konci chodby vedou do kuchyně.
    - Zahradní trojice: dvě měření se liší až o 1 m, v plánu je průměr (~2,7–8,5).
  - Tvrzení a zadání: `prace/overeni/zpresneni-zadani.md`.
- 2026-11-04 (oprava od uživatele, viz `fakta.md`): byt A nemá předsíň mezi obývákem a halou, z haly se vchází rovnou do chodby. Obývák a šedý pokoj A sahají k hale (x 11,2); stejně pokoj C v patře.
- 2026-11-04 (uživatel: 1. NP OK, „ověř sklep“, „vpravo není spíž“):
  - Nebytová část není sklep: je v úrovni přízemí, bez schodů dolů, okna mají parapet ~1,5 m. Chodba z haly končí kotelnou, ke dveřím ve štítu se jde přes ni. Po stranách chodby jsou dílna, uzávěr vody, sklady, latěné kóje a tmavý sklad (uhelna?). Strany místností jsou odhad; uliční východní část a nízké okno ve štítu nikdo nevyfotil.
  - Byt B: spíž odstraněna, kuchyň vede ke štítu. WhatsApp 13.32.50 (1) je pravděpodobně předsíň C ve 2. NP, ne 1. NP.
- 2026-11-04 (oprava od uživatele): kotelna na konci chodby zabírá celou hloubku domu u pravého štítu (x 21,0–23,4, y 0,4–9,65). Patří k ní uliční okno 22,0–22,6, okna ve štítu a dveře ve štítu. Nevyfocená místnost na uliční straně se zmenšila na x 18,9–21,0.
- 2026-11-04 (uživatel): místnost „?“ v přízemí zrušena; sklad na uliční straně sahá ke kotelně (x 17,3–21,0).
- 2026-11-04 (uživatel: „kotelna je určitě širší“): kotelna x 18,7–23,4 přes celou hloubku (~4,7 × 9,25 m), včetně tmavého skladu/uhelny. Opírá se o fotku 090003 (dva kotle a rozdělovač přes celou stěnu), komín nad x ~19–21 a o to, že tmavý sklad byl vyfocený 5 s před kotelnou. Chodba končí na x 18,7, uliční sklad je x 17,3–18,7.
- 2026-11-04 (uživatel):
  - Nebytová chodba: vlevo (zahrada) 3 místnosti – sklad, uzávěr vody, kóje; vpravo (ulice) 2 – dílna, sklad. Které je která, je odhad.
  - Kuchyň B je obdélník x 18,5–23,4, y 5,8–9,65 (k chodbě i ke štítu, bez zubu). Koupelna B y 4,6–5,8, WC y 3,4–4,6. Široké okno ve štítu (změřeno y 5,1–6,4 ±0,4) patří podle uživatele koupelně, v plánu je na y 4,7–5,75.
- 2026-11-04 (uživatel): koupelna a WC u levého štítu mají dveře v jedné rovině → WC A i C x 0,4–2,6, dveře obou na x 2,6.
- 2026-11-04 (uživatel: chodby v jedné ose; okna rovnoměrně; zkontrolovat okna vs. interiér):
  - Chodby A, nebytová, C i B jsou na y 4,45–5,75.
  - Kontrola oken (2 agenti) – zapracováno:
    - A: šedý pokoj má okno u západní příčky (6,8–8,1), příčka lila/šedý na 6,6; WC okno zúženo.
    - Nebytové: dílna 13,8–15,6, sklad 15,6–18,7 se 2 okny; uzávěr vody má okno na zahradu (odvozené); dveře ve štítu širší.
    - C: zelený pokoj 4,8–7,9 (okna zabírají skoro celou stěnu), mezi ním a modrým skříň s koulí; okna koupelny a WC na štítu upravena.
    - B: druhé okno růžového pokoje u západní stěny (~14–15,2, odvozené); okna koupelny a WC posunuta.
  - ROZPOR vyřešen (uživatel: „držet se fotek“) – půdorys zůstává podle fotek:
    - C: okno kuchyně a pokoje jsou těsně u společné příčky (na fasádě dvojice oken s pilířem ~0,25 m).
    - A: lila má okno u západního rohu, pokoj 4 u východního rohu, šedý u západního rohu.
  - Nevyřešeno: okno mezipodesty – fasáda ~9,8–10,9, plán 11,4–12,6 (schodiště je v ose vstupu podle haly).
- 2026-11-04 (uživatel): koupelna B zasahuje do kuchyně (y 4,6–6,6), široké okno ve štítu vráceno na změřených 5,1–6,4; ve chodbě B výklenek se stoupačkou (x 18,4–19,0, odhad).
- 2026-11-04 (uživatel: chodby stejně velké): příčka na konci chodeb sjednocena na x 18,6 v obou podlažích (dřív kotelna 18,7, chodba B 19,0). Okna to připouštějí: 1. NP zahrada 17,2–18,4 | 19,0, ulice 18,3 | 22,0; 2. NP zahrada 18,3 | 18,7, ulice 18,5 | 21,5. Posunuto: kotelna 18,6–23,4 (~4,8 m), sklad a kóje do 18,6, D pokoj 13,6–18,6, šedomodrý a hala B od 18,6, kuchyň B od 18,6, výklenek 18,0–18,6. Šířka chodeb (1,3 m) byla stejná už předtím. Sestavení stránky a SVG: `python3 -I prace/sestav.py`.
- 2026-11-04: Do půdorysů doplněny dveře (`door()` v `prace/pudorys.py`). Plné = vidět na záběrech, čárkované = odvozené (A: kuchyň, WC, 4. pokoj; C: zelený, modrý, WC, kuchyň z konce chodby).

## Co by zvýšilo jistotu (při další prohlídce)
- Byt C: otevřít dveře s kulatou koulí a tmavé dveře s koštětem v chodbě a natočit zelený pokoj s cestou z chodby.
- Vyfotit všechny schránky ve vstupu a štítky zvonků (čísla bytů B a D).
- Byt A: natočit koncovou část chodby (WC, P4, koupelna) v jednom záběru.
- 2026-11-04 (/loop kontrola místností; uživatel: „Ano, posuň“): schodiště 1. i 2. NP x 9,4–12,2 × y 6,0–9,65 (okno mezipodesty na fasádě ~10,0–11,5, uvnitř vystředěné; z haly vidět jen levá část prvního ramene). Šedý pokoj A a pokoj C x …–9,4 (šedý ~1,3 m zdi vpravo od okna – 4 ověřovatelé + 1 ze souběžného sezení). Za halou x 12,2–13,8 × y 6,0–9,65 nevyfocený prostor „?“ (tmavá stěna s hasicím přístrojem). Podesta 2. NP x 9,4–13,8 × y 4,45–6,0, chodba C končí na 9,4, předsíň D do y 4,45. Plochy k prodeji: A ~90, C ~75, B ~67, D ~42 = ~274 m²; s nebytovou částí ~360 m². Zprávy: prace/overeni/mistnosti-A-v1..v3.md, mistnosti-spol-v1..v2.md.
- 2026-11-04 (uživatel přes souběžné sezení: „schodiste neni odhozene je stejne s halou“; pak volba „Podle okna“): zádveří x 9,4–13,8 × y 0,4–1,9 (vchod 11,6–13,5 na pravém kraji), hala 9,4–12,2 × 1,9–6,0, schodiště 9,4–12,2 × 6,0–9,65; obývák A 4,5–9,4 (3 okna 5,1–9,0 teď rovnoměrně), chodba A a dveře z haly na x 9,4, dvoukřídlé dveře obýváku 7,6–9,0. Nebytová chodba a chodba B od x 12,2. Nevyfocené prostory „?“ x 12,2–13,8 (1. NP ulice i zahrada, 2. NP zahrada). Podesta 2. NP 9,4–12,2; dveře D na 10,9–11,8. Plochy k prodeji: A ~80, C ~75, B ~69, D ~42 = ~266 m²; nebytová část ~98 m² (vč. „?“); po přestavbě ~364 m².
- 2026-11-04 (uživatel: „ten otazník je buď chodba nebo pokoj“): prostory x 12,2–13,8 vpravo od haly kresleny jako „ch./pokoj“ (1. NP ulice i zahrada → nebytová část, 2. NP zahrada → byt B). Plochy: B ~75 m², byty dnes ~272 m², po přestavbě ~370 m².
- 2026-11-04 (uživatel poslal 5 fotek ze Street View; volba „Žádný prostor navíc“): hala, schodiště a podesta x 9,4–13,8, prostory „ch./pokoj“ zrušeny, chodby nebytová a B od x 13,8. Čelní fotka uliční fasády (rektilineární, 55,5 px/m): vchodové dveře x ≈ 10,9–12,7 (portál 10,2–13,3) → zakresleno; okno kuchyně A x ≈ 0,7–2,25 → 0,8–2,3 (shoda se 3 ověřovateli). Ostatní uliční okna vycházejí o ~0,3–0,5 m níž v x než plán (v toleranci, neměněno). Šikmá zahradní fotka (projektivní korekce): okna 2. NP 2,4–3,6 / 4,0–5,15 / 6,4–7,7 / okno mezipodesty 9,9–11,3 / 13,6–15,1 / 16,7–18,3 / ~18,7–19,3+; přízemí 13,8–15,0; komín x ≈ 19 (nad kotelnou, ne 15–18,5). Plochy k prodeji: A ~80, C ~75, B ~67, D ~42 = ~264 m²; s nebytovou částí ~350 m²; společné ~60 m².
- 2026-11-04 (/loop kontrola místností DOKONČENA – A, nebytové, společné, C, D, B; vždy 2 ověřovatelé, výsledky prace/overeni/mistnosti-*-vysledek.md a mistnosti-stav.md): navíc zapracováno – vstup D 12,5–13,3 (u rohu s pokojem), levé okno růžového B 13,9–15,3, okno šedomodrého B 21,2–22,5. Otevřené drobnosti: okna ve štítu B možná o 0,4 m k ulici, dveře do kuchyně C z konce chodby (rozpor), skříň s koulí v C neprohlédnuta, sklad u ulice v nebytové části nefocen, žebřík v kuchyni B (průlez na střechu?).
- 2026-11-04 (oprava od uživatele „Byt B: 2+1 → 3+1“, viz `fakta.md`): B zapsán jako 3+1. Video B (103 snímků po 0,5 s) znovu prošlo: jen dva pokoje, třetí nelokalizovaný (dotaz na jeho polohu bez odpovědi). Půdorys beze změny, třetí pokoj v něm chybí. Ověřovatelé se nespouštěli, protože není co ověřit nad obrázky. Otevřená otázka: kde je 3. pokoj B (zazděné dveře na uliční stěně chodby → pokoj se 3 okny dnes u D? rozdělený šedomodrý?).
