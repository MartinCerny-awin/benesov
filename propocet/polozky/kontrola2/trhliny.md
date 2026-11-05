# Kontrola 2: Sanace trhlin (5. 11. 2026)

Web real bez nástavby: **450 tis.** (270 + 54 + 15 + 36 + 38 + 37). Pozor: součet „kontrolních“ hodnot v `report.py` ř. 300–306 je jen 300 tis. (178+40+15+22+23+22); web ukazuje 450, protože se položky dopočítaly na součet z modelu (× 1,5). Cenu proto porovnávám s webem, ne s komentáři v kódu.

## Odpovědi na zvláštní otázky

**Délka 70 m + 50 m.** Z fotek vychází celkem ~120 bm (fasáda: 6 svislých × ~7 m + vodorovná pod atikou ~20 m = 60 bm; uvnitř W21, W26, W27, V3/018, W20, W22, W24 ~60 bm; `strecha-statika.md` ř. 26, `stav-nove-fotky.md` ř. 14–20). 70 + 50 = 120 bm tedy pokrývá všechny trhliny na fotkách. Z fotek se ale nedá měřit (close-upy), chyba ±30 %. Šířka 2–3 mm je jen u W05 a W11, ostatní do ~1 mm, takže „sešít“ celých 70 bm je spíš horní odhad. Rozsah ale určí statik, ne foto.

**Pozor na „metr“.** Web účtuje 70 m *trhliny*. Helikální prut se lepí do spár každých ~450 mm výšky, délka prutu ~1,0–1,2 m. Na 70 bm trhliny je to ~155 prutů = ~190 m výztuže (ne 70 m). Materiál: prut 112–220 Kč/m s DPH ([eshop.helikalni.cz](https://eshop.helikalni.cz/), 5. 11. 2026), Weber Elicafix A8 159,60 Kč/m bez DPH ([dek.cz](https://www.dek.cz/produkty/detail/1640107987-webertec-elicafix-a8-10m)), sada 10 m + pistole + malta 3 207 Kč ([re-art.cz](https://www.re-art.cz/sada-pro-staticke-zajisteni-prasklin-ve-zdivu/)). Helifix a Mapei veřejný ceník nemají (jen na poptávku, [statikasanace.cz](https://statikasanace.cz/statika-staveb/helifix/)). 190 m × ~150 Kč + malta/kartuše ~100 Kč/m prutu ≈ **45–55 tis. s DPH** (ODHAD).

**Práce.** Hotová sešití u firmy: 1 500–3 500 Kč/bm bez DPH ([mobetony.cz](https://mobetony.cz/blog/oprava-prasklin-betonu), 2026, prodejní blog; `overeni/rozpocet-2.md` ř. 122: 1 800 / 2 500 / 3 500). 70 bm × 2 500–3 000 × 1,12 = **196–235 tis.** firma. Řemeslník: ~155 prutů × 0,6 h + omítka kolem fasádních drážek ~40 h = ~130–140 h × 550–650 Kč = 75–90 tis. + materiál 50 tis. = **125–140 tis.** (hodinovka ODHAD, zdroj nenalezen).

**Překryv se „Statické zajištění“ 1,5 mil.** Sešití trhlin je dnes **jen zde** (report.py ř. 159 to říká výslovně, v 1,5 mil. je táhla, ztužení, základy, geologie, rezerva). Dvojí započtení tedy není. Dvě věci k pozornosti: (1) sešití dává smysl až *po* stažení táhly a po 6–12 měsících monitoringu, jinak se trhlina znovu otevře (W11); monitoring (sádrové terče) je ve službách, ne zde. (2) Kdyby statik 1,5 mil. spotřeboval na rezervu, tato položka zůstává nezbytná.

**Překryv s byty.** Částečný, drobný. „Vysprávka vnitřních trhlin 60 m“ (60 bm = všechny vnitřní trhliny) se kryje s drážkami po sešití uvnitř (~35 bm zapraví řemeslník při sešití) a s „Omítky a zapravení po nových rozvodech 111 tis.“ a „Plísně, drobné opravy 89 tis.“ v `byty_povrch` (report.py ř. 281, 284). Odhad zdvojení **10–15 tis.** Dále „Oprava opadané omítky 20 m²“ (W26, W27, V3/018) se kryje s plošným omítáním v bytech B a D, pokud se tam omítá celá stěna.

## 1. Tabulka

| Položka | Web | Můj real (s DPH) | Pes–opt | Potřeba | Nejlevnější rozumná cesta | Zdroj |
|---|---|---|---|---|---|---|
| Sešití trhlin spirálou 70 m | 270 | **200** (196–235 firma; 125–140 řemeslník) | 400–110 | **Ano, ale až po stabilizaci a jen to, co určí statik**. Kupec/banka chtějí posudek, bez sešití se zakryté trhliny otevřou | Řemeslník ~135, úspora ~65 proti firmě. Svépomoc: materiál ~50 (úspora ~85 proti řemeslníkovi) | mobetony.cz, eshop.helikalni.cz, dek.cz, rozpocet-2.md ř. 122, 5. 11. 2026; hodiny ODHAD |
| Injektáž a vyspárování 50 m | 54 | **40** | 70–25 | Jen když trhlina > 0,3 mm; vlasové stačí vytmelit a přetřít | Řemeslník ~25 (50 bm × 450 + materiál). Svépomoc: kartuše PU/akryl ~5 | sanace-injektaze.cz (360–720 Kč/bm), ODHAD |
| Pracovní plošina | 15 | **10** | 15–6 | Ano (2 NP fasáda, ~8 m) | Nůžková 8 m 1 200 Kč/den × 5–8 dní + doprava 3 = 9–13. Obsluha potřebuje zaškolení | dek.cz půjčovna, aldaopava.cz, 5. 11. 2026 |
| Opadaná omítka až na cihly 20 m² | 36 | **22** (1 100 Kč/m²) | 36–15 | Ano (podklad pro malbu, kupec to vidí) | Řemeslník ~14. Svépomoc materiál ~4, 12 h | `stav.md` S1 (omítka 280–620, štuk 120–200 Kč/m²), ODHAD |
| Vysprávka vnitřních trhlin, síťka, štuk 60 m | 38 | **22** | 35–12 | Ano | Řemeslník ~17. **Svépomoc ~3 materiál, ~25 h, laik zvládne** | ODHAD (0,4 h/bm) |
| Penetrace, nátěr, ochrana, úklid | 37 | **25** (penetrace, kontejner 4, lokální dobarvení omítky na fasádě) | 40–15 | Ano | Penetrace a úklid svépomocí ~5 | ODHAD |
| **Součet** | **450** | **319** | ~600–180 | | | |

## 2. Součet

- Web: **450 tis.**
- Můj realistický odhad při současném rozdělení (sešití řemeslník/firma, zbytek řemeslníci): **~320 tis.** (−29 %). Hlavní důvod: web je dopočtený na model × 1,5 a všech šest řádků je o 25–60 % nad vlastní spodní kalkulací. Nejvíc vychází nad realitou sešití (270 vs 200), omítka (36 vs 22) a vysprávka (38 vs 22).
- Nejlevnější rozumná varianta: sešití řemeslníkem podle statika (135), vnitřní vysprávky, penetrace a omítka svépomocí (materiál ~15), injektáž řemeslník 25, plošina 10 = **~190 tis.** (−58 %).

**Svépomoc u spirály.** Technicky ji laik s drážkovačkou (frézka s odsáváním, FFP3) zvládne: drážka 20–25 mm, vyfouknout, dolít maltu, prut vtlačit; ~100–140 h práce. Riziko: (1) statik určuje typ prutu (6/8 mm), rozteč, kotvení a pořadí, musí to být zdokumentované (fotky, zápis ve stavebním deníku) a statik dozor potvrdí; (2) záruka vůči kupcům bytů: bez dokladu o provedení nelze doložit, že sanace proběhla; (3) práce na fasádě ve výšce = plošina s oprávněním, to nechte řemeslníkovi. Doporučení: *vnitřní* sešití (cca 30 bm) lze svépomocí pod statikem, *fasádní* řemeslník s dokladem.

## 3. Chybí / dvakrát / podhodnocené

- **Chybí (volitelně):** sjednocení fasády po opravách. Lokální záplaty v břízolitu budou vidět; nátěr celé fasády (~600 m² × 150 Kč bez DPH ≈ **100 tis.**) nikde není (rozhodnutí „bez zateplení“ to neřeší). Jen když kupci/prodej vyžadují vzhled fasády. Zdroj: ODHAD.
- **Chybí:** plocha 70 bm sešití je jen z fotek; při 100 bm navíc +60–70 tis. (pes).
- **Dvakrát (drobně):** ~10–15 tis. mezi vysprávkami zde a „Omítky a zapravení“ / „Plísně, drobné opravy“ v bytech; viz výše.
- **Není dvakrát:** statické zajištění 1,5 mil. neobsahuje sešití (report.py ř. 159).
- **Časování:** sešití až po monitoringu 6–12 měsíců; při spuštění prodeje do 23 měsíců od dokončení (§ 56) to tlačí harmonogram.

## 4. Doporučení

**Nová hodnota:** real **~350 tis.** (z 450), pes **600**, opt **200**. Důvod: spodní kalkulace dává ~320 tis., ale rozsah (délku sešití) určí až statik a nejistota je jednostranně nahoru, proto zaokrouhlení na 350 a ne na 320. Rozdíl −22 % je nad prahem 10 %. Rozhodnutí „statické zajištění 1,5 mil.“ nezpochybňuji.
