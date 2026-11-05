# Revize propočtu č.p. 1598 Benešov – nezávislý revizor (4. 11. 2026)

**Co jsem prošel:** `model.py` (verze z 13:12 – během revize se v ní změnily jen řádky 31 `dum_asis` opt a 36 `kosmetika`, na níže uvedené nálezy to nemá vliv), `postup.md`, všechny `podklady/*.md`. Soubory v `overeni/` jsem nečetl. Model jsem spustil (`python3 model.py /tmp/x.xlsx`). Dopady jsem počítal na **kopii modelu ve scratchpadu** s opravami zapínanými přepínači (originál beze změny). Pokud není řečeno jinak, „dopad“ = změna **čistého zisku B2 v realistickém scénáři** při ceně 8 326 000 Kč (základ: **0,77 mil., ROI 3,3 %, max. cena 3,91 mil.**).

## Pořadí nálezů podle dopadu

| # | Nález | Kde | Dopad (real) | Směr |
|---|---|---|---|---|
| 1 | D: výstup po 10 letech jen prodejem celku s portfoliovou slevou 30 %, i když prodej po bytech je po 10 letech bez daně i bez DPH | model.py:393–394, 429–432 | **D10 +5,2 mil.** (3,24 → 8,5); max. cena D 6,67 → **10,96 mil.** | pro investora |
| 2 | Rozsah „střední“ (bez ETICS a sanace vlhkosti) se prodává za ceny „po kompletní rekonstrukci domu“ | model.py:22–24, 38–41; postup.md:20 | B2 **−0,65 mil.** při −5 % cen (kompletní rozsah: −2,6 mil.) | proti |
| 3 | D: daň z nájmu paušálem 30 % místo skutečných výdajů (odpisy + úroky → daň ≈ 0) | model.py:421 | **D10 +1,0 mil.** | pro |
| 4 | Test 30 % (DPH § 56): jmenovatel s DPH, bez rezervy a rizik, souhrnně za dům → falešné „útesy“ v citlivostech a v opt | model.py:204, 255–258 | real B2 **0** (podstatná změna platí i po jednotkách: 0,31–0,34, se spotřebovanou rezervou 0,36–0,40); citlivost B „ceny +10 %“ nadsazena o ~1 mil.; opt B/B2 osvobozeno neprávem | proti (citl./opt) |
| 5 | Lokalita −2 % obsahuje prémii +4 % za nádraží, kterou cenový podklad výslovně zakazuje počítat; chybí srážka za nulové parkování | model.py:25; lokalita.md:154,160; ceny-byty-realizovane.md:76,146 | B2 **−0,53 mil.** (C2 −0,75) | proti |
| 6 | B2h: nájem 24 měsíců zdaněn jako § 7 i s odvody (≈ 46 % na okraji) místo § 9 | model.py:237–244, 350 | B2h **+0,2 až +0,44 mil.** | pro |
| 7 | Prémie kk se přičítá k ceně malých bytů, jejíž srovnávací vzorek už jsou převážně kk byty (dvojí započtení) | model.py:26, 157 | B2 **−0,38 mil.** | proti |
| 8 | Rezerva 15 % se v realistickém scénáři celá spotřebuje, i když režie 12 % už obsahuje „nepředvídané drobnosti“ a očekávaná hodnota rizik R1–R9 je ~0,8 mil. | model.py:42, 216; stav.md:91–101, 138 | B2 **+0,36 mil.** (8,5 % místo 15 %) | pro |
| 9 | Přístup přes SPÚ až v 9. měsíci, ale úvěr na koupi se čerpá v měsíci 0 – banka bez věcného břemene nepůjčí | model.py:58–59, 167, 218–219; dane-financovani.md:157–158 | B2 **−0,25 až −0,4 mil.** (překlenovací úvěr 10–14 %) nebo +5,8 mil. VK v t=0 | proti |
| 10 | Při registraci k DPH chybí odpočet DPH z rezervy, provize RK, advokáta, geodeta, PENB | model.py:205, 260–262, 288–291 | B2 **+0,23 mil.** (C2 +0,32) | pro |
| 11 | E: náklady na projekt (60 % `nastavba_soft`) kupec proplatí vždy ze 100 %, i když za samotné povolení zaplatí jen `permit_podil` (pes 0 %) | model.py:273 | E real **−0,41 mil.**, pes −0,90; max. cena E 5,48 → 5,18 mil. | proti |
| 12 | A2/D: hodnota hotového domu 15,94 mil. je nad vlastním podkladem (kompletní rekonstrukce 14,25 mil., standard 11,7 mil.) | model.py:223, 393–394; ceny-domy-2.md:154–158 | A2 **−1,7 až −4,2 mil.** (je ztrátová i tak); D celek −1,5 mil. | proti |
| 13 | D: nájem 295 Kč/m² (nabídky malých bytů) bez lokality a slevy; podklad pro celý dům dává 270 | model.py:88, 418; ceny-domy-2.md:106, 188 | D10 **−0,63 mil.**, B2h −0,07 | proti |
| 14 | Opt scénář je vnitřně nekonzistentní: náklady ze stav.md počítané na 205 m² bytů, tržby na 285 m² (`plocha_koef` 1,10) | model.py:27; stav.md:138–140 | B2 opt 13,2 → 6,3 mil.; max. cena B2 opt **18,16 → 11,46 mil.** | proti (opt) |
| 15 | Úvěr na stavbu do 70 % součtu cen bytů (GDV), ne do 70 % bankovního ocenění domu | model.py:303–304; postup.md:23 | zisk +0,08 mil., ale **VK 6,4 → 8,7 mil.**, IRR −0,6 p.b. | feasibility |
| 16 | Byty A1/A2 jsou v přízemí u silnice, vedle dílny a kotelny – bez srážky za přízemí | model.py:98 | B2 **−0,25 mil.** (−5 % na A1/A2) | proti |
| 17 | Chybí užitek z 86 m² nebytových prostor v 1. NP (v B/B2 nejsou ani prodány, ani přičleněny) | model.py:97–99; dispozice-zmeny.md:116–132 | B2 **+0,5 až +0,8 mil.** čistého (varianta s novým bytem) | pro (chybí) |
| 18 | Vítězná cena ve VŘ: podklad čeká +8 % (9,0 mil.), základ počítá s minimem | model.py:11; ceny-domy-2.md:169 | B2 **−0,46 mil.** (výstup „zisk@9,0“ už to ukazuje) | proti |
| 19 | D: úroky před dokončením z celé výše úvěru od 1. měsíce | model.py:395–410 | D10 **+0,15 mil.** | pro |
| 20 | B2: povolení dělení A posouvá start celé stavby o 4 měsíce, ač jde dělat souběžně | model.py:194; dispozice-zmeny.md:183 | B2 **+0,1 mil.** | pro |
| 21 | B2h drží 24 měs. od rozdělení, zákon chce 23 měs. po měsíci dokončení → přeplácí ~2 měsíce | model.py:237–244 | B2h **+0,05–0,1 mil.** | pro |
| 22 | Drobnosti (viz konec) | | < 0,1 mil. každá | |

Součet oprav **jen ve prospěch investora** (8 + 10 + 15) dává B2 real **1,37 mil. (6,2 %)**, B2h 1,99 mil. (8,9 %), C2 2,31 mil. (7,1 %). Realistická kombinace oprav (2 [−5 %], 5, 7, 8, 10, 15) dává B2 **−0,09 mil. (−0,4 %), max. cena 3,10 mil.**; B2h 0,59 mil. (2,7 %); C2 0,48 mil. (1,5 %).

---

## Podrobně

### 1. D: prodej po 10 letech jen jako celek se slevou 30 % (výpočet / chybí)
- **Kde:** model.py:393–394 (`hodnota0 … * (1 - portfolio_sleva)`), 429–432.
- **Co je špatně:** po 10 letech je prodej FO osvobozen od daně z příjmů (§ 4 odst. 1 písm. b) ZDP) a dávno mimo 23měsíční lhůtu DPH. Rozdělení na jednotky stojí 70 tis. Kč. Model přesto počítá jen prodej celku se slevou 30 % (tj. 22,1 mil. při konci). Prodej po bytech (nájmy na dobu určitou, srážka 12 % za opotřebení po 10 letech, podle rozdílu „udržovaný × po rekonstrukci“ v ceny-byty-realizovane.md:102–107) dává 27,7 mil.
- **Dopad:** D10 real 3,24 → 8,47 mil., ROI 12 % → 32 %, IRR 3,1 % → 6,7 %; max. cena D 6,67 → 10,96 mil. Se všemi opravami D (č. 3, 13, 19) **8,91 mil., ROI 34 %, IRR 7,1 %**. Citlivé na růst cen: při 1,5 % ročně ROI 19 %, při 0 % jen 6 %.
- **Oprava:** výstup D = max(prodej celku, součet bytů × opotřebení − rozdělení − náklady prodeje po bytech). Kritérium „20 % z nákladů“ u D nahradit IRR (20 % za 11 let je ~1,7 % ročně, s flipem nesrovnatelné).
- **Navíc:** samotná hodnota celku 22,1 mil. odpovídá hrubému výnosu jen ~5,1 % z nájmu 1,13 mil./rok, podklad požaduje 6,3 % (ceny-domy-2.md:186) → při výnosovém ocenění by celek měl jen ~18 mil. Prodej celku tedy model u D spíš nadhodnocuje (viz č. 12), prodej po bytech podhodnocuje tím, že chybí.

### 2. Střední rozsah prací, ale ceny „po kompletní rekonstrukci domu“ (ceny / nesrovnatelné srovnání)
- **Kde:** model.py:22 (komentář „byt po kompletní rekonstrukci domu“), 23–24; rozsah model.py:38–41 a postup.md:20.
- **Co je špatně:** střední úroveň vynechává ETICS, sanaci vlhkosti a okna mimo byty. Srovnávací prodeje „po rekonstrukci“ jsou ale v revitalizovaných (zateplených) domech nebo mají garáž (Nálepky, Antuškova, Vlašimská S7). Jediný srovnatelný částečně opravený byt bez zateplení (Bezručova, třída G) se prodal za 75 tis. Kč/m². Plísně v A a C (stav.md:51) jsou typicky z tepelných mostů – bez zateplení a sanace se vrátí. PENB vyjde nízký a kupující to uvidí v inzerátu.
- **Dopad:** −5 % cen → B2 0,77 → 0,12 mil. Varianta „kompletní“ při stejných cenách: B2 −1,86 mil. Platí tedy jedno nebo druhé.
- **Oprava:** buď cenová srážka 3–8 % za nezateplený dům se třídou PENB E–G, nebo kompletní rozsah. Druhá možnost zároveň zvýší podíl nákladů nad 30 %.

### 3. D: daň z nájmu paušálem (daně)
- **Kde:** model.py:421 `dn = 0.15 * 0.7 * hruby`.
- **Co je špatně:** u § 9 lze místo paušálu uplatnit skutečné výdaje: odpisy budovy včetně technického zhodnocení (~17 mil. v odpisové skupině 5, ~0,58 mil. ročně), úroky (~0,6 mil. ročně) a údržbu. Základ daně bude 10 let ≈ 0. Odpisy osvobození po 10 letech neruší (dane-financovani.md:25, 57).
- **Dopad:** D10 +1,02 mil.; D5 +0,47 mil.
- **Oprava:** u D daň § 9 = max(0; nájem − provoz − úroky − odpisy), případně lepší z paušálu a skutečných výdajů.

### 4. Test podstatné změny 30 % (DPH § 56 od 7/2025)
- **Kde:** model.py:204 (`stavba_bez_dph`), 255–258.
- **Co je špatně:** (a) zákon měří náklady proti **základu daně** dodání (dane-financovani.md:66), tj. při zdanitelném prodeji proti ceně ÷ 1,12. Model dělí tržbou s DPH, takže podíl podhodnocuje o 12 %. (b) Do nákladů patří všechny skutečně vynaložené náklady (i spotřebovaná rezerva a `rizika_navic`). Model je vynechává. (c) GFŘ chce test **po jednotkách** (model: souhrnně, viz `ponytail:` komentář).
- **Ověřil jsem po jednotkách (B2 real, stav.md kap. 8, společné náklady podle ploch):** podíl nákladů bez DPH k ceně A1 0,337, A2 0,337, B 0,309, C 0,344, D 0,333. K základu bez DPH 0,35–0,39, se spotřebovanou rezervou 0,36–0,44. **V realistickém scénáři je tedy závěr „podstatná změna“ správný a robustní.**
- **Kde chyba škodí:** model má „útes“ už při podílu 0,30. B real při cenách +10 % spadne na 0,296 → osvobozeno → citlivost B „+10 %“ 2,62 mil., z toho ~1 mil. jen artefakt. Při stavba −9 % skočí B2 z 1,30 na 2,27 mil. V opt jsou A2/B/B2 „osvobozeno“ (podíl 0,13–0,17), ale opt počítá náklady na menší plochu (č. 14). Lhůta 23 měsíců je v modelu správně (všechny prodeje B/B2 do 7 měsíců po dokončení → zdanitelné).
- **Oprava:** `podil = (náklady_bez_DPH + rezerva/1,12 + rizika/1,12) / (tržby/1,12 if zdanitelné else tržby)`, test po jednotkách (přímé + společné podle ploch). U hranice 0,28–0,40 hlásit „nejisté“, ne přepínat.
- **K registraci:** předpoklad real/opt (dobrovolná registrace před stavbou, odpočet) je v pořádku. Pro plátce platí u stavebních prací přenesená daňová povinnost (§ 92e) → DPH na vstupu se nepředfinancuje. Model ji vrací až v posledním měsíci (cash-flow, < 0,1 mil.). V pes (bez odpočtu) chybí, že neplátce se stane plátcem až **dnem po** překročení 2 536 500 Kč (první byt tak jde bez DPH) a že má nárok na odpočet podle § 79 u majetku pořízeného 12 měsíců před registrací. Pes je tím přehnaně pesimistický o ~0,5–1 mil.

### 5. Lokalita – prémie za nádraží a chybějící parkování (ceny)
- **Kde:** model.py:25 (`lokalita` 0,92/0,98/1,05) z lokalita.md:154–160 (−2 % = +4 % nádraží −2 % silnice −3 % areál −1 % obchody).
- **Co je špatně:** ceny-byty-realizovane.md:76 a 146 výslovně říká „Poloha u nádraží: žádná prémie v datech, nepočítat“. Lokalita.md nemá složku za **nemožnost parkovat** (pozemek = půdorys domu, srovnávací prodeje Antuškova a Nálepky mají garáž).
- **Dopad:** lokalita 0,94 → B2 −0,53 mil.; 0,92 → −0,82 mil. (B2 ≈ 0).
- **Oprava:** real 0,93–0,94 (bez +4 % za nádraží, −1 až −3 % za parkování).

### 6. B2h – zdanění nájmu (daně)
- **Kde:** model.py:237–244 (nájem v `rev`), 251 a 350 (vše v režimu s7).
- **Co je špatně:** 1,47 mil. čistého nájmu se daní jako § 7 se sociálním a zdravotním (na okraji 23 % + 16 % + 6,75 %). Nájem je v principu § 9 bez odvodů (dane-financovani.md:57). Zda půjde u bytů držených k prodeji o § 9, nebo o § 7, je otázka pro poradce.
- **Dopad:** B2h +0,44 mil. (§ 9 paušál 30 %), opatrně +0,2 mil.
- **Oprava:** nájem zdanit zvlášť podle § 9, prodej podle § 7.

### 7. Dvojí započtení prémie kk (ceny)
- **Kde:** model.py:26 a 157.
- **Co je špatně:** `m2_maly` 98 tis. je odvozen ze vzorku ≤ 60 m², kde jsou téměř jen kk byty (S6 2+kk, R2 3+kk, S11/R1/S3/S14 2+kk, prodeje 2+kk a 1+kk; ceny-byty-realizovane.md:101–103, 54–59). Prémie +3 % je tak podruhé. Naopak v B jsou 2+1 a 1+1 oceněny jako kk (ve městě 2+1 85,9 tis. vs 2+kk 103 tis., dispozice-zmeny.md:156–157).
- **Dopad:** B2 −0,38 mil. (B2h −0,37, C2 −0,33). U B by srážka za „+1“ byla −0,3 až −0,5 mil.
- **Oprava:** základ malých bytů brát jako kk; v B pro 2+1/1+1 srážka −3 až −5 %, v B2 `kk_premie` 0.

### 8. Rezerva vs. rizika vs. režie (náklady)
- **Kde:** model.py:42 a 216 (rezerva 15 % ze stavby i služeb, v real celá utracena); stav.md:138 (režie 8/12/18 % zahrnuje „nepředvídané drobnosti“); stav.md:91–101 (rizika s pravděpodobnostmi).
- **Co je špatně:** nejde o přímé dvojí započtení, ale realistický scénář má být očekávaná hodnota. Očekávaná hodnota rizik relevantních pro střední rozsah (R1, R2, R3, R4, R6, R7, R8, R9 × pravděpodobnost) je ≈ 0,78 mil. Model počítá 1,36 mil. a k tomu režii 12 % s rezervou na drobnosti. Rezerva 15 % podle zadání patří do VK (likvidita), ne celá do nákladů reálného scénáře.
- **Dopad:** rezerva 8,5 % → B2 +0,36 mil., C2 +0,57 mil.
- **Oprava:** real = očekávaná hodnota rizik (~8–9 %), pes = 15 % + `rizika_navic`, VK počítat s celými 15 %.

### 9. Přístup (SPÚ) vs. čerpání úvěru (časová osa, financování)
- **Kde:** model.py:58–59 (přístup za 9 měsíců), 167 (úvěr na koupi v t=0), 218–219.
- **Co je špatně:** podle dane-financovani.md:157–158 a katastr.md (Shrnutí) banka bez zapsané služebnosti nefinancuje nebo silně snižuje zástavní hodnotu. Model čerpá 5,83 mil. hned při koupi.
- **Dopad:** překlenovací/nebankovní úvěr 10–14 % na 9 měsíců → −0,25 až −0,4 mil. Alternativou je +5,8 mil. VK v t=0 (zisk mírně vyšší, ale celkové VK ~12 mil.).
- **Oprava:** do vyřešení přístupu úvěr za sazbu 11 % (pes z dane-financovani.md:215), nebo VK. Do podmínek nabídky ve VŘ chtít služebnost od ČD/SPÚ.

### 10. Chybějící odpočet DPH (náklady, DPH)
- **Kde:** model.py:205 (`dph_in_rek` jen stavba, služby a změny B2), 260–262.
- **Co je špatně:** registrovaný plátce si odpočte i DPH z rezervy (12 %), z provize RK (21 % – v modelu je provize včetně DPH), z advokáta, geodeta a PENB.
- **Dopad:** B2 +0,23 mil., B +0,21 mil., C2 +0,32 mil.
- **Oprava:** odpočet ze všech zdanitelných vstupů po registraci.

### 11. E – proplacení projektu (výpočet)
- **Kde:** model.py:273 `… + x("permit_podil") * rlv + soft`.
- **Co je špatně:** kupec proplatí 100 % utracených nákladů na projekt (0,72 mil. real) i v pes, kde za povolení nezaplatí nic (`permit_podil` 0, reziduál 0). Reziduál už úsporu kupce na projektu obsahuje.
- **Dopad:** E real −0,41 mil., pes −0,90 mil., opt −0,11; max. cena E real 5,48 → 5,18 mil.
- **Oprava:** `soft * permit_podil`, nebo projekt nepřičítat a do reziduálu dát úsporu kupce.

### 12. A2/D – hodnota hotového domu nad podkladem (ceny, nesrovnatelné)
- **Kde:** model.py:223 (A2 = součet bytů × 0,7), 393–394 (D `hodnota0`).
- **Co je špatně:** A2 real 15,94 mil. při **středním** rozsahu. Podklad pro celý dům dává 14,25 mil. při **kompletní** a 11,7 mil. při standardní rekonstrukci (ceny-domy-2.md:154–158).
- **Dopad:** A2 −1,7 až −4,2 mil. (závěr se nemění, A2 je ztrátová). Totéž číslo vstupuje do D (výstup celku i limit úvěru).
- **Oprava:** A2/D celek brát z ceny-domy-2 (b)/(c), případně z výnosu 6,3 %.

### 13. Nájemné (ceny)
- **Kde:** model.py:88 (295 = medián nabídek malých bytů), 240 a 418 (bez lokality).
- **Co je špatně:** podklad pro celý dům s velkými byty (A 95 m²) navrhuje 270 Kč/m² (ceny-domy-2.md:106, 188). Lokalita (silnice, areál) se na nájem neuplatní a nabídkové nájmy nejsou kráceny.
- **Dopad:** D10 −0,63 mil., B2h −0,07 mil.
- **Oprava:** real 270 (pes 245, opt 293), případně × lokalita.

### 14. Opt scénář – plocha nákladů ≠ plocha tržeb (výpočet)
- **Kde:** model.py:27 (`plocha_koef` opt 1,10 → 285 m² bytů) × stav.md:138–140 (opt náklady na 205 m² bytů / 300 m² celku).
- **Co je špatně:** opt prodává o 39 % víc bytové plochy, než opraví. Opt výsledky a max. ceny opt (B2 18,16, B 16,58 mil.) jsou výrazně nadsazené.
- **Dopad:** při konzistentní ploše B2 opt 13,17 → 6,28 mil., max. cena B2 opt 18,16 → 11,46 mil.
- **Oprava:** náklady opt škálovat podle plochy, nebo `plocha_koef` opt vázat na plochu ze stav.md.

### 15. LTV a úvěr na stavbu (financování, ČNB)
- **Kde:** model.py:303–304 `cap = ltv * max(gdv, P)`; postup.md:23.
- **Co je špatně:** banka zastavuje dům jako celek a oceňuje ho (s portfoliovou slevou), ne jako součet cen bytů. U developerského/rekonstrukčního úvěru navíc platí LTC 60–70 % (dane-financovani.md:152). Model tak financuje B2 do 14,6 mil. (~78 % nákladů). DTI 7 (dane-financovani.md:147) při úvěru 12–14,6 mil. znamená čistý příjem ≥ 1,7–2,1 mil. ročně. Zda doporučení ČNB dopadá na podnikatelský úvěr FO, je nejasné. Pozor: VK v modelu (6,4 mil.) už je nad parametrem „30 % kupní ceny + rezerva“ (3,9 mil., postup.md:6).
- **Dopad:** zisk B2 +0,08 mil. (méně úroků), ale **VK 6,43 → 8,69 mil.**, IRR 9,3 → 8,7 %. Úvěr 14,6 → 12,0 mil.
- **Oprava:** `cap = ltv × hodnota celku po dokončení` (jako u D), případně LTC.

### 16. Přízemí A1/A2 (ceny)
- **Kde:** model.py:98. A1 a A2 jsou v 1. NP, 19 m od silnice II/110, vedle dílny a kotelny.
- **Dopad:** −5 % na A1/A2 ≈ −0,25 mil. čistého.

### 17. Nebytové prostory 1. NP (chybí)
- **Kde:** model.py:97–99 – 86 m² dílny, skladů a kotelny se v B/B2 neprodá ani nepřičlení. Podklad dispozice-zmeny.md:116–132 počítá s novým bytem (+2,9 mil. hrubého přínosu, náklady 1,44 mil., +8 měsíců).
- **Dopad:** po DPH 12 %, rezervě, provizi, dani a čase ≈ +0,5–0,8 mil. (nebo menší částka za prodej jako sklad/garáž). Rozhodnutí nemění.

### 18. Vítězná cena ve VŘ
- ceny-domy-2.md:169: realisticky +8 % (9,0 mil.). B2 při 9,0 mil. 0,31 mil.; B2h 1,06; D 2,57. Nový výstup modelu „zisk@9,0“ to pokrývá – doporučuji ho dát do hlavní tabulky.

### 19. D – úroky před dokončením (výpočet)
- **Kde:** model.py:395–410. Smyčka přes `cost` nejdřív načte celé čerpání, pak se v měsících 1…t_start počítá úrok z **konečné** výše úvěru (včetně stavby čerpané až v měsících 3–12).
- **Dopad:** D10 +0,15 mil. Oprava: úrok ze zůstatku podle měsíce čerpání. U D chybí i poplatek za zpracování (−0,05 mil.).

### 20.–21. Časová osa B2/B2h
- **Č. 20:** model.py:194 – `t_b2_navic` (4 měsíce povolení dělení A) posouvá start celé stavby. Podle dispozice-zmeny.md:183 jde B, C, D a společné části dělat souběžně → +0,1 mil.
- **Č. 21:** model.py:237–244 – B2h čeká 24 měsíců od `t_start` (= dokončení + rozdělení). § 56: osvobozeno po konci 23. kalendářního měsíce po měsíci dokončení → stačí prodávat od t_hotovo + 24. Úspora ~2 měsíce (+0,05–0,1 mil.).

### 22. Drobnosti (< 0,1 mil. každá)
- model.py:203–205: `b2_zmeny` bez inflace stavby (−0,03 mil.).
- model.py:285–286: `drzeni_mes` (energie, zabezpečení) běží i během stavby, kdy je to v zařízení staveniště v režii (~0,05 mil. dvakrát).
- b2_zmeny obsahuje projekt a „prohlášení vlastníka za +1 jednotku“ (dispozice-zmeny.md:106, 108). Částečně se to kryje se službami 9,6 % a s `rozdeleni` (~0,05 mil.).
- ROI = čistý / náklady, kde náklady obsahují i DPH na výstupu (2,6 mil.). Na čisté tržbě je ROI B2 3,6 % místo 3,3 %, max. cena o ~0,2 mil. výš. Definici sjednotit.
- C (model.py:258): `nast` vynutí DPH i u stávajících 5 bytů. V opt tak zdaní i byty, které by v B2 opt byly osvobozené (C opt podhodnoceno). V real bez vlivu.
- D citlivost „zpoždění“ (model.py:429) je skoro nulová, protože hodnota roste od t=0 a 120 měsíců nájmu se jen posune.
- Citlivost „rekonstrukce +20 %“ se v A0/E neprojeví (správně). `stavba_mult` se ale neprojeví na `rizika_navic`, `parkovani` ani `pristup`.
- `kosmetika` (A1) nemá žádný vliv na cenu domu (jen `marketing_uplift` 3 % za balíček), takže A1 je z konstrukce horší než A0. `dum_asis` real = vyvolávací cena ČD (ceny-domy-2.md:136 – kruhová kotva).
- dane-financovani.md:40 tvrdí, že pojistné OSVČ je daňově uznatelné s posunem. Pojistné OSVČ za sebe uznatelné **není**. Model to nepoužívá, opravit jen v podkladu. Pokud § 7 bude hlavní činností (není zaměstnání), chybí minimální zálohy na pojistné v ztrátovém roce 2027 (~0,1–0,2 mil.).
- ÚP: výklad v modelu sedí (BI: 2 NP + podkroví nebo ustoupené podlaží → C1, C2 ano, C3 ne; parkování 1/120 m² podle vyhl. 146/2024). Riziko: ÚP s. 84 chce parkování „na vlastním pozemku“. U dělení A (B2, změna stavby, +1 byt) to úřad může vyžadovat i bez přírůstku plochy (pozemek 239 m² = půdorys). V modelu na to v B2 není žádná položka. C2: povolení (10 měsíců real) padá na přechod stavebních úřadů 1. 1. 2028 (uzemni-plan.md:92).
- § 10 × § 7 a úroky v § 10 (model.py:180, 251, 350): v souladu s podkladem a konzervativní. Pro B2 real by § 10 (bez úroků jako výdaje) dal daň 0,40 místo 0,47 mil. → rozdíl jen +0,07 mil.

---

## Je závěr robustní?

Pro flipové varianty (B, B2, B2h, C1/C2) je závěr robustní. Na 20 % by bylo potřeba o 18–21 % vyšší realizované ceny bytů (B2 1,18×, B2h 1,21×, C2 1,28×, tj. zhruba úroveň nabídek, ne prodejů), nebo o ~30 % levnější stavbu. I když sečtu jen opravy ve prospěch investora, vyjde B2 6 %, B2h 9 % a C2 7 %. Realistická kombinace všech oprav stáhne B2 k nule (max. cena ~3,1 mil.). Jediné místo, kde se závěr formálně otočí, je D: prodej po bytech po 10 letech a daň z nájmu se skutečnými výdaji dávají ROI 32–34 % (max. cena ~11 mil.). Je to ale ~7 % IRR ročně za 11 let a stojí to na růstu cen 3 % ročně (při 1,5 % je ROI 19 %), takže krátkodobý cíl „20 % za projekt“ to nesplňuje. U D je potřeba posuzovat IRR, ne 20 % z nákladů.
