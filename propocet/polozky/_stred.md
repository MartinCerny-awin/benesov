# Kontrola středu nákladových položek (/loop od 4. 11. 2026)

Cíl: u každé nákladové položky z tabulky „1. Náklady“ v reportu posoudit, jestli realistická hodnota leží uprostřed (není moc pesimistická ani optimistická), a když ne, posunout ji. Jedna položka za iteraci. Rozhodnutí, která uživatel schválil (postup.md: sazba 9 %, rezerva 15 % / pes 10 %, lokalita 0,95, střední rekonstrukce…), neměním, jen je zapíšu jako poznámku. Měním jen při rozdílu ≥ 10 % nebo při jasné chybě.

## Pořadí
1. Koupě od ČD a poplatky (`koupe_transakce`)
2. Přístup přes SPÚ a parkování (`pristup`, `pristup_mes`, `parkovani`)
3. Střecha (`strecha_v_rekonstrukci`, část `stredni`)
4. Vytápění: tepelné čerpadlo (část `stredni`)
5. Rozvody domu (část `stredni`)
6. Sanace trhlin (část `stredni`)
7. Společné prostory (část `stredni`)
8. Byty A, B, C, D (část `stredni`)
9. Statické zajištění (`rizika_navic`)
10. Byt B 2+1 → 3+1 (`b31_zmeny`)
11. Nebytová část → 2 byty (`nebyt_zmeny`, `nebyt_druhy_byt`)
12. Ustupující podlaží (`nastavba_m2`, `nastavba_soft`, `nastavba_statika`)
13. Projekt, dozor, statik (`stredni_sluzby`)
14. Vlastní dodavatelé: úspora (`material_podil`, `rezie_gd`, `remeslnici_sleva`, `remeslnici_platci`, `koordinace`)
15. Rezerva (`rezerva`) – schváleno uživatelem, jen posoudit
16. Úroky a poplatky úvěru (`sazba` schváleno; `uver_poplatek`, `predcasne`, `ltv`)
17. DPH z prodeje po odpočtu (počítá model, jen kontrola)
18. Prodej bytů (`provize`, `advokat_prodej`, `marketing_byt`)
19. Ostatní: držení, PENB, rozdělení (`drzeni_mes`, `pojisteni_dan_mes`, `penb`, `rozdeleni`)

## Hotovo

### 1. Koupě od ČD a poplatky – beze změny (centrované)
- Model real 116 tis. (pes 229 / opt 65). Rozpis `koupe.md`: advokát 40, 2× vklad 4, odhad 12, elektřina 60 tis.
- Advokát 40 tis. je spíš horní polovina (kontrola vzorové smlouvy ČD + úschova 8,3 mil. obvykle 25–40 tis.; bankovní/notářská úschova levnější) → střed ~30–35 tis.
- Elektřina 60 tis. předpokládá zrušené odběrné místo. I když zrušené není, z 4 bytů na 6 bytů + TČ 2 × 16 kW se rezervovaný příkon zvyšuje a podíl se platí za navýšení → nějaká platba je skoro jistá; 60 tis. je rozumný střed. Sazbu Kč/A (500 vs 800 Kč/A) se nepodařilo ověřit (rešerše 5. 11. bez českého ceníku) – ověřit u ČEZ Distribuce.
- Součet střed ~105–116 tis., rozdíl < 10 % → beze změny. Pes 229 / opt 65 symetrické kolem středu přiměřeně (pes kryje novou přípojku).

### 2. Přístup přes SPÚ a parkování – upraveno
- `pristup` 600/150/30 tis. – střed sedí (25 m² pruhu po 3 500 Kč + GP, posudek, právník), beze změny.
- `pristup_mes` 18/9/6 → **24/12/6**: 9 měs. bylo pod spodní mezí koupě od SPÚ (uzemni-plan.md ř. 197: 12–24 měs.; služebnost 6–18 měs., dane-financovani.md ř. 114). Real 12 = střed mezi služebností a koupí, opt 6 = VB už zapsané.
- Parkování: model dával 300 tis. (2 stání) i verzi bez nástavby, která potřebuje jen 1 stání (86/120 m² = 0,72) → nový vstup **`parkovani_1` 800/200/60 tis.** pro V1, Bn, B2n (1 stání ~190 tis., vážené s 0 stání a výkladem „celý dům“). S nástavbou (V2, C1, C2) zůstává `parkovani` 800/300/100 tis.
- Report: popisky rozpisu parkování bez pevného „2 stání“.
- Dopad real (čistý zisk): V1 1,89 → **2,08** (parkování +0,05, přístup +0,14), V2 1,97 → 2,07, D 4,74 → 4,99.
- ⚠ (viz níže) Delší přístup zvedá zisk jen proto, že úvěr se čerpá až po zapsání přístupu → méně úroků, ale **vlastní peníze V1 12,4 → 17,1 mil.** (stavba začíná v 7. měsíci a do 12. se platí z vlastního). Model nepočítá cenu vlastního kapitálu, takže delší čekání vypadá výhodně. Realisticky by se se stavbou čekalo nebo banka půjčila se zástavou bez přístupu dražší úvěr – k rozhodnutí uživatele.

### 3. Střecha – upraveno (byla spíš pesimistická)
- Model 3 600 Kč/m² bez režie a DPH (215 m² = 774 tis.; s režií, DPH, plochou a inflací 1,02 mil.). Rozpětí stav.md 2 600 / 3 600 / 5 200. Tržní kalkulačky 2026 dávají plnou rekonstrukci ploché střechy 2 500–3 500 Kč/m² bez DPH i s firmou (strecha-statika.md: tržně ~0,85 mil., −17 %). PVC fólie 1 050 Kč/m² a PIR 1 400 Kč/m² jsou horní polovina (fólie mechanicky kotvená obvykle 600–900, spád z EPS klínů + PIR levnější než celé PIR).
- Real **3 600 → 3 200 Kč/m²** (688 tis. bez režie) = střed mezi stav.md a trhem: izolace 1 150, fólie 900 Kč/m², ostatní beze změny. Pes 1,44 a opt 0,60 mil. beze změny (pes je kalibrovaný na rozpocet-2).
- Model: `strecha_v_rekonstrukci` real 971 → **863 tis.**, `stredni` real 7 990 → **7 872 tis.** (−108 stavba, −10 služby), `stredni_sluzby` 700 → **690 tis.** Report: řádky izolace 325 a fólie 254 tis.
- Dopad real (čistý zisk): V1 2,11 → **2,18**, V2 2,10 → 2,13, D 5,04 → 5,18 mil.
- Pozn.: V1 mezi kroky 2 a 3 vzrostl 2,08 → 2,11 bez mé změny – model.py souběžně upravuje jiná session („Rozdělení nákupu pozemku a parkování“ nebo „Výraz by 2+1“).

### 4. Vytápění: tepelné čerpadlo – upraveno (cena TČ byla pesimistická)
- Skupina v reportu (V1, s DPH): 1,66 mil.; z toho TČ 2 × 16 kW 998 tis. = 380 tis. bez DPH za kus vč. montáže (technika.md, ODHAD z TČ 10 kW 180–420 tis.).
- Trh: TČ vzduch–voda 16 kW „na klíč“ pro RD 199–289 tis. Kč (zbozi.cz, rešerše 5. 11. 2026; LG Therma V 16 kW, Panasonic ~213 tis.). Bez DPH ~175–255 tis.; pro bytový dům s firmou, kaskádou a dopravou na střechu (jeřáb je zvlášť) střed ~300 tis./ks. Akumulace, regulace a rozvody jsou v jiných řádcích, takže 380 tis. bylo v horní části.
- Výkon 2 × 16 kW ponechán: na nezateplený dům je to spíš bezpečná strana (ztráta 27–34 kW, bivalence elektrem); 2 × 14 kW by stálo podobně.
- Real **380 → 300 tis./ks** bez DPH (−160 tis. bez DPH). Model: `stredni` real 7 872 → **7 652 tis.** (−201 stavba, −19 služby), `stredni_sluzby` 690 → **671 tis.** Report: řádek TČ 788 tis. Pes/opt beze změny.
- Ostatní řádky vytápění (akumulace 131, rozvody a měřiče 221, demontáž kotlů 59, komín 79, topení v bytech 131 tis.) leží uprostřed svých zdrojů → beze změny. Topení druhého bytu 2+kk (105 tis., technika.md) v rozpisu reportu chybí – patří k nebytové části (položka 11).
- Dopad real (čistý zisk): V1 2,18 → **2,31**, V2 2,13 → 2,26, D 5,18 → 5,45 mil.

### 5. Rozvody domu: voda, kanalizace, elektro – beze změny (střed sedí)
- Skupina v reportu (V1, s DPH) ~0,77 mil. = 588 tis. bez DPH (technika.md).
- Elektro (rozvaděče 90, stoupací vedení 60, osvětlení + zvonky + telefon 70, hromosvod 45, revize + přívod TČ 55 = 320 tis.) proti nezávislému overeni/rozpocet-2.md ř. 118, 128, 129 (hlavní elektro 250 + hromosvod 45 + zvonky z portálu) ≈ 300–320 tis. → střed.
- Voda a kanalizace (stoupačky kanalizace 112, vody + hlavní vodoměr 104, kamera a drážky 52 = 268 tis.) proti rozpocet-2.md ř. 127 (120/200/300) o 34 % výš; střed obou ~235 tis. → ZTI spíš mírně pesimistické (hlavní vodoměrná sestava 50 tis. je vysoko, obvykle 15–30 tis.).
- Skupina celkem střed ~555 tis. vs model 588 tis. = −6 % → pod prahem 10 %, beze změny. Pozn. do rezervy: ZTI −35 tis. bez DPH, kdyby se rozpočet zpřesňoval.

### 6. Sanace trhlin – beze změny (střed sedí, mírně pesimistické)
- Skupina v reportu (V1, s DPH) 394 tis. = 300 tis. bez DPH (stav.md 5a 80 + 5c 220; strecha-statika.md B): sešití 70 bm × 2 500 Kč, injektáž 50 bm × 700, plošina 10, omítky na cihly 20 m² × 1 300, vysprávka 60 bm × 450, nátěr a úklid 27 tis.
- Sešití: rozpětí overeni/rozpocet-2.md 1 800 / 2 500 / 3 500 Kč/bm. Technika (Weber, prospekt helikální výztuže 2025): pruty po 450 mm, kotvení ≥ 500 mm na každou stranu → ~2,2 prutu na 1 bm trhliny; materiál levný (UK ~3 £/m prutu), cenu dělá práce v drážkách → realisticky 1 800–2 500 Kč/bm, 2 500 je horní polovina středu. Česká cena za bm na webu nenalezena (rešerše 5. 11.).
- Délka 70 bm je odhad z fotek (z detailů nejde měřit) – nejistota délky je větší než nejistota ceny a je oboustranná.
- Střed skupiny ~280 tis. bez DPH vs model 300 tis. = −7 % → pod prahem, beze změny.

### 7. Společné prostory – upraveno (bylo spíš pesimistické)
- Skupina v reportu (V1, s DPH) 289 tis. = 220 tis. bez DPH (technika.md): dlažba chodeb 30 m² × 2 400 + schodiště 24 m² × 700 = 89; zábradlí 40, omítky a malba ~200 m² 38, 4 dveře 44, schránky 9 = 131 tis.
- Nezávislý overeni/rozpocet-2.md ř. 130: společné prostory 95/165/260 tis. (schránky a zvonky má v portálu) → model bez schránek 211 vs 165 = +28 %. Dlažba 2 400 Kč/m² vč. podkladu je horní část (dlažba položená 1 200–1 800 + podklad na dřevotřísce ~500), zábradlí 1 600 Kč/bm za očištění a nátěr je vysoko (obvykle 600–1 000), malba 190 Kč/m² vs rozpocet-2 80 Kč/m² (ale s opravami omítek).
- Real **220 → 185 tis.** bez DPH (dlažba 2 000 Kč/m², zábradlí 25, omítky a malba 30 tis.; dveře a schránky beze změny). Model: `stredni` real 7 652 → **7 604 tis.** (−44 stavba, −4 služby), `stredni_sluzby` 671 → **667 tis.** Report: 101 + 142 tis.
- Dopad real: V1 2,70 → **2,74**, V2 3,04 → 3,07 mil.
- Pozn.: mezi položkami 6 a 7 vzrostl V1 2,31 → 2,70 bez mé změny – jiná session přidala neplacenou práci kamaráda architekta (`arch_sluzby`, `arch_nebyt`, `arch_nastavba`, uživatel 5. 11.). Zohlednit u položky 13 (projekt).

### 8. Byty A, B, C, D – upraveno po řádcích (celek −5 %, ale několik řádků mimo střed oběma směry)
- Skupina (V1, s DPH) 3,51 mil. = 2 675 tis. bez DPH (byty.md). Srovnání řádků s nezávislým overeni/rozpocet-2.md (ř. 80–97):
  - **Jádra B, C, D 120 → 150 tis./byt** (optimistické): rozpocet-2 200 tis./byt, S1 120–240, S2 80–160, S3 126 → střed ~150 (+90 tis.).
  - **Okna 26 → 20 ks** (pesimistické): rozpocet-2 ř. 67 – plastová okna v A, C a části 2. NP zůstávají, staré dřevěné jen v B, D (a nebytové části); stav.md ale bere A za dřevěná → střed 20 ks (12 velkých + 8 malých), −90 tis.
  - **Malba 170 → 110 Kč/m²** (pesimistické): rozpocet-2 80, stav.md 170 → střed, −51 tis.
  - **Vyklizení 100 → 60 tis.**: rozpocet-2 75 tis. včetně dílny, skladů a kotelny (ty jsou i v nebytové části) → −40 tis.
  - **Plísně 60 → 40, úklid 45 → 25 tis.**: rozpocet-2 20 a 23 tis. → −40 tis.
  - Ostatní (kuchyně 80 tis., elektro 1 200 Kč/m², dveře, podlahy 1 400 Kč/m², voda 600, omítky 450) jsou uprostřed svých rozpětí → beze změny.
- Netto −131 tis. bez DPH. Model: `stredni` real 7 604 → **7 424 tis.** (−164 stavba, −16 služby), `stredni_sluzby` 667 → **651 tis.** Report: jádra 591, okna 326, malba 122, bourání 236, plísně/úklid 164 tis.
- Dopad real: V1 2,74 → **2,87**, V2 3,07 → 3,20 mil.
- Pozn.: jiná session rozdělila v reportu parkování na pozemek a stavbu (`parkovani_poz`, `parkovani_stavba`).
- **Oprava 5. 11. (uživatel): vyměnit všechna okna v bytech.** Okna 20 → **28 ks** (20 velkých × 15 tis. + 8 malých × 8,5 tis. = 368 tis. bez DPH; byty.md: v bytech ~28–30 oken). `stredni` real 7 424 → **7 590 tis.**, `stredni_sluzby` 651 → **666 tis.** Report: okna 483 tis. Výsledek real: V1 **2,75**, V2 **3,08** mil.

### 9. Statické zajištění (`rizika_navic`) – beze změny
- Model 2,0 / 0,8 / 0,25 mil. s DPH. Rozpis real (strecha-statika.md C): geologie a sondy 118, táhla 12 ks 275, ztužení překladů a věnec 118, lokální zesílení základů ~10 bm 105, rezerva na rozsah 30 % 184 tis. Na tuto položku se rezerva 15 % nepočítá, má jen vlastních 30 %.
- Ceny řádků jsou uprostřed zdrojů: IG průzkum 14–80 tis. + odkopy, táhla 40–100 tis. za roh nebo dům podle poptávek, mikropiloty 1 800–4 500 Kč/bm (jen pes).
- Rozdělení výsledků je zešikmené: asi 1/4 jen sešití (~0,25), 1/2 táhla a lokální zásahy (0,6–1,0), 1/4 podchycení (2–3,5 mil.). **Medián ~0,8 = model real**, střední hodnota ~1,0–1,1 mil. Real 0,8 leží i geometricky mezi opt a pes (√(0,25 × 2,0) = 0,71). Pes 2,0 je schválené snížení (dříve 3,5).
- Bez posudku statika není důvod hodnotu měnit. Riziko podchycení zůstává v textu reportu, ne v real.

### 10. Byt B 2+1 → 3+1 (`b31_zmeny`) – upraveno (bylo optimistické)
- Model 180 / 82 / 70 tis. s DPH; real ležel skoro na opt. Rozpis nebyt-bytb.md kap. 5: příčka 14, nový otvor z chodby vč. dveří 18, elektro 12, radiátor 12, podlaha a malby 12, statik 5 tis. bez DPH.
- Otvor z chodby je v domě z roku 1981 spíš v nosné zdi (sám rozpis počítá se statikem a překladem): proražení s ocelovým překladem ~25 tis. + dveře se zárubní ~8 tis. místo 18 tis. celkem → 88 tis. bez DPH × VRN 1,05 × DPH 1,12 = **105 tis.**
- `b31_zmeny` → **180 / 105 / 70 tis.** Report: řádek „Nový vchod z chodby“ 64 tis. Dopad real: V1 2,75 → **2,73**, V2 3,08 → 3,06 mil.
- ⚠ report.py teď nejde spustit (`NameError: rv`) – rozpracovaná úprava jiné session; report přegeneruji v dalším kroku.

### 11. Nebytová část → 2 byty – upraveno (jednotkové ceny sjednoceny s byty nahoře)
- Model real 3,64 mil. s DPH (nebyt_zmeny 2 963 + nebyt_druhy_byt 517 tis. × 1,045). Rozpis zdola nebyt-bytb.md 3 598 tis. Celek se proti modelu liší jen o −1 %, ale několik jednotkových cen bylo výš než stejné práce v bytech nahoře (položka 8), ačkoli je dělá stejná firma:
  - okna: velká akustická 25 → **20 tis.** (byty 15 + ~5 za akustické sklo), malá 10 → **9 tis.** (byty 8,5) → 240 → 200 tis.
  - koupelna s WC 150 → **130 tis.** (menší koupelna 2+kk; v bytech je 150 za koupelnu a samostatné WC), linka 100 → **85 tis.** (byty 80) → 614 → 528 tis.
  - elektro 1 500 → **1 250 Kč/m²** (byty 1 200), podlahové topení 1 600 → **1 000 Kč/m²** (obvykle 800–1 200 vč. rozdělovače) → rozvody 629 → 555 tis.
  - bourání a vyklizení 1 750 → **1 300 Kč/m²** (v bytech ~680 Kč/m², tady navíc podlahy a příčky) → 198 → 147 tis.
  - Vlhkost a podlaha (580), příčky, omítky a dveře (414), technická místnost (172) a projekt (450; část dělá architekt, viz `arch_nebyt`) zůstávají, jsou uprostřed zdrojů.
- Celkem −251 tis. s DPH (−7 %). `nebyt_zmeny` real základ 2 482 → **2 281 tis.** (před přepočtem na 86 m²). Report: 147 / 200 / 528 / 555 tis.
- Dopad real: V1 3,50 → **3,67**, V2 4,17 → **4,34** mil.
- Pozn.: mezi položkami 10 a 11 se V1 posunul 2,73 → 3,50 bez mé změny – uživatel rozhodl prodávat bez realitky (`provize` 0, postup.md 5. 11.). Položka 18 (prodej) je tím z velké části vyřešená.

### 12. Ustupující podlaží – upraveno (sjednoceno s rekonstrukcí)
- Model `nastavba_m2` 54 / 43,5 / 34,5 tis. Kč/m² hrubé bez DPH (150 m² = 6,53 mil.), `nastavba_statika` 2,5 / 2,0 / 0,5, `nastavba_soft` 1,6 / 1,2 / 0,8 mil. Rozpis nastavba.md.
- Sjednoceno s cenami, které už byly upravené u rekonstrukce (položky 3, 4, 8, 11):
  - střecha nástavby 3 600 → 3 200 Kč/m² (−60 tis.)
  - další TČ 10 kW 300 → 230 tis. (TČ 16 kW v rekonstrukci je teď 300 tis.)
  - 2 koupelny 125 → 130, 2 linky 100 → 85 tis. (−20 tis.)
- Prodloužení schodiště 600 → **450 tis.** bez DPH: ocelové schodiště o 2 ramenech 250–350 + otvor ve stropě se statikou 80–150 + požární obklad ~50 tis. – ODHAD, 600 byla horní mez.
- Beze změny: konstrukce 14 tis./m² (1/3 z dřevostavby na klíč 35–50 tis.), okna 15 tis. (= byty), terasa, vnitřní dokončení 4 600 Kč/m², lešení a jeřáb, požární úpravy; mikropiloty 2,0 mil. (60 ks × 8 m × 2 800 Kč/bm, střed 1 500–4 500); projekt 1,2 mil. (střed 0,8–1,35 mil.).
- `nastavba_m2` real 43,5 → **41,5 tis.** (−300 tis. bez DPH, −0,35 mil. s DPH). Report: střecha 562, schodiště 527, rozvody 889, koupelny a kuchyně 503 tis.
- Dopad real: V2 4,34 → **4,60** mil. (V1 beze změny 3,67).
- Pes poznámka (beze změny, rozhodnutí uživatele): podchycení je v pes dvakrát (`rizika_navic` 2,0 + `nastavba_statika` 2,5), pes V2 může být nadsazený o 1–1,5 mil.

### 13. Projekt, dozor, statik (`stredni_sluzby`) – vráceno na 700 tis. (střed)
- Rozpis projekt-rezerva.md 733 tis. s DPH: zaměření 40, projekt stavebních úprav 160, prováděcí TZB 200, PBŘ 45, statik 110, TDS 145 (1,9 %), BOZP 25, poplatky 8. Nezávislý overeni/rozpocet-2.md ř. 132 (bez DPH): zaměření 60, projekt + rozpočet 380, statik 90, TDS + BOZP 2,5 % stavby ≈ 667 tis. bez DPH = **~0,81 mil. s DPH**.
- Při položkách 3, 4, 7, 8 jsem služby snižoval úměrně stavbě (700 → 666 tis.). To nebylo správně: projekt se cení podle rozsahu, ne podle ceny stavby, škáluje jen TDS. → `stredni_sluzby` real zpět na **700 tis.**, `stredni` real 7 590 → **7 624 tis.** V V1 je to s inflací a plochou ~0,73 mil. = rozpis, mezi modelem a rozpocet-2 (0,81). Pes 1,28 / opt 0,30 beze změny.
- Kamarád architekt (`arch_sluzby` 47 %: zaměření, projekt stavebních úprav, TDS) – rozhodnutí uživatele, report ukazuje v závorkách; neměním.
- Dopad real: V1 3,67 → **3,65**, V2 4,60 → **4,58** mil.

### 14. Vlastní dodavatelé: úspora proti firmě – beze změny (všechny vstupy jsou středy)
- Report teď počítá směs (`MIX` v report.py, jiná session): každá položka stavby má štítek firma / řemeslník a parametry platí jen pro řemeslnické položky.
- Vstupy real a jejich rozpětí: přirážka GD 12 % (8–18), podíl materiálu 50 % (45–55), sleva práce neplátců 10 % (0–20), podíl práce plátců 25 % (0–50), koordinace 4 % (3–5), stavba +1 měs. (0–2), pes rezerva +5 p.b. Real je ve všech případech uprostřed. Zdroje nejsou (ODHAD), takže není důvod je posouvat jedním směrem.
- Prodloužení o 1 měsíc jsem zvažoval zvednout na 2 (koordinace řemesel bez GD se obvykle protáhne). Koordinaci ale teď dělá kamarád architekt (`arch_kc["koordinace"]`), proto beze změny.
- Pozn.: materiál kupovaný investorem s DPH 21 % místo 12 % a odpočet DPH u plátce jsou v modelu správně.

### 15. Rezerva – beze změny (zadání a rozhodnutí uživatele)
- Model 10 / 15 / 15 % ze stavby, změn dispozic, úspory řemeslníků a stavby nástavby (ne ze statiky, ta má vlastních 30 %). Zadání (prompt-propocet.md ř. 64) chce „rezervu aspoň 15 %“ → real a opt 15 % jsou minimum zadání. Pes 10 % je výslovně schválená výjimka (4. 11.), protože pes stavba už je horní mez cen.
- K posouzení středu: model rezervu počítá jako celou utracenou. Po položkách 3–13 jsou odhady stavby vycentrované, takže 15 % navíc je realisticky spíš opatrné. Obvyklé překročení u rekonstrukce domu z 80. let je 10–20 %, tady ještě s trhlinami; střed ~12–15 %. Takže 15 % je horní část středu, ne pesimismus → beze změny.
- Kdyby uživatel chtěl čistý střed bez minima ze zadání: real 12 % → V1 asi +0,25 mil. (jen poznámka, neměněno).

### 16. Úroky a poplatky úvěru – poplatek za zpracování upraven (byl optimistický)
- `sazba` 9,8 / 9,0 / 8,5 % = rozhodnutí uživatele 5. 11. (podnikatelský úvěr), neměním.
- `uver_poplatek` 1,0 / 0,5 / 0 % pocházel z investiční hypotéky (Raiffeisenbank 0 Kč zpracování). U podnikatelského nebo developerského úvěru se obvykle platí ~1 % (financovani-dph.md ř. 23: 7,5 % + 1 %; nebankovní až 4 %) → **1,5 / 1,0 / 0,5 %**. Dopad real: V1 3,65 → **3,60**, V2 4,58 → **4,51** mil.
- `predcasne` 1,0 / 0,5 / 0 % beze změny: u podnikatelského úvěru je poplatek smluvní (§ 117 zák. 257/2016 platí jen pro spotřebitele); developerské úvěry se splácejí z prodeje bytů často bez poplatku, jinde 0,5–2 % → 0,5 % je střed.
- `ltv` 0,60 / 0,70 / 0,70 beze změny, ale poznámka: strop 70 % z hodnoty po dokončení je spíš optimistický. Developerské úvěry se řídí i podílem z nákladů (LTC 60–75 %) a dům s trhlinami banka ocení podle dnešního stavu. Realisticky by mohlo být víc vlastních peněz. Je to rozhodnutí o financování, ne cena, proto neměním.

### 17. DPH z prodeje po odpočtu – beze změny (není odhad, počítá model)
- Kontrola výpočtu (real, firma): V1 DPH na výstupu 3,35 mil. = 12/112 × tržby 31,26 mil. (sazba 12 %, byty do 120 m², § 48 ZDPH), odpočet −1,44 mil. (DPH 12 % ze stavby a rezervy, 21 % ze služeb, 12 % ze statiky) → netto 1,90 mil. V2 4,81 − 2,63 = 2,18 mil. Výpočet sedí.
- Režim „podstatná změna“ (§ 56 odst. 5: náklady > 30 % ceny, prodej do 5 let od kolaudace změny → zdanitelné) je právní posouzení, ne odhad se středem. Otevřené body zůstávají pro daňového poradce: test 30 % po jednotkách (GFŘ), registrace k DPH a odpočet až při prodeji (+0,3–0,5 mil.).
- U vlastních dodavatelů (MIX) je odpočet menší (neplátci nemají DPH), model to počítá zvlášť.

### 18. Prodej bytů – marketing na byt upraven (po zrušení realitky byl optimistický)
- `provize` 0 = rozhodnutí uživatele 5. 11. (prodává sám), neměním.
- `marketing_byt` 25 / 15 / 8 tis. počítal s realitkou, která část marketingu kryje z provize. Bez ní platí prodávající foto (~4), 3D prohlídku (~5), půdorys (~1,5) a placenou inzerci na portálech za 2–3 měsíce (~8–10 tis.) → **30 / 20 / 10 tis. na byt**. ODHAD, ceník bezrealitky.cz pro soukromníky se 5. 11. nenašel. Dopad: 6 bytů × 5 tis. = +30 tis. (V2 8 bytů +40 tis.).
- **Oprava 5. 11. odpoledne:** foto, 3D a půdorys udělá uživatel sám → 0 Kč. Zbývá placená inzerce **4 měsíce na byt**, s DPH. Sreality, ceník pro fyzické osoby (produktový list platný od 2. 11. 2026, https://szno.cz/cs/b2b/ann9ojcu/): balíček „prodej“ 3 300 Kč bez DPH na 90 dní vč. 6× topování (3 993 s DPH) + prodloužení 1 100 Kč na 30 dní → 5 324 Kč. Max. 6 balíčků najednou na inzerenta. Bezrealitky (bezrealitky.com/price-list/sale): Základ 599 Kč/2 měs., Komplet 1 499 Kč/2 měs. s exportem (iDNES, RealityMIX…, Sreality v seznamu není). → **8,3 / 6,5 / 5,3 tis. na byt** (pes. Sreality + Bezrealitky Komplet, střed + Základ, opt. jen Sreality).
- `advokat_prodej` 40 / 25 / 10 tis. na byt (kupní smlouva + advokátní úschova; obvykle 15–30 tis., náklady si často dělí s kupujícím) – střed, beze změny.
- Pozn. k času: `t_prodej_byty` 12 / 6 / 3 měs. – bez realitky může prodej trvat déle, 6 měs. na 6 bytů je spíš optimistické hranice středu. Neměním (mění úroky, ne cenu), jen poznámka.
- Dopad real: V1 3,60 → **3,58**, V2 4,51 → **4,48** mil.

### 19. Ostatní: držení, PENB, rozdělení na jednotky – beze změny
- Držení 3 000 Kč/měs. (energie a zabezpečení prázdného domu, 1 500–5 000) a pojištění + daň z nemovitých věcí 1 650 Kč/měs. (pojištění 15 tis./rok ≈ 0,05–0,1 % hodnoty, daň 4,8 tis.) – střed.
- PENB 15 tis. (bytový dům, obvykle 10–25 tis.) – střed.
- Rozdělení na jednotky 70 tis. (prohlášení vlastníka 25, geodet 30, katastr 6, SVJ 13) – SVJ je u 6 jednotek povinné (§ 1198 OZ), geodet a advokát uprostřed obvyklých cen → střed.

## Shrnutí smyčky (5. 11. 2026)
| # | Položka | Změna real | Směr |
|---|---|---|---|
| 1 | Koupě a poplatky | – | střed |
| 2 | Přístup SPÚ, parkování | `pristup_mes` 9 → 12 měs.; `parkovani_1` 200 tis. (1 stání bez nástavby) | byl optimistický čas / pesimistické parkování |
| 3 | Střecha | 3 600 → 3 200 Kč/m² (−0,11 mil.) | pesimistická |
| 4 | Tepelné čerpadlo | 380 → 300 tis./ks (−0,22 mil.) | pesimistické |
| 5 | Rozvody domu | – (−6 %, pod prahem) | střed |
| 6 | Sanace trhlin | – (−7 %) | střed |
| 7 | Společné prostory | 220 → 185 tis. bez DPH | pesimistické |
| 8 | Byty A, B, C, D | jádra +, okna všechna 28 ks (uživatel), malba, vyklizení, úklid − | smíšené |
| 9 | Statické zajištění | – (medián 0,8, průměr ~1,0–1,1) | střed |
| 10 | Byt B 2+1 → 3+1 | 82 → 105 tis. | optimistický |
| 11 | Nebytová část | −0,25 mil. (ceny sjednoceny s byty) | pesimistická |
| 12 | Ustupující podlaží | 43,5 → 41,5 tis./m² (−0,35 mil.) | pesimistické |
| 13 | Projekt, dozor | služby zpět na 700 tis. (moje chybné škálování) | střed |
| 14 | Vlastní dodavatelé | – | střed |
| 15 | Rezerva | – (15 % = minimum zadání) | horní část středu |
| 16 | Úvěr | poplatek za zpracování 0,5 → 1 % | optimistický |
| 17 | DPH | – (výpočet sedí) | – |
| 18 | Prodej | marketing 15 → 20 tis./byt | optimistický (bez realitky) |
| 19 | Ostatní | – | střed |

- Výsledek real po smyčce (s vlivem souběžných rozhodnutí uživatele – architekt zdarma, prodej bez realitky, MIX dodavatelů): **V1 3,58 mil., V2 4,48 mil.** Před smyčkou V1 1,89 / V2 1,97 mil. Moje úpravy dohromady asi +0,6 mil. u V1; zbytek dělají rozhodnutí uživatele.
- Otevřené k rozhodnutí: vlastní kapitál při čekání na přístup (V1 až ~16 mil.), LTV 70 % z hodnoty po dokončení je spíš optimistické, rezerva 12 % místo 15 % jako čistý střed, doba prodeje bez realitky.
