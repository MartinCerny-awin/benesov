# Ustupující podlaží (nástavba, jen V2) – rozpis a kontrola

Stav 4. 11. 2026. Model: 9 871 000 Kč s DPH = stavba 6 671 000 (150 m² × 38 000 × 1,045 × 1,12) + statika 2 000 000 + projekt a povolení 1 200 000.
Metoda: nezávislý rozpis zdola, ceny 2026 bez DPH, pak × inflace 1,045 × DPH 1,12 (stejně jako model). Rozpětí pes / opt je u všech řádků ODHAD (zhruba +25 % / −15 %, u statiky viz řádek).

## 1. Rozpis (realisticky, Kč s DPH)

| # | Položka | Množství × cena 2026 bez DPH | Real. s DPH | Pes / opt | Zdroj |
|---|---|---|---:|---|---|
| 1 | Nosná konstrukce: dřevěný rám nebo CLT (stěny, strop nad 2. NP, obálka, fasáda) + demontáž staré střechy | 150 m² × ~14 000 + demontáž 150 m² × 800 = 2,22 mil. | 2 598 000 | 3,2 / 2,2 mil. | ODHAD; kotva: dřevostavba RD 35–50 tis. Kč/m² (rámová), CLT 45–60 tis. (nejremeslnici.cz a další, WebSearch 4. 11. 2026), konstrukce ~1/3 |
| 2 | Střecha nástavby (spádové PIR, fólie, atika, oplechování, vpusti) | 150 m² × 3 600 = 0,54 mil. | 632 000 | 0,86 / 0,40 mil. | `stav.md` 5c, ř. 200 (ploché střechy 2 600 / 3 600 / 5 200 Kč/m²) |
| 3 | Okna a balkonové dveře (~14 oken, 4 balkonové dveře) | 14 × 15 000 + 4 × 35 000 = 0,35 mil. (+ rolety/žaluzie ~0,03) | 445 000 | 0,55 / 0,33 mil. | `stav.md` S1 (plastové okno 11–23 tis./ks), ř. 115; balkonové dveře ODHAD |
| 4 | Terasa na zbytku střechy (~89 m²): dlažba na terčích a zábradlí ~40 bm. Hydroizolace sem NEPATŘÍ (viz kontrola) | 89 m² × 1 800 + 40 bm × 4 500 = 0,34 mil. | 398 000 | 0,5 / 0,25 mil. | ODHAD; plocha 239 − 150 = 89 m² (`model.py` c2_hruba, `uzemni-plan.md` ř. 8) |
| 5 | Prodloužení schodiště do 3. NP (ocelové nebo ŽB rameno, otvor ve stropě, požární dveře a obklad) | 1 komplet = 0,60 mil. | 702 000 | 1,0 / 0,45 mil. | ODHAD; v existující hale jde jen pokud se vejde 2. rameno (schodišťové okno velké, `stav.md` ř. 47, 52; rozměr haly neznám, ověřit zaměřením) |
| 6 | Rozvody a vytápění 2 bytů: stoupačky voda a kanalizace, elektro 120 m², podlahové topení, doplnění 1 tepelného čerpadla ~10 kW (kaskáda v rekonstrukci je na dům bez nástavby) | ZTI 0,18 + elektro 0,17 + topení 0,18 + TČ 0,30 = 0,83 mil. | 971 000 | 1,25 / 0,65 mil. | `stav.md` S1 ř. 115 (elektro 700–1 800 Kč/m², TČ 10 kW 180–420 tis.), 5c ř. 204 |
| 7 | 2 koupelny + 2 kuchyně (linka, spotřebiče, obklady, sanita) | 2 × 125 000 + 2 × 100 000 = 0,45 mil. | 527 000 | 0,7 / 0,35 mil. | `stav.md` 5b ř. 172–173 (jádro 135 tis., kuchyně 80 tis./byt), S2, S18 |
| 8 | Vnitřní dokončení 120 m² čisté: příčky a SDK, podlahy, malba, dveře, parapety | 120 m² × ~4 600 = 0,55 mil. | 644 000 | 0,8 / 0,42 mil. | `stav.md` S1–S3 (podlahy 1 100–2 500, malba 90–200 Kč/m²), ODHAD souhrn |
| 9 | Lešení, autojeřáb (montáž panelů), zařízení staveniště, ochrana obyvatel | lešení ~600 m² × 250 + jeřáb 4–5 dnů ~0,12 + ostatní 0,08 = 0,35 mil. | 410 000 | 0,55 / 0,28 mil. | ODHAD; obvod domu 23,8 × 10 m (`overeni/b2n-rozpocet.md` ř. 15) |
| 10 | Požární opatření (obklad REI 30–45, ověření stropu nad 2. NP) + nový elektroměrový rozvaděč a navýšení příkonu pro 2 byty | 0,15 + 0,12 = 0,27 mil. | 316 000 | 0,45 / 0,2 mil. | `uzemni-plan.md` ř. 110–112 (h ≈ 6 m, nízká budova); `stav.md` R8 ř. 99 (příkon 150–400 tis. za celý dům) |
| | **Mezisoučet stavba** | 6,53 mil. bez DPH | **7 643 000** | 9,6 / 6,0 mil. | |
| 11 | Statika: mikropiloty (cca 60 ks × 8 m) + ŽB převázky a hlavice, věnec nad 2. NP (~68 bm) | 480 bm × 2 800 = 1,34 mil. + věnec 68 bm × 5 000 = 0,34 mil. + zkoušky/ostatní 0,1 | 2 000 000 | 2,5 / 0,5 mil. (jako model) | mikropiloty24.cz 1 800–4 500 Kč/bm, nejstav.cz 1 500–3 000 Kč/bm (WebSearch 4. 11. 2026); počet ODHAD, rozhodne statik |
| 12 | Projekt, statika, inženýring, PBŘ, povolení | beze změny | 1 200 000 | 1,6 / 0,8 mil. | `uzemni-plan.md` ř. 177–182: projekt 0,45–0,70 + průzkumy 0,15–0,35 + inženýring 0,2–0,3 = 0,8–1,35 mil. |
| | **Celkem** | | **10 843 000** | | |

## 2. Kontrola proti modelu

| | Model | Můj součet | Rozdíl |
|---|---:|---:|---:|
| Stavba (řádky 1–10) | 6 671 000 | 7 643 000 | +972 000 (+14,6 %) |
| Statika | 2 000 000 | 2 000 000 | 0 |
| Projekt | 1 200 000 | 1 200 000 | 0 |
| Celkem | 9 871 000 | 10 843 000 | +972 000 (+9,8 %) |

- **Pokrývá 38 tis. Kč/m² hrubé vnitřní dokončení?** Ano, zhruba. 38 tis. na hrubou plochu je 47,5 tis. Kč na m² čisté (150/120), tedy horní polovina rozpětí dřevostavby RD na klíč (35–50 tis. Kč/m², zdroje výše), a ta už zahrnuje koupelny, kuchyně a povrchy. Uzemni-plan.md ř. 162 počítá s koeficientem 1,0–1,4 proti novostavbě. Co 38 tis. nepokrývá nebo kryje jen těsně: terasa 89 m² se zábradlím, prodloužení schodiště, doplnění TČ, lešení a jeřáb, přípojka a požární úpravy. Jejich součet (řádky 4, 5, 6 část TČ, 9, 10) je ~1,3 mil. bez DPH, a proto vychází +14,6 % u stavby.
- **Terasa a dvojí střecha:** hydroizolace zbytku střechy (89 m², ~37 % střechy) je už v rekonstrukci. Model z ní odečítá jen 50 % (`strecha_podil_c2`, −0,51 mil.), takže zbytek zůstává v rekonstrukci. Do nástavby jsem proto dal jen dlažbu a zábradlí. Odečet 50 % je o něco vyšší než reálných 63 % střechy pod nástavbou, rozdíl je zanedbatelný (~0,1 mil.), neměnit.
- **Statika 2,0 mil. vs. statické zajištění 1,0 mil. (`rizika_navic`):** částka 2,0 mil. mikropilotám odpovídá (60 ks, ~1,7 mil. bez DPH). Překryv je malý, v reálném scénáři jen geologie, monitoring a ztužení (~0,2–0,3 mil.), protože `rizika_navic` real obsahuje táhla, sešití a monitoring, ne podchycení. V pesimistickém scénáři se překrývá víc: oba vstupy počítají podchycení (rizika_navic pes 2,0 + nastavba_statika pes 2,5 = 4,5 mil.), ale mikropiloty pod domem jsou jedny. Pes tedy může být nadhodnocen o ~1–1,5 mil., to je rozhodnutí uživatele z 4. 11., jen poznámka.
- **Výška a požár:** podlaha 3. NP asi 6 m nad terénem, h < 9 m, nízká budova (`uzemni-plan.md` ř. 110). Každý byt je samostatný požární úsek, dřevěná konstrukce chce obklad a ověření stropu 1981. Zásadní překážku to není. Celková výška ~9–10 m je pod hranicí výškové stavby 12 m (ř. 84).
- **Napojení na TČ:** kaskáda 2 × 10 kW v rekonstrukci (`stav.md` ř. 204, 750 tis.) je dimenzovaná na 4 byty, nástavba ji přetíží, proto řádek 6 počítá s další jednotkou. V modelu to jinde není.
- **Navíc oproti modelu:** model stavbu nástavby nijak nerozepisuje, takže nic nepočítá dvakrát; rezerva 15 % se přičte nad všechny řádky (v modelu už je).
- **Slabé místo:** celý rozpis jsou ODHADy bez nabídky dodavatele. Cena nástavby bytového domu za m² v 2026 jako zdroj neexistuje (`uzemni-plan.md` ř. 162).

## 3. Doporučení

**Beze změny** (rozdíl celku +9,8 %, pod prahem 10 %, vše ODHAD). Pokud by uživatel chtěl pokrýt extra položky, stačí `nastavba_m2` real 38 000 → 43 500 (+0,97 mil. s DPH); pes a opt nechat. Rozhodne poptávka u 2–3 dodavatelů dřevostaveb a posudek statika (počet mikropilot).

## 4. Pro report

```python
[
 ("nosná dřevěná konstrukce nástavby (150 m²) a demontáž staré střechy", 2_598_000),
 ("střecha nástavby (spádová izolace, fólie, atika, oplechování)", 632_000),
 ("okna (14 ks) a balkonové dveře (4 ks)", 445_000),
 ("terasa na zbytku střechy (89 m²): dlažba a zábradlí", 398_000),
 ("prodloužení schodiště do 3. NP", 702_000),
 ("rozvody vody, odpadů, elektra, topení a další tepelné čerpadlo", 971_000),
 ("2 koupelny a 2 kuchyně", 527_000),
 ("vnitřní dokončení 120 m² (příčky, podlahy, malba, dveře)", 644_000),
 ("lešení, autojeřáb a zařízení staveniště", 410_000),
 ("požární úpravy, elektroměrový rozvaděč a navýšení příkonu", 316_000),
 ("podchycení základů mikropilotami a věnec nad 2. NP", 2_000_000),
 ("projekt, statika, inženýring, požární řešení, povolení", 1_200_000),
]  # součet 10 843 000 (model 9 871 000)
```
