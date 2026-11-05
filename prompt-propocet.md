# Prompt: propočet koupě, renovace a prodeje – č.p. 1598 Benešov

> Vlož celý text níže do nové session ve složce `Benesov`. Úloha je na dlouho (desítky minut až hodiny) a jde ji kdykoli přerušit a navázat, protože stav se drží v souborech.

---

Chci propočítat, jestli se vyplatí koupit dům č.p. 1598 v Benešově a co s ním potom: rovnou ho přeprodat (třeba jen s lepším marketingem), opravit a prodat celý nebo po bytech, změnit dispozice bytů, nebo přistavět půdní vestavbu či ustupující podlaží. Pracuj důkladně a dlouho, používej subagenty, důležitá čísla nech nezávisle ověřit a nespokoj se prvním odhadem. Na konci chci srovnání možností, doporučení, co dává smysl, čísla se zdroji a seznam věcí, které musím ověřit sám.

## Co už máme

- `NB503213.pdf` – inzerát prodávajícího (ČD): netypový bytový dům, 2 nadzemní podlaží, 384,46 m² budovy, 239 m² pozemku, 8 326 000 Kč. Přečti celý, včetně podmínek prodeje (výběrové řízení, kauce, lhůty, stav nájmů).
- `photos/` a `prace/` – fotky a videa z prohlídky 3. 11. 2026 a rozpracované dispozice bytů. Výsledky dispozic jsou v `postup.md` (byty A, B, C, E; dispozice ještě nejsou ověřené – ber je jako předběžné).
- `fakta.md` – fakta potvrzená mnou. Mají přednost před vším, co najdeš.
- `poznatky.md` – co se ukázalo jako zavádějící. Přečti před začátkem a doplňuj.

## Moje parametry (pokud nejsou vyplněné, použij výchozí a uveď to ve výsledku)

- Vlastní kapitál: _?_ (výchozí: 30 % kupní ceny + celá rezerva)
- Financování: _?_ (výchozí: úvěr na investiční nemovitost, aktuální sazby listopad 2026)
- Kupuji jako: _?_ (výchozí: fyzická osoba, neplátce DPH)
- Cílový zisk: _?_ (výchozí: aspoň 20 % ze všech vložených nákladů)
- Rekonstrukce: _?_ (výchozí: vše dodavatelsky, nic svépomocí)

## Stav práce

Založ `propocet/postup.md` (co je hotovo, otevřené otázky, rozhodnutí) a průběžné výsledky subagentů ukládej do `propocet/podklady/<tema>.md`. Po každém kroku aktualizuj `postup.md`, aby šlo po přerušení navázat. Když navazuješ, nejdřív přečti `postup.md`, `fakta.md` a `poznatky.md` a nedělej hotové znovu.

## Krok 1 – sběr podkladů (subagenti paralelně)

Spusť naráz subagenty, každého s úzkým zadáním a výstupem do vlastního souboru v `propocet/podklady/`. Na mechanický sběr inzerátů stačí levný model (Haiku), na rešerše předpisů a územního plánu silnější (Sonnet). Každé číslo musí mít zdroj (URL nebo soubor) a datum. Odhad bez zdroje musí být označený jako odhad.

1. **Katastr a právní stav** (`katastr.md`): adresa, parcely, LV, druh a způsob využití stavby, věcná břemena, zástavy, předkupní práva, ochrana (památka, ochranné pásmo dráhy). Zdroj nahlizenidokn.cuzk.cz. Jestli dům sousedí s tratí nebo nádražím, zjisti, co z toho plyne (hluk, ochranné pásmo, omezení stavby).
2. **Technický stav a rozpočet rekonstrukce** (`stav.md`): z fotek, videí a popisů v `prace/` sepiš po bytech a po společných částech (střecha, krov, fasáda, okna, rozvody elektro/voda/odpady, topení a kotelna, vlhkost ve sklepě, schodiště, statika). U každé položky urči stav (dobrý / opotřebený / na konci životnosti / nejde poznat) s odkazem na konkrétní fotku nebo snímek, který to dokládá. Pak sestav rozpočet ve třech úrovních: **kosmetika** (vyklidit, vymalovat, podlahy, úklid – na prodej), **standardní rekonstrukce** (bytová jádra, kuchyně, elektro a voda v bytech, okna) a **kompletní** (i společné části, střecha, fasáda/zateplení, topení, stoupačky). Ceny podle aktuálních cen 2026 v Kč/m² nebo za kus, ze zdrojů (ceníky firem, ÚRS, články s cenami), a přepočti na Kč/m² podlahové plochy, aby šly porovnat s běžnými cenami rekonstrukcí. Co z fotek nejde poznat, zapiš jako riziko s rozpětím ceny. Zohledni `poznatky.md` – popisy od Haiku jsou jen vodítko, stav posuzuj z obrázků samotných.
3. **Srovnání cen – byty** (`ceny-byty.md`): byty v Benešově, zvlášť původní stav / po rekonstrukci / novostavba, v Kč/m². Rozliš nabídkové ceny (Sreality, Bezrealitky, iDNES Reality) a realizované ceny (cenová mapa, statistiky ČSÚ, Deloitte, Valuo a podobné). Uveď běžnou slevu z nabídkové ceny a průměrnou realizovanou cenu za posledních 12–24 měsíců zvlášť pro malé (1+kk až 2+1) a velké byty (3+1 a víc) – podle toho se rozhoduje o změně dispozic. Aspoň 15 srovnatelných bytů s odkazem, plochou, dispozicí, stavem a ulicí. Čím blíž k č.p. 1598, tím lépe.
4. **Srovnání cen – celé domy a nájmy** (`ceny-domy.md`): prodané a nabízené činžovní a vícebytové domy v Benešově a okolí (Kč/m²), a nájmy bytů v Benešově (Kč/m²/měsíc) pro variantu „držet a pronajímat“.
5. **Lokalita** (`lokalita.md`): kde přesně dům je, vzdálenost k nádraží, centru, školám, obchodům; doprava do Prahy; hluk (železnice, silnice), záplavové území; plánované projekty ve městě, které cenu zvednou nebo sníží.
6. **Územní plán a nástavba** (`uzemni-plan.md`): platný ÚP Benešova a jeho změny (a regulační plán nebo územní studie, pokud pro lokalitu existují) – do jaké plochy parcela patří, výšková regulace / max. počet podlaží nebo výška římsy a hřebene, koeficient zastavění a zeleně, regulativy pro bytové domy. Posuď zvlášť tři možnosti: **půdní vestavba** do stávajícího krovu (z fotek a videí zjisti, jestli dům má půdu, jaký tvar a sklon střechy, zda jde o přípustnou výšku pro obytné podkroví), **ustupující podlaží** a **plné 3. nadzemní podlaží**. U každé: co ÚP dovoluje, co k tomu chce stavební zákon 283/2021 Sb. (povolení záměru, lhůty), parkovací stání pro nové byty, požární bezpečnost, výtah, co musí ověřit statik (založení, nosnost zdí a stropů, krov), přidaná podlahová plocha, počet nových bytů a cena v Kč/m². Rozlišuj, co ÚP výslovně říká a co je tvůj výklad.
7. **Změny dispozic** (`dispozice-zmeny.md`): z předběžných dispozic v `postup.md` navrhni, jestli dává smysl byty rozdělit (např. velký byt na dva menší), spojit nebo přeuspořádat. U každé změny: kolik bytů a jakých dispozic vznikne, kudy vedou stoupačky a nosné zdi (nakolik to jde z fotek poznat), nové koupelny a kuchyně, zda jde o stavební úpravu bez povolení, nebo změnu stavby s povolením, dopad na parkovací stání a na rozdělení na jednotky. Cenu změn odhadni zvlášť nad standardní rekonstrukci.
8. **Daně, transakce a financování** (`dane-financovani.md`): daň z příjmu při prodeji (časový test, živnost vs. ostatní příjem), DPH u prodeje bytů po rekonstrukci a nástavbě, náklady rozdělení domu na jednotky (prohlášení vlastníka, vznik SVJ, zápis do KN), PENB, provize RK, advokátní úschova, poplatky KN, pojištění, daň z nemovitých věcí, aktuální sazby a LTV úvěrů na investiční nemovitost a pravidla ČNB. Všechno k listopadu 2026.

Když subagent narazí na CAPTCHA nebo přihlášení, nesnaží se ho obejít, zapíše to a jede dál. Nikomu nic neposílej (stavební úřad, RK, ČD) – dotazy jen sepiš, pošlu je sám.

## Krok 2 – kontrola podkladů

Projdi soubory z kroku 1. Kde je číslo bez zdroje, kde si zdroje odporují nebo je vzorek srovnání malý, pošli cíleného subagenta doplnit. Rozpory zapiš do `postup.md`. Opakuj, dokud každý vstup modelu nemá zdroj nebo jasně označený odhad s rozpětím.

Pak udělej **rychlou kontrolu stopek**: podmínky prodeje ČD (výběrové řízení, kauce, zákazy přeprodeje), nájemníci, ochranné pásmo dráhy, zástavy, ÚP vylučující nástavbu. Co některou variantu vylučuje, zapiš do `postup.md` a tu variantu dál nepočítej, jen uveď proč. Když je vyloučené všechno, skonči rovnou krokem 5.

## Krok 3 – model

Spočítej v Pythonu (skript `propocet/model.py`, výstup i do `propocet/model.xlsx`) tyto varianty:

- **A0** – koupit a rovnou přeprodat bez úprav (jen transakční náklady a čas)
- **A1** – koupit, vyklidit, kosmetika a lepší marketing (profi fotky, půdorysy, 3D prohlídka, home staging, popis s možnostmi nástavby a rozdělení) a prodat celý dům; odhadni, o kolik marketing reálně zvedne cenu a zkrátí prodej, se zdroji
- **A2** – koupit, opravit společné části a byty, prodat celý dům
- **B** – koupit, opravit, rozdělit na jednotky a prodat po bytech
- **B2** – jako B plus změna dispozic z `dispozice-zmeny.md`
- **C1 / C2 / C3** – jako B (nebo B2, pokud vyjde líp) plus půdní vestavba / ustupující podlaží / plné 3. NP; jen ty, které ÚP připouští, u ostatních uveď, za jakých podmínek by šly
- **D** – koupit, opravit a pronajímat (výnos, cash flow, hodnota po 5 a 10 letech)
- **E** – koupit, získat povolení nástavby a prodat dům s povolením (bez stavby) – často lepší poměr zisku k riziku

U každé varianty pesimistický, realistický a optimistický scénář a časová osa po měsících (koupě, projekt a povolení, stavba, prodej), protože úroky během čekání rozhodují. Pokud jsou byty pronajaté, počítej v každé variantě s nájemníky: příjem z nájmu během čekání, doba a náklady ukončení nájmů podle občanského zákoníku a nižší cena při prodeji s nájemníky. Výstupy:

- všechny náklady (koupě, transakce, projekt, povolení, stavba, rezerva aspoň 15 %, financování, daně, prodej)
- čistý zisk, ROI, IRR, roční výnos z vlastního kapitálu
- **maximální kupní cena**, při které varianta ještě dá cílový zisk – to je nejdůležitější číslo pro nabídku
- citlivost: prodejní cena ±10 %, náklady rekonstrukce +20 %, prodloužení o 6 a 12 měsíců, sazba +1 p.b.

Skript musí mít jednoduchou kontrolu (`assert`), že součty sedí.

## Krok 4 – nezávislé ověření

Spusť paralelně tři nezávislé subagenty, žádný nedostane tvoje závěry:

1. **Druhý odhad rozpočtu rekonstrukce** – dostane jen fotky, snímky z `prace/` a plochy, ne `stav.md`, a odhadne kosmetiku, standardní a kompletní rekonstrukci sám.
2. **Druhý odhad prodejních cen** – dostane jen adresu, plochy a dispozice a sám najde srovnatelné byty a domy.
3. **Revizor** – dostane soubory v `propocet/podklady/` a `model.py` a hledá chyby: dvakrát započtené nebo zapomenuté náklady, nereálné prodejní ceny, srovnání, která nejsou srovnatelná, chybný výklad ÚP nebo daní.

Kde se odhady 1 a 2 liší od tvých o víc než 15 %, dohledej proč a rozhodni se se zdůvodněním. Nálezy revizora zapracuj nebo napiš, proč ne. Po opravách přepočítej model.

## Krok 5 – výstup

Vytvoř přehledný report (artifact) s:

1. doporučením v jedné větě a maximální kupní cenou pro každou variantu,
2. **co dává smysl**: varianty seřazené podle zisku vůči riziku a vlastnímu kapitálu, u vyřazených jednou větou proč (např. „nástavba nevychází, protože…“), a možné kombinace a postup (např. koupit, nejdřív požádat o povolení nástavby a podle výsledku prodat nebo stavět),
3. odhadem současného stavu domu po bytech a společných částech s odkazy na fotky a rozpočty kosmetika / standard / kompletní,
4. tabulkou variant a scénářů,
5. hlavními riziky seřazenými podle dopadu,
6. srovnávacími byty a domy s odkazy a průměrnými realizovanými cenami,
7. **seznamem otázek k ověření** – co se zeptat ČD, stavebního úřadu Benešov, statika, banky a co prohlédnout při druhé prohlídce.

Do `poznatky.md` zapiš, co se ukázalo jako zavádějící (zdroje, které lžou, nesrovnatelná data apod.).
