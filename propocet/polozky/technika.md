# Technika: vytápění, rozvody domu, společné prostory (V1, firma, realisticky)

Přepočet: tis. Kč bez DPH a bez režie (ceny 2026) × 1,3135 = Kč s DPH. Pes / opt = rozpětí k s DPH částce (TČ ×0,75 / ×1,4; ostatní ODHAD ×0,65 / ×1,6).

## Úvaha o výkonu TČ
Vytápěná plocha V1 = 264 m² bytů + 86 m² bývalé nebytové části + část společných ≈ 380 m². Dům 1981, cihla, bez zateplení, z části původní okna. Měrná ztráta 70–90 W/m² (stejný odhad jako `podklady/stav.md` 5d) dává **27–34 kW, počítám 30 kW**. Model počítá kaskádu 2 × 10–12 kW (20–24 kW), to je pro nezateplený dům málo: TČ vzduch–voda při −15 °C dává jen ~70 % jmenovitého výkonu. Navrhuji **2 × 16 kW (32 kW) + elektrická bivalence** (stejný řád jako `overeni/rozpocet-2.md` ř. 124: 2 × 16 kW). Výkon ověří projektant výpočtem ztrát.

## 1. Rozpis

| Položka | Množství | Jedn. cena (bez DPH) | Realisticky Kč s DPH | Pes / opt (Kč s DPH) | Zdroj |
|---|---|---|---:|---|---|
| TČ vzduch–voda 2 × 16 kW vč. montáže a uvedení do provozu | 2 ks | 380 tis./ks | 998 000 | 1,4 mil. / 0,75 mil. | ODHAD z S1 (TČ 10 kW vč. instalace 180–420 tis.) a S15 (260–430 + 110–140 tis. RD), `stav.md` kap. 4 ř. 115, 129; rozpocet-2 ř. 124 |
| Jeřáb na střechu, podstavce, propojovací potrubí a kabeláž (venkovní jednotky na střechu, pozemek je jen půdorys) | 1 kpl | 30 tis. | 39 000 | 55 000 / 25 000 | ODHAD; poloha jednotek podle `overeni/b2n-rozpocet.md` ř. 73 |
| Akumulační nádrž 1 000 l, hydraulický rozdělovač, čerpadla, regulace, elektrická bivalence | 1 kpl | 100 tis. | 131 000 | 210 000 / 85 000 | `stav.md` 5d ř. 228 (akumulace, hydraulika, regulace 100–250 tis.) |
| Rozvody topení v domě (ležaté + stoupací): výměna vadných úseků, izolace, vyvážení; 6 podružných měřičů tepla vč. montáže | 1 kpl + 6 ks | 120 tis. + 6 × 8 tis. | 221 000 | 350 000 / 140 000 | ODHAD; `rozpocet-2.md` ř. 126 (100–300 tis.), `stav.md` 5c ř. 206 |
| Demontáž 2 kotlů na tuhá paliva, rozdělovače, starých rozvodů v kotelně, odvoz šrotu | 1 kpl | 45 tis. | 59 000 | 105 000 / 40 000 | `b2n-rozpocet.md` A2 (25/45/80 tis.) |
| Odstranění komínového nástavce kotelny, zapravení střechy a prostupů | 1 kpl | 60 tis. | 79 000 | 160 000 / 40 000 | `rozpocet-2.md` ř. 121 (30/60/120 tis.) |
| Topení ve 4 stávajících bytech: termostatické hlavice, proplach, tlaková zkouška, výměna vadných těles | 4 byty | 25 tis. | 131 000 | 210 000 / 85 000 | `rozpocet-2.md` ř. 103 (15/30/60 tis./byt); `stav.md` 5b ř. 179 |
| Vytápění druhého nového bytu 2+kk (podlahové topení nízkoteplotní, měřič tepla) | 1 byt | 80 tis. | 105 000 | 170 000 / 60 000 | `b2n-rozpocet.md` E4 (60/90/130 tis.); v modelu **chybí** (viz kontrola) |
| Stoupačky kanalizace (HT DN 110, odvětrání nad střechu) | 4 ks × 6 m | 28 tis./ks | 147 000 | 235 000 / 95 000 | ODHAD; `stav.md` 5c ř. 207; materiál stoupaček neznámý (`stav.md` ř. 49) |
| Stoupačky vody (3 větve PPR s izolací, uzávěry po bytech), hlavní vodoměrná sestava a napojení v 1. NP | 3 větve + 1 kpl | 18 tis./větev + 50 tis. | 137 000 | 220 000 / 90 000 | ODHAD; `rozpocet-2.md` ř. 127 (120–300 tis. vč. hlavního vodoměru) |
| Kamerová prohlídka svodů, zapravení drážek a požární ucpávky prostupů | 1 kpl | 52 tis. | 68 000 | 110 000 / 45 000 | `stav.md` R1 (kamerová zkouška 8–15 tis.); zbytek ODHAD |
| Hlavní domovní rozvaděč + elektroměrový rozvaděč (8 míst: 6 bytů, společné prostory, TČ) | 1 kpl | 90 tis. | 118 000 | 190 000 / 75 000 | ODHAD; stav rozvaděčů `stav.md` ř. 48; `b2n-rozpocet.md` ř. 59–61 |
| Stoupací vedení k bytům a ke střeše (měděné kabely, žlaby) | ~7 vedení × 2 NP | 60 tis. | 79 000 | 125 000 / 50 000 | ODHAD; `rozpocet-2.md` ř. 128 |
| Společné osvětlení (LED s čidly, nouzové), zvonky a domovní telefon | ~20 svítidel + 6 bytů | 70 tis. | 92 000 | 150 000 / 60 000 | ODHAD; `rozpocet-2.md` ř. 128 |
| Hromosvod nový vč. revize hromosvodu | 1 kpl | 45 tis. | 59 000 | 95 000 / 40 000 | `rozpocet-2.md` ř. 120 (30/45/60 tis.) |
| Revize elektroinstalace hlavních rozvodů + silový přívod k TČ na střechu (3 × 32 A) | 1 kpl | 55 tis. | 72 000 | 115 000 / 45 000 | ODHAD |
| Společné prostory ~60 m²: nová dlažba v chodbách (30 m²), očištění a protiskluz schodiště (24 m²) | 30 + 24 m² | 2 400 / 700 Kč/m² | 117 000 | 180 000 / 70 000 | ODHAD; stav dlažby OK, chodba 1. NP holý beton, 2. NP dřevotříska (`stav.md` ř. 52) |
| Společné prostory: renovace zábradlí (25 m), opravy omítek a malba ~200 m², 4 dveře, 6 schránek | kpl | 40 + 38 + 44 + 9 tis. | 172 000 | 275 000 / 110 000 | ODHAD; `rozpocet-2.md` ř. 87 (malba 60/80/110 Kč/m²) |
| **Součet** | | **2 151 tis. bez DPH** | **2 825 000** | cca 4,3 mil. / 1,8 mil. | |

Dílčí součty: vytápění 1 343 tis. → 1 764 000 Kč; rozvody domu 588 tis. → 772 000 Kč; společné prostory 220 tis. → 289 000 Kč.

## 2. Kontrola proti modelu

| Skupina | Model (tis. bez DPH → Kč s DPH) | Můj součet | Rozdíl |
|---|---|---|---|
| Vytápění | 1 060 → 1,39 mil. | 1 343 → 1,76 mil. | **+27 %** |
| Rozvody domu | 590 → 0,77 mil. | 588 → 0,77 mil. | 0 % |
| Společné prostory | 228 → 0,30 mil. | 220 → 0,29 mil. | −4 % |
| **Celkem** | 1 878 → 2,47 mil. | 2 151 → 2,83 mil. | **+15 %** (+0,36 mil. s DPH) |

Vysvětlení:
- **TČ podhodnoceno.** Model má 2 × 10–12 kW (20–24 kW), ale `stav.md` 5d sám uvádí ztrátu nezatepleného domu 23–35 kW a dům zůstává bez zateplení (schválené rozhodnutí). Při 6 bytech a 86 m² navíc nestačí. 2 × 16 kW + akumulace stojí cca 890 tis. oproti 750 tis. (+19 %).
- **TČ se nepočítá dvakrát, ale vytápění 2. nového bytu chybí.** Model `nebyt2_m2` říká „vlastní zdroj tepla v bytech“, ale nikde není nic naceněno: `nebyt_druhy_byt` obsahuje jen jádro, kuchyň, dveře, elektroměr, vodu a příčku. První nový byt má podlahové topení a přepojení okruhů v `nebyt_zmeny` (E4 + G1), druhý nic. Nový samostatný zdroj tepla (druhé TČ) by byl zbytečný, bytům stačí napojení na centrální TČ. Doplňuji 80 tis. za podlahové topení a měřič.
- **Možné překrytí:** demontáž kotlů (A2, 45 tis.) je pravděpodobně i v `nebyt_zmeny` (přepočet celého b2n rozpočtu). Netto to dělá cca −45 tis. bez DPH (−0,06 mil. s DPH), takže vytápění je spíš +23 %. Nelze potvrdit bez rozpisu `nebyt_zmeny`.
- **Technická místnost TČ.** `nebyt2_m2` = 2 × 36–42 m² ze 86 m², takže pro akumulaci, hydromodul a rozvaděč TČ (v b2n 12–20 m²) nezbývá místo. Venkovní jednotky půjdou na střechu, ale nádrž 1 000 l a rozdělovač potřebují ~6–8 m² (kotelna 20 m² je v nebytové části). Jen poznámka k dispozici, neměním.
- **Dotace NZÚ: nezapočítána, do modelu nedávat.** Podle E.ON a TZB-info (výsledky hledání 4. 11. 2026, nepotvrzeno na SFŽP) dostávají bytové domy u TČ vzduch–voda jen bezúročný úvěr max. 150 tis. Kč na bytovou jednotku (podmínka: renovační pas), přímá dotace 150 tis. platí jen pro nízkopříjmové domácnosti (NZÚ Light). Prodej bytů jako podnikání se sem nehodí, úvěr navíc nesníží cenu. https://www.eon.cz/radce/blog/jake-dotace-lze-ziskat-na-tepelne-cerpadlo/ , https://stavba.tzb-info.cz/zelena-usporam-na-tzb-info/29942-nova-zelena-usporam-2026-zvyhodnene-uvery-pro-bytove-domy
- **Přípojka elektřiny a navýšení příkonu (TČ 15–20 kW, 6 měření) v této položce nejsou.** Dům je odpojený (`rozpocet-2.md` ř. 54, 186). Jsou jen jako riziko R8 (0 / 150 / 400 tis., `stav.md` ř. 99) a v `nebyt_druhy_byt` (elektroměr E2). Při příkonu 6 bytů + TČ bych R8 považoval za reálný náklad, ne jen riziko. Podíl na připojení 500 Kč/A (b2n ř. 221) × 63 A = ~30 tis., ale s novým přívodem a pilířem běžně 150–400 tis.
- **Revize:** revize elektro a hromosvodu jsou v rozpisu. Revize spalinových cest po zrušení kotlů odpadá. Azbest v kotelně a komíně je v R4, nepočítám.
- **Ohřev vody:** zůstávají elektrické bojlery v bytech (`stav.md` ř. 50); centrální ohřev s cirkulací nepočítám, byl by +250 až 400 tis.
- **Společné prostory:** model počítá 35 m² × 6 500 Kč/m², ale ani při ploše 60 m² nevychází víc, protože se obnovuje jen povrch (dlažba schodiště se ponechá). Osvětlení a vstupní portál jsou už v elektru a v oknech, tady je nepočítám.

## 3. Doporučení

Vstupy `IN["stredni"]` (Kč s DPH, součet stavba + služby): jen **real zvýšit o ~0,35 mil.**, tj. **7 990 000 → 8 345 000**, protože TČ je pro nezateplený dům poddimenzované (20–24 kW proti 27–34 kW) a chybí topení 2. nového bytu. Výpočet: +283 tis. (1 343 − 1 060) × režie 12 % × DPH 12 %. Pes (11,91 mil.) a opt (4,33 mil.) beze změny: pes už je kalibrovaný na `rozpocet-2.md`, jehož TČ 650–1 100 tis. rozpětí je podobné, opt je optimistický a nemám zdroj pro změnu. Celkově jde o +4 % střední úrovně, takže pokud je to jen pro jednu položku pod 10 %, je „beze změny“ přijatelná alternativa. Výkon TČ i R8 (příkon) řešit v projektu a při poptávce.

## 4. Pro report

```python
[
    ("Tepelné čerpadlo vzduch–voda 2 × 16 kW vč. montáže (výkon pro nezateplený dům)", 998_000),
    ("Jeřáb, podstavce a propojení venkovních jednotek na střeše", 39_000),
    ("Akumulační nádrž 1 000 l, rozdělovač, čerpadla, regulace, elektrická dotopná patrona", 131_000),
    ("Rozvody topení v domě, izolace, vyvážení, 6 měřičů tepla po bytech", 221_000),
    ("Demontáž 2 kotlů na tuhá paliva a starých rozvodů v kotelně", 59_000),
    ("Odstranění komínového nástavce kotelny, zapravení střechy", 79_000),
    ("Topení ve 4 stávajících bytech (hlavice, proplach, výměna vadných těles)", 131_000),
    ("Vytápění druhého nového bytu 2+kk (podlahové topení, měřič tepla)", 105_000),
    ("Stoupačky kanalizace, 4 kusy po 6 m, odvětrání nad střechu", 147_000),
    ("Stoupačky vody, hlavní vodoměr a napojení v přízemí", 137_000),
    ("Kamerová prohlídka svodů, zapravení drážek a požární ucpávky", 68_000),
    ("Hlavní domovní rozvaděč a elektroměrový rozvaděč na 8 měření", 118_000),
    ("Stoupací elektrické vedení k bytům a ke střeše", 79_000),
    ("Společné osvětlení s čidly, zvonky a domovní telefon", 92_000),
    ("Nový hromosvod vč. revize", 59_000),
    ("Revize elektro a silový přívod k čerpadlu na střeše", 72_000),
    ("Společné prostory: dlažba chodeb 30 m², oprava schodiště 24 m²", 117_000),
    ("Společné prostory: zábradlí, omítky a malba, 4 dveře, schránky", 172_000),
]
# součet 2 824 000 Kč s DPH (zaokrouhleno po řádcích; 2 151 tis. × 1,3135 = 2 825 tis.)
```
