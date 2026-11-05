# Kontrola 2: Střecha (plochá, 215 m²), 5. 11. 2026

Web: real bez nástavby **1 063 tis.** (součet dílčích položek 100+55+382+298+127+62+39 = 1 063; model `strecha_v_rekonstrukci` real 863 tis. × režie/DPH/inflace, v `POL` ×~1,17 jako náhrada zrušené rezervy). Ceny níže: firma (plátce, DPH 12 %), bez režie GD, pokud nepíšu jinak. Kalkulačky = cenanovestrechy.cz/cena-rekonstrukce-ploche-strechy (bez data, obrázky 03/2026), kolikmaterialu.cz/zatepleni-strechy-cena a planstavby.cz/blog/strecha-taska-plech-folie-2026 (čteno 5. 11. 2026); starší rozpis polozky/strecha-statika.md ř. 8–21.

## Zvlášť prověřené otázky

**Strhnout, nebo přes staré?** Strhnout. Přes staré souvrství lze jen tehdy, když sondy ukážou suchou skladbu (izolace.cz, tzb-info "Rekonstrukce střešního pláště"; PVC se musí od asfaltu oddělit separací). Tady zatéká, v B (V/091024109/0000363, 0000423) a C jsou mapy a plíseň, žlutá skvrna v chodbě 2. NP (podklady/stav.md ř. 45) → skladba je skoro jistě mokrá a navíc bez dnešní izolace. Úspora přetažením (opt) je ~50 tis., ale s rizikem zatékání do prodaných bytů; nedoporučuju. **Nejdřív sondy (4–6 otvorů, ~10 tis. nebo v dozoru)**, jinak neznáme, jestli se nebude bourat i škvárový/spádový beton (R2 v stav.md ř. 92: 0–1,5 mil., real 0,3 mil. – po zrušení rezervy v modelu není nikde kromě 17% přirážky).

**Povinné zateplení?** Vyhl. 264/2020 sama neříká "při výměně hydroizolace zatepli". Povinnost vzniká při **větší změně dokončené budovy** (>25 % plochy obálky; střecha 239 m² + nová okna + případná fasáda; zde reálně ano, protože okna se mění všechna) – pak PENB a splnění požadovaných U (plochá střecha požadované ~0,24, doporučené ~0,16 W/m²K; hodnotu ověřit u projektanta v příloze vyhlášky, nenašel jsem ji přímo v textu, zdroj: e-sbirka.gov.cz/sb/2020/264, mmr.gov.cz společné stanovisko k PENB). Kupci bytů a banka navíc zateplení čekají. **Tloušťka:** web říká 160–200 mm (to je EPS). Na U 0,24 stačí cca **PIR 100–120 mm** (λ 0,023) nebo **EPS ~150–170 mm průměr vč. klínů** (λ 0,037). Střecha 9,5 m široká se spádem 2 % do vnitřních vpustí → klíny průměrně ~100 mm, takže EPS celý (základ 100 + klín ~80) je přirozená skladba, PIR jen kde vadí výška (atika, výlez).

**Tržní ceny:** kalkulačky 2 500–3 500 Kč/m² bez DPH za kompletní rekonstrukci s izolací a spádem (cenanovestrechy.cz, kolikmaterialu.cz, 2026; jde o RD a bez skladby). Web: 1 063 tis. / 1,12 / 215 = ~4 410 Kč/m² bez DPH s přirážkou, můj odspodu ~3 800 Kč/m² bez DPH (bytový dům, firma jako GD, atika 68 bm, vpusti, bourání do hloubky). Web je nad kalkulačkami (+20–60 %), ale ty nepočítají bourání dole ani atiku.

## 1. Tabulka po dílčích položkách (tis. Kč s DPH)

| Položka | web | můj real | pes–opt | potřeba | nejlevnější rozumná cesta | zdroj |
|---|---|---|---|---|---|---|
| Odstranění starých vrstev a suť (215 m²) | 100 | 110 | 160–55 | ano (mokré vrstvy; bez toho nové neudrží a PVC nesmí na asfalt) | **svépomoc bourání −60** (viz níže) | bourání hydroizolace 80–150 + izolace 120–200 Kč/m² (cenanovestrechy.cz) → ~280 Kč/m² = 60 + kontejnery/skládka ~40 bez DPH; pes dehtové/škvárové vrstvy, nebezpečný odpad |
| Parozábrana a penetrace | 55 | 45 | 65–30 | ano (pod izolací na betonu) | firma (svařovaný pás hořákem = pokrývač), bez úspory | 70–120 Kč/m² montáž + pás ~100 → ~170 Kč/m² × 215 × 1,12; cenanovestrechy.cz |
| Spádová izolace (web EPS/PIR 160–200) | 382 | 300 (PIR 100 + EPS klíny) | 430–230 | ano (U, PENB, kupci) | **jen EPS (základ + klíny) −90 až −100**; svépomoc kladení EPS možná, −30 | PIR mat. 580–780 Kč/m² na 100 mm (kolikmaterialu.cz); klín EPS 100 100/120 mm 223 Kč/m² bez DPH (e-zatepleni.cz, bez data), EPS 100 ~2 300 Kč/m³ (prokrb.cz); montáž izolace 120–250 + klíny 120–220 Kč/m² (cenanovestrechy.cz). Mix ~1 250 Kč/m² bez DPH; EPS-only ~800 |
| Hydroizolace PVC mech. kotvená vč. lemů | 298 | 260 | 360–190 | ano | firma s certifikací výrobce (záruka 15–20 let), svépomoc ne | fólie 1,5 mm mat. ~250–350 + geotextilie ~60 + pokládka 220–380 Kč/m² + lemy na atiku 68 bm; planstavby.cz 700–1 500 Kč/m² mat.+mont.; cenanovestrechy.cz 1 400–2 200 Kč/m² za novou hydroizolaci (vč. všeho). Můj ~950 Kč/m² |
| Oplechování atiky 68 bm | 127 | 95 | 140–65 | ano (bez toho teče pod fólii) | klempíř-řemeslník −10 až −15 | web 1 870 Kč/bm s DPH je vysoko; kalkulačka 180–350 Kč/bm je jen montáž; rozpocet-2.md 900/1 200/1 600 Kč/bm; mat. ~200–280 Kč/bm (dek.cz, oplechovani.cz). Můj 1 250 Kč/bm bez DPH |
| Vpusti 4 ks s přepady | 62 | 48 | 70–32 | ano (nouzové přepady vyžaduje norma u atiky) | firma, součást fólie | vpust 800–2 000 Kč/ks mat. (cenanovestrechy.cz) + montáž, napojení, přepady → ~9–12 tis./ks s DPH; ODHAD |
| Prostupy, lem komína, výlez | 39 | 30 | 45–18 | ano; **lem komína odpadá, pokud se komín kotelny bourá** | firma | ODHAD |
| *(chybí)* Přístup na střechu, záchytný systém/jeřáb, sondy | 0 | 35 | 60–15 | ano (BOZP, atika 68 bm, výška ~8 m) | – | ODHAD (zvedání desek a pásů, ochrana okraje, sondy ~10) |

## 2. Součet

| | tis. Kč |
|---|---|
| Web (real) | **1 063** |
| Můj real odspodu, firma (vč. 35 tis. za přístup a sondy) | **~925** (−13 %) |
| Můj real + 10 % na neznámou skladbu (rezerva je zrušená) | ~1 015 (−4 %) |
| Nejlevnější rozumná varianta | **~760** (−28 % vs web) |

Nejlevnější varianta: izolace jen z EPS (−95), bourání svépomocí (−60), ostatní firma → 925 − 155 = ~770. Hlavní důvod rozdílu: web počítá PIR/EPS 160–200 mm jako dražší skladbu, než U 0,24 vyžaduje, a zvýšené jednotkové ceny atiky (1 870 Kč/bm). Web je naopak nízký v tom, že neobsahuje nic na přístup a na neznámou skladbu (R2 0–1,5 mil.). Součet obou efektů ukazuje, že 1 063 je přiměřený strop s rezervou, ne nadsazení.

**Svépomoc u střechy.** Bourání staré skladby: ~215 m² × 0,35 h/m² ≈ 75 h, 3–4 lidé, 3–4 dny, pád z výšky (atika nižší než 1,1 m? ověřit), 8–10 kontejnerů. Laik zvládne. Rizika: (1) dehtové lepenky a případně azbest v 1981 (vzorek na PAH/azbest ~3 tis., jinak nebezpečný odpad 17 03 01*); (2) poškození stropní desky; (3) pokrývač musí podklad **písemně převzít**, jinak odmítne záruku na celou střechu. Úspora ~55–65 tis. s DPH (jen práce, kontejnery platíte). Pokládka EPS po převzetí podkladu (55 h) by ušetřila dalších ~30 tis., ale chyba ve spádu = kaluže = reklamace od kupců, nedoporučuju. Parozábrana (hořák), fólie, lemy, klempířina: firma/řemeslník, ne svépomoc. Řemeslník (OSVČ neplátce) u klempířiny: ušetří 10–15 % (bez režie a bez DPH na práci, materiál s 21 %), u fólie nesmí, protože výrobce garantuje záruku jen certifikovanému montážníkovi.

## 3. Chybí / dvakrát / podhodnocené

- **Chybí 35 tis.:** přístup na střechu (jeřáb/výtah na desky a role, záchytný systém atiky), sondy před návrhem skladby.
- **Dvakrát ~15–25 tis.:** "Odstranění komínového nástavce kotelny, zapravení střechy" 39 tis. (rozvody, report.py ř. 313) a "lemování komína" ve střeše (v položce Prostupy 39 tis.). Když se komín bourá, lem komína se nedělá, zapravení střechy udělá pokrývač v rámci nové fólie. Řešit v jedné z položek.
- **Hromosvod** je v rozvodech (26 tis.), ne ve střeše: v pořádku, nedvojí se.
- **Neznámá skladba/podklad (R2, 0–1,5 mil.)** po zrušení rezervy není v modelu krytá nikde než v přirážce ×1,17; to je největší riziko položky, ne cenová hladina. Pokud sondy ukážou mokrý spádový beton nebo škváru, +100–300 tis.
- Zateplení střechy slouží i bytům B, C (kondenzace/plíseň od nezateplené desky): vyřeší příčinu, takže drobné "ošetření plísní" v bytech (89 tis.) se dělá až po střeše.

## 4. Doporučení

**Beze změny, 1 063 tis.** (real). Odspodu vychází ~925 tis. (−13 %), ale po zrušení rezervy chybí krytí neznámé skladby, takže přirážka ×1,17 funguje správně jako rezerva; pes–opt beze změny. Kde ušetřit: v dílčích řádcích přejmenovat "EPS/PIR 160–200 mm" na "EPS (případně PIR 100–120 mm), U ≤ 0,24" a v plánu nechat bourání staré skladby na svépomoc (−60 tis.) a EPS místo PIR (−95 tis.), pokud sondy neodhalí problém. Před objednávkou: 3 sondy + vzorek na PAH/azbest.
