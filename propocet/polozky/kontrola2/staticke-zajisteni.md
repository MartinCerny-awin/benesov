# Kontrola 2: Statické zajištění domu (5. 11. 2026)

Rozhodnutí uživatele: pevně 1 500 tis. ve všech scénářích bez posudku (`model.py` ř. 66, `rizika_navic`). **Neměním, jen posuzuji.**

**Důležité k číslům na webu:** `rizika_navic` se v modelu neškáluje. Dílčí řádky na webu (221 / 516 / 221 / 197 / 345) jsou původní rozpis `polozky/strecha-statika.md` (118 / 275 / 118 / 105 / 184 = 800 tis.) přepočtený poměrem 1 500/800 = 1,875 (`report.py` ř. 327–332). Skutečné práce v rozpisu jsou tedy 800 tis., a **vše nad to (700 tis.) je de facto rezerva**, ne jen 345 tis. Řádky na webu proto nejsou cena prací.

## 1. Tabulka po dílčích položkách (tis. Kč s DPH, real bez nástavby)

| Položka | Web | Můj real | Pes–opt | Potřeba | Nejlevnější rozumná cesta | Zdroj |
|---|---|---|---|---|---|---|
| Geologický průzkum a sondy (3 vrty, 2 odkopy) | 221 | **110** | 200–70 | **Ano, před jakýmkoli podchycením**; statik bez něj nenavrhne zajištění, bez něj by se táhla dělala naslepo. Vynechat jde jen pro scénář „ustalo“ (stačí 2 sondy k patě základu, ~40) | Firma (IG organizace s oprávněním). Svépomoc: ruční odkopy 2 × (1,5 × 1 × 1,5 m) ≈ 16 h/2 lidé, ušetří ~10 | 3 vrty × 6 m = 18 bm × 2 100 Kč/m (ageologie.cz/cenik) 38 + penetrace 12 bm × 900 = 11 + 2 odkopy bagrem 12 + laboratoř 10 + zpráva 15 + doprava 5 = ~90 bez DPH → 110 s 21 %. Typický IG pro RD 14–25 tis., rozšířený 40–80 tis. (ageologie.cz, aikatastr.cz/poradna/zakladove-pomery, geokomplet.cz, 5. 11. 2026). Přístup: pozemek je jen půdorys, vrtná souprava stojí na SPÚ, potřeba souhlas |
| Ocelová táhla, stažení domu (12 ks) | 516 | **330** | 500–200 | **Ano jako standard** pro zděný dům s trhlinami přes sokl a oba podlaží; levné ve srovnání s podchycením, zastaví rozevírání. Nezastaví ale sedání | Řemeslník (práce bez DPH, materiál 21 %), ~−40. Svépomocí **ne** (statik navrhuje sílu předpětí, kotvení) | Materiál: tyč Ø20–24, 10 m, 2 desky, matice, napínák ≈ 6 tis./ks příčné, ~12 tis. podélné = ~85 + práce 12 × 14 (průchody zdí, kotvení, napnutí, začištění) = 170 → ~330 s DPH. Tržní poptávky: roh domu 40–80 tis., celý dům 10 × 10 m 50–200 tis. (nejremeslnici.cz/poptavka/809218, epoptavka.cz poptávky 3536364, 4282868; 2019–2023, ne nabídky). Dům 25 × 9,5 m 2 NP je 2–3× větší než 10 × 10 |
| Ztužení: překlady, lokální věnec | 221 | **170** | 250–80 | **Jen když** statik potvrdí poddimenzované překlady (F/090113113) | Řemeslník, ~−15. Svépomocí ne | 3 překlady × ~15 tis. + lokální věnec/ocelový prvek ~100; ODHAD 100–250 |
| Lokální zesílení základů (~10 bm) | 197 | **140** | 250–80 | **Jen když** sondy ukážou, že roh/štít klesá; při „ustalo“ vynechat | Firma (záruka, statik). Svépomoc: ruční výkop ~18 m³ ≈ 36 h, ušetří ~10–15 tis., zbytek (podbetonování po úsecích, injektáž) ne | Odkop 7 + beton 5 m³ s bedněním a výztuží 30 + cementová injektáž 30 + hydroizolace a zásyp 20 ≈ 90–120 bez DPH → 100–135 s 12 %; podchycení po úsecích 6–10 tis./bm (ODHAD, daibau.cz/clanek/961: sanace základů RD od 130 tis.) |
| Rezerva na rozsah (30 %) | 345 | **240** (30 % z 800) | – | Ano, posudek zatím není | – | 30 % z 750 přímých + 50 projekt zajištění (viz kap. 3) |
| **Součet** | **1 500** | **~1 040** | – | | | |

## 2. Součet

| | tis. Kč |
|---|---|
| Web (pevně) | 1 500 |
| Můj real při současném rozdělení firma/řemeslník, scénář „lokální zajištění, bez podchycení“ | ~1 040 (−31 %) |
| Nejlevnější rozumná varianta (řemeslník na táhla a ztužení, ruční odkopy) | ~975 (−35 %) |

Svépomoc zde šetří jen ~25–40 tis. (2–4 %), protože zbytek je nosná konstrukce, kterou dělá firma podle statika. Rozdíl 31 % je dán tím, že 1 500 už obsahuje 700 tis. rezervy.

### Scénáře: „sedání ustalo“ vs „aktivní“ (celkem s DPH, mil. Kč)

| Scénář | Co se dělá | Cena | Poznámka |
|---|---|---|---|
| **Ustalo** (sezónní pohyb, teplota nezateplené stropní desky, staré sedání) | 2 sondy 40–110, táhla jen část (6 ks) ~170, překlady 60–120, sešití v Sanaci trhlin | **0,4–0,6** | Hotovo po 6–12 měsících monitoringu terčů. 1 500 je 2,5–3× nadsazené |
| **Aktivní, lokální** (roh/štít, jedna strana) | geologie 110 + táhla 330 + ztužení 170 + lokální podchycení 10–20 bm po úsecích nebo geopolymer ~300–600 (celkem po zaokrouhlení) | **1,0–1,5** | 1 500 sedí přesně |
| **Aktivní, celý dům** | geologie 110 + táhla 330 + ztužení 170 + mikropiloty (obvod 68 bm, rozteč 1,5 m ≈ 45 ks × 7 m ≈ 315 bm × 3 000 = 945 bez DPH) + převázání roznášecími prahy 68 bm × 4 000 = 270 + bourání podlah, odkopy ≈ 1,8–2,8 | **2,4–3,4** | 1 500 pokryje jen polovinu. Souhlasí s `stav.md` R6b (3,5 mil. pes) |

Subjektivní váhy 30 % / 35 % / 35 % (ODHAD, dům z 1981 stojí 45 let, ale znovu otevřená trhlina a trhlina přes sokl do terénu mluví pro pohyb) dávají střední hodnotu 0,3 × 0,5 + 0,35 × 1,25 + 0,35 × 2,9 ≈ **1,6 mil.** Pevných 1,5 mil. je tedy **přibližně rovno očekávané hodnotě**. Při neznalosti posudku je to rozumná pojistka, ne nadsazení ani podhodnocení.

### Typická sanační opatření pro zděný dům 2 NP s trhlinami 2–3 mm od sedání (ceny ČR 2026)

| Metoda | Kdy | Cena | Zdroj |
|---|---|---|---|
| Sešití trhlin spirálou / injektáž | Vždy po stabilizaci, neřeší příčinu | 1 800–3 500 Kč/bm | rozpocet-2.md ř. 122; už v Sanaci trhlin |
| Ocelová táhla, stažení | Rozevírání trhlin, chybí věnec | 40–200 tis. za dům (RD 10 × 10) | nejremeslnici.cz, epoptavka.cz (poptávky, ne nabídky) |
| Podbetonování / lokální podchycení po úsecích | Mělké základy, lokální pokles | 6–10 tis./bm (ODHAD) | daibau.cz/clanek/961, sanace základů od 130 tis. |
| Mikropiloty | Aktivní sedání, nesoudržná zemina, hloubka únosné vrstvy 5–8 m | 1 500–4 500 Kč/bm vrtu (u starších budov až 5 000) | mikropiloty24.cz, nejstav.cz/clanky/detail/4810, 4676; poptávka 20 bm × 6 m ≈ 600 tis. (poptavky.cz) |
| Injektáž zeminy pryskyřicí/geopolymerem (URETEK apod.) | Slabá vrstva do ~3–6 m, bez nutnosti vrtat hluboko, rychlé (1–2 dny) | **cena nenalezena veřejně, ODHAD 250–600 tis. pro dům 239 m²**, jen na poptávku po prohlídce | Hledání 5. 11. 2026 cenu URETEK nenašlo |

Geopolymer by byl pro „aktivní lokální“ varianta levnější než mikropiloty a bez výkopů v domě, ale: statik musí potvrdit vhodnost, zrovna na vlhčí zeminy s nízkou pevností, a firma dává záruku jen na zvednutí, ne na příčinu (voda, odvodnění). Doporučuji požádat o nabídku u jedné firmy hned po geologii jako alternativu k mikropilotám.

## 3. Chybí / dvakrát / podhodnocené

- **Dvakrát: ne.** Statické zajištění nesmí obsahovat sešití spirálou a neobsahuje (rozpis výše). Sanace trhlin má 178 tis. (web 270) na 70 bm sešití + omítky + dlažba chodeb a zábradlí (72 + 57 tis., s trhlinami nesouvisí, jen s „Sanací“ v názvu). Zbytek (monitoring, posudek) je v „Projekt, dozor, statik“ (110 tis. „posudek trhlin a návrh sanace“).
- **Jemné překryvy:** po osazení táhel půjde snížit rozsah sešití (táhla zabraňují dalšímu rozevírání), možná −30–40 % z 178 = **−50–70 tis.** v Sanaci trhlin. Do odhadu nepromítám.
- **Chybí 50 tis.:** projekt zajištění (výkres táhel, podchycení) a autorský dozor statika po posudku. Posudek 110 tis. v projektu pokrývá „návrh sanace“, ale ne prováděcí výkresy a dozor při napínání.
- **Chybí 15–30 tis.:** monitoring terčů/trhlinoměrů 6–12 měsíců včetně odečtů (levné terče stovky Kč, ale odečty statika).
- **Chybí (jen scénář aktivní):** hydroizolace a odvodnění kolem domu (drenáž, chodník s odvodem od soklu) 100–250 tis.; bez nich sedání pokračuje i po podchycení. Pozemek je jen půdorys, drenáž leží na SPÚ, je třeba souhlas.
- **Termín:** zajištění musí předcházet sešití a vysprávkám (jinak se trhlina znovu otevře, viz W11) a kosmetice bytů. Monitoring tedy zdržuje práce o 6–12 měsíců, hodí se zahájit hned po koupi.
- **Je potřeba pro prodej:** ano. Banka kupce i znalec si vyžádají posudek statika a doklad o provedení; byty s viditelnými trhlinami bez dokladu se prodávají s odpočtem.

## 4. Doporučení

**Beze změny (1 500 tis. real).** Je to přibližně očekávaná hodnota napříč scénáři (~1,6 mil.), pokrývá lokální aktivní scénář celý a v „ustalo“ je záměrně velká rezerva. Poznámka k rozhodnutí: pokud se potvrdí aktivní sedání celého domu, 1 500 bude **podhodnoceno o 1–2 mil.**, proto je vhodné nechat pes na 3,5 mil. v textu rizik (R6b) a po geologii a prvním měsíci monitoringu hodnotu přehodnotit. Pro reportér: do popisu doplnit, že ~700 tis. z 1 500 je rezerva, ne jen „30 %“ (rozpis na webu je škálovaný ×1,875 a klame o jednotlivých cenách).
