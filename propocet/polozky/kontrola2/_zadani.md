# Kontrola nákladů po položkách, kolo 2 (5. 11. 2026) – společné zadání

Kontroluješ **jednu nákladovou položku** propočtu koupě, rekonstrukce a prodeje po bytech domu č.p. 1598, Jana Nohy, Benešov. Čísla jsou z webu https://benesov.noirloop.com (tabulka „1. Náklady“, scénář **realisticky**, verze **bez nástavby**, pokud zadání neříká jinak), tis. Kč s DPH.

## Na co odpovídáš (u každé dílčí položky)
1. **Je potřeba?** Musí se to dělat, aby šly byty prodat (kolaudace/revize, banka kupce, zákon), nebo je to „hezké mít“? Co se stane, když se to vynechá nebo odloží?
2. **Je cena nadsazená, nebo podhodnocená?** Spočítej zdola: množství × jednotková cena (listopad 2026), se zdrojem. Porovnej s hodnotou na webu.
3. **Jde to levněji jinak?** Tři cesty: **firma** (plátce DPH, faktura 12 % na bytový dům), **řemeslník** (OSVČ neplátce, materiál kupuje investor s DPH 21 %), **svépomocí** (investor s kamarády, jen materiál). U svépomoci odhadni hodiny práce a řekni, jestli to laik zvládne a jaké je riziko (záruka vůči kupcům bytů, revize, statik, pojišťovna). Nenavrhuj svépomoc u věcí, které ze zákona dělá osoba s oprávněním (elektro revize, plyn, chladiva, statika).
4. **Co chybí nebo je dvakrát?** Náklad, který v položce chybí (nebo v celém rozpočtu), a co je započtené i v jiné položce (seznam všech položek je dole).

## Dům (aktuální stav)
- Zděný bytový dům z roku 1981, 2 NP, plochá střecha, bez sklepa a výtahu, zastavěná plocha 239 m². Pozemek = jen půdorys, přístup přes pozemek SPÚ 2128/3. Odpojený od elektřiny, kotle na tuhá paliva, plyn není.
- Byty A 4+1 80 m² (1. NP, už zrekonstruovaná koupelna), B 2+1 67 m² (zůstává 2+1), C 3+1 75 m², D 1+1 42 m² (2. NP) = 264 m². Nebytová část v 1. NP (dílna, sklady, kotelna) 86 m² → 2 byty 2+kk po ~40 m². Verze **bez nástavby** = 6 bytů, 344 m²; **s nástavbou** + ustupující podlaží se 2 byty (120 m²).
- Trhliny 2–3 mm přes obě podlaží a sokl, vyplněná trhlina se znovu otevřela → sedání asi pokračuje.
- Kupuje fyzická osoba, prodává po bytech sama (bez realitky), registrace k DPH (§ 56: rekonstrukce > 30 % a prodej do 23 měs. → prodej bytů s DPH 12 %, odpočet DPH na vstupu). Architekt je Ondřej zdarma.
- Stavba se dělá kombinací firma + řemeslníci (štítek u každé dílčí položky). Řemeslník neplátce: z jeho práce se DPH neodečítá, z materiálu se odečte 21 %. Svépomoc proto ušetří méně, než ukazují čísla s DPH – zohledni to.

## Důležité o číslech na webu
- Čísla v tvém zadání jsou z webu k 5. 11. 13:44. Model mezitím upravují jiná sezení, takže si na začátku přečti aktuální hodnotu své položky (WebFetch https://benesov.noirloop.com, scénář realisticky, nebo lokální `/Users/martincerny/Documents/Benesov/web/index.html`) a pracuj s ní.
- Dílčí položky v rozpisu jsou **dopočtené na součet z modelu**: vlastní odhady z `propocet/polozky/*.md` se v reportu poměrně škálují, u stavby zhruba **× 1,17** (rezerva v realistickém scénáři je zrušená a ta přirážka teď funguje jako rezerva). Porovnávej proto svůj součet hlavně s hodnotou celé položky.
- Model: `propocet/model.py` (vstupy ve slovníku `IN`: pes / real / opt; výpočet `projekt()`), report `propocet/report.py` (seznamy dílčích položek `POL`, ř. ~254–380). **Na model.py a report.py souběžně pracují jiná sezení – jen čti.**

## Podklady
- Starší rozpis a zdroje k položce: `propocet/polozky/<soubor>.md` (uvedený v tvém zadání), ceny a stav domu `propocet/podklady/stav.md` (rozpočet 5a/5b/5c, ceny kap. 4, rizika kap. 3), `propocet/podklady/stav-nove-fotky.md`, nezávislý rozpočet `propocet/overeni/rozpocet-2.md`, dispozice a plochy `/Users/martincerny/Documents/Benesov/dispozice.md`, rozhodnutí `propocet/postup.md`.
- Fotky: `propocet/nove/W01–W36.jpg`, koláže `/Users/martincerny/Documents/Benesov/prace/prehledy/*.jpg`, popisy `propocet/nove/popisy-*.jsonl` (jen vodítko).
- Web: WebSearch / WebFetch pro ceny 2026 (e-shopy, ceníky firem, kalkulačky, ÚRS). Uveď URL a datum.
- **Rozhodnutí uživatele neměň, jen k nim připiš poznámku, když nesouhlasíš:** statické zajištění pevně 1,5 mil.; rezerva v realistickém scénáři zrušená; byt B zůstává 2+1; koupelny B, C, D jen obnova; bez zateplení fasády; podlaha nebytové části bez zahloubení; architekt zdarma; prodej bez realitky; úvěr 9–10,5 %.

## Seznam všech položek (kvůli dvojímu započtení), real bez nástavby, tis. Kč s DPH
Koupě od ČD 8 330 · Pozemek SPÚ přístup a stání 236 · Střecha 1 063 · Vytápění TČ 1 230 · Rozvody domu 810 · Sanace trhlin 450 · Společné prostory 166 · Byty elektro a voda 707 · Byty bourání, omítky, podlahy, malby 1 076 · Byty koupelny, kuchyně, okna, dveře 1 471 · Zateplení fasády (nedělá se, 0; kdyby ano 1 200) · Statické zajištění 1 500 · Nebytová část → 2 byty 3 071 · Ustupující podlaží (jen s nástavbou) 9 861 · Projekt, dozor, statik 390 · Parkovací stání stavba 90 · Elektřina obnovení připojení 60 · Úroky a poplatky úvěru 1 382 · DPH z prodeje po odpočtu 1 792 · Prodej bytů 63 · Ostatní (držení, PENB, rozdělení, s. r. o.) 279. Stavba celkem 12 085, náklady celkem 24 165.

## Co odevzdat
Soubor `propocet/polozky/kontrola2/<slug>.md` (slug v tvém zadání), česky, stručně:

1. **Tabulka po dílčích položkách**: položka · web (tis.) · tvůj odhad real (tis., s DPH) · pes–opt · potřeba (ano / ne / jen když…) · nejlevnější rozumná cesta (firma / řemeslník / svépomoc) a kolik ušetří · zdroj (soubor + řádek nebo URL + datum; jinak „ODHAD“).
2. **Součet**: web vs. tvůj realistický odhad (při současném rozdělení firma/řemeslník) vs. nejlevnější rozumná varianta se svépomocí. Rozdíl v % a hlavní důvod.
3. **Chybí / dvakrát / podhodnocené**: konkrétně, s částkou.
4. **Doporučení**: „beze změny“, nebo nová hodnota položky (real, případně pes/opt) s jednou větou proč. Měň jen při rozdílu ≥ 10 % nebo jasné chybě.

## Pravidla
- Každé číslo potřebuje zdroj; bez zdroje „ODHAD“ s rozpětím. Ceny k listopadu 2026.
- Nepiš do žádného jiného souboru než svého výstupu. Nikomu nic neposílej, nic nekupuj, nic neodesílej.
- Prohlížeč jen ve vlastním novém panelu a na konci ho zavři; CAPTCHA ani přihlášení neobcházej.
- Na konci vrať 3–5 vět: web vs. tvůj součet, nejlevnější rozumná varianta, doporučení.
