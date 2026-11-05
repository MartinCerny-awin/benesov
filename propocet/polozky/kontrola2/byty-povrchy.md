# Kontrola 2: Byty – bourání, omítky, podlahy, malby (5. 11. 2026)

Web (real, bez nástavby): **1 076 tis.** s DPH = 248 + 164 + 363 + 128 + 173. Model: `kosmetika` real 800 tis. × stavba_mult × adj (`model.py` ř. 45, 310). Dílčí položky v `report.py` ř. 279–284 mají základ 128 / 111 / 333 / 89 / 89 = 750 tis. a na web se škálují jinak, než píše zadání (u bourání ×1,9, u podlah ×1,1). Rozpis na webu proto není úměrný základu, rozhoduje součet.

Odhady jsou v tis. Kč s DPH, při současném rozdělení: práce řemeslníka OSVČ neplátce bez DPH, materiál s 21 %, kontejnery s DPH.

## 1. Tabulka

| Položka | Web | Můj real | pes–opt | Potřeba | Nejlevnější rozumná cesta | Zdroj |
|---|---|---|---|---|---|---|
| Bourání, vyklizení, odvoz suti | 248 | **117** | 175–70 | Ano. Bez vyklizení a odstranění lina a koberců se nedá pokládat ani malovat. | Svépomoc: vyklizení a demontáž ~170 h, zbývají kontejnery a ochranné pomůcky (~55). Úspora ~62. | viz 2.1 |
| Omítky a zapravení (264 m²) | 164 | **140** | 200–90 | Ano, ale rozsah je zapravení drážek, ostění a lokální štuk, ne omítání 264 m². Vynechat nejde, malba by ukázala drážky. | Drážky a zárubně zapravit svépomocí (~120 h): úspora ~50. Štuk pod malbu raději řemeslník. | viz 2.2 |
| Podlahy (vinyl B+C 129 m², brus D, koberce A 40 m²) | 363 | **235** | 330–175 | Ano. Banka ani kupci nevyžadují novou podlahu, ale B (potěr se sutí) a C (lino, PVC) se prodat bez podlahy nedají. D a A mohou jít levněji. | Click vinyl kladený svépomocí (~100 h vč. stěrky): úspora ~50. Brus parket nechat firmě. | viz 2.3 |
| Malba bytů (845 m²) | 128 | **100** | 145–70 | Ano. Je to nejlevnější úprava s největším vlivem na cenu. | Svépomoc ~100 h: úspora ~68. Malíř 70–100 Kč/m². | viz 2.4 |
| Plísně, drobné opravy, generální úklid | 173 | **70** | 120–40 | Plísně: ano, ale jen lokálně a až po střeše. Drobné opravy: z velké části už jsou v oknech, dveřích a elektru. Úklid: ano. | Svépomoc (~40 h úklid, fungicid): úspora ~35. | viz 2.5 |
| **Součet** | **1 076** | **662** | **970–445** | | **Svépomoc: ~420** (úspora ~240) | |

## 2. Podklady k položkám

### 2.1 Co se v bytech vlastně bourá
- Koupelny a WC B, C, D jsou jen obnova (nátěr obkladu, sanita, baterie): žádné bourání. Kuchyně se mění, ne přestavují: demontáž 3 linek (B rozbitá, D otlučená, C původní) a obkladů nad nimi. Byt A linku a koupelnu zachovává. Byt B zůstává 2+1, příčka v B je jiná položka.
- Bourá se tedy hlavně podlahová krytina: lino a PVC v B a C (`stav.md` ř. 63–70, popisy fotek), 3 koberce v A (~40 m²), celkem ~170 m². Dále drážky pro elektro (suť a drážkování jsou v položce elektro).
- Vyklizení: B je plný harampádí (`stav.md` ř. 21), D rozpracovaný, C a A obývané/opotřebené. Odhad ~17 m³ nábytku a věcí + ~5 m³ krytin + ~5 m³ kuchyňských linek a obkladů + ~5 m³ ostatní suti = **~32 m³**, tedy **~10 kontejnerů 3 m³ po ~5 000 Kč = ~50 tis.** (rozpětí 8–12 kusů × 3,5–5,6 tis. = 28–67 tis.). ODHAD objemu, ověřit na místě.
- Cena kontejneru 3 m³ 2026: sběrný dvůr Kamenice (zóna 16–20 km, tedy Benešov) 5 000–5 600 Kč s DPH, platný od 5. 5. 2026, https://www.obr-odpady.cz/cz/ceniky/ (5. 11. 2026). Další ceníky: Bikramka 3 497 s DPH (suť, platí od 1. 1. 2026, Benešov nepotvrzen) https://bikramka.cz/odvoz-suti-zeminy-a-odpadu/, odvoz-suti.cz 4 477 https://www.odvoz-suti.cz/cenik/, Hladík 4 538 https://hladik-odpady.cz/cenik-kontejnery-3-t. Směsný odpad z vyklizení je dražší než čistá suť, proto počítám 5 000.
- Demontáž krytin 170 m² × 120 Kč = 20 tis. (S2 `stav.md` ř. 116: demontáž 80–200 Kč/m²), demontáž 3 linek 3 × 4 tis. = 12, vyklizení brigádou ~30, ochranné pomůcky ~5. Součet 117.
- Web 248 odpovídá zhruba dvojnásobku. Starý rozpis (vyklizení 100 + bourání 120 tis. bez DPH, `stav.md` ř. 146, `byty.md`) počítal i dílnu, sklady a kotelnu, které patří do položky nebytové části (`byty.md` kap. 2), a bourání koupelen, které se už nedělá.
- Riziko azbestu: u lina a lepených dlaždic z 80. let je možné. Průzkum vzorku 3–5 tis. (ODHAD); nebytová část ho už má ve své položce, tady chybí.

### 2.2 Omítky
- `stav-garant.cz` omítka 280–620 Kč/m² platí pro celé omítání, ne pro zapravení (S1, `stav.md` ř. 115). Web ale počítá plošně 264 m² (621 Kč/m² podlahy), což je horní hrana celého omítání.
- Zdola: zapravení drážek ~400 bm × 130 Kč (práce) = 52, lokální štuk a vyspravení ~120 m² × 350 = 42, ostění a zárubně ~20 ks × 1,5 tis. = 30, materiál ~16. Součet ~140. ODHAD, kolem ±35 %.
- Překryv: položka „Nové elektro“ (`report.py` ř. 277) výslovně obsahuje „drážky a zapravení svépomocí“ a „Oprava opadané omítky až na cihly 20 m²“ (ř. 304, trhliny) je jinde. Pokud je zapravení drážek už v elektru, patří sem jen štuk a ostění (~70 tis.). Nutno vyjasnit s položkou `k-elektrina`, jinak je to dvakrát.

### 2.3 Podlahy
- Vinyl na klik vs lepený: pro tyto byty click. Lepený vinyl (2–2,5 mm) vyžaduje dokonale rovný podklad a stěrku na celé ploše, pokládka je dražší (220–380 Kč/m² vs 130–240) a špatný podklad vidí kupec hned. Click 5 mm s pevnou podložkou odpustí nerovnosti ~2 mm/2 m a jde snadno opravit. Click vinyl je v bytech dnes běžný standard (ODHAD, bez zdroje).
- Materiál 2026: Hornbach 5,0 Crater 599 Kč/m² s DPH https://www.hornbach.cz/p/vinylova-podlaha-5-0-crater/6103560/; Lasamba 5,0 549 Kč/m² https://www.lasamba.cz/vinylove-podlahy-c28; s integrovanou podložkou 699–999 https://www.vinylove-podlahy.cz/vinylova-podlaha-click-vinylova-plovouci-podlaha/p-celkova-tloustka-skupiny/5-00-6-50-mm-vc-podlozky. Beru **650 Kč/m²** (kvalita s vrstvou 0,3–0,55 mm).
- Pokládka click 200–240 Kč/m² (CK podlahy, magma.cz, vinylove.cz), vyrovnání/penetrace +100–120 Kč/m²: https://www.ckpodlahy.cz/cena-pokladky-vinylove-podlahy/, https://magma.cz/kolik-stoji-pokladka-vinylove-podlahy-kompletni-cenik-praci/, https://kolikmaterialu.cz/cena-pokladky-podlahy/ (5. 11. 2026). Komplet i s materiálem 1 100–1 400 Kč/m² (CK podlahy).
- Výpočet: vinyl 169 m² (B+C 129 + A 40) + 5 % odpad × 650 = 116; lišty 120 bm × 80 = 10; stěrka 100 m² (B celé, C 40 %, A 20 %) × 270 (materiál+práce) = 27; pokládka 169 × 220 = 37; brus parket D 35 m² × 500 (brus + lak, `stavimbydlim.cz`, qjob.cz: 450–600 Kč/m²) = 18 + tmel a lišty 5; oprava laminátu A 8 (základ `byty.md`); součet **~235**. Hrubé srovnání: 1 400 Kč/m² × 169 + 23 = 260.
- Web 363 je o 54 % výš. Starý rozpis (335 tis. bez DPH) bral 1 400 Kč/m² vč. stěrky + 2 000 Kč/m² u dražší varianty.
- **Parkety jinde?** Parkety v rybí kosti jsou doložené jen v D (popisy fotek V3, `H/D/040`, `stav.md` ř. 78: „po broušení použitelné“). B má parkety poškozené až na potěr (`stav.md` ř. 66, 0001088: „zničené až na podklad“), C lino a PVC, A laminát v obýváku/kuchyni/chodbě a koberce. Pod linem a koberci mohou být parkety nebo palubky. Stačí odkrýt roh koberce v A a lino v C (pár minut, před objednávkou). Kdyby byly použitelné na polovině z 169 m², vyjde brus ~550 Kč/m² místo ~1 350, úspora ~65 tis. Zatím bez nároku v odhadu.

### 2.4 Malba
- 845 m² = 3,2 × 264 (`stav.md` ř. 147). Po odečtení obkladů v koupelnách a kuchyních cca 780–800 m², držím 845.
- Firma/malíř: 120–250 Kč/m² vč. přípravy a penetrace; jednoduchý dvojitý nátěr 40–70, s tmelením a broušením 70–120; strop 50–90: https://www.daibau.cz/ceny/malovani_malir_pokoju, https://sitprace.cz/pruvodce/kolik-stoji-malovani-bytu, https://fman.cz/clanek/malovani-bytu-2026-cenik-kalkulacka-jak-vybrat-malire, https://www.nejremeslnici.cz/blog/kolik-stoji-malovani-bytu-cena-za-naradi-barvy-i-malirske-sluzby/ (5. 11. 2026).
- Řemeslník (práce 80 Kč/m² vč. oškrabání, tmelení a penetrace) 68 + materiál: disperzní barva ~215 kg, penetrace ~85 l, tmel, krycí fólie a pásky ~30 Kč/m² s DPH = 25 + režie/doprava 7. Celkem **~100** (118 Kč/m²). Web 128 (151 Kč/m²) je o 28 % výš, přemrštěné to není, ale starý odhad 170 Kč/m² je u horní hranice (rozpocet-2 měl 80, `rozpocet-2.md` ř. 86).
- Svépomoc: ~0,12 h/m² vč. přípravy = ~100 h, laik zvládne stěny, stropy a ostré přechody hůře. Úspora práce 68 tis., materiál zůstává 32.

### 2.5 Plísně, drobné opravy, úklid
- **Plísně se odstraní hlavně opravou střechy a sanací příčiny.** Z fotek: stropní skvrny a plíseň v B, C a ve stropě chodby 2. NP = zatékání/kondenzace pod plochou střechou (`stav.md` ř. 28–29, 130; střecha 1 063 je samostatná položka); plíseň v A u paty vnější stěny a u okna C mezi okny = tepelný most nebo vzlínání (`stav.md` ř. 24, 30; příčina „nejde poznat“, ř. 309); plíseň nad obkladem v koupelně C patří do koupelny. Zdroje: oprava střechy/příčiny je první krok, jinak se plíseň vrací, https://www.max-reality.cz/kolik-stoji-plisen-a-vlhkost-v-byte/ (5. 11. 2026). Fungicid 200–400 Kč/balení, sanace příčiny je jinde (injektáž 2 000–4 500 Kč/m²).
- Potřebné je tedy jen: oškrábat, fungicidní přípravek + protiplísňová penetrace, přemalovat (malba) po vyschnutí zdiva, tedy po střeše. Pořadí: střecha, vyschnout, plíseň, štuk, malba. Odhad 30 m² × 300 = 9 + materiál 5, s rezervou **20** (rozpocet-2 měl 20 tis., `rozpocet-2.md` ř. 85). Bez zateplení fasády se tepelný most v A a u oken C neodstraní: plíseň se v rozích může vrátit (riziko pro záruku vůči kupci).
- Drobné opravy (kliky, zámky, svítidla, zásuvky, vypínače): nové dveře a okna s klikami a zásuvky v elektru jsou v jiných položkách. Zbývá žaluzie, rolety, lišty, tmel, pár zámků: **~20** (4 × 5 tis.).
- Generální úklid po stavbě: úklidové firmy cca 40–90 Kč/m² (ODHAD, zdroj nedohledán), 264 m² × 60 = **16**, plus mezi-úklid sutě a prachu **~5**.
- Součet 20 + 20 + 16 + 5 = ~61, s drobností **70**. Web 173 je 2,5× víc. Starý rozpis (60 plísně + 60 drobné + 45 úklid) byl bez domluvy se střechou.

## 3. Svépomoc (hodiny, riziko)
| Práce | Hodiny | Úspora | Laik? | Riziko |
|---|---|---|---|---|
| Vyklizení, demontáž krytin a linek | ~170 | 62 | Ano | Nízké. Azbest v lepidle/lino: vzorek před odstraněním. |
| Zapravení drážek, zárubní, ostění | ~120 | 50 | Drážky ano, štuk těžko | Nízké, viditelné jen při špatném štuku. |
| Stěrka + pokládka click vinylu | ~100 | 50 | Ano, s návodem | Praskliny při nerovném podkladu, záruka kupcům 5 let u bytu v novostavbě/rekonstrukci. |
| Malba | ~100 | 68 | Ano | Nízké. |
| Úklid, fungicid | ~40 | 15 | Ano | Nízké. |
| **Celkem** | **~530 h** (4–5 lidí, 3 víkendy) | **~240** | | Statik, revize ani pojišťovna se těchto prací netýkají. |

Brus a lakování parket (D) doporučuji nechat firmě. Nejde o zákonný požadavek, ale svépomocná pronajatá bruska bývá viditelně horší a lak se špatně opravuje.

## 4. Chybí / dvakrát
- **Dvakrát:** (a) drážky a zapravení: v elektru „svépomocí“ i zde (~50–60 tis.); (b) opadaná omítka 20 m² v položce trhliny (22 tis., `report.py` ř. 304) vs. lokální štuk tady; (c) plíseň v koupelně C v koupelnách (`report.py` ř. 286) vs. plísně tady; (d) vyklizení dílny, skladů a kotelny je v nebytové části (`report.py` ř. 362), původní `stav.md` 5a je počítalo tady (30–40 tis.); (e) drobné opravy (kliky, zásuvky) vs dveře a elektro (~20 tis.); (f) malba společných prostor je ve společných (ř. 326), tady správně není.
- **Chybí:** průzkum azbestu ve starých krytinách (3–5 tis.); ochrana společných prostor a schodiště při vynášení sutě (folie, desky, ~5 tis.); demontáž starých dveří a oken s odvozem (je asi v těch položkách, ověřit); nová prahová a přechodová lišta mezi místnostmi (v lištách zahrnuto). Podhodnoceno žádná položka.
- **Podhodnocené:** u podlah v B je potěr se sutí (`stav.md` ř. 32): kdyby se ukázalo, že vyžaduje zalití tenkým potěrem 40–50 mm místo stěrky, +67 m² × 500 = +35 tis. Je to už v pes.

## 5. Doporučení
**Snížit položku na real ~700 tis. (z 1 076; −35 %)**, pes ~1 000, opt ~480. Součet mých položek je 662 tis.; přidávám ~40 tis. jako pojistku na B (potěr), azbest a objem sutě, protože rezerva v realistickém scénáři je zrušená. Hlavní důvody: bourání a vyklizení je dvojnásobné (koupelny se nebourají, nebytová část je jinde), plísně/drobné opravy/úklid mají překryvy s koupelnami, dveřmi a elektrem a podlahy se při click vinylu vejdou do ~1 350 Kč/m². Při svépomoci je nejlevnější rozumná varianta ~420 tis., ale doporučuji ji jen u vyklizení, demontáže, malby a pokládky clicku. Pokud chcete držet částku na webu vyšší jako rezervu pro nejistý stav bytů A a B (zatékání), je to vaše rozhodnutí, nikoli chyba v položce.

Poznámka k modelu: `kosmetika` 800 tis. real × stavba_mult vychází na 1 076 tis. a obsahuje i položky ze `stav.md` 5a, které jsou už jinde. Změna by znamenala snížit `IN["kosmetika"]` real úměrně (1 076 → ~700 tis.), nezasahuji do něj.
