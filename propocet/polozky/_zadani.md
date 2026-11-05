# Společné zadání – rozpis nákladových položek (4. 11. 2026)

Cíl: u **jedné nákladové položky** propočtu domu č.p. 1598, Jana Nohy, Benešov, ověřit částku a rozepsat ji na dílčí položky, které report ukáže v rozklikávacím řádku. Nic nepočítej od nuly, pokud to není nutné. Vezmi, co už je v podkladech, zkontroluj to a zpřesni.

## Dům (aktuální stav, má přednost před staršími podklady)
- Zděný bytový dům z roku 1981, 2 NP, plochá střecha, bez sklepa a výtahu. Zastavěná plocha 239 m², pozemek 2113/3 = jen půdorys domu. Přístup přes pozemek SPÚ 2128/3. Dům je odpojený od elektřiny, topí se kotli na tuhá paliva v kotelně, plyn tu není.
- Plochy podle NV 366/2013 (`/Users/martincerny/Documents/Benesov/dispozice.md`): byty A 4+1 80 m² (1. NP), B 67 m² (2. NP, dnes 2+1, bude 3+1), C 3+1 75 m² (2. NP), E 1+1 42 m² (2. NP) = 264 m². Nebytová část v 1. NP (dílna, sklady, kotelna) má 86 m² a přestaví se na 2 byty 2+kk po ~40 m². Společné prostory ~60 m².
- Trhliny 2–3 mm přes obě podlaží a sokl, vyplněná trhlina se znovu otevřela, takže sedání asi pokračuje (`propocet/podklady/stav-nove-fotky.md`).
- Dvě verze, které report ukazuje: **Bez nástavby (V1)** = 6 bytů, 344 m². **S nástavbou (V2)** = V1 + ustupující podlaží se 2 byty (150 m² hrubé, 120 m² čisté).
- Stavbu dělá buď **firma** (generální dodavatel, plátce DPH, stavební práce na bytový dům s DPH 12 %), nebo **vlastní dodavatelé** (řemeslníci, většinou neplátci; materiál investor kupuje s DPH 21 %).
- Kupující je fyzická osoba. Prodej po bytech je podnikání (§ 7), registrace k DPH a odpočet. Úvěr 70 % LTV.

## Model
- `propocet/model.py`: vstupy jsou ve slovníku `IN` (pesimisticky / realisticky / opt), výpočet ve funkci `projekt()`. Report `propocet/report.py` a `propocet/report.html` (sekce „1. Náklady“).
- Podklady: `propocet/podklady/*.md` (hlavně `stav.md` – rozpočet 5a/5b/5c, ceny a zdroje v kap. 4, rizika v kap. 3; `dane-financovani.md`; `uzemni-plan.md`; `marketing.md`; `katastr.md`), ověření `propocet/overeni/*.md`, postup a rozhodnutí `propocet/postup.md`.
- Rozhodnutí v `postup.md` schválená uživatelem (úroveň rekonstrukce „střední“, rezerva 15 %, bez zateplení, podlaha nebytové části bez zahloubení, lokalita 0,95…) **neměň**. Když s nimi nesouhlasíš, napiš to jen jako poznámku.

## Co odevzdat
Soubor `propocet/polozky/<tvůj-slug>.md`, česky a stručně:

1. **Rozpis**: tabulka dílčích položek. Sloupce: položka (srozumitelně, co se dělá nebo platí), množství a jednotka, jednotková cena, **realisticky Kč s DPH**, pes / opt (stačí rozpětí), zdroj (soubor + řádek/kapitola, nebo URL + datum; jinak „ODHAD“). Zpravidla 4–12 řádků. Dílčí položky musí dát dohromady tvůj realistický součet.
2. **Kontrola proti modelu**: hodnota v modelu (uvedená v tvém zadání), tvůj součet, rozdíl v % a proč. Co chybí, co je započtené dvakrát (i v jiné položce), co je navíc.
3. **Doporučení**: buď „beze změny“, nebo konkrétní nové hodnoty vstupů `IN[...]` (pes / real / opt) s jednou větou proč. Měň jen tehdy, když máš zdroj nebo jasnou chybu, ne kvůli drobnému rozdílu (pod 10 %).
4. **Pro report**: Python seznam řádků pro rozklikávací rozpis ve tvaru
   ```python
   [("krátký název dílčí položky (co a kolik)", realisticky_Kc_s_DPH), ...]
   ```
   Názvy do ~90 znaků, bez zkratek, které laik nezná. Součet = tvůj realistický součet.

## Pravidla
- Každé číslo potřebuje zdroj (soubor nebo URL s datem). Odhad bez zdroje označ „ODHAD“ a dej rozpětí. Ceny k listopadu 2026.
- Web: WebSearch / WebFetch. Prohlížeč jen v novém vlastním panelu a na konci ho zavři. CAPTCHA ani přihlášení neobcházej.
- **Nikomu nic neposílej.** Nepiš do žádného jiného souboru než svého výstupu. `model.py`, `report.py`, `postup.md` neupravuj.
- Fotky, pokud je potřebuješ: `propocet/nove/W01–W36.jpg` (4. 11.), `/Users/martincerny/Documents/Benesov/prace/prehledy/*.jpg` (koláže), popisy `propocet/nove/popisy-*.jsonl` (jen vodítko, popisovač se plete).
- Na konci vrať 3–5 vět: součet, rozdíl proti modelu, doporučení.
