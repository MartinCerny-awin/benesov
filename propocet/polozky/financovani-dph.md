# Úroky a poplatky úvěru + DPH z prodeje po odpočtu (V1 firma, realisticky)

Stav: `model.py` z 4. 11. 2026 23:09 (soubor se v průběhu práce měnil, např. `rizika_navic` a `b31_zmeny`, proto čísla níže mírně nesedí s čísly ze zadání). Pomocný skript mimo projekt: `/private/tmp/claude-501/-Users-martincerny-Documents-Benesov/10c8aba8-814f-4139-8a50-ee85d67762d3/scratchpad/fd.py` (kopie logiky `simuluj()` s rozpadem po složkách; součty se shodují s modelem na 1 Kč).

## A. Úroky a poplatky úvěru

Průběh úvěru (V1 firma, real): sazba 6,2 % (`model.py` ř. 113), úvěr na koupi se čerpá v měsíci 9 (po zapsání přístupu), stavba se čerpá průběžně od měsíce 9, strop úvěru = 70 % × 21,88 mil. Kč (tržby 31,26 mil. × (1 − 30 % sleva za dům vcelku)) = **15,32 mil. Kč** (strop je dosažen). Tranše v měsíci 9: **8,63 mil. Kč** (5,83 mil. = 70 % kupní ceny + 2,80 mil. už proinvestované stavby), další stavební tranše celkem **6,69 mil. Kč**. Splácení z prodeje bytů v měsících 18–23, konec měsíc 23.

### Rozpis

| Položka | Množství | Jedn. cena | Realisticky Kč | Pes / opt | Zdroj |
|---|---|---|---|---|---|
| Úroky z úvěru na koupi a dřívější stavbu | tranše 8,63 mil. Kč, 14 měs. úročení do postupného splácení | 6,2 % p. a. | 433 044 | pes 7,0 %, opt 5,7 % | `model.py` `simuluj()` ř. 407–411, `IN["sazba"]` ř. 113 |
| Úroky z čerpání na stavbu | 6,69 mil. Kč čerpáno průběžně | 6,2 % p. a. | 269 767 | viz výše | totéž |
| Poplatek za zpracování úvěru, tranše na koupi | 8,63 mil. Kč | 0,5 % | 43 139 | pes 1,0 %, opt 0 % | `IN["uver_poplatek"]` ř. 115 |
| Poplatek za zpracování, stavební tranše | 6,69 mil. Kč | 0,5 % | 33 436 | totéž | totéž |
| Poplatek za předčasné splacení při prodejích | 15,32 mil. Kč splaceno | 0,5 % | 76 576 | pes 1,0 %, opt 0 % | `IN["predcasne"]` ř. 116, zák. 257/2016 § 117 |
| **Součet** | | | **855 962** (úroky 702 811 + poplatky 153 151) | pes 607 986 + 177 434 = 785 420, opt 509 933 + 0 | |

Pes / opt jsou celé V1 scénáře z modelu (jiná doba: pes 39 měs., opt 14 měs.), proto nejsou rozpočítané na řádky.

Další varianty (V1 firma, real, přepočet mimo model):
- sazba 7,5 % + poplatek 1 % (typ „developerský / podnikatelský úvěr“): úroky 850 174, poplatky 229 727, celkem **1 079 901** (+26 %).
- sazba 5,84 % (čistý Hypoindex 5 let): úroky 662 002 (−6 %).
- předčasné splacení 1 % místo 0,5 %: +76 576.
- nebankovní (6,9 %, poplatek 4 %, bez poplatku za předčasné splacení): úroky 782 160 + poplatky 612 605 = **1 394 765** (+63 %).
- LTV 60 %: úroky 605 095 (−14 %), ale víc vlastních peněz.
- V1 s vlastními dodavateli (`dodavatel=remeslnici`): úroky 757 687 + poplatky 153 529 = 911 216 (stavba trvá o měsíc déle).

### Kontrola proti modelu a ověření vstupů (k 4. 11. 2026)

**Sazba.** Hypoindex 10/2026: průměr 5,79 %, fixace 5 let 5,84 % (LTV do 80 %); listopadová hodnota vyjde až v prosinci (`podklady/dane-financovani.md` ř. 139–140). Investiční hypotéky na pronájem: Raiffeisenbank 5,69 % (70 % LTV, fixace 15 let, 0 Kč zpracování), mBank 5,99 % (fixace 7 let, 0 Kč), Oberbank 6,10 % (fixace 5 let, zpracování 1 %); vedení úvěru 0 Kč, povinný účet ne (banky.cz, investiční hypotéky na pronájem, 4. 11. 2026; stránka neuvádí datum revize). Přirážka investiční hypotéky proti hypotéce na bydlení ~0,3–1,0 p. b. (financera.cz, bez jasného data). Model 6,2 % je tedy nad těmito sazbami o 0,1–0,5 p. b., což pokrývá přirážku za dům s trhlinami a rekonstrukci.

**Hlavní nejistota není sazba, ale typ úvěru.** Banky.cz, financera.cz ani KB metodika hypotečních úvěrů (platná od 25. 8. 2026) nezmiňují financování koupě, rekonstrukce a přeprodeje; investiční hypotéky předpokládají pronájem nebo započtení nájmu. Prodej po bytech je podnikání (§ 7), takže banka s největší pravděpodobností dá FO podnikatelský investiční / rekonstrukční úvěr (podklady uvádějí PRIBOR 3M + 2,5–4 % ≈ 6,5–8 %, zpracování 0,5–1 %, čerpání po etapách, `podklady/dane-financovani.md` ř. 152), případně nebankovní developerský úvěr: ZOXO od 6,9 %, poplatek 4 % (reprezentativní příklad), zdarma předčasné splacení po 6 měs., jen pro podnikatele s IČO, výhradně podnikatelské účely (zoxo.cz/developerske-projekty, stránka bez data, čtena 4. 11. 2026); Ronda Invest zhruba 9 % p. a. pro investora. Developerský úvěr pro FO jsem dohledal jen u nebankovních poskytovatelů; u bank nic konkrétního. Oproti modelu je to +1,3 p. b. u sazby a +0,5 p. b. u poplatku, tedy celkem 1,08 mil. Kč místo 0,86 mil. Kč, a nebankovní cesta až 1,39 mil. Kč. To je rozdíl +26 % až +63 % jen u této položky, ale ve dvojici s úrokem je to 0,2–0,5 mil. Kč z nákladů ~28 mil. Kč. Pes. scénář modelu (7,0 % a 1 %) tento případ z poloviny kryje.

**Strop úvěru 15,3 mil. Kč je optimistický.** Model počítá LTV 70 % z hodnoty bytů po dokončení (21,9 mil. Kč). Banky u hypoték a u domu s trhlinami berou odhad současného stavu (`podklady/dane-financovani.md` ř. 149 počítá max ~5,8 mil. Kč); LTV z budoucí hodnoty dávají jen rekonstrukční / developerské úvěry. Raiffeisenbank má strop úvěru 20 mil. Kč (V2 s 22 mil. by ho přesáhla). Menší úvěr snižuje úroky (LTV 60 % = −98 tis. Kč), ale zvyšuje potřebný vlastní kapitál (`vk`), což tato položka neukazuje.

**Poplatek za předčasné splacení (257/2016 § 117, znění 1. 10. 2026, zakonyprolidi.cz 4. 11. 2026).** Platí jen pro spotřebitelský úvěr; úvěr pro podnikání tam nespadá a poplatek je smluvní. Pro spotřebitelský úvěr na bydlení (§ 2 odst. 2 písm. b) je náhrada nejvýše 0,25 % za každý započatý rok zbývající fixace, max. 1 % z předčasně splacené části (§ 117 odst. 4), a zároveň jen „účelně vynaložené náklady“ = max. 1 000 Kč administrativa + kladný úrokový rozdíl proti referenční sazbě ČNB (§ 117a). Zadarmo je až při převodu nemovitosti po 24 měsících od uzavření smlouvy (§ 117 odst. 3 písm. e) a při úplatě do 25 % jistiny měsíc před výročím (písm. h). U nás je smlouva od měsíce 9, prodeje v měsících 18–23, takže je to 9–14 měsíců od uzavření a zdarma to není; při 5leté fixaci by zákonný strop byl 1 % (úrokový rozdíl při 6,2 % proti průměru ČNB nad 5 % by 1 % obvykle také dosáhl, ověřit u banky). Model 0,5 % je střed mezi spotřebitelským 1 % a podnikatelským 0–1 % (ZOXO po 6 měsících 0 %). V mém rozpisu 1 % = +76 576 Kč.

**Další náklady na úvěr, které položka nezahrnuje.** Odhad nemovitosti pro banku je v `IN["koupe_transakce"]` („posudek pro banku“), nepřidávám dvakrát. Pojištění nemovitosti s vinkulací je v `pojisteni_dan_mes` (15 tis. Kč ročně, položka „držení“). Vedení úvěru a účtu u investičních hypoték 0 Kč (banky.cz). Nezahrnuto nikde: kontroly čerpání stavby bankou (podklady ř. 152: 5–15 tis. Kč na etapu; při 4–8 čerpáních **~20–120 tis. Kč, ODHAD**) a dodatečný odhad při dělení zástavy po vzniku jednotek (**~10–30 tis. Kč, ODHAD**). Dohromady do 0,15 mil. Kč, tj. ~0,5 % nákladů; do rozpisu je nedávám a neměním kvůli tomu vstup.

**Časování a rozdíl proti zadání.** Zadání uvádí 683 641 + 145 380 = 829 021; aktuální `model.py` dává 702 811 + 153 151 = 855 962 (+3,2 %), nižší číslo je ze starší verze modelu (jiné náklady stavby, tedy jiné čerpání). Model.xlsx (23:04) ještě ukazuje 705 612 / 153 151, model.py se od něj ještě změnil (23:09). Rozdíl pod 10 %.

## B. DPH z prodeje po odpočtu

Režim V1 real: podstatná změna (§ 56 odst. 5 ZDPH) – náklady bez DPH 13,2 mil. Kč tvoří **46,5 %** základu daně (hranice 30 %) → první dodání bytů do konce 23. měsíce po kolaudaci je zdanitelné sazbou 12 %, FO je plátce od registrace před stavbou a odpočítává vstupy (`model.py` ř. 347–354, 380–385).

### Rozpis (Kč s DPH 12 %, z cen bytů s růstem do měsíce prodeje, `r["byty"]` × `idx`)

| Položka | Základ | Sazba | Realisticky Kč | Pes / opt | Zdroj |
|---|---|---|---|---|---|
| DPH na výstupu – byt A 4+1, 80 m², prodej měs. 18 | 6 833 360 | 12/112 | 732 145 | | `model.py` ř. 353, `rev` |
| DPH na výstupu – byt B 3+1, 67 m², měs. 19 | 6 020 527 | 12/112 | 645 057 | | totéž |
| DPH na výstupu – byt C 3+1, 75 m², měs. 20 | 6 756 018 | 12/112 | 723 859 | | totéž |
| DPH na výstupu – byt E 1+1, 42 m², měs. 21 | 4 117 789 | 12/112 | 441 192 | | totéž |
| DPH na výstupu – nový byt 2+kk č. 1 (1. NP), 40 m², měs. 22 | 3 759 204 | 12/112 | 402 772 | | totéž |
| DPH na výstupu – nový byt 2+kk č. 2 (1. NP), 40 m², měs. 23 | 3 768 475 | 12/112 | 403 765 | | totéž |
| **DPH na výstupu celkem** | 31 255 374 | | **3 348 790** | pes 2 640 390, opt 0 (osvobozeno, 24 % < 30 %) | |
| Odpočet – stavební práce 12 % (rekonstrukce, B→3+1, nebytová část → 2 byty) včetně spotřebované rezervy 15 % | 11,45 mil. s DPH × 1,15 | 12/112 | −1 399 507 | | ř. 270–281, `rozpis` |
| Odpočet – projekt, dozor, statik (služby) | 733 169 | 21/121 | −127 244 | | ř. 280–281 |
| Odpočet – statické zajištění trhlin | 800 000 | 12/112 | −85 714 | | `IN["rizika_navic"]` |
| Odpočet – provize realitní kanceláře | 1 323 tis. Kč (4,235 % z tržeb) | 21/121 | −229 727 | | ř. 380–382 |
| **Odpočet celkem** | | | **−1 842 192** | pes −2 773 540, opt 0 | |
| **DPH po odpočtu** (odvod státu) | | | **1 506 598** | pes −133 tis. (vratka), V2 real 1,53 mil. | |

Pes ukazuje odpočet vyšší než DPH na výstupu (stavba v pes. je 20 mil. Kč při tržbách ~24 mil.); skutečný výsledek je tedy vždy jen několik set tisíc až 1,5 mil. Kč a roste s tím, o kolik jsou ceny bytů vyšší než náklady.

V2 real (pro srovnání): DPH 4 807 730 − odpočet 3 275 426 = 1 532 304; z toho nástavba 12 % 1,07 mil. Kč a její projekt (21 %) 0,21 mil. Kč v odpočtu. Při V2 je podíl nákladů 31,1 % (těsně nad 30 %), ale nástavba tak jako tak zdaňuje první dodání nových bytů (`nast` v ř. 351).

### Kontrola sazby 12 % a vymezení (primární text ZDPH, verze 1. 1. – 31. 12. 2026, zakonyprolidi.cz, čteno 4. 11. 2026)

- **§ 48a odst. 5**: obytný prostor pro sociální bydlení = obytný prostor s podlahovou plochou **do 120 m²** (plus místnosti užívané s ním ve stejné stavbě). Jde o podlahovou plochu podle vyhlášky MF (§ 48a odst. 6), ne o plochu z NV 366/2013; všechny naše byty (42–80 m², nově vzniklé 40 m²) jsou hluboko pod limitem (nejvyšší A 4+1: 80 m²).
- **§ 49 odst. 3 písm. d)**: snížená sazba (12 %) u dodání **jednotky**, která nezahrnuje jiný prostor než obytný prostor pro sociální bydlení. Podmínka „jiný prostor“: pokud by byt zahrnoval garáž / nebytový prostor kromě místností užívaných s bytem, byl by 21 %. Naše jednotky takové nezahrnují (stání na pozemku SPÚ se prodává mimo jednotku).
- **§ 48a odst. 1 písm. a)** (celý bytový dům) vyžaduje, aby obytný prostor pro sociální bydlení tvořil více než polovinu podlahové plochy; pro prodej po bytech (jednotek) to nehraje roli, pro prodej vcelku (A0, A2) ano a splněno by bylo (byty ≤ 120 m²).
- **Stavební práce**: § 49 odst. 4 (práce na dokončené stavbě pro bydlení 12 %) a odst. 2 (přestavba nebytového prostoru na sociální bydlení 12 %). Materiál kupovaný zvlášť (varianta vlastní dodavatelé) a služby 21 % (model je tak počítá). Tyto sazby v modelu sedí.
- **Zdanitelnost, § 56**: odst. 1 – první dodání do konce 23. kalendářního měsíce po měsíci dokončení / podstatné změny je zdanitelné, jinak osvobozeno; odst. 3 – počátek lhůty je kolaudace po podstatné změně; odst. 5 – podstatná změna = změna využití nebo podmínek obývání, pokud náklady bez DPH, které nesl prodávající, přesáhnou **30 % základu daně** při následujícím dodání. Úroky se do nákladů nepočítají (GFŘ, `podklady/dane-financovani.md` ř. 66). Změna nebytové části na byty je změna využití, takže test se plní.
- Test je podle GFŘ po jednotkách (`podklady/dane-financovani.md` ř. 66), model počítá souhrnně (ponytail komentář ř. 346). Hrubý přepočet (ODHAD): staré byty A, B, C, E ~45 %, dva nové byty z nebytové části ~56 % (jejich přestavba 3,6 mil. Kč je i s rezervou ~3,7 mil. bez DPH proti 6,7 mil. základu daně). Všechny jednotky jsou nad 30 %, takže souhrnný test nic nezkresluje.

### Může být prodej nezdaněný? (jen popis, rozhodnutí je na uživateli)

1. **Náklady do 30 % na každou jednotku.** U V1 by stavba bez DPH musela klesnout z 13,2 mil. na ~8,4 mil. Kč (−4,8 mil., při tržbách ~27,9 mil. bez DPH), což znamená vynechat střechu, trhliny nebo nebytové byty, jak `postup.md` ř. 20 uvádí jako důvod střední úrovně. V opt scénáři modelu (24 %) je prodej osvobozen sám od sebe a registrace nevznikne.
2. **Počkat se zdaněním na konec lhůty (§ 56 odst. 1).** Kolaudace je v modelu v měsíci 16 (`t_projekt` 3 + `t_nebyt_navic` 4 + `t_stavba` 9), osvobozené první dodání je možné od měsíce ~40, tj. o ~17 měsíců později než plánovaný prodej v měsících 18–23. Pak odpadá i registrace a odpočet; ušetří se čistých **1,51 mil. Kč**. Náklad: dalších 17 měsíců úroků z ~15,3 mil. Kč (~1,35 mil. Kč při 6,2 %), držení ~0,08 mil. Kč, vázaný kapitál a riziko trhu; protistrana: nájem bytů je v DPH osvobozen (§ 56a) a při 344 m², 280 Kč/m², obsazenosti 92 % a nákladech 12 % dává ~78 tis. Kč měsíčně (**ODHAD**, ~1,3 mil. Kč za 17 měsíců; `IN["najem_m2"]`, `neobsazenost`, `najem_opex`) a ceny rostou ~3 % ročně. Podobný scénář už model má jako `B2h` (nájem 24 měsíců). Výsledek je zhruba vyrovnaný až mírně příznivý, ale vážné je, že plán banky a nájemci by se řešily úplně jinak; k rozhodnutí patří poradce.
3. **Daňová volba (§ 56 odst. 8)** je opačný směr: zdanit i osvobozené dodání; pro FO kupující neplátce k ničemu.
4. Pozor na úpravu odpočtu: pokud se první dodání nakonec posune mimo zdanitelné okno, nebo se použije osvobozeně, vrací se odpočet za ~10 let (§ 78d ZDPH, nutno ověřit s poradcem). Registrace musí proběhnout před prvními nákupy materiálu a prací, jinak odpočet z nich nevznikne (model to předpokládá, ř. 354).

### Kontrola proti modelu

Zadání: 3 178 870 − 1 860 719 = **1 318 151**. Aktuální model: 3 348 790 − 1 842 192 = **1 506 598** (+14 %, +188 tis. Kč). Příčina je změna modelu po vytvoření zadání, ne chyba rozpisu: DPH na výstupu je o 170 tis. Kč vyšší (vyšší ceny bytů / jiný růst `idx`), odpočet o 18 tis. Kč nižší (menší stavba: `rizika_navic` 1,0 → 0,8 mil., `b31_zmeny` 150 → 82 tis.). Rozpis sedí s modelem na 1 Kč.

Co v odpočtu **chybí** (nezahrnuje ho model): DPH 21 % z služeb souvisejících s prodejem a přípravou, které jsou ve firemních fakturách: advokát a marketing při prodeji 6 × 40 000 Kč = 240 000 (DPH 41 tis.), PENB 15 000 (2,6 tis.), rozdělení na jednotky 70 000 (12 tis.), energie v držení ~69 000 (12 tis.), advokát při koupi z `koupe_transakce` (část, ODHAD). Celkem **~70–100 tis. Kč** další odpočet (**ODHAD**, ~6 % položky), pokud faktury vystaví plátci. Neměním: pod 10 % a ověřit, kdo faktury vystaví.

Časování: model dává odpočet i výstup do posledního měsíce. Ve skutečnosti se odpočet uplatní průběžně (vratka do 30 dní po kontrole) a DPH z prodeje se odvádí do 25. dne po měsíci uskutečnění (u bytu vklad do KN), takže raná vratka sníží kapitálovou potřebu (nikoli úrok, protože úvěr je zastropovaný) a DPH z prvních prodejů je potřeba držet stranou, aby se nepoužilo na splátky úvěru. Model počítá celé tržby na splácení úvěru, což mírně podhodnocuje cenu úvěru (nejvíc u prvních prodejů, zhruba +20–50 tis. Kč úroků, **ODHAD**).

## C. Doporučení

**Beze změny** u `sazba`, `ltv`, `uver_poplatek`, `predcasne`, `pristup_mes` a vzorců DPH. Důvod: sazba 6,2 % je v pásmu zdrojů (investiční hypotéky 5,69–6,10 %, Hypoindex 5,84 %, podnikatelský úvěr 6,5–8 %), poplatky a rozdíl proti zadání jsou v obou položkách pod nebo u hranice 10 % rozdílu, který vyvolává změnu, a 14 % rozdíl DPH je způsoben vývojem modelu, ne mým zdrojem.

Poznámky pro rozhodnutí uživatele (nic nepřepisuji): (1) typ úvěru (investiční hypotéka vs. podnikatelský / rekonstrukční / nebankovní úvěr) je největší nejistota; při 7,5 % a 1 % by položka byla 1,08 mil. Kč místo 0,86 mil. Kč, při nebankovním 6,9 % a 4 % ~1,4 mil. Kč; (2) strop úvěru 15,3 mil. Kč je z hodnoty po dokončení, hypotéka z odhadu současného stavu dá jen ~5,8 mil. Kč; (3) cesta bez DPH (počkat 17 měsíců po kolaudaci) je vyrovnaná, jak je popsáno výše, a je na uživateli.

## D. Pro report (V1 firma, realisticky)

Úroky a poplatky úvěru (součet 855 962):

```python
[
    ("úroky z úvěru na koupi domu (tranše 8,63 mil. Kč, sazba 6,2 %)", 433044),
    ("úroky z čerpání na stavbu (6,69 mil. Kč průběžně, sazba 6,2 %)", 269767),
    ("poplatek bance za zpracování úvěru na koupi (0,5 %)", 43139),
    ("poplatek bance za zpracování stavebních čerpání (0,5 %)", 33436),
    ("poplatek za předčasné splacení při prodeji bytů (0,5 % z 15,3 mil. Kč)", 76576),
]
```

DPH z prodeje po odpočtu (součet 1 506 598; kladné = platí se státu, záporné = odpočet):

```python
[
    ("DPH 12 % z prodeje bytu A 4+1 (80 m²)", 732145),
    ("DPH 12 % z prodeje bytu B 3+1 (67 m²)", 645057),
    ("DPH 12 % z prodeje bytu C 3+1 (75 m²)", 723859),
    ("DPH 12 % z prodeje bytu E 1+1 (42 m²)", 441192),
    ("DPH 12 % z prodeje dvou nových bytů 2+kk v přízemí (2 × 40 m²)", 806537),
    ("odpočet DPH ze stavebních prací včetně rezervy", -1399507),
    ("odpočet DPH z projektu, dozoru a statika", -127244),
    ("odpočet DPH ze statického zajištění", -85714),
    ("odpočet DPH z provize realitní kanceláře", -229727),
]
```
