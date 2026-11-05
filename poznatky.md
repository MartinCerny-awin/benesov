# Poznatky

Co se ukázalo jako zavádějící a jak se tomu vyhnout.

- 2026-11-04: Ověřovatel se všemi 26 tvrzeními najednou (~100 obrázků) se zasekl. Ověřovat po bytech.
- 2026-11-04: Snímky po 2 s nestačí na počítání pokojů u rychle natočeného videa; pro sporné byty vytáhnout snímky po 0,5 s (`prace/husto/`).
- 2026-11-04: Mentolový sokl je ve vstupní hale v přízemí i na horní podestě – podle barvy stěny nejde určit podlaží. Lepší je časová návaznost videí a zábradlí kolem schodiště dolů.
- 2026-11-04: Moje tvrzení „do zeleného pokoje C se vchází dveřmi s kulatou koulí“ bylo přehnané – ty dveře vypadají jako skříň. Nepřipisovat vstup do místnosti dveřím, které nikdo neotevřel; stačí časová návaznost a shodné prvky.
- 2026-11-04: Dva ověřovatelé shodně označili zelenkavý kout bytu B za komoru. Byl to roh kuchyně, viditelný při otočení kamery od sporáku. U „malé místnosti bez okna“ vždy zkontrolovat, jestli nejde o jiný úhel sousední místnosti (stejná tapeta, plynulé otočení kamery).
- 2026-11-04: Rozložení (strany, pořadí dveří) se nejlépe ověřuje dvoufázově: agent nejdřív rekonstruuje naslepo, pak jiný agent ověří sjednocená tvrzení.
- 2026-11-04: Topologická schémata bytu po bytu „nedávají smysl“ – uživatel chce půdorys podlaží. Vždy začít obrysem z RÚIAN (ags.cuzk.cz, vrstva StavebniObjekt, dotaz podle čísla domovního a části obce) a okny na fasádách; byty musí zapadnout do jednoho podlaží.
- 2026-11-04: Nejsilnější vazba interiér ↔ fasáda je tvar a pořadí oken (zevnitř zrcadlově), barva rámů, žaluzie a záclony. Polohy ze šikmé fotky přepočítávat s perspektivní korekcí, i tak ±1 m.
- 2026-11-04: Popisovač (Haiku) občas plete chodbu bytu se společnou chodbou domu a viděl „šikmý strop“ tam, kde žádný není. Jeho popisy berte jen jako vodítko.

- 2026-11-04 (propočet): „384,46 m² (budovy)“ v inzerátu ČD není plocha bytů ani zastavěná plocha (RÚIAN 239 m²); nejspíš čistá plocha obou podlaží vč. dílny, kotelny, skladů. Byty mají jen ~260 m² (odhad z fotek). Kč/m² z 384 m² nelze srovnávat s Kč/m² bytů.
- 2026-11-04 (propočet): Karta nabídky ČD je nespolehlivá – „Stav: Dobrý“ (trhliny, plíseň), „Voda/Kanalizace: Ne“ (RÚIAN ano), „Věcné břemeno: Ne“ (přístup přes cizí pozemek SPÚ bez VB), tvrzení o ochranném pásmu dráhy (kolej ~290 m, pásmo 60 m) a FAQ s daní z nabytí, která neplatí od 2020. Brát jen jako upozornění, ověřit z RÚIAN/KN.
- 2026-11-04 (propočet): Sdílený limit WebSearch se vyčerpá, když běží ~9 subagentů naráz; pozdější agenti pak nemají vyhledávání. Rešerše dávkovat a nechat jim WebFetch na konkrétní URL.
- 2026-11-04 (propočet): Sreality kategorie „činžovní domy“ přes URL/API nefungovala (vracela rodinné domy / 404). Ceny celých domů z portálů jsou nabídkové a vzorek v okrese je malý.
- 2026-11-04 (propočet): Výchozí předpoklady v zadání byly zastaralé: limit 40 mil. Kč u časového testu platí jen pro krypto, ne nemovitosti; DPH od 7/2025 = 23 měsíců a podstatná změna nad 30 % ceny (dřív 5 let a 50 %); § 34 stavebního zákona neupravuje stavební úpravy.
- 2026-11-04 (propočet): Klasifikace stavu bytů z inzerátů podle výpisu portálu je nespolehlivá – „po rekonstrukci“ často znamená jen osvěžení nebo rekonstrukci domu, ne bytu; ve skupině „malé původní“ nebyl ani jeden skutečně původní byt. Stav ověřovat v textu inzerátu.
- 2026-11-04 (propočet): Nabídkové ceny bytů v Benešově (95–130 tis. Kč/m²) jsou vysoko nad realizovanými (REAS medián 78,8 tis., ČSÚ okres 2025 61,4 tis. přes všechny stavy). Nabídky nebrat jako prodejní ceny.
- 2026-11-04 (propočet): Ceny celých domů z nabídek (40–60 tis. Kč/m²) neodpovídají reziduální hodnotě domu k rekonstrukci; nezávislý odhad 11,5 mil. vs. reziduálně ~8–9,5 mil. U domů k rekonstrukci vždy dopočítat reziduálně.
- 2026-11-04 (propočet): Sreality JSON API funguje jako `/api/v1/estates/search?...` a `/api/v1/estates/<id>` (Benešov locality_district_id=48, činžovní domy category_main_cb=4&category_sub_cb=38); staré `/api/cs/v2` vrací 404.
- 2026-11-04 (propočet): Výchozí parametr „vlastní kapitál 30 % ceny + rezerva“ je u domu k rekonstrukci nereálný – banka půjčí do 70 % hodnoty hotového domu jako celku (ne součtu bytů) a bez zapsaného přístupu vůbec.
- 2026-11-04: Byt B jsme dvakrát „ověřili“ jako 2+1 a uživatel to opravil na 3+1. Ověřovatelé potvrzují jen to, co je na záběrech. Když video nepokrývá celý byt (rychlá prohlídka, neotevřené nebo zazděné dveře), „žádný další pokoj“ nesmí být **jisté**. Nejvýš pravděpodobné, s poznámkou, která část bytu nebyla natočená.
- 2026-11-05: REAS chytrý odhad plochu bytu nezjistí, jen se na ni ptá. Nový odhad přes formulář vyžaduje e-mail a souhlas s podmínkami; bez toho jde přepínat parametry uloženého bytu v „Moje nemovitosti“ (Upravit údaje) a číst přesné ceny z `atlas.reas.cz/atlas/units/<unitId>/dashboard?withEstimate=true&model=FLAT_APPROX` (`data.estimate.price` low/mid/high). Formulář /chci-odhad blokuje odchod dialogem „Opustit stránku?“ – neodcházet z něj historií.
