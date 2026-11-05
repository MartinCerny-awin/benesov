# Koupě od ČD a poplatky (slug: koupe)

Kupní cena 8 326 000 Kč je fixní (minimum výběrového řízení ČD NB503213). Níže jen `IN["koupe_transakce"]`.

## 1. Rozpis (realisticky, Kč s DPH)

| Položka | Množství | Jedn. cena | Realisticky | Pes / opt | Zdroj |
|---|---|---|---|---|---|
| Kupní cena (fixní) | 1 | 8 326 000 | 8 326 000 | stejně | NB503213.pdf; katastr.md ř. 168–177 |
| Správní poplatek, vklad vlastnictví (kupní smlouva) | 1 návrh | 2 000 | 2 000 | 2 000 | ČÚZK, sazebník, položka 120 zák. 634/2004 Sb.; web ověřen 4. 11. 2026 (rešerše, komerční weby citují položku 120) |
| Správní poplatek, vklad zástavního práva banky | 1 návrh | 2 000 | 2 000 | 2 000 | stejně; banka poplatek obvykle nehradí. Podání elektronicky -20 % (1 600 Kč), nezapočteno |
| Elektřina: podíl na nákladech připojení, hlavní jistič 3×63 A | 63 A | 800 Kč/A | 50 400 | až 80 000 / 25 000 | vyhl. 16/2016 Sb. dle blogu (nepotvrzeno u ČEZ), rešerše 4. 11. 2026 |
| Elektřina: žádost přes portál, smlouva o připojení, přepojení měření, drobné práce distributora | 1 | | 9 600 | | ODHAD (ceník ČEZ Distribuce od 1. 2. 2026: obnovení dodávky nn jen 1 815 Kč, tedy jen při zachovaném odběrném místě) |
| Daň z nabytí nemovitých věcí | | | 0 | 0 (pes v katastr.md 332 tis. jen pro případ, že by platila) | zák. 386/2020 Sb., dane-financovani.md ř. 12, 92, 195 |
| **Součet transakce** | | | **64 000** | **124 000 / 34 000** | |

## 2. Kontrola proti modelu

- Model 64 000 Kč (pes 124 000, opt 34 000). Advokát a odhad pro banku vyřazeny 4. 11. 2026. Pes: 4+120 tis., opt 4+30 tis.
- Daň z nabytí: zrušena (386/2020 Sb.), v modelu správně 0. Text na webu ČD je zastaralý.
- Vklad: 2 000 Kč za návrh, 2 návrhy = 4 000, sedí. Pozor, pes 120 tis. na elektřinu je vysoký, ale kryje scénář zrušeného odběrného místa, nového hlavního jističe pro TČ (3×100 A = 80 tis.) a studie přípojky.
- Dvojí započtení: rekonstrukce „Hlavní elektro“ (stav.md ř. 208, real 330 tis. bez DPH; rozpocet-2.md ř. 128) kryje elektroměrový rozvaděč, elektroměry, stoupačky, společné osvětlení a revizi. Moje položka obsahuje jen to, co platí distributorovi (podíl na nákladech, žádost, smlouva), takže se nepřekrývá. Revizi elektro před připojením sem nepatří (je v rekonstrukci). Elektroměry dodá a plombuje distributor v rámci připojení.
- Co v modelu nikde nevidím: dočasné napájení stavby (rozpocet-2.md ř. 79, 10/20/35 tis.), pokud ho rekonstrukce nekryje. Je to mimo tuto položku, jen upozornění.
- Riziko ztráty rezervovaného příkonu a nové přípojky (stav.md R8, 0/150/400 tis.) je v rizicích rekonstrukce, ne zde. Navýšení příkonu pro TČ (stav.md ř. 228) také ne zde.

## 3. Doporučení

Beze změny. Rozdíl 0 %, všechny hodnoty jsou ve zdrojích nebo označeny jako odhad. Jediná slabina je elektřina (60 tis., ODHAD): upřesní se po dotazu u ČEZ Distribuce, zda odběrné místo ještě existuje.

## 4. Pro report

```python
[
    ("Poplatek za vklad vlastnictví do katastru (2 000 Kč)", 2_000),
    ("Poplatek za vklad zástavního práva banky (2 000 Kč)", 2_000),
    ("Obnovení elektřiny: podíl na připojení 3×63 A u distributora", 50_400),
    ("Obnovení elektřiny: žádost, smlouva, přepojení měření (odhad)", 9_600),
]
```
Součet 64 000 Kč. Kupní cena 8 326 000 Kč se přičítá zvlášť.
