# DPH: test 30 % po jednotkách (5. 11. 2026)

Výpočet: `model.py` V1 real (kombinace firma + řemeslníci jako na webu), dílčí položky z `report.py` (`STAV`), skript ve scratchpadu sezení (`dph/test.py`). Čísla jsou v mil. Kč.

## Pravidlo
- § 56 odst. 5 ZDPH: podstatná změna nastane, když náklady na změnu bez DPH, které nese prodávající, „přesáhnou 30 % základu daně při bezprostředně následujícím dodání“. Odst. 7: jednotka je samostatná vybraná nemovitá věc, takže **test se dělá za každý prodávaný byt zvlášť**. To plyne ze zákona.
- Jak rozdělit společné náklady na byty, zákon neříká. Informace GFŘ č. j. 1127/26/7100-30116-051722 (podle `podklady/dane-financovani.md` ř. 66): **přímé náklady bytu přímo, společné podle podlahových ploch**, včetně svépomoci, bez úroků. Stejný klíč používá prohlášení vlastníka pro podíly na společných částech (§ 1161 OZ), takže je konzistentní.
- Do testu jde stavba, projekt a statika bez DPH (8,13 mil.). Koupě, pozemek, úroky, elektrická přípojka a parkovací stání ne.

## Rozdělení nákladů
- **Přímo N1 a N2:** celá přestavba nebytové části, 2,17 mil., napůl.
- **Přímo A–D:** 2,09 mil.
  - Elektro v bytech: podle ploch A–D.
  - Kuchyně, koupelny B, C, D: třetinou. Byt A: vlastní obnova koupelny a kuchyně.
  - Okna: A, B, D podle ploch; C jen seřízení.
  - Vinyl: A 40 m², B 67 m², C 62 m². Stěrka 70 % B / 30 % C. Parkety D. Plísně B a C. Vyklizení hlavně B.
  - Vstupní dveře: čtvrtinou.
  - Topení v bytech (ventily, proplach): podle ploch A–D.
- **Společné podle ploch všech 6 bytů (344 m²):** 3,88 mil.: střecha, tepelné čerpadlo a kotelna, rozvody domu, trhliny, společné prostory, projekt a statik, statické zajištění 1,5 mil.

## Výsledek
| Byt | m² | Cena s DPH | Základ (÷ 1,12) | Přímé | Společné | Celkem | Test | Režim |
|---|---:|---:|---:|---:|---:|---:|---:|---|
| A 4+1 | 80 | 6,33 | 5,65 | 0,53 | 0,90 | 1,43 | **25,3 %** | osvobozeno |
| B 2+1 | 67 | 5,70 | 5,09 | 0,63 | 0,76 | 1,38 | **27,1 %** | osvobozeno |
| C 3+1 | 75 | 6,38 | 5,70 | 0,53 | 0,85 | 1,38 | **24,1 %** | osvobozeno |
| D 1+1 | 42 | 3,91 | 3,49 | 0,41 | 0,47 | 0,88 | **25,2 %** | osvobozeno |
| N1 2+kk | 40 | 3,29 | 2,94 | 1,08 | 0,45 | 1,53 | 52,3 % | DPH 12 % |
| N2 2+kk | 40 | 3,29 | 2,94 | 1,08 | 0,45 | 1,53 | 52,3 % | DPH 12 % |
| Dům souhrnně | 344 | 28,89 | 25,80 | | | 8,13 | 31,5 % | (model dnes: vše 12 %) |

Ceny jsou z modelu včetně růstu 3 %/rok do prodeje (× 1,053). Do základu dělím 1,12 (konzervativně); u osvobozeného prodeje je základem celá cena a procenta by byla o ~3 p. b. nižší.

Kontrola krajnosti: kdyby se **všechny** společné náklady daly jen na A–D, vyjde A 30,1 %, B 31,6 %, C 28,6 %, D 29,3 % (s celou cenou v základu 26–28 %). Klíč podle ploch včetně N1 a N2 je proto podstatný.

## Čisté DPH
- DPH z prodeje N1 + N2: 2 × 3,29 × 12/112 = **0,70**
- Odpočet přímých nákladů N1, N2: ~0,27
- Odpočet ze společných nákladů krácený koeficientem § 76 (zdanitelné / všechna plnění = 5,87 / (5,87 + 22,32) ≈ 21 %): ~0,10
- Z nákladů A–D se nic neodečítá.
- **Čisté DPH ≈ 0,34 místo 2,10 → o ~1,76 mil. méně.** Po dani z příjmů (s. r. o. a dividenda, v modelu efektivně ~39 %) je čistý zisk vyšší o **~1,1 mil.** (V1 real 4,97 → ~6,0 mil.).

## Jak blízko je hranice
- Nejtěsnější je **byt B**: rezerva 0,15 mil. vlastních nákladů bez DPH.
- B by přešel přes 30 %, když:
  - společné náklady vzrostou o ~0,75 mil. bez DPH (např. statika při aktivním sedání +1–2 mil. → B zdaněný),
  - nebo cena B klesne o ~10 %,
  - nebo přímé náklady B vzrostou o 0,15 mil.
- Když přejde jen B, úspora klesne asi o 0,5 mil., nezmizí celá.
- A, C, D mají rezervu 0,26–0,34 mil. vlastních nákladů.

## Jak to dělat v praxi
1. **Faktury po bytech:** po dodavatelích chtít rozpis podle bytů (A, B, C, D, N1, N2, společné). Svépomoc a nákupy materiálu evidovat stejně. Bez toho se test těžko obhájí.
2. **Klíč pro společné náklady = podlahové plochy jednotek**, stejné jako podíly v prohlášení vlastníka. Plochy bytů (A 80, B 67, C 75, D 42, N1 40, N2 40) mít doložené od geodeta.
3. Hlídat průběžně podíl u bytu B, hlavně až bude jasný rozsah statiky.
4. **Daňový poradce, nejlépe závazné posouzení FÚ před stavbou:** potvrdit klíč, započtení statiky, svépomoci a základ (s DPH / bez), koeficient § 76 a úpravu odpočtu.
5. Registrace k DPH zůstává nutná kvůli N1 a N2.

## Neověřeno
- Informaci GFŘ 1127/26 jsem nečetl v originále (je převzatá z podkladů).
- Je nejisté, jestli se statické zajištění (oprava, ne změna obývání) do testu vůbec počítá. Když ne, rezervy se zvětší.
- Rozdělení oken mezi A, B a D (počet kusů po bytech) je podle ploch, ne podle skutečných kusů.
