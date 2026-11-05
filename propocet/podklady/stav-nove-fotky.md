# Nové fotky a videa ze 4. 11. 2026 – co je nového

Zdroj: 36 fotek „WhatsApp Image 2026-11-04 at 13.32.*.jpeg“ a 3 videa „WhatsApp Video 2026-11-04 at 13.32.41/44/48.mp4“ v `photos/`. Kopie s krátkými názvy v `propocet/nove/` (`W01–W36.jpg`, snímky z videí po 1 s `V1/`, `V2/`, `V3/`, převodní tabulka `soubory.csv`, koláže `kolaz_*.jpg`). Popisy levným popisovačem: `nove/popisy-*.jsonl` (jen vodítko). Klíčové snímky (W02, W05, W10, W11, W12, W22, W24, W26–W29) jsem prohlédl sám.

## Co je na nich
- **W01** snímek inzerátu ČD, **W02** snímek regulativů ÚP (plocha BI).
- **Exteriér** W03, W06–W13, W18: plochá střecha s atikou, žebřík na fasádě, komín, svod; vstup s tabulkou 1598 (W13); **auto a dřevěná bouda u bočního vchodu na zpevněné ploše (W10)** – plocha je nejspíš na pozemku SPÚ 2128/3, kdo ji užívá, nevíme.
- **Společné prostory**: rozvaděče a stoupací vedení (W14, W15, W19, W33 – nálepky 2002), schodiště (W17), chodby (W16, W32, W36), kotelna s kotlem na tuhá paliva (W33), sklad (W31).
- **Byty**: V1 = byt C (žlutá kuchyň, modrý pokoj, zelený koberec, tmavá skvrna u okna obýváku V1/005); V2 = byt B (chodba se schodovitou trhlinou, růžové pokoje, kuchyň, koupelna, trhliny u stoupačky); V3 = byt E (WC, kuchyň s otlučeným obkladem, pokoj s parketami a šikmou trhlinou s opadanou omítkou V3/018); fotky W20–W30, W34–W35.

## Trhliny – přehodnocení (hlavní změna)
| Snímek | Co je vidět |
|---|---|
| W05 | svislá trhlina fasádou přes celý záběr, otevřená; podle prstů (1,5–2 cm) šířka **2–3 mm**, nahoře ~1 mm (pozn.: rychlý přehled mateřské session odhadoval 5–10 mm; po přeměření podle prstů 2–3 mm) |
| W11 | **trhlina dříve vyplněná bílým tmelem je znovu otevřená** (tmel roztržený, rezavé stopy); vedle druhá svislá trhlina 1–2 mm; **obě pokračují přes obklad soklu až do terénu/chodníku**; nad nimi vodorovná trhlina přes celou šířku |
| W08, W12, W18 | další svislé a šikmé trhliny fasádou od oken k soklu, do ~1 mm |
| W20, W22 | vodorovné trhliny ve styku strop–stěna, rozvětvené trhliny ve stropě a v rozích (2. NP) |
| W21, W26, W27, V3/018 | šikmé a schodovité trhliny přes stěny, **omítka opadaná až na cihly**, na W26 viditelný posun mezi řadami cihel |
| W24, V2 | vodorovné trhliny ve výšce ~1,5 m a kolem prostupu stoupačky stropem |
| W28, W31 | jemné vodorovné a svislé trhliny v chodbě bytu a ve skladu |

**Výklad (můj, ne posudek):** trhliny jsou v obou podlažích, na fasádě i uvnitř, svislé trhliny procházejí soklem do terénu a vyplněná trhlina se znovu otevřela. To ukazuje na **pohyb, který pokračuje** – nejspíš nerovnoměrné sedání základů (svislé trhliny přes sokl, schodovité trhliny), u trhlin pod stropem 2. NP může spolupůsobit teplotní pohyb nezateplené stropní desky ploché střechy. Kosmetická sanace nestačí. Rozhodne statik (sádrové terče / měrky, monitoring 6–12 měsíců, sondy k základům, geologie).

## Dopad na propočet (zapracováno do model.py 4. 11.)
- **Statické zajištění v realistickém scénáři**: `rizika_navic` 0,25 / 1,0 / 3,5 mil. Kč s DPH (opt sešití; real stažení táhly, sešití, ztužení, geologie, monitoring; pes podchycení / mikropiloty jako stav.md R6b). Dříve jen v textu jako riziko 5–10 % pravděpodobnosti.
- **Nástavby C1/C2**: `nastavba_statika` 0,5 / 2,0 / 2,5 mil. navíc (přitížení domu, který se hýbe → realisticky podchycení základů a věnec). **Bez posudku statika nástavbu nepovolovat ani nekupovat s ní v plánu** (podmíněná stopka).
- **Hodnota domu v dnešním stavu** (A0, A1, E) snížena na 5,0 / 7,5 / 11,0 mil., protože kupec odečte očekávané statické zajištění.
- Byty: nic zásadně nového k dispozicím; potvrzena plíseň/vlhkost u okna obýváku C (V1/005) a otlučená kuchyň E.

## Parkování podle ÚP (W02)
Doslovné znění regulativu BI (W02, shodné s `uzemni-plan.md`, ÚP s. 84): „parkování vozidel je nutné řešit na vlastním pozemku; pro přípustné využití na vlastním nebo k tomu účelu určeném pozemku“; „max. 2 nadzemních podlažích s využitelným podkrovím nebo ustoupeným podlažím“; „U novostaveb je podmínkou garáž v objektu nebo na vlastním pozemku“; „KZ = 0,65 z výměry pozemku do 800 m²“.
- Pozemek 2113/3 je jen půdorys domu → **každá změna, která vyvolá nová stání (B2n, C1, C2), potřebuje vlastní pozemek pro stání** – koupi části 2128/3 od SPÚ. Počet stání podle vyhl. 146/2024 (1 / 120 m² podlahové plochy bytů): B a B2 nemění plochu → bez nových stání; B2n +50 m² → 0–1; C1/C2 +120–130 m² → 1–2; při přepočtu celého domu 3–5.
- Není to výslovné vyloučení, ale **podmínka**: když SPÚ pozemek neprodá (nebo úřad nepřijme jiné „k tomu účelu určené“ místo), B2n/C1/C2 se nepovolí. V modelu `parkovani` 0,1 / 0,3 / 0,8 mil. Kč u B2n, C1, C2.
- KZ 0,65 se týká nových zástaveb; u stávajícího domu na pozemku = půdorys ho nelze splnit a nástavba půdorys nemění (výklad).

## Otázky navíc
- Statik: jsou trhliny aktivní? Sádrové terče na W05, W11, W26 a měření 6–12 měsíců; sonda k základům; geologie. Je dům vůbec zatížitelný nástavbou?
- ČD: proč byla trhlina na W11 vyplněná, kdy, a existuje statický posudek nebo záznam o sedání?
- SPÚ / soused: kdo užívá zpevněnou plochu s autem a boudou u bočního vchodu (W10)?
