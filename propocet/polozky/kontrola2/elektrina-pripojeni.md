# Kontrola 2: Elektřina, obnovení připojení (5. 11. 2026)

Web: real 60 tis. (podíl 50 + žádost, smlouva, přepojení 10). Zdroje: `polozky/koupe.md` ř. 12–13 (podíl 63 A × 800 Kč/A = 50 400; ostatní 9 600 ODHAD), `podklady/stav.md` R8 ř. 99 (příkon a přívod 0/150/400 tis., v rizicích), `podklady/katastr.md` ř. 171 (obnovení na náklady kupujícího), `overeni/rozpocet-2.md` ř. 79 (dočasné napájení 10/20/35 tis. bez DPH).

**Poctivé omezení:** sazbu Kč/A a pravidlo pro zrušené odběrné místo jsem na webu 5. 11. 2026 nedohledal (WebSearch/WebFetch vrátily jen starší PDF ČEZ z let 2018–2020 a tiskovou zprávu ČEZ Distribuce https://www.cez.cz/cs/pro-media/tiskove-zpravy/jednodussi-cesta-k-pripojeni-i-vice-kapacit-pro-nove-zajemce.-cez-distribuce-oslovi-39-tisic-zakazniku-237055 – ta uvádí jen nevratnou část podílu pro NN = 0 %, ne Kč/A). Sazba 800 Kč/A pochází z blogu v koupe.md, není ověřená u ČEZ. Vše níže, co tím závisí, je ODHAD.

## 1. Tabulka

| Položka | web | můj real | pes–opt | potřeba | nejlevnější cesta | zdroj |
|---|---|---|---|---|---|---|
| Podíl na připojení 3×63 A (při zrušeném OM) | 50 | 50–80 (viz výpočet jističe; 80 při 3×100 A) | 120–25 | ano, bez elektřiny nejde stavba ani kolaudace/prodej | žádná; jen snížit počet A (viz bod 5) | koupe.md ř. 12; 800 Kč/A nepotvrzeno |
| Žádost, smlouva, přepojení měření | 10 | 10 (obnovení dodávky u zachovaného OM jen 1,8 tis.) | 15–2 | ano | žádost přes portál sám, 0 Kč | koupe.md ř. 13 (ceník ČEZ od 1. 2. 2026) |
| Staveništní rozvaděč + dočasné napojení (chybí) | 0 | 20 | 35–10 | ano | elektrikář s pronájmem rozvaděče | rozpocet-2.md ř. 79 |
| Přípojka (kabel, SR/SS skříň), jen když ji ČEZ odstranil | 0 (v R8) | 0 v položce | R8: 400–0 | jen když… | distributor staví do 50 m z vlastních, skříň na pozemku investor | R8, ODHAD |

## 2. Jaký hlavní jistič (ČSN 33 2130 / PNE 33 0000-1, ODHAD výpočtu)
- 6 bytů × 9 kW (el. vaření) = 54 kW, soudobost β = 0,2 + 0,8/√n = 0,53 → 28,5 kW.
- Bojlery 6 × 2 kW, soudobost 0,5 → 6 kW. Společné 3 kW.
- 2 TČ 16 kW: elektrický příkon ~5 kW každá = 10 kW, dotopné patrony 2 × 6 kW = 12 kW (nejhorší mrazový den).
- Součet ≈ 60 kW → 87 A → **3×100 A**. Bez provozu patron (blokace) ≈ 48 kW → 70 A → 3×80 A. **3×63 A (web) stačí jen s omezením patron a bojlerů (blokovací relé)**, jinak je podhodnoceno. Navýšení pro TČ je podle koupe.md ř. 24 už v R8 / stav.md ř. 228, ne zde: je to hranice mezi položkami, ne dvojí započtení.
- Podíl: 100 A × 800 = 80 tis. při zrušeném OM; při zachovaném OM platí jen přírůstek nad dosavadním jističem (např. 63 → 100 A = 30 tis.; dosavadní hodnota je neznámá, 4 elektroměry z RÚIAN naznačují 4 × 3×25 A). Nová OM bytů: zjistit u ČEZ, zda se podíl počítá za každé OM zvlášť a zda 3×25 A na byt je zdarma (ve starších podmínkách ČEZ je limit 3×25 A pro domácnosti). Pokud ano, 6 bytů × 3×25 A neplatí nic a platí jen OM pro TČ a společné (~3×40 A: (40−25)×800 = 12 tis.). To je největší možná úspora, ale NEOVĚŘENO.

## 3. Součet
| | tis. |
|---|---|
| Web | 60 |
| Můj real (podíl 60 uprostřed + 10 + staveništní 20) | 90 |
| Nejlevnější rozumná (OM po bytech ≤ 25 A, žádost sám, staveništní rozvaděč 10) | ~30 |

Rozdíl real vs. web +50 %, hlavně chybějící staveništní rozvaděč a jistič pro TČ. Elektro práce a revize jsou jinde, svépomoc u elektra nenavrhuji.

## 4. Chybí / dvakrát
- **Chybí staveništní rozvaděč a dočasné napojení ~20 tis.** (10–35). Spotřeba energie je v `drzeni_mes` (model.py ř. 97), rozvaděč ne; ověřit, zda není v režii „zařízení staveniště“.
- **Věcné břemeno / přístup:** pozemek je jen půdorys, případná nová přípojka vede přes pozemek SPÚ 2128/3, takže potřeba souhlasu a zřízení břemene (náklad v položce SPÚ, ne zde). Dále stanovisko Správy železnic ke stavbě.
- Dvakrát nic. Elektroměrový rozvaděč a revize jsou v „Hlavní elektro“ 330 tis. bez DPH (stav.md ř. 208); elektroměry dodává a plombuje distributor v rámci připojení.
- Termín: ČEZ vyřizuje žádost týdny až měsíce; bez připojení nelze zahájit práce na TČ a zkoušky.

## 5. Doporučení
Změnit real na **80 tis.** (podíl 50 + žádost 10 + staveništní rozvaděč 20; při jističi 3×100 A po sečtení až 110), pes beze změny 120, opt 25. Důvod: chybí staveništní napájení a 63 A nekryje TČ s patronami. Před kupní nabídkou 16. 11. se zeptat ČEZ Distribuce: (1) existuje OM a jaký je rezervovaný příkon, (2) sazba Kč/A pro NN 2026 a pravidlo na OM, (3) zda je přípojka a skříň fyzicky na místě.
