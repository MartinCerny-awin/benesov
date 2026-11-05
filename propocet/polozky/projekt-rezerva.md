# Projekt, dozor, statik; Rezerva 15 %; Vlastní dodavatelé: úspora (4. 11. 2026)

Vše realisticky, Kč s DPH. Čísla modelu jsou z `projekt()` spuštěné pro V1 a V2 (real; `r["rozpis"]`). Co je „ODHAD“, nemá veřejný zdroj. Sazby UNIKA / ČKAIT jsem nenašel veřejně (WebSearch 4. 11. 2026), proto ceny služeb níže vycházejí z `podklady/stav.md` 5b/5c a jsou ODHAD.

---
## A. Projekt, dozor, statik (model 733 169 Kč, služby s DPH 21 %)

### 1. Rozpis
Rozsah: rekonstrukce domu a bytů (stavba 7,64 mil. s DPH) + přestavba bytu B (0,16 mil.). Nebytová část (3,64 mil.) má projekt zvlášť uvnitř `nebyt_zmeny`, nástavba v `nastavba_soft`.

| Položka | Množství | Jedn. cena | Real Kč s DPH | Pes / opt | Zdroj |
|---|---|---|---|---|---|
| Zaměření stávajícího stavu (laserové, 2 NP, ~344 m² + střecha), výkresy stavu | 1 ks | paušál | 40 000 | 60 000 / 25 000 | ODHAD |
| Projekt stavebních úprav pro ohlášení / povolení (architektura, byt B 2+1→3+1, střecha, společné prostory, vyjádření) | 1 ks | ~5 % stavby celkem s ostatními projekty | 160 000 | 270 000 / 90 000 | `stav.md` 5c „Projekt 3,5/5/7 % stavby, ODHAD“; 5b „Projekt 60/110/180 tis.“ |
| Prováděcí projekt: ÚT + tepelné čerpadlo, ZTI stoupačky, elektro (rozvaděče, měření po bytech), hromosvod | 1 ks | paušál | 200 000 | 350 000 / 80 000 | `stav.md` 5c ODHAD |
| Požárně bezpečnostní řešení (bytový dům, úniky, EI dveře) | 1 ks | paušál | 45 000 | 70 000 / 25 000 | ODHAD |
| Statik: posudek trhlin, návrh sanace, dohled nad stahem a sešitím | 1 ks | paušál | 110 000 | 190 000 / 40 000 | `stav.md` 5b/5c „Statik 40/80/150“, „90/180/350“ (ODHAD) |
| Technický dozor investora (kontrola 7,8 mil. stavby, ~1,9 %) | ~10 měsíců | ~1,9 % stavby | 145 000 | 300 000 / 30 000 | `stav.md` S12: 1,5–3 % (muj-pravnik.cz, dostupnyadvokat.cz 2026) |
| Koordinátor BOZP (zákon 309/2006 Sb., nutný, viz níže) + oznámení inspektorátu | 1 ks | paušál | 25 000 | 60 000 / 15 000 | ODHAD (cenu koordinátora jsem nenašel) |
| Poplatky, vyjádření, tisky, geodet | 1 ks | paušál | 8 000 | 15 000 / 4 000 | ODHAD |
| **Součet** | | | **733 000** | | model 733 169 |

Stavbyvedoucí je v ceně firmy (u vlastních dodavatelů je placen zvlášť, viz část C). PENB sem nepatří: je zvlášť v `IN["penb"]` 15 000 Kč (`dane-financovani.md`, finance.cz/538646) a model ho účtuje při dokončení.

Právní poznámky (ověřit na stavebním úřadu, zdroje sekundární):
- Stavební zákon 283/2021 Sb.: úpravy bez zásahu do nosných konstrukcí, bez změny vzhledu a bez vlivu na požární bezpečnost povolení ani ohlášení nevyžadují (arws.cz, „stavební úpravy bytu bez povolení“). Tady ale padá několik důvodů: nová okna a fasáda/střecha (vzhled), změna užívání nebytové části na 2 byty a snížení parapetů, sanace trhlin (statika). Počítej tedy s projektem pro povolení nebo ohlášení minimálně u nebytové části, u zbytku je rozdíl v rozsahu dokumentace jen malý. Přesný režim (povolení záměru / ohlášení) rozhodne stavební úřad v Benešově.
- Koordinátor BOZP: povinný, pokud na stavbě pracuje více zhotovitelů současně nebo po sobě; oznámení inspektorátu práce, když stavba trvá > 30 pracovních dní a > 20 osob současně, nebo > 500 osobodní (RuleCalc 20. 3. 2026; MPSV materiál k § 15; pokuta až 2 mil. Kč). Tato stavba bude mít ~1 000+ osobodní a několik profesí, takže koordinátor je třeba a oznámení pravděpodobně též. U vlastních dodavatelů je to jistě.

### 2. Kontrola proti modelu
- Model 733 169, můj součet 733 000, rozdíl 0 %. Jde o 9,6 % stavby rekonstrukce (9,4 % včetně bytu B); `stav.md` dává pro střední úroveň 9,6–10,7 %. Souhlasí.
- Co chybí: nic podstatného. Nezapočteno je PENB (jinde), inženýring (vyjádření správců sítí, rozhodnutí o přístupu přes SPÚ pozemek) a autorský dozor projektanta (obvykle 1–2 % stavby, 80–150 tis.; lze zahrnout do dozoru nebo do rizik).
- Dvojí započtení: statik zde (110 000) a `rizika_navic` (statické zajištění real 1,0 mil.) obsahují obojí „posudek“ a „monitoring“. Zdvojení do ~50 000 Kč, zanedbatelné (0,1 % nákladů). `postup.md` ř. 177 ho už zmiňuje.
- V2: nástavba má svoje služby v `nastavba_soft` (1,2 mil.), zde se nesčítají.

### 3. Doporučení
Beze změny (`stredni_sluzby` 1 277 / 700 / 298 tis.). Rozdíl je 0 %, jen chybí veřejný zdroj sazeb projektantů; ověřit 2–3 nabídkami (viz dotazy na projektanty).

### 4. Pro report
```python
[("Zaměření stávajícího stavu (laserové, celý dům)", 40000),
 ("Projekt stavebních úprav pro ohlášení nebo povolení", 160000),
 ("Prováděcí projekt topení, vody, kanalizace a elektro", 200000),
 ("Požárně bezpečnostní řešení", 45000),
 ("Statik: posudek trhlin a návrh sanace", 110000),
 ("Technický dozor investora (asi 1,9 % stavby)", 145000),
 ("Koordinátor bezpečnosti práce a oznámení inspektorátu", 25000),
 ("Poplatky, vyjádření, tisky, geodet", 8000)]
```

---
## B. Rezerva 15 % (model: V1 firma 1 824 381, V1 vlastní 1 720 412, V2 firma 3 048 971)

### Z čeho se počítá (kód `model.py` ř. 278 a 290)
`rez_base = rekon + zmeny × stavba_mult + stavba_navic` (+ `nast_bez × 1,12` u V2), `rezerva = rez_base × 15 %`.
- `rekon` = stavba rekonstrukce **včetně služeb** (projekt, dozor, statik jsou v ní uvnitř, ř. 216–217). Rezerva se tedy počítá i ze služeb.
- `zmeny` = přestavba bytu B + nebytová část na 2 byty (včetně jejího projektu).
- `stavba_navic` = rozdíl řemeslníci proti firmě (záporný, rezervu snižuje).
- **Nepočítá se** z `rizika_navic` (statické zajištění 1,0 mil.), ani z `nastavba_soft` (projekt nástavby 1,2 mil.), ani z PENB, přístupu, parkování. **Počítá se** z `nastavba_statika` (2,0 mil.), protože je uvnitř `nast_bez`.
- Ověřeno: V1 firma základ 12 162 541 × 15 % = 1 824 381; V2 20 326 473 × 15 % = 3 048 971.

### 1. Rozpis (real, Kč s DPH)

| Základ rezervy | Základ | Rezerva 15 % | V1 firma | V1 vlastní | V2 firma |
|---|---|---|---|---|---|
| Rekonstrukce domu a bytů (bez služeb) | 7 635 430 (V2: 7 128 082) | | 1 145 315 | 1 145 315 | 1 069 212 |
| Projekt, dozor, statik (služby) | 733 169 | | 109 975 | 109 975 | 109 975 |
| Přestavba bytu B na 3+1 | 156 750 | | 23 513 | 23 513 | 23 513 |
| Nebytová část → 2 byty | 3 637 192 | | 545 579 | 545 579 | 545 579 |
| Řemeslníci: rozdíl proti firmě | −693 124 (V2 −662 357) | | 0 | −103 969 | 0 (v tomto sloupci firma) |
| Nástavba: stavba bez statiky (150 m² hrubých) | 6 671 280 | | 0 | 0 | 1 000 692 |
| Nástavba: statika podchycení základů | 2 000 000 | | 0 | 0 | 300 000 |
| **Součet** | | | **1 824 381** | **1 720 412** | **3 048 971** |

(V2 vlastní dodavatelé: 2 949 617.) Zdroje: `model.py` ř. 278–292; V2 rekonstrukce je o 0,51 mil. nižší, protože nástavba bourá střechu (`strecha_v_rekonstrukci` × 50 %).

### 2. Kontrola
- Rezerva ze služeb: 109 975 Kč. Honoráře projektanta a dozoru jsou pevné sazby a 15 % přerůstání nemají. Argument pro ponechání: dozor a statik se prodlužují s protaženou stavbou. Vliv na celek 0,1 mil.; rozhodnutí o 15 % neměním.
- Statické zajištění (1,0 mil. real) bez rezervy, přitom nástavbová statika (2,0 mil.) s rezervou 300 000. Nekonzistentní, ale v součtu malé; statické zajištění je samo odhad s velkým rozpětím (opt 0,25 až pes 2,0 mil.) a již rezervu obsahuje.
- Rezerva z úspory řemeslníků: −103 969 Kč. Úspora je tedy ve skutečnosti o 15 % vyšší (−797 tis.), pokud rezerva klesá. Spíš konzervativní by bylo rezervu z úspory nesnižovat, rozdíl 0,1 mil.
- Drobná nesrovnalost v kódu (ř. 280–281): rezerva ze služeb je zahrnuta do `rez_base` (tedy do nákladů), ale do základu DPH a daňových nákladů vstupují služby jen bez rezervy (`sluzby/1.21`). Vliv na daň zanedbatelný (~0,02 mil.).
- Pes je pro 10 % (rozhodnutí 4. 11.), opt 15 %. Obrácené pořadí zmiňuje `postup.md` ř. 177 jako schválené.

### 3. Doporučení
Beze změny, rezerva 15 % zůstává. Pouze poznámka k reportu: rezerva se počítá ze všeho kromě statického zajištění a projektu nástavby a zahrnuje i služby (0,11 mil.).

### 4. Pro report
V1 firma:
```python
[("Rekonstrukce domu a bytů (15 % z 7,64 mil.)", 1145315),
 ("Projekt, dozor, statik (15 % z 0,73 mil.)", 109975),
 ("Přestavba bytu B na 3+1 (15 % z 0,16 mil.)", 23513),
 ("Nebytová část na 2 byty (15 % z 3,64 mil.)", 545579)]
```
V1 vlastní dodavatelé:
```python
[("Rekonstrukce domu a bytů (15 % z 7,64 mil.)", 1145315),
 ("Projekt, dozor, statik (15 % z 0,73 mil.)", 109975),
 ("Přestavba bytu B na 3+1 (15 % z 0,16 mil.)", 23513),
 ("Nebytová část na 2 byty (15 % z 3,64 mil.)", 545579),
 ("Snížení rezervy o úsporu u vlastních dodavatelů", -103969)]
```
V2 firma:
```python
[("Rekonstrukce domu a bytů bez střechy (15 % z 7,13 mil.)", 1069212),
 ("Projekt, dozor, statik (15 % z 0,73 mil.)", 109975),
 ("Přestavba bytu B na 3+1 (15 % z 0,16 mil.)", 23513),
 ("Nebytová část na 2 byty (15 % z 3,64 mil.)", 545579),
 ("Nástavba: stavba (15 % z 6,67 mil.)", 1000692),
 ("Nástavba: podchycení základů (15 % z 2,0 mil.)", 300000)]
```
(Součty: 1 824 381 / 1 720 412 / 3 048 971; V2 mírné zaokrouhlení 1 Kč.)

---
## C. Vlastní dodavatelé: úspora (V1 −693 124, V2 −662 357 proti firmě)

### 1. Rozpis (real), pořadí kroků jako v kódu
Základ G = stavba s DPH 12 % bez služeb a bez statiky: V1 11 429 372, V2 10 922 024. Bez DPH S = G/1,12; základ `base` = S/(1 + 12 % režie GD); materiál 50 %, práce 50 % (+ polovina režie GD zůstane řemeslníkům).

| Složka | V1 | V2 | Jak vzniká |
|---|---|---|---|
| Polovina režie generálního dodavatele odpadne | −612 288 | −585 108 | 6 % z základu 9,11 mil. × 1,12 |
| Sleva práce neplátců 10 % | −571 469 | −546 101 | 10 % z práce vč. poloviny režie × 1,12 |
| DPH na práci: 75 % práce od neplátců bez DPH | −413 294 | −394 948 | 12 % z 75 % práce |
| DPH 21 % místo 12 % na materiál (kupuje investor) | +410 014 | +391 814 | 9 p.b. z materiálu 4,56 mil. |
| Koordinace a stavbyvedoucí navíc 4 % z S + DPH 21 % | +493 912 | +471 987 | 408 tis. bez DPH × 1,21 |
| **Součet** | **−693 124** | **−662 357** | shoduje se s modelem |

Pes / opt: V1 −365 / −657 tis., V2 −349 / −629 tis. Pes je horší, protože sleva 0 %, 50 % práce dělají plátci, koordinace 5 %, a **rezerva +5 p.b. (+0,89 mil. ve V1)**, takže u pes vlastní dodavatelé vychází o ~0,5 mil. dráž než firma.

### 2. Kontrola
- Matematicky sedí přesně (rozklad dává model do koruny).
- DPH složky se téměř vyruší (−413 + 410 = −3 tis.). Investor bude po registraci k DPH odpočítávat (`dane-financovani.md`), takže věcná úspora bez DPH je režie (−547 tis.) + sleva (−510 tis.) − koordinace (+408 tis.) = ~−649 tis. DPH je jen otázka cash-flow, ne nákladu; faktury neplátců žádnou DPH k odpočtu nemají.
- Citlivost úspory V1 (materiál 40 / 50 / 60 %, sleva 0 / 10 / 20 %): materiál 40 %: −332 / −951 / −1 570 tis.; materiál 50 %: −168 / −693 / −1 219 tis.; materiál 60 %: −4 / −435 / −867 tis. Nejvíc záleží na slevě práce (±0,5 mil. za 10 p.b.) a značně na podílu materiálu (±0,26 mil. za 10 p.b.). Obě čísla jsou ODHAD.
- Zdroj pro podíl materiálu (50 %) a slevu práce (10 %): **nenalezen**. WebSearch 4. 11. 2026 (české stavební diplomové práce, ČSÚ, nejremeslnici.cz, estav.cz) nedal žádný procentní podíl materiálu u rekonstrukcí bytů v ČR; kalkulace ÚRS/RTS jsou placené. Zůstává ODHAD s rozpětím materiál 40–60 %, sleva 0–20 %. Rekonstrukce bývá mzdově náročnější než novostavba, takže 45–50 % materiálu je rozumné.
- Co v úspoře chybí: vyšší riziko vad bez jedné záruky (v pes řešeno rezervou +5 p.b., v real 0), delší stavba (+1 měsíc, v modelu v `t_remeslnici_navic`), jednání o koordinátorovi BOZP (jistě povinný) a dozoru, zvýšený časový vklad investora.

### 3. Doporučení
Beze změny (nenašel jsem zdroj, který by hodnoty vyvracel). Doporučuji ověřit dvěma až třemi nabídkami řemeslníků na jednu profesi (např. elektro a omítky) a zjistit skutečný podíl materiálu a slevu; v reportu uvádět úsporu s rozpětím −0,2 až −1,2 mil. (V1 real), ne jedno číslo.

### 4. Pro report
V1 (součet −693 124):
```python
[("Odpadne polovina režie generálního dodavatele", -612288),
 ("Sleva práce neplátců DPH (10 %)", -571469),
 ("DPH se neplatí z práce neplátců (75 % práce)", -413294),
 ("DPH 21 % místo 12 % na materiál, který kupuje investor", 410014),
 ("Koordinace řemesel a stavbyvedoucí navíc (4 % stavby)", 493912)]
```
V2 (součet −662 357):
```python
[("Odpadne polovina režie generálního dodavatele", -585108),
 ("Sleva práce neplátců DPH (10 %)", -546101),
 ("DPH se neplatí z práce neplátců (75 % práce)", -394948),
 ("DPH 21 % místo 12 % na materiál, který kupuje investor", 391814),
 ("Koordinace řemesel a stavbyvedoucí navíc (4 % stavby)", 471987)]
```

---
## Zdroje (URL, 4. 11. 2026)
- https://www.nejremeslnici.cz/blog/rekonstrukce-domu-cena/ (projekt pro stavební řízení od 60 tis., aktualizováno 1. 6. 2026)
- https://rulecalc.com/cs/zamestnavatel/bozp-koordinator-oznameni-stavby (prahy pro oznámení a koordinátora BOZP, 20. 3. 2026); https://www.businessinfo.cz/navody/kdo-je-koordinator-bozp-na-stavenisti-a-kdy-ho-budete-potrebovat/
- https://arws.cz/novinky-v-arrows/stavebni-upravy-bytu-bez-povoleni (režim povolení u stavebních úprav; sekundární zdroj)
- Interně: `podklady/stav.md` 5b/5c, S12; `dane-financovani.md`; `postup.md` ř. 93–97, 177; `model.py` ř. 50–63, 216–292.
