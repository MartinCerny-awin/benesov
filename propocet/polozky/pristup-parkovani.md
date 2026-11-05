# Přístup přes pozemek SPÚ a parkování (`IN["pristup"]`, `IN["parkovani"]`)

Ceny s DPH 21 % tam, kde fakturuje plátce (geodet, znalec, právník, dlažba). Koupě pozemku od SPÚ bez DPH (zemědělský pozemek, osvobozeno; ODHAD, u pozemku určeného k zastavění by mohlo být DPH 21 % a cena by vzrostla o ~20 %).

## Předpoklady (z čeho se počítá)
- Cena pozemku: **3 500 Kč/m²** (rozpětí 2 000–6 000). Nabídky v okrese Benešov: zahrada 364 m² v Benešově 899 000 Kč = ~2 470 Kč/m², stavební parcely 2 600–3 830 Kč/m² (Bedrč, Mariánovice), průměr okresu 2 394 Kč/m² (WebSearch 4. 11. 2026, realitymix.cz, reality-benesov.cz). SPÚ prodává podle znaleckého posudku (min. cena obvyklá, § 10 odst. 3 písm. b), odst. 4 zák. 503/2012, `podklady/katastr.md` r. 100–104); malý pozemek vedle domu v ploše BI se oceňuje spíš jako zastavitelný, proto horní polovina nabídek. Konkrétní cenu určí až posudek (ODHAD).
- **Kolik stání** (vyhl. 146/2024, 1 stání / 120 m² bytové plochy bez společných prostor, zaokrouhlení jednou na konci; `podklady/uzemni-plan.md` r. 103, Obsidian `2026-11-04-benesov-1598-parkovani(-doplneni).md`):
  - V1 jen přírůstek: 86 / 120 = 0,72 → **1 stání** (může být i 0, pokud byla dílna zkolaudovaná jako provozovna); celý dům 344 / 120 = 2,9 → 3.
  - V2 jen přírůstek: (86 + 120) / 120 = 1,7 → **2 stání**; celý dům 464 / 120 = 3,9 → 4.
  - Praxe MěÚ Benešov (MUBN/189104/2023/VÝST) chtěla jen rozdíl a stání povolila na cizím pozemku, takže přírůstek je nejpravděpodobnější výklad (neověřeno úřadem).
- Plocha: stání 2,5 × 5 m = 12,5 m², 2 stání 25 m² + manipulace a vjezd ~25 m² = 50 m². Přístupový pruh od ulice 3501 k domu: nejméně 4,7 m (`katastr.md` r. 12, 73) × ~5 m = 25 m².
- Společné náklady (geometrický plán, posudek, vklad, smlouva) jsou ve jménu přehlednosti jen v položce přístup, protože jde o **jednu smlouvu a jeden plán** pro pruh i stání.

## 1. Rozpis – přístup (model: 150 000)

| Položka | Množství | Jedn. cena | Realisticky Kč | Pes / opt | Zdroj |
|---|---|---|---|---|---|
| Koupě pruhu 2128/3 od ulice k domu | 25 m² | 3 500 | 87 500 | pes 500 000 (100 m² × 5 000, celé okolí domu) / opt 0 (VB už zapsané, ověřit LV) | cena: viz výše, ODHAD; `katastr.md` r. 217 |
| Geometrický plán (oddělení pruhu i stání z 2128/3, vytyčení) | 1 | 18 000 | 18 000 | 12 000–30 000 | ceníky geodetů 7 000–12 000 Kč za oddělení bez vytyčení (digistav.cz, geodezievysocina.cz, 4. 11. 2026), 2 části + vytyčení + DPH = ODHAD |
| Znalecký posudek na cenu obvyklou (platí kupující) | 1 | 15 000 | 15 000 | 10 000–25 000 | ODHAD (veřejný ceník nenalezen) |
| Právník: žádost podle § 10, smlouva, jednání se SPÚ | 1 | 24 500 | 24 500 | 15 000–50 000 | ODHAD |
| Vklad do katastru | 1 | 2 000 | 2 000 | stejné | správní poplatek za vklad 2 000 Kč (z paměti, ověřit u ČÚZK) |
| Nájem části 2128/3 do převodu (§ 10 chce „oprávněného uživatele“), ~18 měs. | ~100 m² | ~30 Kč/m² | 3 000 | 0–10 000 | ODHAD; `katastr.md` r. 103 |
| **Součet** | | | **150 000** | pes 600 000 / opt 30 000 | |

Alternativa VB místo koupě pruhu: jednorázová náhrada podle posudku (ODHAD 30–50 % hodnoty pruhu = ~30 000) + stejný GP, posudek, vklad a právník = ~90 000, tedy levnější, ale slabší ochrana (`katastr.md` r. 106; `dane-financovani.md` r. 114: 30–200 tis.). SPÚ platí náklady GP, posudku a vkladu na oprávněném (vzorové smlouvy na smlouvy.gov.cz).

## 2. Rozpis – parkování (model: 300 000)

| Položka | Množství | Jedn. cena | Realisticky Kč | Pes / opt | Zdroj |
|---|---|---|---|---|---|
| Koupě pozemku pro 2 stání a manipulaci | 50 m² | 3 500 | 175 000 | pes 600 000 (100 m² × 6 000) / opt 60 000 (30 m² × 2 000) | cena pozemku viz výše |
| Geometrický plán, příplatek za druhou část a vytyčení | 1 | 6 000 | 6 000 | 3 000–12 000 | ODHAD |
| Zpevnění 2 stání, pojezdová zámková dlažba s podložím | 25 m² | 1 750 | 43 750 | pes 1 750 / opt 1 300 Kč/m² | 700–1 300 Kč/m² pochozí, 800–1 750 pojezdová na klíč (cenikzahrad.cz, daibau.cz, 4. 11. 2026); horní hranice jako rezerva |
| Zpevnění manipulační plochy a vjezdu | 25 m² | 1 750 | 43 750 | jako výše | totéž |
| Obrubníky, odvodnění, změna druhu pozemku (zahrada → ostatní plocha), případné odvody ze ZPF | 1 | 25 000 | 25 000 | 5 000–60 000 | ODHAD |
| Projekt stání, vyjádření úřadu, zákres do stavebního řízení | 1 | 6 500 | 6 500 | 3 000–15 000 | ODHAD; `uzemni-plan.md` r. 183 (poplatky) |
| **Součet** | | | **300 000** | pes 800 000 / opt 100 000 | |

## 3. Kontrola proti modelu

| | Model | Můj součet | Rozdíl |
|---|---|---|---|
| `pristup` | 150 000 | 150 000 | 0 % |
| `parkovani` | 300 000 | 300 000 | 0 % |
| Celkem | 450 000 | 450 000 | **0 %** |

- Žádná položka u mě není započtená dvakrát: GP, posudek, vklad a právník jsou jen v přístupu. V modelu (`model.py` r. 277, 289, 306, 359) jsou obě položky samostatné a V2 má parkování jen jednou, což sedí s jednou smlouvou o koupi.
- **Stačí 1 položka parkování i pro V2?** Ano. Položka je dimenzovaná na 2 stání (50 m²), což je přírůstkový požadavek V2. V1 potřebuje 1 stání (~25 m² pozemku, dlažba ~44 000 Kč, tedy parkování ~190 000 Kč), takže pro V1 je 300 000 mírně konzervativní (+110 000). Pesimistická hodnota 800 000 pokryje i výklad „celý dům“ (3–4 stání = 90–100 m²).
- Nezohledněno: DPH 21 % u prodeje pozemku, ztráta času (`pristup_mes` 9 měs. je při nájem → žádost → posudek → smlouva → vklad krátká, SPÚ obvykle 12–24 měs.; `uzemni-plan.md` r. 197), nejistota, zda je 2128/3 převoditelný (§ 6 zák. 503/2012, VPS/komunikace v ÚP) a zda podnět o změně č. 5 ÚP (BI → BH) nezmění podmínky.

## 4. Doporučení

**Beze změny** (`pristup` 600 000 / 150 000 / 30 000, `parkovani` 800 000 / 300 000 / 100 000). Součet vychází přesně a nová data (nabídky pozemků 2 400–3 800 Kč/m², dlažba 800–1 750 Kč/m²) leží uvnitř původního rozpětí 2–6 tis. Kč/m². Jediná poznámka: dodat do modelu na V1 samostatný zdroj, že stačí 1 stání (~190 000 Kč); rozdíl 110 000 Kč je pro V1 rezerva, ne chyba.

## 5. Pro report

```python
# přístup (realisticky 150 000)
[("Koupě pruhu pozemku SPÚ od ulice k domu (25 m² po 3 500 Kč)", 87500),
 ("Geometrický plán pro oddělení pruhu a stání", 18000),
 ("Znalecký posudek na cenu pozemku (platí kupující)", 15000),
 ("Právník: žádost, smlouva, jednání se SPÚ", 24500),
 ("Vklad do katastru nemovitostí", 2000),
 ("Nájem části pozemku SPÚ do převodu (asi 18 měsíců)", 3000)]

# parkování (realisticky 300 000)
[("Koupě pozemku pro 2 stání a manipulaci (50 m² po 3 500 Kč)", 175000),
 ("Geometrický plán: příplatek za druhou část pozemku", 6000),
 ("Zpevnění 2 parkovacích stání, zámková dlažba (25 m² po 1 750 Kč)", 43750),
 ("Zpevnění vjezdu a manipulační plochy (25 m² po 1 750 Kč)", 43750),
 ("Obrubníky, odvodnění, změna druhu pozemku", 25000),
 ("Projekt stání a vyjádření úřadu", 6500)]
```

## 6. Rozdělení parkování na pozemek a stavbu (4. 11. 2026)

Položka `parkovani` / `parkovani_1` je v modelu rozdělená na dvě:

| Vstup | Pes / real / opt | Kdy se platí | Kategorie v modelu |
|---|---|---|---|
| `parkovani_poz` (2 stání, s nástavbou) | 600 / 180 / 60 tis. | měsíc 0, spolu s přístupem (jedna smlouva se SPÚ) | „pozemek pro stání (SPÚ)“ |
| `parkovani_stavba` | 200 / 120 / 40 tis. | konec stavby (`t_hotovo`) | „parkování“ |
| `parkovani_1_poz` (1 stání, bez nástavby) | 600 / 110 / 30 tis. | měsíc 0 | „pozemek pro stání (SPÚ)“ |
| `parkovani_1_stavba` | 200 / 90 / 30 tis. | konec stavby | „parkování“ |

- Součty jsou stejné jako dřív (800/300/100 a 800/200/60 tis.), změnil se jen čas plateb.
- Pozemek se ve variantě D neodepisuje (stejně jako přístup).
- Dopad (real): čistý zisk beze změny, vlastní peníze V1 17,01 → 16,92 mil., Bn 16,61 → 16,52, B2n 10,68 → 10,63. Pozemek se platí dřív, ale stavba stání se přesunula z měsíce povolení na konec stavby, kdy už se čerpá úvěr.
- Když se ke koupi přidá zahrada od SPÚ, patří do stejné kategorie jako pozemek pro stání, ne do parkování.
