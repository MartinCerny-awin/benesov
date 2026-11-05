# Postup – propočet koupě, renovace a prodeje č.p. 1598 Benešov

Zadání: `../prompt-propocet.md`. Společné zadání pro subagenty: `podklady/_spolecne.md`.

## Parametry (uživatel nevyplnil → výchozí)
- Vlastní kapitál: 30 % kupní ceny + celá rezerva
- Financování: úvěr na investiční nemovitost, sazby listopad 2026
- Kupuje: fyzická osoba, neplátce DPH
- Cílový zisk: ≥ 20 % ze všech vložených nákladů
- Rekonstrukce: vše dodavatelsky

## Hotovo
- 2026-11-04: přečten inzerát (1 strana; podmínky výběrového řízení jsou samostatná příloha na webu ČD – v PDF nejsou), fakta, poznatky, dispozice (kolo 2).
- 2026-11-04: krok 1 – spuštěno 8 subagentů → `podklady/*.md`

- 2026-11-04: krok 1 hotový – katastr, stav, ceny-byty, ceny-domy, lokalita, uzemni-plan, dispozice-zmeny, dane-financovani, marketing (`podklady/`).
- 2026-11-04: krok 2 – doplňují se `ceny-byty-realizovane.md` (realizované ceny chyběly) a `ceny-domy-2.md` (slabý vzorek 6 domů, cena celku byla jen odhad). Stopky vyhodnoceny (níže).
- 2026-11-04: krok 3 – `model.py` napsán a běží (assert OK), `model.xlsx` se zapisuje. Ceny bytů a celého domu zatím PROVIZORNÍ.

- Úroveň rekonstrukce pro A2/B/B2/C/D = **střední** (standard 5b + z 5c střecha, trhliny, TČ, demontáž kotlů, svody ÚT, stoupačky, hlavní elektro, společné prostory; bez ETICS, sanace vlhkosti, nebytových prostor). Výpočet z cen `stav.md` (tis. Kč bez DPH, před režií, opt/real/pes): standard 1 766/3 021/4 534 + vybrané 1 567/2 792/4 683 = 3 333/5 813/9 217; × režie 1,08/1,12/1,18 × DPH 1,12 = **4 032/7 292/12 181** stavba s DPH; služby ~7,4/9,6/12 % = 298/700/1 462 → **4,33/7,99/13,64 mil.** Kompletní (10,7 mil. real) jen jako citlivost. Důvod: bez nového tepla, střechy a elektra byty nejdou prodat „po rekonstrukci“, ale ETICS a sanace vlhkosti tlačí náklady nad hranici 30 % pro DPH a kupci bytů je nezaplatí.
- **DPH (§ 56 ZDPH od 7/2025)**: náklady bez DPH > 30 % ceny a prodej do 23 měs. → zdanitelné 12 %. Model: pes bez odpočtu, real/opt s registrací a odpočtem; test souhrnně za dům (ponytail – správně po jednotkách). Varianta **B2h** = pronajímat 24 měs. a prodat osvobozeně.
- Daň z příjmů: prodej celku § 10 (pes § 7), prodej po bytech § 7 (opt § 10); § 10 bez úroků jako výdaje.
- Financování: úvěr 70 % (pes 60 %) kupní ceny + stavba čerpaná průběžně do 70 % hodnoty po dokončení; zbytek, rezerva, úroky a služby z VK.
- Cílová marže = **čistý zisk po dani / všechny náklady** ≥ 20 %.
- Nájemníci: dům bereme jako prázdný (viz Stopky).

## Klíčová zjištění zatím
- Plochá střecha, 2 NP → půdní vestavba (C1) prakticky nejde; zbývá ustupující podlaží / 3. NP podle ÚP.
- Přístup přes pozemek SPÚ 2128/3 bez zmínky o věcném břemeni → riziko pro financování i prodej po bytech.
- Pozemek jen 239 m² (zastavěná plocha a nádvoří) → parkovací stání pro nové byty na vlastním pozemku asi nejsou.
- Trhliny na fasádě i uvnitř → statik před nabídkou.

## Doplnění zadání (2026-11-04, od mateřské session)
- Konec kroku 2: kontrola stopek – podmínky prodeje ČD (VŘ, kauce, zákaz přeprodeje), nájemníci, OP dráhy, zástavy, ÚP vylučující nástavbu. Vyloučené varianty zapsat sem a dál nepočítat (jen proč).
- Krok 3: jsou-li byty pronajaté, v každé variantě počítat s nájmem během čekání, dobou a náklady ukončení nájmů podle OZ a nižší cenou při prodeji s nájemníky.

## Stopky (kontrola na konci kroku 2)
| Stopka | Zjištění | Dopad |
|---|---|---|
| Podmínky ČD | VŘ obálkovou metodou, **nabídky do 16. 11. 2026 12:00**, min. 8 326 000 Kč, rozhoduje jen cena, další kola možná; **kauce ani zákaz přeprodeje nejsou**; cena se platí před podpisem (úschova OK); ČD nedá zástavu; schvaluje představenstvo + DR; dům odpojen od elektřiny (`katastr.md` §5) | Nic nevylučuje. Financování přes úschovu, zástava až po vkladu. |
| Nájemníci | ČD neuvádí; byty prázdné na prohlídce, odpojená elektřina | Model počítá s prázdným domem (bez nájmů během čekání, bez nákladů na ukončení nájmů). Ověřit u ČD. |
| Ochranné pásmo dráhy | Geometrie ZABAGED: kolej ~290 m → mimo zákonné OP (60 m). ČD ale ve smlouvě chce stanovisko SŽ ke každé stavbě | Nic nevylučuje; C/E +1–3 měsíce a riziko SŽ. |
| Zástavy, předkupní práva, VB | LV za CAPTCHA – neověřeno | Nutné ověřit před nabídkou (uživatel). |
| Statika (nové fotky 4. 11.) | Trhliny 2–3 mm přes sokl do terénu, znovu otevřená vyplněná trhlina, schodovité trhliny v obou podlažích (`podklady/stav-nove-fotky.md`) | Nevylučuje, ale realisticky +1 mil.; **C1/C2 podmíněná stopka bez posudku statika**. |
| Parkování podle ÚP (W02) | „parkování vozidel je nutné řešit na vlastním pozemku“; pozemek = půdorys | **B2n, C1, C2 podmíněné koupí části 2128/3 od SPÚ**; B, B2, B2h, D bez nových stání. |
| ÚP | Plocha **BI**: „max. 2 NP s využitelným podkrovím nebo ustoupeným podlažím“ (`uzemni-plan.md`) | **C3 (plné 3. NP) VYLOUČENO** – jen po změně ÚP (36–60 měs.). C1 (nástavba šikmé střechy s podkrovím; půda dnes není, střecha plochá) a C2 (ustupující) přípustné. |
| Přístup | Pozemek = jen půdorys domu, přístup přes 2128/3 SPÚ bez doloženého VB | Nevylučuje, ale je předpoklad každé varianty kromě A0; v modelu náklad + čas. |

## Krok 4 – stav
- Spuštěno: `overeni/rozpocet-2.md` (jen fotky a plochy), `overeni/ceny-2.md` (jen adresa, plochy, dispozice), `overeni/revize.md` (revizor podkladů a model.py).
- Výsledek modelu před ověřením (ceny z `ceny-byty-realizovane.md` a `ceny-domy-2.md`, střední rekonstrukce): realisticky nejlepší B2h 6,4 %, C2 4,1 %, B2 3,3 %, D (10 let) IRR 3,1 %; A0/A1/A2/E ztráta. Max. kupní cena pro 20 % realisticky: B2h 5,0 / D 6,7 / A0 6,0 mil.; bod zvratu B2h 10,5, C2 10,4, B2 9,5, D 11,6 mil. Při vítězné ceně 9,0 mil. B2 +0,3, B2h +1,1, D +2,6 mil.

- **4.1 rozpočet-2** (jen fotky): kosmetika 0,62 / standard 4,44 / střední 8,91 / kompletní 12,51 mil. real (vč. rezervy 10 %, bez ní ~0,57/4,03/8,10/11,37). Proti mému: standard −2 %, střední +1 %, kompletní +6 % → v toleranci 15 %, beze změny. **Kosmetika −39 %** (malba 80 vs 170 Kč/m², levnější vyklizení, menší režie) → rozhodnutí: střed obou 0,45/0,80/1,35 mil.; A1 to neotočí. Nové riziko z rozpočtu-2: chybí elektroměry, možná ztráta rezervovaného příkonu (odpojeno), podchycení základů 0,5–1,5 mil.
- **4.2 ceny-2** (jen adresa, plochy, dispozice): součet 4 bytů po rek. 23,44 mil. (můj 22,77, −3 %), 5 bytů B2 24,42 (můj 24,41), dům po rekonstrukci 16,5 (A2 15,94), nástavba 92 tis./m² (můj ~101, +10 %), nájem 274 Kč/m² (můj 295, +8 %) → v toleranci. **Dům dnes 11,5 vs můj 8,3 mil. (+39 %)** → rozhodnutí: real zůstává 8,3 mil., opt zvýšen na 11,5 mil. Důvod: reziduálně (bod zvratu B2 ~9,5 mil. při real cenách a nákladech) racionální kupec víc nedá; pronajímatel by při 11,5 + ~9 mil. rekonstrukce měl hrubý výnos ~4 %; srovnání v ceny-2 jsou nabídky domů v lepším stavu (Na Chmelnici s nájemníky).
- **4.3 revize** (`overeni/revize.md`, 15 nálezů) – zapracováno:
  - přijato: D exit po bytech se srážkou za opotřebení 8/12/15 % za 10 let (1); daň z nájmu = lepší z paušálu a skutečných výdajů s odpisy 30 let (3); test 30 % pro DPH s rezervou a riziky, děleno základem bez DPH (4); kk prémie jen opt 3 % (7); úvěr na koupi až po zajištění přístupu (pes/real), A0/A1 bez úvěru (9); odpočet DPH i z rezervy a provize (10); E – náhrada projektu jen v podílu (11); nájem 250/280/310 Kč/m² (13); náklady přepočteny na plochu (60 % s plochou) (14); LTV z ocenění domu jako celku (15).
  - sloučeno: lokalita + nezateplený dům + nulové parkování bez prémie za nádraží → 0,90/0,95/1,00 (2, 5).
  - nezapracováno: rezerva 15 % se celá utratí (8) – zadání chce rezervu ≥ 15 %, konzervativní; zdanění nájmu v B2h přes § 7 (6) – dopad +0,2–0,4 mil., konzervativní, uvedeno v reportu.
- Po opravách (real): B2h +1,21 mil. (5,4 %), C2 +1,08, B +0,68, B2 +0,52, C1 −0,33, A0 −0,59, A1 −1,43, E −1,45, A2 −4,50; D10 +8,19 (ROI 31,8 %, ale IRR 6,4 %, CF rok 1 −0,17 mil., hrubý výnos 3,3 %). Max. cena pro 20 %: B2h 4,4, B 3,9, B2 3,6, C2 2,0, A0 6,2, A1 5,3, E 5,3 mil. Bod zvratu: B2h 10,3, C2 10,0, B 9,4, B2 9,2 mil. Kompletní místo střední: B2 −2,0 mil.
- VK: banka bez služebnosti přístupu nepůjčí → realisticky 11–15 mil. vlastních zdrojů na začátku, pokud se přístup nevyřeší před koupí.

## Krok 5 – report
- 2026-11-04: `report.html` generuje `report.py` z `model.py` (čísla vždy z modelu; po změně vstupů spustit `python3 model.py` a `python3 report.py` a `sh deploy-web.sh`). Web: https://benesov.noirloop.com
- Závěr: za 8,326 mil. na přeprodej nekupovat; realisticky flipy 0,7–1,2 mil. (3–5 %), max. cena pro 20 % 2–6 mil., bod zvratu B 9,4 / B2h 10,3 mil.; D jen jako dlouhodobý nájem (IRR 6,4 %, závisí na růstu cen). Otočit to může: přístup zapsaný, statika OK, rekonstrukce −30 % nebo ceny bytů +20 %.

## Přepočet s ověřenými plochami (2026-11-04, na žádost mateřské session)
- **Zdroj ploch: `../dispozice.md`, sekce „Plochy – odhad“ (ř. 53–81).** Byty A 90–100 (model 95), B 55, C 75, D 40 → 265 / 270 / 275 m² (pes/real/opt, `plocha_koef`); 384,46 m² = čistá plocha obou podlaží vč. nebytových; chodby a schodiště 45–50 m²; nebytové prostory v přízemí 60–70 m². Nahrazuje dřívějších 259 m² × koef. B2: A1 53 + A2 42 + B 55 + C 75 + D 40.
- Nová dílčí varianta **B2n** = B2 + byt 2+kk z dílny, skladů a kotelny (50/55/60 m² po odečtu technické místnosti pro TČ; srážka 15/10/5 % za přízemí a okna; náklady 2,49/1,44/0,85 mil. = dispozice-zmeny.md var. C minus B2; +6/4/3 měs. na změnu v užívání; +1 parkovací stání 0,4/0,15/0,02 mil.).
- Výsledek (real): **B2n +2,13 mil. (8,5 %, IRR 13,6 %, VK 8,9 mil.)**, max. cena pro 20 % 5,12 mil., bod zvratu 11,9 mil.; v zisku při všech citlivostech; stavba −30 % → 29 %, ceny +20 % → 21 %. B +1,03 (4,8 %), B2 +1,02, B2h +1,71, C2 +1,52, D10 +9,08 (IRR 7,0 %). Report přegenerován a znovu publikován.
- Ověření krokem 4 platí dál: plochy se změnily o +2–4 %, druhý rozpočet i ceny počítaly s 260 m²; B2n je nová a nezávisle ověřená není (náklady z dispozice-zmeny.md, ODHAD).

## Ověření B2n a opravy modelu (2026-11-04, na žádost mateřské session, schváleno uživatelem)
- **Nezávislé ověření B2n** (agenti nedostali moje čísla ani dispozice-zmeny.md):
  - `overeni/b2n-cena.md`: realizovaně 67/83/97 tis. Kč/m² (přízemí −7 %, nebytový původ −3 %, nabídka→prodej −6 %); můj vstup 65/84/104 tis. → do 15 %, beze změny.
  - `overeni/b2n-rozpocet.md`: proveditelné s výhradami (pes „ne“); byt 40/50/58 m², přestavba **5,3/2,8/1,5 mil.** s DPH, +9/4/2 měs. Můj vstup 2,49/1,44/0,85 mil. a 50/55/60 m² → rozdíl +94 % (real) → **převzato ověření**. Důvod: můj odhad (dispozice-zmeny.md var. C) nepočítal se zahloubením podlahy kvůli světlé výšce 2,5 m (vyhl. 146/2024 ve znění 97/2026), snížením parapetů na 1/10 plochy oken (u trhlin), odvlhčením, akustickými okny a rekuperací (silnice II/110). Parkování ponecháno 0,4/0,15/0,02 mil. (ověření: 0–3 stání).
  - Výsledek: B2n real 2,13 → **1,17 mil. (4,4 %)**, max. cena pro 20 % 3,49 mil., bod zvratu 10,2 mil. B2n už není nejlepší.
- **Kalibrace pesimistického scénáře:** `stredni` pes 13,64 → 11,91 mil. (služby 1,46 → 1,28), takže stavba + služby + rezerva 15 % = 13,7 mil. jako `overeni/rozpocet-2.md` (bez změn dispozic a inflace; s plochou ×1,005 = 13,76). `rizika_navic` pes 2,0 → 0 (rizika R1–R9 kryje rezerva; vysoká rizika jen v textu). `c1_hruba`/`c2_hruba` = 200/150 m² ve všech scénářích (rozměr domu). Pes stavba+projekt+rezerva: B2 20,2 → 16,1 mil.; C1 celkové náklady 52,8 → 46,3 mil. Do reportu věta, že pes = horní mez cen, ne součet všech rizik.
- **Dvojí střecha u nástavby:** nový vstup `strecha_v_rekonstrukci` 1,44/0,97/0,60 mil. s DPH (stav.md 5c 1 248/774/494 tis. × režie 1,18/1,12/1,08 × DPH 1,12; pes navíc × 0,873 jako kalibrovaná střední úroveň) odečten z rekonstrukce před rezervou a testem 30 % pro DPH: C1 celý, C2 50 % (ustupující podlaží kryje 60–70 % střechy, zbytek pochozí terasa s novou hydroizolací – ODHAD). C1 real 0,29 → 0,95, C2 1,52 → 1,80 mil.
- **Pořadí po všech opravách (real, čistý zisk):** D 9,08 (11 let, IRR 7,0 %) › **C2 1,80** (5,5 %, IRR 8,7 %) › **B2h 1,71** › B2n 1,17 › B 1,03 › B2 1,02 › C1 0,95 › A0 −0,59 › A1 −1,45 › E −1,45 › A2 −4,18. Report přepsán (C2 jako nejlepší přeprodej) a znovu publikován (verze 3).

## Nové fotky a videa ze 4. 11. 2026 (na žádost mateřské session)
- 36 fotek + 3 videa z `photos/` → `nove/` (W01–W36, snímky V1–V3 po 1 s), popisy `nove/popisy-*.jsonl` (4 popisovače), shrnutí `podklady/stav-nove-fotky.md`, dodatek na konci `podklady/stav.md`.
- **Statika:** svislé trhliny fasádou 2–3 mm (podle prstů na W05; rychlý odhad „0,5–1 cm“ se po přeměření nepotvrdil) pokračují přes sokl do terénu, vyplněná trhlina se znovu otevřela (W11), schodovité trhliny s cihlami a posunem (W26, W27, V3), vodorovné pod stropem 2. NP (W20, W22, W24). → pohyb pokračuje, pravděpodobně sedání.
  - Rozhodnutí: `rizika_navic` = statické zajištění **0,25 / 1,0 / 3,5 mil.** (opt/real/pes) u všech rekonstrukcí; `nastavba_statika` 0,5 / 2,0 / 2,5 mil. (podchycení pod nástavbou); `dum_asis` 5,0 / 7,5 / 11,0 mil. (kupec odečte statiku).
- **Parkování (W02, ÚP s. 84):** „parkování vozidel je nutné řešit na vlastním pozemku“; pozemek = půdorys → `parkovani` 0,1 / 0,3 / 0,8 mil. (koupě části 2128/3) u B2n, C1, C2. B, B2, B2h, D nová stání nepotřebují (plocha bytů se nemění).
- **Stopky doplněny:**
  - C1/C2 – **podmíněná stopka: bez posudku statika (aktivní sedání?) nástavbu nepočítat jako reálnou**; v modelu ponechány s podchycením.
  - B2n, C1, C2 – **podmínka: vlastní pozemek pro stání** (koupě části 2128/3 od SPÚ); když SPÚ neprodá, nepovolí se.
  - Všechny varianty – statik před nabídkou; bez vyloučení aktivního sedání je dům bez hypotéky těžko prodejný.
- **Výsledek (real, čistý zisk):** D 8,08 (IRR 6,0 %) › **B2h 1,16** (4,9 %) › B2n 0,53 › B 0,47 › B2 0,46 › C2 0,13 › C1 −1,32 › A0 −1,35 › A1 −2,24 › E −2,25 › A2 −5,07. Max. cena pro 20 %: B2h 4,0, B 3,4 mil.; bod zvratu přeprodejů 8,5–10,2 mil.
- **Co se změnilo proti verzi 3:** nejlepší přeprodej už není C2 (1,80 → 0,13 mil.), ale B2h (1,71 → 1,16); nástavby po statice a parkování ztratily smysl; A0 je hlouběji ve ztrátě (−0,59 → −1,35). Report (verze 4) přegenerován, galerie s novými fotkami trhlin a regulativu ÚP.

## Firma vs. řemeslníci (2026-11-04, na žádost mateřské session)
- Přepínač `ov={"dodavatel": "remeslnici"}` (ne nová varianta), počítáno pro B, B2, B2n, B2h, D; nástavby ne; statické zajištění (`rizika_navic`) dál firma.
- Rozpad stavby s DPH 12 % (G): S = G/1,12; základ = S/(1 + režie GD 18/12/8 %); materiál = základ × 45/50/55 % (ODHAD, zdroj pro ČR 2026 nenalezen) s DPH 21 %; práce = základ × (1 − materiál + ½ režie) × (1 − sleva 0/10/20 %, ODHAD); 50/25/0 % práce dělají plátci (12 %) kvůli limitu obratu 2 mil. Kč/rok (§ 6 ZDPH od 1. 1. 2025, okamžitě nad 2 536 500 Kč; FS č.j. 11977/25); koordinace 5/4/3 % S s DPH 21 %; stavba +2/1/0 měs.; pes rezerva +5 p.b. (vady bez jedné záruky).
- Test 30 %: materiál bez DPH + faktury neplátců celé + plátci bez DPH; odpočet při registraci: 21 % z materiálu, 12 % z práce plátců, 21 % z koordinace. **Režim DPH se u žádné varianty nemění** (B, B2, B2n zdanitelné; B2h, D osvobozené).
- Výsledek (real, čistý zisk firma → řemeslníci): B 0,47 → 0,75; B2 0,46 → 0,77; B2n 0,53 → 0,95; B2h 1,16 → 1,45; D 8,08 → 8,56 mil. Stavba levnější o 0,5–0,8 mil. (~5 %). Pes horší o 0,4–0,6 mil. Max. cena pro 20 % se zvedne o 0,5–0,7 mil. (B2h 4,0 → 4,5). V reportu tabulka „Firma, nebo řemeslníci“ (verze 5).

## Opravy vstupů: přízemí a inflace změn (2026-11-04, schváleno uživatelem)
- Nový vstup `prizemi_srazka` 0,93 / 0,95 / 0,97 (overeni/b2n-cena.md: přízemí −7 %, rozpětí 3–12 %) jen v ceně bytů A, A1, A2 (B, B2, B2n, B2h, C1, C2, A2 přes součet bytů, D v exitu); přepočet nákladů z plochy (`adj`) beze změny.
- Nový byt N: `prizemi_srazka` × `nebyt_srazka`, kde `nebyt_srazka` je nově jen za nebytový původ a okna 0,91 / 0,95 / 0,98 (součin = dřívějších 0,85 / 0,90 / 0,95, přízemí se nepočítá dvakrát).
- `b2_zmeny` a `nebyt_zmeny` nově × (1 + `inflace_stavby`) jako ostatní stavba.
- Výsledek (real, čistý zisk): **D 7,75** (IRR 5,7 %) › **B2h 0,90** (3,8 %) › B 0,27 › B2 0,20 › B2n 0,20 › C2 −0,20 › A0 −1,35 › C1 −1,74 › A1 −2,24 › E −2,25 › A2 −5,30. Max. cena pro 20 %: B2h 3,65, B 3,15 mil. Řemeslníci real +0,28 až +0,48 mil. Report verze 6.

## Hotovo – co zbývá uživateli
- Odpovědi na otázky k ověření (sekce 7 reportu), hlavně LV 6313 a 2128/3 před 16. 11. 2026 12:00.
- Po odpovědích upravit vstupy v `model.py` (IN) a přegenerovat report.

## Rozpory a otevřené otázky
- Ceny celého domu: `ceny-domy.md` real 40 tis. Kč/m² (odhad) × `ceny-domy-2.md` 21,5 tis./m² podlahové (29 tis./m² bytů) → použit `ceny-domy-2.md` (5 jádrových srovnání, jasná metodika).
- Plocha bytů: fotky ~259 m² × katastr 290–330 m² × ceny-domy-2 285 m² → model 259 m² × plocha_koef 0,95/1,0/1,10.
- OP dráhy: ČD tvrdí „v pásmu“, ZABAGED ~290 m od koleje → mimo; smluvní závazek ČD platí stejně.
- Sítě: ČD voda/kanalizace „Ne“, RÚIAN ano.

## 4. 11. 2026 – plochy bytů při prodeji
- Model nese u každé prodávané jednotky plochu (`r["byty"]`: název, m², cena s DPH); výsledky beze změny.
- Report: tabulka „Plochy a ceny bytů při prodeji“ v sekci Varianty; xlsx: list „Plochy a ceny bytů“.

## 4. 11. 2026 – plochy z půdorysu (dispozice.md, NV 366/2013)
- Byty A 97 / B 67 / C 84 / D 41 = 289 m² (dříve 95/55/75/40 = 265), plocha_koef 280/290/300. B2: A1 53 + A2 43 (−1 m² zeď).
- B a N jsou nad 60 m² → cena velkých bytů (ceny-byty-realizovane.md). N = 86 m² nebytové části minus TČ, vestibul, kóje → 64/71/77 m²; nebyt_zmeny ×1,194 (plošné položky 65 → 86 m², ODHAD).
- Výsledek real: B 0,48, B2 0,36, B2n 0,49, B2h 1,11, C2 0,03, D 8,64 (IRR 6,3 
## 4. 11. 2026 – plochy z půdorysu (dispozice.md, NV 366/2013)
- Byty A 97 / B 67 / C 84 / D 41 = 289 m² (dříve 95/55/75/40 = 265), plocha_koef 280/290/300. B2: A1 53 + A2 43 (−1 m² zeď).
- B a N jsou nad 60 m² → cena velkých bytů (ceny-byty-realizovane.md). N = 86 m² nebytové části minus TČ, vestibul, kóje → 64/71/77 m²; nebyt_zmeny ×1,194 (plošné položky 65 → 86 m², ODHAD).
- Výsledek real: B 0,48, B2 0,36, B2n 0,49, B2h 1,11, C2 0,03, D 8,64 (IRR 6,3 %). Závěr beze změny.
- Report: tabulka „Cena a náklady na m² prodávané plochy“ (prodejní cena, rekonstrukce = projekt + stavba + rezerva + nástavba, všechny náklady, čistý zisk; Kč/m²).

## 4. 11. 2026 – užší rozpětí prodejních cen (oprava schválena uživatelem)
- lokalita 0,95 ve všech scénářích (dříve 0,90/0,95/1,00 – vlastnost domu se sčítala s krajními cenami; pes 68 tis. Kč/m² ≈ cena neopravených bytů, opt 100+ nad všemi prodeji).
- m2_maly opt 105 (dříve 110): prodeje 115–116 tis. jsou garsonky 30–37 m².
- Cena B za m²: 72 / 81 / 89 tis. (dříve 68 / 81 / 94). Čistý zisk B pes −12,05, opt 7,83; realistický scénář beze změny.

## 4. 11. 2026 – varianta Bn a pesimistická rekonstrukce (schváleno uživatelem)
- Nová varianta Bn = B (4 byty beze změny) + byt N z nebytové části → 5 bytů, 344 / 360 / 377 m². Real 0,59 mil. (2,1 %), max. cena pro 20 % 2,42; s N 86 m² 1,15 mil. Nejlepší přeprodej bez nájmu; B2 (dělení A) je horší než B.
- Pes. rezerva 10 % (dříve 15) a statika 2,0 mil. (dříve 3,5 = nejhorší podchycení, zůstává v textu jako riziko). Rekonstrukce B pes 66 → 59 tis. Kč/m² (novostavba ~62). B pes −12,05 → −9,89. Realistický scénář beze změny.

## 4. 11. 2026 – plochy po posunu schodiště (dispozice.md přepočteno jiným vláknem)
- Byty A 80 / B 75 / C 75 / D 42 = 272 m² (plocha_koef 262/282); B2: A1 2+kk 44 + A2 1+kk 35. Nebytová část 98 m² → N 76/83/86 m², nebyt_zmeny ×1,305.
- Varianta Bn = B + byt N; report doplněn o Bn (doporučení, tabulky, parkování).
- Výsledek real: D 7,39 (IRR 5,4 %), B2h 0,47, Bn 0,36 (s N 98 m² 0,93), B2n 0,16, B 0,01, B2 −0,34, C2 −0,86, C1 −2,40. Závěr beze změny.

## 4. 11. 2026 – plochy znovu změněny v dispozice.md (B 67, nebytová 86)
- Byty A 80 / B 67 / C 75 / D 42 = 264 m², nebytová 86 → N 64/71/74. Plochy jsou teď konstanty PLOCHA_BYTU, NEBYT_CELKEM, NEBYT_ODECET v model.py; report text je čte odtud (při další změně upravit jen model.py).
- Tabulka Varianty a scénáře má sloupce „m² k prodeji“ a „Cena bytů, tis. Kč/m²“ (u A2 po slevě investora).
- Výsledek real: D 6,76 (IRR 5,0 %), B2h 0,20, Bn −0,19 (s N 86 m² 0,45), B −0,37, B2n −0,51, B2 −0,72, C2 −1,24, C1 −2,77. Žádný přeprodej hned po rekonstrukci už nevychází v zisku.

## 4. 11. 2026 – přestavba nebytové části bez zahloubení (uživatel)
- Podlaha nebytové části je v úrovni bytu A, zahlubovat se nemusí: v overeni/b2n-rozpocet.md A4 jen vybourání (40/25/15 tis.), C3 skladba na stávající desku (140/100/70 tis.).
- Nalezena chyba: rozpočet b2n už obsahoval rezervu 20/10/5 % a model přidával 15 % → vnitřní rezerva vyřazena.
- Přestavba před přepočtem na 86 m²: 4,35 / 2,48 / 1,31 mil. (dříve 5,31 / 2,84 / 1,46); v modelu 5,19 / 2,96 / 1,57 mil.
- Výsledek real: Bn +0,14 (dříve −0,19; s N 86 m² 0,70), B2n −0,10, ostatní beze změny.

## 4. 11. 2026 – report přestavěn na 2 verze (požadavek uživatele)
- V1 = 6 bytů: A 4+1 80, N1 + N2 2+kk po 40 (nebytová část, chodba společná, bez centrální technické místnosti), B 3+1 67 (z 2+1), C 3+1 75, D 1+1 42 = 344 m². V2 = V1 + ustupující podlaží (2 × 60 m²) = 464 m².
- Nové vstupy (ODHAD): nebyt2_m2 36/40/42, nebyt_druhy_byt (druhé jádro) 0,79/0,52/0,32 mil., b31_zmeny 0,25/0,15/0,10 mil. Řemeslníci se u V2 počítají pro rekonstrukci, nástavba dál firma.
- Model vrací r["rozpis"] (stavba po položkách, součet = projekt + stavba + rezerva + nástavba).
- Report: Shrnutí → 1. Náklady (firma vs. vlastní dodavatelé) → 2. Prodej (realisticky, po bytech) → 3. Shrnutí → stav, předpoklady, rizika, srovnání, otázky. Pronájem D a ostatní varianty z reportu odstraněny (v modelu a xlsx zůstávají).
- Výsledek real: V1 0,47 (firma) / 0,90 (vlastní dodavatelé); V2 0,14 / 0,53. Průměrná cena V1 82 tis. Kč/m²; pro 20 % potřeba ~108–111 tis. Při 87 tis. Kč/m² V1 1,32 / 1,69.

## 4. 11. 2026 – report zjednodušen (požadavek uživatele)
- Verze pojmenované „Bez nástavby“ (V1) a „S nástavbou“ (V2), popis obou nahoře; tabulky s dvouřádkovou hlavičkou (verze → firma / vlastní dodavatelé).
- Nová tabulka „Rozpočet stavby po položkách“ (stav.md 5a + 5b + vybrané 5c, součet 5 813 tis. = vstup stredni; nebytová část z b2n-rozpocet.md; nástavba).
- Odstraněno: současný stav domu (fotky), otázky k ověření. Srovnávací byty a domy přesunuty na srovnani.html, na webu https://benesov.noirloop.com/srovnani.html. Report 32 kB místo 660 kB.

## 4. 11. 2026 – audit propočtu 5 subagenty a opravy (session „Agent pro ověření kalkulace“, schváleno uživatelem)
- Audit: scénáře, mechanika kódu, vstupy + daně, report vs. model, návrhy zlepšení. Zpráva: `~/Obsidian/raw/sessions/2026-11-04-benesov-audit-propoctu.md`.
- **Opraveno v model.py:**
  - Scénáře sjednoceny (rozhodnutí ≠ scénář): registrace k DPH a odpočet i v pes (§ 79: pozdní plátce odečte vstupy za 12 měs.; dřív pes bez odpočtu); prodej po bytech § 7 ve všech scénářích (dřív opt § 10); prodej celku § 10 ve všech (dřív pes § 7).
  - Ceny bytů a domů rostou do měsíce prodeje o `hodnota_rust` 0/3/5 % ročně jako v D (dřív jen stavba s inflací, přeprodeje bez růstu cen). Citlivost „ceny bez růstu“.
  - A0/A1/E bez úvěru ve všech scénářích (dřív opt A0/A1 úvěr od t=0 → IRR 711 %; E úvěr bez užitku).
  - V2 parkování jen jednou; odpočet DPH z rezervy i u nástavby; citlivost „rekonstrukce +20 %“ zvedá i `nastavba_statika` a reziduál u E.
  - ROI = čistý zisk / náklady bez DPH odvedené z prodeje (DPH od kupců není vložený náklad).
  - D5: § 10 základ zvýšen o uplatněné odpisy (§ 10 odst. 5 – ověřit u poradce); `hruby_vynos` z investice do začátku nájmu; `uver_max` skutečný úvěr.
  - `irr_mes`: záporný poslední tok (DPH, daň) → IRR chyběla (V1 opt); hledá změnu znaménka nejblíž 0. Nové asserty (IRR, parkování V2).
  - Citlivosti lokalita −8 % / +5 % (lokalita.md −2 %, −8 až +5); popisy A2/B/D „střední“; text kalibrace `stredni` pes.
- **Nezměněno (rozhodnutí uživatele nebo čeká na odborníka):** pes rezerva 10 % (obrácené pořadí proti real 15 %, ale schváleno); lokalita 0,95 ve všech scénářích; test 30 % souhrnně za dům (GFŘ 1127/26 chce po jednotkách – mění jen opt); registrace k DPH až prodejem (+0,3–0,5 real, daňový poradce); možné dvojí započtení statiky (statik); úvěr na rekonstrukci 7,5 % místo hypotéky 6,2 % (−0,1 až −0,3); kupní cena podle scénáře (opt by při ~10,4 mil. vyšel o 1,5–2 mil. hůř); Monte Carlo; varianta A3 (prodej bytů k rekonstrukci).
- **Report:** opraveny věty „nabídka za minimum má smysl, když…“ (ani stavba −30 % ani ceny +20 % samy 20 % nedají), „držet rozsah pod 30 %“, VK, § 7 pojistné, nájem 280 vs. medián 292/315, „nástavba zisk nezvedne“; pes/opt označeny jako krajní případy; DPH a růst cen v předpokladech.
- **Výsledek real (čistý zisk, předtím → teď):** V1 0,47 → 1,20 (4,5 %; vlastní dodavatelé 1,61), V2 0,14 → 1,70 (4,4 %), B2h 0,20 → 1,55, Bn 0,14 → 0,85, B −0,37 → 0,23, C2 −1,24 → 0,51, A0 −1,35 → −1,26, D10 6,76 beze změny, D5 2,73 → 2,04. Většinu zlepšení dělá růst cen 3 %/rok (V1 bez růstu 0,47). Max. kupní cena pro 20 %: V1 3,48 (vlastní dodavatelé 4,23), V2 1,71; bod zvratu V1 10,3, V2 11,1 mil. **Závěr beze změny:** za 8,33 mil. žádná varianta realisticky nedá 20 %.
- Pes: V1 −15,07 → −12,30 (odpočet DPH). Opt: V1 10,58 → 10,27 (§ 7 místo § 10).

- 2026-11-04 (večer, rozhodnutí uživatele): byty větší než 1+1 (2+kk a víc, nástavba ≥ 50 m²/byt) +5 tis. Kč/m² k ceně po srážkách, vstup `m2_nad_1p1` v `model.py`. Real čistý zisk: V1 1,20 → 1,92 (7,3 %; vlastní dodavatelé 2,33), V2 1,70 → 2,80. Report: z tabulky prodeje odebrán sloupec Verze, číselné hlavičky zarovnány doprava (i firma / vlastní dodavatelé ve shrnutí). Publikováno (verze 19).

## 5. 11. 2026 – rozpis nákladů po položkách (10 subagentů, rozklikávací tabulka)
- Každá nákladová položka zkontrolována a rozepsána subagentem: `polozky/<slug>.md` (koupe, pristup-parkovani, strecha-statika, technika, byty, nebyt-bytb, nastavba, projekt-rezerva, financovani-dph, prodej-ostatni); společné zadání `polozky/_zadani.md`.
- **Opraveno v model.py (jasné chyby, ne drobné rozdíly):**
  - `rizika_navic` real 1,0 → 0,8 mil.: sešití trhlin se počítalo i v sanaci trhlin (stav.md 220 tis.), monitoring ve službách.
  - `nastavba_m2` 46/38/32 → 54/43,5/34,5 tis.: sazba nepokrývala terasu, prodloužení schodiště, další TČ, lešení a jeřáb, požární úpravy a příkon (rozpis zdola 6,53 mil. bez DPH).
  - `b31_zmeny` 250/150/100 → 180/82/70 tis.: rozpis zdola (příčka, nový vchod z chodby, elektro, radiátor).
- **Beze změny celku, změněno složení:** `stredni` – rozpis zdola 7,644 mil. vs. model 7,635 mil. (TČ 2 × 16 kW místo 2 × 10–12 kW +0,37 mil.; byt A jen obnova koupelny a kuchyně, malba společných prostor přesunuta do společných prostor −0,24 mil.). Koupě, přístup a parkování, nebytová část (−1 %), projekt, prodej, úroky, DPH v toleranci.
- Výsledek real (čistý zisk, předtím → teď): V1 1,92 → 2,06 (7,9 %; vlastní dodavatelé 2,33 → 2,47), V2 2,80 → 2,31 (5,9 %). Max. kupní cena pro 20 %: V1 4,74 (vlastní 5,48), V2 2,35; bod zvratu V1 11,8, V2 12,2 mil.
- Report: dvě tabulky nákladů nahrazeny jednou (`tab_naklady()`, tis. Kč, čísla zarovnaná vpravo ve všech 4 sloupcích); každá položka rozklikávací, „Rozbalit vše“. Dílčí položky ze seznamů `POL` v report.py se přepočtou na hodnotu z modelu, assert: součet položek = náklady z modelu.
- **Otevřené (nezměněno, k rozhodnutí):**
  - Úvěr: FO prodávající po bytech dostane spíš podnikatelský/developerský úvěr (7,5 % a 1 % → úroky +0,22 mil.; nebankovní ~6,9 % + 4 % poplatek → +0,53 mil.). Strop úvěru 70 % z hodnoty po dokončení je optimistický (z dnešního odhadu ~5,8 mil.).
  - Technická místnost pro TČ: V1 počítá centrální TČ, ale 2 × 40 m² bytů z 86 m² nenechá místo (~6 m²) → byty spíš 2 × 37 m².
  - `pristup_mes` 9 měs. je krátké, SPÚ jedná 12–24 měs.; prodej pozemku SPÚ může nést DPH 21 %.
  - Pes nástavby: podchycení je v `rizika_navic` 2,0 i `nastavba_statika` 2,5 → pes možná nadsazený o 1–1,5 mil.
  - Elektřina: podíl na připojení 50 tis. platí, jen pokud distributor zrušil odběrné místo; dočasné napájení stavby (10–35 tis.) v modelu není.
  - Realitka často dává foto, 3D a úschovu v provizi → marketing a právník (240 tis.) možná navíc; prodej bez RK by ušetřil ~1,1 mil. čistě.

## 5. 11. 2026 – úvěr 9 % (rozhodnutí uživatele)
- `sazba` 7,0 / 6,2 / 5,7 → 9,8 / 9,0 / 8,5 % (podnikatelský úvěr místo investiční hypotéky; pes/opt se stejným odstupem). Platí i pro D (pronájem).
- Výsledek real (čistý zisk): V1 2,06 → 1,89 (7,1 %; vlastní dodavatelé 2,28), V2 2,31 → 1,97 (4,9 %). Úroky a poplatky V1 0,86 → 1,17 mil. (úroky snižují základ daně § 7, proto zisk klesne jen o ~0,17). Max. kupní cena pro 20 %: V1 4,46 (vlastní 5,18), V2 1,86; bod zvratu V1 11,5, V2 11,6 mil. Report verze 21.

## 5. 11. 2026 – prodej bez realitky, tabulka prodeje (rozhodnutí uživatele)
- `provize` 0 ve všech scénářích (uživatel prodává sám); marketing a advokát na byt zůstávají. Z reportu odebrána provize a odpočet DPH z provize.
- Tabulka 2. Prodej: byty bez nástavby → Bez nástavby (součet) → U1, U2 (nástavba) → S nástavbou (součet).
- Výsledek real (čistý zisk, vlastní dodavatelé dle MIX): V1 3,67 mil. (15,7 %), V2 +0,68 mil. proti V1. Max. kupní cena pro 20 %: V1 7,2 mil.; 20 % splní už stavba −30 % nebo ceny +20 % samy.

## 5. 11. 2026 – kontrola středu nákladových položek (/loop, polozky/_stred.md)
- Všech 19 položek tabulky „1. Náklady“ posouzeno, jestli realistická hodnota leží uprostřed. Změny real: `pristup_mes` 9 → 12; nový `parkovani_1` 800/200/60 tis. (bez nástavby 1 stání); střecha 3 600 → 3 200 Kč/m² (`strecha_v_rekonstrukci` 863 tis.); TČ 380 → 300 tis./ks; společné prostory 220 → 185 tis.; byty (jádra 150 tis., okna všechna 28 ks – uživatel, malba 110 Kč/m², vyklizení 60, plísně 40, úklid 25) → `stredni` real 7 990 → 7 624 tis., `stredni_sluzby` 700 (beze změny po opravě); `b31_zmeny` 82 → 105 tis.; `nebyt_zmeny` základ 2 482 → 2 281 tis.; `nastavba_m2` 43,5 → 41,5 tis.; `uver_poplatek` 1,5/1,0/0,5 %; `marketing_byt` 30/20/10 tis.
- Beze změny (střed): koupě, rozvody, trhliny, statika, vlastní dodavatelé, rezerva, DPH, advokát, držení, PENB, rozdělení.
- Výsledek real: V1 3,58 mil., V2 4,48 mil. (vč. souběžných rozhodnutí uživatele: architekt, prodej bez RK).

## REAS odhad bytů po rekonstrukci (2026-11-05)
- REAS plochy bytů **nezná** (formulář se na plochu ptá), takže velikosti bytů z něj zjistit nejdou; zadány plochy z půdorysu (`../dispozice.md`). Půdorysy beze změny.
- Zadáno v účtu uživatele (reas.cz/moje-nemovitosti, uložený byt Jana Nohy 1598 přepínaný po bytech, nakonec vrácen na C 3+1 75 m², 2. NP; PENB změněna z A na C – na odhad bez vlivu). Parametry: stav kuchyně/koupelny/místností výborný, tepelné čerpadlo, cihla, 2 podlaží, bez výtahu, balkonu, sklepu, parkování.
- Střed (rozpětí) mil. Kč: A 4+1 80 m² 1. NP 6,96 (6,61–7,31); B 3+1 67 m² 6,14 (5,83–6,44); C 3+1 75 m² 6,64 (6,31–6,98); D 1+1 42 m² 4,55 (4,32–4,77); N1/N2 2+kk 40 m² 1. NP 4,42 (4,20–4,64); nástavba 3+kk 60 m² 3/3 NP bez terasy 5,69 (5,41–5,97). V1 celkem 33,12 mil. (model 29,75, −10 %).
- Model beze změny (REAS v `model.py` jen jako `REAS` pro srovnání v reportu). Největší rozdíl u malých bytů (D +16 %, N +24 %): REAS nezná silnici, parkování ani nebytový původ. Při cenách REAS: V1 čistý zisk 5,93 mil. (model 3,75), V2 6,24 (model 4,66).
