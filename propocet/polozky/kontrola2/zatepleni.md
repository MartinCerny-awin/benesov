# Kontrola 2: Zateplení fasády (nedělá se, v nákladech 0; na webu jen informativně 1 200 tis.)

Stav 5. 11. 2026. Rozhodnutí „bez zateplení“ neměním a souhlasím s ním (viz závěr). Web: `report.py` ř. 153–155, řádek přeškrtnutý, do součtů nevstupuje.

## 1. Tabulka (tis. Kč s DPH, real, bez nástavby; jen pro případ, že by se dělalo)

| Položka | Web | Můj odhad real | Pes–opt | Potřeba | Nejlevnější rozumná cesta | Zdroj |
|---|---|---|---|---|---|---|
| ETICS EPS 160 mm vč. lešení, soklu XPS, omítky (~420 m²) | 1 200 | **1 065** (firma, DPH 12 %) | 1 550–800 | ne (viz bod 2) | řemeslník −230 tis. čistě; svépomoc −400 tis. čistě | `podklady/stav.md` ř. 201 (340/420/500 m² × 1 600/2 200/3 000 Kč, bez DPH; 544/924/1 500); [kolikmaterialu.cz](https://kolikmaterialu.cz/kolik-stoji-zatepleni-domu/) EPS 1 505–2 205 Kč/m² bez DPH vč. lešení, 5. 11. 2026 |
| Příplatky: ostění 40–48 oken, parapety, atika, sokl, odstranění břečťanu | v ceně | 100–150 (bez DPH) | | ano, kdyby se dělalo | firma | ODHAD |

Výpočet zdola (bez DPH): 420 m² × 1 900 Kč (střed 1 500–2 200) = 800 + příplatky 125 = ~925 tis. → × 1,12 = **1 036**; s režií firmy ~3 % ≈ 1 065. Plocha: obvod ~64 m × 7,5 m = 480 m² − ~45 oken × 1,8 m² = ~400–420 m² (`stav.md` ř. 35, shoda). Web 1 200 je o ~10 % výš, tj. na hraně tolerance; lešení je v ceně (120–220 Kč/m² podle dcompany.cz). Shoda se stav.md real (924 × 1,12 = 1 035, × 1,17 škálování = 1 210), takže 1 200 je jen škálované číslo z modelu. Beze změny.

Varianty (čistě = po odpočtu DPH):
- **Firma**: 1 065 s DPH, čistě ~950.
- **Řemeslník (OSVČ neplátce)**: materiál ~420 tis. bez DPH (+21 % = 508, odpočet) + práce 600–800 Kč/m² = 250–335 tis. bez DPH odpočtu, lešení nájem+montáž ~130 tis. Čistě ~720 tis., tedy −230 tis. ODHAD.
- **Svépomoc**: materiál + lešení ~550 tis. čistě, −400 tis. oproti firmě. Práce laik ~1,2–1,5 h/m² = 500–650 h (+ lešení). Riziko vysoké: práce ve 8 m, ETICS bez certifikovaného zhotovitele ztrácí záruku výrobce systému, záruka vůči kupcům bytů 5 let, banky kupců i dotace chtějí doklady. Nedoporučuji.

## 2. Je povinnost zateplit?
- **Ne.** Zákon 406/2000 Sb.: větší změna dokončené budovy = změna na >25 % plochy obálky. Obálka domu ≈ 480 fasáda + okna (45 × 1,8 = 80) + střecha 215 + podlaha 239 ≈ 1 000 m². Výměna střechy (215) + oken (~80) = ~295 m² = ~30 % → **větší změna je pravděpodobně naplněna** (PENB před zahájením, vyhl. 264/2020 Sb.). Požadavky se ale vztahují jen na **měněné konstrukce** (střecha, okna musí splnit U_N,20 a kritérium budovy), **ne na nedotčenou fasádu**. Zdroje: [společné stanovisko MPO/MMR](https://mmr.gov.cz/getattachment/08eb1b23-d6c7-41ed-8a7d-c2ed14731710/Spolecne-stanovisko-MPO-a-MMR-k-PENB.pdf.aspx?lang=cs-CZ&ext=.pdf), [vyhl. 264/2020](https://e-sbirka.gov.cz/sb/2020/264). Podmínku „kritérium budovy“ (primární neobnovitelná energie) po výměně střechy, oken a zdroje (TČ) projektant PENB ověří; s TČ je splnění snadné (nízký faktor primární energie). ODHAD, ověřit u energetického specialisty.
- **PENB při prodeji ano** (platnost 10 let, předat nejpozději při podpisu; `podklady/dane-financovani.md` ř. 110, v modelu 15 tis.), ale **minimální třída pro prodej bytů v ČR není** předepsána.

## 3. Co by zateplení přidalo?
- **Cena bytů**: komerční zdroje 3–8 % mezi třídami C a F/G, ~3,2 % na třídu (Deloitte 2023 přes sekundární zdroj), byty ~7,5 % (studie UK Praha 2025, primárně nedohledáno) – [brivo.cz 2026](https://www.brivo.cz/blog/penb-a-vs-g-cena-bytu-2026), [stavebnice-svepomoci.cz](https://stavebnice-svepomoci.cz/jak-energeticka-narocnost-ovlivnuje-cenu-nemovitosti-v-cr) – spolehlivost nízká, ČSÚ energetickou třídu nesleduje. Dům bude **bez fasády už po střeše, oknech a TČ** pravděpodobně v D–C (ODHAD); fasáda pak posune o 1 třídu: **+1,5–3 %**, tj. +1,5–2,5 tis. Kč/m² z ~85 tis. (V1 real 82–91 tis./m², 344 m²; `postup.md` ř. 159). Tržby bytů ~30 mil. → **+0,45–0,9 mil. s DPH, čistě +0,4–0,8 mil.** (prodej s DPH 12 %).
- **Menší TČ**: ztráta stěn z U ≈ 1,1 na 0,2 W/m²K × 420 m² × ΔT 35 K = ~11–12 kW. Dům z 27–34 kW na ~16–22 kW (`technika.md` ř. 44; `stav.md` ř. 228). Model má 2 × 16 kW (470 tis. celkem); 2 × 10 kW by bylo levnější o ~100–200 tis. ODHAD. Plus nižší provozní náklady kupců, což cena částečně zohlední (už v prémii výše).
- **Bilance**: náklad čistě ~950 vs. přínos 0,4–0,8 (cena) + 0,1–0,2 (TČ) = 0,5–1,0 mil. → **ztráta ~ −0,0 až −0,45 mil.**, ve středu −0,25 mil. a časová náročnost +2–3 měsíce stavby (úrok ~ 9,5 % z 1,2 mil. po 3 měsíce ≈ 30 tis.). Se svépomocí (−400 tis. nákladu) by vyšlo přibližně na nule, ale s rizikem výše.

## 4. Dotace
- NZÚ 2026+ (od léta 2026, [zdroj](https://depositumreality.cz/aktuality/nova-zelena-usporam-v-novem-rezimu-co-se-zmenilo-v-roce-2026)): pro bytové domy **bezúročný úvěr** (ne dotace), až 250 tis. Kč/byt dílčí a 750 tis. Kč/byt komplexní renovace; bonus až 120 tis./byt jen pro nízkopříjmové domácnosti; žadatel **SVJ nebo bytové družstvo** ([tzb-info](https://stavba.tzb-info.cz/zelena-usporam-na-tzb-info/29942-nova-zelena-usporam-2026-zvyhodnene-uvery-pro-bytove-domy), [dumplnyuspor.cz](https://www.dumplnyuspor.cz/nzu2026/)). Další omezení: podnikání/pronájem do 20 % plochy, udržitelnost 5 let. „Oprav dům po babičce“ je jen pro rodinné domy a nízké příjmy.
- **Při prodeji bytů se dotace získat nedá**: investor je fyzická osoba (po registraci k DPH podnikatel), SVJ vznikne až po prodeji prvního bytu a o úvěr by musel žádat nový vlastník. Dotaci proto **nezapočítávat** (technika.md ř. 48 to potvrzuje pro TČ). Údaje z komerčních webů, primární pokyny SFŽP nedostupné (PDF MŽP nešlo přečíst), ověřit na sfzp.cz.

## 5. Riziko trhlin a sedání
Svislé trhliny 2–3 mm přes obě podlaží a sokl, znovu otevřená trhlina (`stav.md` ř. 46, 326; `postup.md` ř. 83). ETICS na pohybující se zdivo praská, skryje trhliny a znemožní jejich monitoring (sádrové terče, měření). Zateplovat lze **až po statickém zajištění a ustálení** (monitoring minimálně 6–12 měsíců), tedy po prodeji nebo těsně před ním. Kupci by pak nemohli trhliny pozorovat, ale řešili by případný spor o skryté vady. Další důvod proti.

## Součet
| | tis. Kč s DPH |
|---|---|
| Web (informativně) | 1 200 |
| Můj real, firma | 1 065 (−11 %) |
| Řemeslník (čistě po odpočtu) | ~720 |
| Svépomoc (čistě) | ~550 |
V nákladech 0 (rozhodnutí).

## Chybí / dvakrát
- Dvakrát nic. Zateplení střechy je v položce Střecha (1 063), ne tady.
- Kdyby se dělalo, chybí v ceně: statik/dozor (v Projekt), úprava rozvodů a vstupů (hromosvod, žaluzie, oplechování), ~50–100 tis. ODHAD. Sanace trhlin pod ETICS by byla navíc.
- Celkový rozpočet: **PENB musí být zpracován před zahájením stavby** (větší změna, 25 %); model má 15 tis. na začátku, dostatečné.

## Doporučení
**Beze změny: zateplení se nedělá, v nákladech 0.** Nevyplatí se: čistý náklad ~0,95 mil. vs. přínos 0,5–1,0 mil. (cena bytů + menší TČ), tedy kolem −0,25 mil. a 2–3 měsíce navíc; dotace při prodeji nedostupná; povinnost zateplit není; před statikou nedává smysl. Hodnotu 1 200 na webu lze ponechat (rozdíl 11 % k mé 1 065 je jen informativní). Pro firmu stačí do popisu dopsat „PENB: větší změna, kritérium splní střecha+okna+TČ, ověřit“.
