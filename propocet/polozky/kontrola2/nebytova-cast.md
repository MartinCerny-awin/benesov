# Kontrola 2: Nebytová část → 2 byty 2+kk (5. 11. 2026)

Web 3 071 tis. (model teď dává real **3 130**, pes 5 940, opt 1 792; architekt je mimo, viz `report.py` ARCH_POL). Dílčí řádky na webu jsou škálované ~×1,2 (nad vlastním rozpisem `polozky/nebyt-bytb.md`), proto hodnotím hlavně součet. Můj odhad je zdola, real, s DPH 12 %/21 % u služeb, VRN 5 % a zdražením 5 % (`model.py` `inflace_stavby`), bez rezervy.

## 1. Tabulka (tis. Kč s DPH)

| Položka | Web | Můj real | pes–opt | Potřeba | Nejlevnější rozumná cesta (úspora) | Zdroj |
|---|---:|---:|---|---|---|---|
| Vyklizení, bourání příček a podlah, průzkum azbestu | 135 | 125 | 220–70 | ano (bez toho nejde stavět) | **svépomoc**: vyklizení, příčky, kladivo na podlahu, odhad 100–150 hod pro 3 lidi, −55. Odběr vzorků azbestu a případné odstranění jen firma s oprávněním | `overeni/b2n-rozpocet.md` A1–A5, ODHAD |
| Zvětšení 5 okenních otvorů, sešití trhlin | 308 | 255 | 450–150 | **ano**: § 20 odst. 1 vyhl. 146/2024: otvory ≥ 1/10 podlahy obytné místnosti (obývák 20 m² → 2 m², dnes 0,6–0,8 m²) | **řemeslník** (zedník podle statika), −25. Svépomoc ne (nosná zeď přes trhliny, statik) | [e-Sbírka 146/2024 § 20](https://www.zakonyprolidi.cz/cs/2024-146) (3 řádky z vyhledávání 5. 11. 2026), `nebyt-bytb.md` ř. 11–17; jednotky ODHAD |
| Nová okna 12 ks (5 velkých akustických) | 205 | 180 | 300–120 | ano (stávající dřevěná hnijí, ulice II/110) | dvojsklo s asymetrickým sklem na zahradní straně, −15. Trojsklo jen do ulice | okna 9–18 tis./ks vč. montáže (kolikmaterialu.cz, duben 2026; daibau.cz 2026), `stav.md` S1 (11–23 tis.) |
| Vlhkost a podlaha (injektáž, sanační omítky, skladba, nášlapné vrstvy) | 594 | 500 | 800–330 | podlaha ano; **injektáž a sanační omítky jen když průzkum ukáže vlhkost** (sklad má mapy do ~1,5 m, `b2n` 3.7, pravděpodobné) | injektáž jen kde je mokro, −100; vinyl/plovoucí podlaha **svépomocí** (80 m², ~25 hod), −35 | injektáž je v ceníkách za m² průřezu zdi, ne za bm: 2 000–4 500 Kč/m² (kralmotoru.cz, sanace-staveb.cz, 5. 11. 2026) → ~1 500–1 800 Kč/bm místo 3 000 v rozpisu (−40 až −50 při plném rozsahu); sanační omítka 680–1 450 Kč/m² (daibau.cz, 10. 2. 2026); podlaha `stav.md` S1 |
| 2 koupelny s WC, 2 kuchyňské linky | 540 | 450 | 750–330 | koupelny ano; **linka ne** (nová byt bývají prodávané bez linky, ale hůř se prodávají) | koupelny **řemeslník** −40; linky jednodušší (45–60 tis./ks) −60. Dohromady −100 | koupelna 80–200 tis., kuchyně 80–300 tis. (sitprace.cz, sousede.cz 2026); `stav.md` S2 |
| Rozvody: elektro, 2 elektroměry, voda, kanalizace, podlahové topení, větrání | 568 | 470 | 780–300 | elektro, voda, topení ano; **rekuperace ne**; elektroměry viz kap. 3 | −40 elektroměry (už v rozvaděči 8 měření), −35 větrání (2 jednotky do ložnic na ulici místo 4). Elektro a revize jen oprávněná osoba, svépomoc ne | `technika.md` ř. 23 (rozvaděč 8 měření 118 tis.), `b2n` E1–E5, 3.5 hluk; koky-stavby.cz 2026 (elektro 80–180 tis.) |
| Příčky, omítky, malby, 2 vstupní EI dveře, vnitřní dveře | 380 | 380 | 600–250 | ano (EI 30 DP3 je podmínka kolaudace) | malby **svépomocí** (290 m², ~60 hod), příčky mezi místnostmi zdění svépomocí; zvuková příčka mezi byty firma. Dohromady −60 | `b2n` F1–F5; ODHAD |
| Technická místnost TČ, požární oddělení, úprava chodby | 176 | 145 | 260–80 | ano (požární oddělení je v povolení); technická místnost jen když je TČ centrální v kotelně | beze změny | `b2n` G1–G3; ODHAD |
| Statik, PBŘ, akustika, osvětlení, průzkum vlhkosti, poplatky | 166 | 125 | 220–90 | ano (změna užívání) | −35 překryv s položkou Projekt 390 (tam PBŘ 45 a statik 111) | `b2n` S3–S7 + poplatky; `_kontrola.md` ř. 90–92 |
| **Součet** | **3 071** | **2 630** | **~4 700–1 500** | | | |

Jednotkové ceny jsou ODHAD s uvedenými kotvami; ceny přestavby nebytu na byt jsem na webu 5. 11. 2026 nenašel (ceníky jsou jen pro běžnou rekonstrukci bytu).

## 2. Součet

- Web 3 071 (model 3 130) vs můj real **2 630**: **−14 %**. Hlavní důvod: vyšší škálování ×1,2 oproti vlastnímu rozpisu, jednotka injektáže, elektroměry a větrání dvakrát, překryv služeb.
- Nejlevnější rozumná varianta (svépomoc vyklizení/bourání/malby/vinyl, řemeslník na zdi a koupelny, bez rekuperace, injektáž jen kde mokro, jednodušší linky): **~2 165**, tedy **−30 % proti webu**, −18 % proti mému real. Úspora ~465, z toho svépomoc jen ~180 (materiál se odpočítá, ušetří se hlavně práce).
- ~38 tis. Kč/m² (3 071/80 m²; z 86 m² 36 tis.; můj odhad 31 tis./m²): komplet rekonstrukce bytu je 2026 12–25 tis./m² (kolikmaterialu.cz, qjob.cz), přestavba s vybouráním jádra a rozvodů 15–30 (autorskesperky.com), půdní vestavba 15–40 (realfree.cz). Nebyt navíc: vlhkost, nové otvory v nosné zdi, akustická okna, EI dveře. **38 je horní polovina pásma, ne nesmysl.**

## 3. Chybí / dvakrát / podhodnocené

- **Dvakrát: elektroměry** (~45 tis.). `nebyt-bytb.md` počítá 2 elektroměry s přívodem 60, ale `technika.md` ř. 23 má rozvaděč na 8 měření (6 bytů, společné, TČ) za 118 tis. Zůstává jen přívod k bytu.
- **Dvakrát: PBŘ a statik** (~35 tis.) v této položce i v „Projekt, dozor, statik 390“.
- **Přeceněná jednotka injektáže** (~40–50 tis.): 3 000 Kč/bm vychází z ceny za m² průřezu zdi (tendr Klatovy, `nebyt-bytb.md` kap. 4).
- **Rekuperace** (72 tis. v rozpisu, 4 ks): zákon ji nevyžaduje (ověřit u KHS), potřeba je jen větrání ložnic na uliční straně při zavřených oknech (`b2n` 3.5).
- **Chybí (mimo položku, jen upozornění):** přípojka a příkon pro 6 bytů + TČ, `technika.md` ř. 49 (R8 150–400 tis.); světlá výška 2,5 m při skladbě podlahy bez zahloubení (`b2n` bod 2, výjimka nebo +72–112 tis. na zahloubení; rozhodnutí uživatele neměním, jen poznámka); odvodnění soklu na pozemku SPÚ; technická místnost TČ ubírá z 86 m² (byty vyjdou ~37 m², `nebyt-bytb.md` kap. 0).
- **Podlahové topení vs radiátory:** při nové skladbě podlahy je rozdíl v ceně malý (podlahovka ~90–95 tis. za 86 m², radiátory ~80–120), podlahovka je vhodnější pro nízkou teplotu TČ. Nechat. Nezateplený dům a radiátory v bytech A–D už nutí TČ jet vyšší teplotu, nové byty si to nezhoršují.
- **Jeden větší byt místo dvou:** ušetří jedno jádro (koupelna, linka, EI dveře, přívod, voda, příčka ≈ 340 s DPH), ale model dává 2 × 40 m² = 6,24 mil. vs ~71 m² jeden byt ≈ 5,06 mil. (`model.py` `m2_maly` 93 000, `m2_velky` 85 000 a srážky). Dva byty vyhrávají o ~0,7 mil. po úspoře. Nedělat.

## 4. Doporučení

**Snížit real o ~10 %: 3 130 → ~2 750** (model: konstanta `nebyt_zmeny` real 2 281 → ~1 940 tis. před × (0,4 + 0,6 × 86/65)). Důvod: dvojí započtení elektroměrů a služeb, přeceněná injektáž a rekuperace. Zbylých ~4 % mezi mým real 2 630 a 2 750 nechat jako jedinou rezervu, protože tato položka má největší neznámé (vlhkost, azbest, statika trhlin kolem nových otvorů). Pes 5 940 a opt 1 792 beze změny. Svépomoc a řemeslníci (−465 proti webu) do modelu nepřenášet, patří jen do nejlevnější varianty.
