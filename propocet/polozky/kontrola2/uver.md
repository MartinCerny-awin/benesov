# Kontrola 2: Úroky a poplatky úvěru (5. 11. 2026)

Web 13:44: **1 382 tis.** bez nástavby (úroky na koupi 527 + na stavbu 329 + poplatek 526 + předčasné 0), s nástavbou 2 431. Počítáno importem `model.py` (jen čtení, nic nezapsáno), skripty ve scratchpadu `u2.py`, `u4.py`. Model se mezitím mění (viz bod 2): v `model.py` je od 13:5x `refinancovat` = 0 → položka už klesla.

Moje opakování starého stavu (refinancovat = 1, V1 bez nástavby, real, MIX řemeslníci 60 %): úroky 815 + poplatky 526 = **1 341** (web 1 382, rozdíl 3 % je drift modelu). S nástavbou V2: 2 375 (web 2 431).

## 1. Tabulka po dílčích položkách (V1, tis. Kč)

| Položka | Web | Můj odhad real | pes–opt | Potřeba | Nejlevnější rozumná cesta | Zdroj |
|---|---|---|---|---|---|---|
| Úroky 10,5 % z úvěru na koupi (tranše v 12. měs.) | 527 | 527 (při refin = 1); **0** při půjčce jen na zbývající stavbu | 12,5 %: ~660 · 9 %: ~450 | jen když investor nemá 8,3 mil. vlastních; úvěr na už zaplacenou koupi je jen refinancování | nebrat refinancování koupě: −527 | `model.py` ř. 119 (`sazba`), ř. 506–510 (tranše = LTV × cena + proinvestované), běh `u4.py` |
| Úroky 10,5 % z čerpání na stavbu | 329 | 239–290 (podle driftu modelu; po refin = 0 zbývá 239) | 12,5 %: ~290 · 9 %: ~200 | ano, pokud chybí vlastní peníze na stavbu | úvěr jen na stavbu; menší rozsah (rodina 5 % → 114, viz bod 3) | `model.py` ř. 513–523, `u4.py` |
| Poplatek 4,0 % za zpracování | 526 | 526 (z čerpané částky 13,1 mil.); při refin = 0 **219** (4 % × 5,46 mil.) | 5 %: ~270 / 3 %: ~165 (po refin = 0); starý stav 5 % → 657, 3 % → 394 | ano u platformy, u banky 0,5–1 % | banka 1 %: −55 oproti 219; rodina 0 | `model.py` ř. 122 (Investown 4–5 %, Upvest 2–4 %, ZOXO 4 %), `u4.py` |
| Předčasné splacení | 0 | 0 (pes 0,5 % ≈ +65) | 0–0,5 % | podle smlouvy; Investown zdarma při splnění účelu, jinak 3 % | hlídat ve smlouvě | `model.py` ř. 123 |
| **Součet** | **1 382** | **1 341** (refin = 1) / **458** (refin = 0) | 1,2–1,6 mil. / 0,3–0,6 mil. | | viz bod 2–3 | `u4.py` |

Poznámka: rozpis webu je dopočtený na součet modelu, takže řádky nelze 1:1 srovnat s mým rozpadem.

## 2. Odpovědi na zadání

**(1) Je 10,5 % + 4 % realistické?** Ano, je to střed až mírně vyšší střed pásma. Zdroje (rešerše uložená u `sazba` v `model.py` ř. 119 a 122, dnes ověřeno jen částečně): Investown pro investory 7,7–9,8 % (finex.cz/recenze/investown, 5. 11. 2026) + zprostředkování dlužníka 4–5 % (investown.cz/business, podle poznámky v modelu); Fingood 10–12,9 % pro investory (investnews.cz/fingood-recenze, 5. 11. 2026); Upvest 2–4 % + 0,5–1 % ročně; ZOXO od 6,9 % + 4 % (zoxo.cz/developerske-projekty, čteno 4. 11. 2026); Ronda ~9 %. Efektivní roční náklad při 4 % poplatku a ~1,5 roce držení je ~13 %, tedy 10,5 % všechno včetně poplatku jednorázově je správné pásmo, nikoli nadsazené. Hlavní riziko: platformy půjčují obvykle podnikatelské entitě (s.r.o. se zástavou), ne fyzické osobě; zda půjčí FO, jsem neověřil (**ODHAD**, ověřit u Investown/Upvest dotazem). Sazby pro dlužníky veřejně nikde nejsou, jen v individuální nabídce.
Bankovní podnikatelský / rekonstrukční úvěr: PRIBOR 3M + 2,5–4 % ≈ 6,5–8 %, zpracování 0,5–1 % (`podklady/dane-financovani.md` ř. 152, 4. 11.), jenže banka si vezme hodnotu domu dnes (~5,8 mil. max., ř. 149) a bez zapsaného přístupu nepůjčí (`postup.md` ř. 60).

**(2) Půjčit jen, co chybí.** Model v 13:44 půjčoval i na už zaplacenou koupi (refinancování v 12. měsíci, 13,1 mil.). Jiné sezení (kontrola položek, `model.py` ř. 120) už nastavilo `refinancovat` = 0 (půjčit jen na zbývající stavbu). Výsledek mého srovnání (stejný model, jen ten přepínač):

| | Úroky + poplatky | Max. úvěr | Vlastní kapitál (špička) | Čistý zisk |
|---|---|---|---|---|
| V1 refin = 1 | 1 341 | 13,1 mil. | 12,1 mil. | 4,60 mil. |
| V1 refin = 0 | **458** | 5,5 mil. | 12,7 mil. | 5,14 mil. |
| **Rozdíl V1** | **−883 (−66 %)** | | +0,6 mil. | **+0,54 mil.** |
| V2 refin = 1 → 0 | 2 375 → 1 534 | 18,2 → 14,5 mil. | 12,6 → 14,4 mil. | 4,80 → 5,32 mil. |

Úvěr tedy stojí ~880 tis. a nahrazuje jen 0,6 mil. potřebného kapitálu navíc. Pozor: ani při refin = 0 investor nepotřebuje o moc míň peněz (12,7 mil. špička), protože koupi a první stavbu (do 12. měs.) platí z vlastních. Nesnižovat LTV pod 65 % u V1 nic nemění (u refin = 0 je úvěr dán stavbou, ne stropem); u V2 další snižování LTV šetří (0,30 → −0,5 mil. oproti refin = 0, ale vlastní kapitál 19,9 mil.). Pokud investor 12,7 mil. nemá, je správná odpověď úvěr na koupi **až v den, kdy je třeba**, ne refinancování.
Poplatek 4 % z čerpané částky vs. z rámce: model ho účtuje z čerpané částky (ř. 509, 520). Platformy běžně berou 4 % z celé emise při vyplacení. Pokud by se u stavebního úvěru platilo z rámce 13,1 mil., je to 526 místo 219 (+307). Ve smlouvě chtít poplatek z čerpané tranše, nebo po etapách (více menších emisí).

**(3) Levnější varianty (V1, součet úroky + poplatky, tis.)**

| Varianta | refin = 1 | refin = 0 | Komentář |
|---|---|---|---|
| Model 10,5 % / 4 % | 1 341 | 458 | |
| Investown nižší konec 9 % / 4 % | 1 224 | | |
| Fingood 12 % / 5 % | 1 589 | | horní okraj |
| Bankovní podnikatelský úvěr 8 % / 1 % | 752 (−44 %) | 237 (−48 %) | PRIBOR + marže, ale odhad banky z dnešního stavu a přístup |
| Hypotéka / americká hypotéka na byt A (zástava jiné nemovitosti) 6 % / 0,5 % | 531 (−60 %) | | KB od 5,99 %, ČS americká od 5,89 % (hypoindex.cz, září 2026; kb.cz/americka-hypoteka); strop jen ~70 % hodnoty zástavy |
| Úvěr od rodiny 5 % / 0 | 388 (−71 %) | 114 (−75 %) | smlouva s úrokem v obvyklé výši, jinak daňově problém |
| Postupný prodej bytů splácí úvěr | model už počítá (splácení z tržeb v měs. 18–24, `predcasne` 0) | | další zkrácení nešlo spolehlivě spočítat |

Hypotéka na byt A: americká hypotéka je neúčelová, ale zástavou je jen byt, který investor vlastní; pokud jde o byt A v kupovaném domě, banka jej do zástavy nevezme před koupí. Takže funguje jen s **jinou už vlastněnou nemovitostí**; o té nic nevím, **ODHAD** použitelnosti.

## 3. Součet

- Web: **1 382** (V1), 2 431 (V2).
- Můj realistický odhad při současném zadání (půjčka naplno, platforma 10,5 % / 4 %): **~1 340** (V1), ~2 375 (V2); odchylka −3 % (drift modelu), v pořádku.
- Nejlevnější rozumná varianta: půjčit jen na zbývající stavbu (refin = 0) a ideálně levněji než platforma (banka 8 % / 1 % nebo rodina): **237–458** (V1). Rozdíl proti webu **−67 až −83 %**, hlavní důvod: nepůjčovat 8,3 mil. na už zaplacenou koupi (úroky 527 a poplatek ~300). Svépomoc zde neplatí.

## 4. Chybí / dvakrát

- Chybí: nic zásadního. Při 4 % z rámce (ne z čerpané částky) +307 tis. (V1, po refin = 0); riziko v podmínkách smlouvy, ne v modelu.
- Úroky nejsou DPH; poplatek platformě se do odpočtu nezapočítává (správně, finanční služba osvobozena).
- Dvakrát: ne; `model.py` počítá úroky z úvěru jednou. Starší `polozky/financovani-dph.md` ř. 36–40 uvádí stejný problém (strop úvěru z hodnoty po dokončení je optimistický; banka dá ~5,8 mil.). Při 65 % z dokončené hodnoty je tržní ocenění pro platformu (LTV do 80 % u Ronda) přijatelné, u banky ne.
- Podhodnoceno: roční poplatek platformy je v sazbě 10,5 % (poznámka v `model.py`); pokud je navíc, +0,5–1 % ročně ≈ +40–60 tis. (**ODHAD**).

## 5. Doporučení

Sazbu 10,5 % a poplatek 4 % **neměnit** (rozhodnutí uživatele, v pásmu trhu). Položku **snížit na ~0,46 mil. Kč** (V1; V2 ~1,53 mil.) přepnutím `refinancovat` = 0, což jiné sezení už provedlo v `model.py`; jen ověřit, že web po `deploy-web.sh` ukazuje ~458 a ne 1 382. Poznámka webu „platforma půjčí do 65 % hodnoty po dokončení“ upravit: úvěr se čerpá jen na stavbu, koupě je z vlastních. Ověřit u platformy: půjčí FO bez s.r.o.? A poplatek z čerpané tranše, ne z rámce.

Zdroje (5. 11. 2026): finex.cz/recenze/investown, finex.cz/recenze/fingood, investnews.cz/fingood-recenze, financera.cz/recenze/bondster, hypoindex.cz (ČS 11. 9. 2026), kb.cz/cs/obcane/pujcky/hypoteky/americka-hypoteka, zoxo.cz/developerske-projekty (4. 11.), `model.py` ř. 119–123 a 485–525, `podklady/dane-financovani.md` ř. 149–152, `postup.md` ř. 60.
