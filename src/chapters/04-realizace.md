# Realizace

Pro realizaci aplikace bude použit herní engine *Unity*. *Unity* je multi-platformní herní engine napsaný v C a C++ určený k vývoji her pro PC, konzole a mobilní zařízení. Je to v současnosti jeden z nejvhodnějších a nejpopulárnějších nástrojů na vývoj her pro virtuální realitu.

Ač jde o nástroj pro tvorbu her, je vhodným nástrojem i pro tvorbu aplikace určené pro virtuální realitu, jelikož aplikace pro virtuální realitu jsou vykreslovány stereoskopicky a trojrozměrně. Předmětem tvorby této aplikace by neměla být tvorba takového vykreslovacího jádra, ale spíše samotné aplikace. Proto je využito herního enginu, aby čas strávený tvorbou vykreslovacího jádra byl využit spíše pro tvorbu samotné aplikace.

Jako název aplikace jsem zvolil sousloví **Immersion VR**, které slouží k jednoznačné identifikaci produktu. Slovo "immersion" lze přeložit jako "ponoření" a symbolicky tak vyjadřuje uživatelův proces "ponoření" do virtuální reality.

## Jazyk implementace

Herní engine *Unity* podporuje několik programovacích jazyků, ve kterých můžou být vytvořeny skripty pro ovládání logiky aplikace. Jsou to jazyky *C#*, *JavaScript* a *Boo*. Tato kapitola se bude zabývat volbou jednoho z těchto jazyků, ovšem výhradně v souvislosti s použitím v enginu *Unity*.

Výběr jazyku budou ovlivňovat i mé předchozí zkušenosti. V *Unity* jsem doposud napsal několik skriptů pouze v jazyce *C#*. Na druhou stranu mám s jazykem *JavaScript* mnohem hlubší zkušenosti a znalosti, ovšem mimo herní vývoj -- především ve webovém prostředí.

Po rešerši z různorodých názorů vývojářů bylo možné vyderivovat následující doporučení, týkající se výběru jazyka pro *Unity*:

 - Záleží na předchozích zkušenostech s jazykem.
 - JavaScript, resp. UnityScript není totožný s webovým JavaScriptem. Jde spíše o JavaScript-like syntaxi.
 - JavaScript je ve srovnání s C# méně upovídaný.
 - JavaScript za vývojáře řeší na pozadí více věcí, než C#. Jde tak o jednodušší jazyk.
 - C# používá majorita Unity vývojářů. Je tak snazší vyhledat pomoc při problémech.
 - C# má kvalitní MSDN dokumentaci.
 - C# je rychlejší, než JavaScript ale ne znatelně.
 - Boo se nedoporučuje, používá jej pouze malý zlomek vývojářů.

Jako jazyk implementace tak byl zvolen jazyk *C#*, z důvodu mých předchozích zkušeností, majority komunity, která může poskytnout pomoc v případě problémů a z důvodu existence kvalitní dokumentace.

## Proof of Concept

V aplikaci lze rozlišit klíčové funkce, které jsou poněkud specifické a charakteristické pro danou aplikaci. Ač je snadné navrhnout způsob řešení implementace takových funkcí, je vhodné tyto funkce podrobit principem **Proof of Concept** — důkaz existence původně jen teoreticky předpokládané funkcionality, tedy rychlou implementací konkrétních funkcí nezávisle na zasazení do koncové aplikace.

Na základě takové implementace je pak možné potvrdit, zda-li je návrh implementace klíčových funkcí, na kterých aplikace stojí, realizovatelný.

Jednou z takových funkcí je zobrazení her, které vlastní herna na svém účtu platformy *Steam*. Aby bylo možné zobrazení provést, je nutné o hrách stáhnout informace, podle požadavku *F-C02* -- stažení dat o VR aplikacích. Taková data jsou přístupná pomocí některého z API rozhraní služby *Steam*. Předmětem POC bude takový zdroj dat nalézt a implementovat práci s takovým zdrojem do enginu *Unity*.

Další funkcí, kterou je nutné podrobit POC je samotný spouštěč her a to konkrétně funkci spuštění a opouštění VR aplikací, podle požadavků *F-C03* a *F-C04* -- spuštění a ukončení uživatelem vybrané VR aplikace. Je nutné vyzkoušet, jak z aplikace vytvořené v *Unity* spouštět aplikace nainstalované skrz platformu *Steam* a jak detekovat jejich ukončení a vyvolání spouštěče opět do popředí.

### Stahování informací o aplikacích

Aby došlo ke splnění požadavku *F-C02*, je nutné získat následující informace:

 - Jaké aplikace jsou zakoupené na účtě herny platformy Steam
 - Které z nich jsou nainstalovány na konkrétním počítači
 - Název aplikace, její krátký oficiální popis od výrobce, obrázek aplikace

Mezi informace nepatří navržené krátké video ze hry, či popis úrovně intenzity, jelikož platforma Steam není zdrojem takových dat. Předmětem zíkáním těchto dat se bude zabývat jedna z následujících kapitol.

Steam nabízí více API rozhraní pro komunikaci, specifická pro různá použití, jako je např. přístup k různorodým API v rámci partnerského progrmu *Steamworks*, které by dávalo smysl použít, jelikož je běžně používáno pro aplikace a hry distribuované skrz platformu Steam, které jsou s platformou integrovány a pracují s ní, což se velmi podobá aplikací této závěrečné práce (minimálně splňuje podmínku práce s platformou Steam). *Steamworks SDK* je ovšem dostupné pouze pro partnery společnosti, což nejeví problém, partnerství je možné získat. Jde však o mírně zdlouhavý proces a pro účely stažení informací by šlo o neefektivní postup. Komplikaci by mohly představovat i licenční podmínky platformy, při použití pro účely závěrečné práce.

Ideálním API rozhraním se tak ukázalo veřejné *Steam Web API*, které ač, jak je z názvu patrné, je určeno pro použití webovými službami, je ideálním a snadno přístupným zdrojem informací, které jsou nutné pro splnění požadavku. Rozhraní disponuje několika endpointy, nabízejícími různá data, pro nás zajímavým endpointem je však *GetOwnedGames-v0001*, který vrací seznam všech her, které vlastní určitý účet platformy Steam.

Situace se však komplikuje ve dvou bodech -- viditelností dat a autentizací:

Pro stažení takových dat z účtu pomocí tohoto API, je nutné, aby daný účet měl v nastavení účtu platformy Steam povolen veřejný přístup k datům, jako je např. seznam her, který potřebujeme. V naší situaci by to neměl být problém za předpokladu, že herna nemá důvod chtít skrývat seznam her, který vlastní na svých účtech. V případě, že herna z libovolného důvodu nebude chtít zveřejnit svůj seznam her na platformě Steam, tento postup tak selhává a není možné herně nabídnout takovou aplikaci bez toho, aniž by se využilo jiného API rozhraní služby Steam. Tomuto problému však nepřikládám vážnost, protože se obecně dá předpokládat, že herna svůj účet zveřejní. Lze totiž vycházet z faktu, že seznam her většina heren již zveřejnila na svých webových stránkách, aby zákazníci mohli vidět, jaké tituly herna nabízí.

Další, tentokrát už mnohem méně závažnější komplikací, je způsob autentizace pro použití *Steam Web API*. Steam nabízí dva způsoby -- vygenerováním statického klíče na jejich stránkách a jeho použitím při vytváření požadavků na API, nebo implementací OpenID přihlašování. Vzhledem k tomu, že je aplikace z podstaty zadání učená pro použití (resp. konfiguraci) jedním subjektem (či malým počtem subjektů), vygenerování klíče je velmi jednoduché a v ideálním případě je nutné takový proces provést jen jednou, je z důvodu časové efektivity a jednoduchosti implementace použita autorizace pomocí klíče.

Získáním takových dat z tohoto API rozhraní jsou však splněny pouze dva z tří výše zmíněných bodů -- jaké aplikace jsou zakoupené a jaké jsou jejich názvy, krátké popisy a obrázky aplikací. Chybí informace o tom, zda-li jsou na systému nainstalovány a připraveny ke spuštění.

Pokud na chvíli odběhneme do následující kapitoly zabývající se spouštěním aplikací, zjistíme, že lze aplikace výhodně a jednoduše spouštět pomocí systémového protokolu `steam://` a jeho akce `steam://run/<appid>`. Tato akce se chová tak, že pokud je v systému aplikace nainstalovaná, provede její spuštění. V opačném případě se zahájí proces instalace a provede uživatele procesem stažení a nainstalování takové aplikace. Z pohledu návštěvníka herny je však takové chování nežádoucí. Potřebujeme tedy vědět, které aplikace jsou nainstalovány a ty, které nainstalovány nejsou je nutné ze spouštěče vyřadit, aby nebyly uživatelům nabízeny, pokud nejsou připraveny ke spuštění.

Detekce připravenosti aplikace se však ukázala jako potenciálně problémová. Podle dostupných zdrojů v současné chvíli Steam neexponuje žádné rozhraní pro detekci instalovaných aplikacích na konkrétním systému. Takovou detekci je tak nutné provádět ručně. Ze zkušeností ostatních vývojářů, kteří se o detekci nainstalovaných her pokusili plyne, že ruční sken složek není tak jednoduchý. Většina her splňuje tu podmínku, že se v jejich složkách nachází soubor `steam_appid.txt`, který jednoznačně složku se hrou identifikuje, ovšem to není pravidlem a ve vyjímečných případech může dojít k tomu, že se tam soubor nebude nacházet a tím pádem ruční detekce označí takovou hru jako nenainstalovanou i přesto, že nainstalovaná je. To může způsobovat problémy se spouštěčem.

Jiné řešení však podle dostupných zdrojů neexistuje. Nabízí se tak motivace přidat do konfigurace aplikace možnost zobrazení všech titulů ve spouštěči a obsluha herny pak bude zodpovědná za udržení všech her nainstalovaých a připravených ke spuštění. Což dává v herně smysl -- herna bude chtít svým návštěvníkům nabídnout všechny hry, které zakoupila. Neměl by z toho tak plynout žádný zásadní problém.

### Spouštění aplikací

Požadavky *F-C03* a *F-C04* jsou nezbytnou součástí spouštěče aplikací. Hry je nutné na uživatelův pokyn spouštět a po jeho ukončení práce se spuštěnou aplikací je nutné uživateli znova zobrazit předešlý výběr aplikací.

Spouštění aplikace se díky systémového protokolu `steam://` stává velmi jednoduchým úkonem. Úryvek z dokumentace odhaluje příkaz systémového protokolu `steam` a činnosti `run`, kterou lze pro účel spouštěče použít:

> `steam://run/<id>`  
> Runs an application. It will be installed if necessary.

Z popsaného chování plyne, že se tímto příkazem spustí hra, a pokud je to nutné, tak se spustí instalační proces. Problémová situace nastává ve chvíli, kdy chceme spustit opět náš spouštěč ve chvíli, kdy uživatel ukončí jím spuštěnou VR aplikaci. OpenVR, které má na starosti komunikaci se systémem virtuální reality, je koncipovaná takový způsobem, aby vykreslovala pouze jednu hlavní scénu.

Vhodným řešením tohoto problému se jeví použití OpenVR knihovny, která dovoluje pracovat s událostmi, kterým můžeme naslouchat a reagovat na ně. Z dokumentace je patrné, že k tomuto účelu slouží událost s názvem `VREvent_SceneApplicationChanged`. Ovšem tím není vyřešen problém výchozího chování systému *SteamVR*, potažmo knihovny *OpenVR*. Po spuštění jiné VR aplikace je ta původní automaticky ukončena. Je totiž dovoleno, aby se na popředí vykreslovala pouze jedna VR aplikace. Jako řešení se ukázala nutnost napsat malý jednoduchý program -- agenta, který bude detekovat spuštěnou aplikaci právě pomocí zmíněného odposlouchávání události a pokud dojde k ukončení aplikace, spustí znovu spouštěč aplikace této práce.

> TODO: Here goes agent screenshot

Agent je psán taktéž v jazyce C#, poskytuje jednoduché uživatelské rozhraní, určené pro obsluhu, které je psáno pomocí knihovny WPF. Uživatelské rozhraní nabízí primární tlačítko určené ke spuštění a zastavení celé aplikace (pokud bude zastavena, přestane se tak i automaticky spouštět spouštěč) a přehlednou informaci o aktuálním stavu agenta -- zda-li se podařilo připojit k OpenVR systému apod.

## Implementace

V kapitole jsou uvedeny konkrétnější detaily implementační fáze práce. Je popsána struktura celé scény, jakým způsobem jsou ukládána data o scénáři výuky, jak je generováno uživatelské rozhraní spouštěče a jakým způsobem se vyvářel voice-over výuky.

### Struktura scény



### Formát ukládání dat scénáře

Aby se předešlo do kódu napevno zadrátovaného průběhu scénáře, bude načítán z externího souboru, který scénář bude popisovat. Díky tomu bude možné kdykoliv jednoduše provádět úpravy, nebo texty přeložit do libovolného jazyka. Aplikace díky tomu bude lokalizovatelná.

Interně je formát souboru pojmenován **STXT** a bude mu příslušet běžně známá koncovka `.txt`, jelikož jde o čitelný textový soubor, který může být upravován v běžných editorech.

V aplikaci se nachází třída `StxtReader`, jejíž jediný úkol bude právě čtení tohoto formátu. S touto třídou souvisí i `ScenarioCue`, což je třída primárně koncipovaná jako datová struktura, zahrnující všechny údaje o jednom úseku scénáře. `StxtReader` pak principiálně vrací pole objektů třídy `ScenarioCue`. Toto pole je chronologicky seřazeno a celý scénář bude přehráván postupně podle řazení prvků v poli.

Vlastnosti třídy `ScenarioCue` jsou následující:
 - časové odsazení od předchozího úseku (offset)
 - délka časového úseku (duration)
 - identifikátor souvisejícího zvukového úseku (audio cue id)
 - text úseku (text)
 - činnost úseku (action)
 - skupina úseku (groupname)

Časové vlastnosti jsou určeny pro pozicování a časování úseků. Identifikátor zvukového úseku určuje, která zvuková část má být ve chvíli průchodu úsekem přehrávána. Text úseku je pak přepisem toho, co lze ve zvukovém úseku slyšet. Skupina úseku je čistě organizační záležitostí pro přehlednost *STXT* souboru.

#### Syntaxe STXT souboru

U syntaxe formátu byl kladen důraz na jednoduchost implementace čtení formátu. Obecně lze syntaxi definovat následovně:

```
#<groupname>
<offset>;<duration>;<audio cue id>:(<text>|%<action>)
[<offset>;<duration>;<audio cue id>:(<text>|%<action>)] ...

[#<groupname>
<offset>;<duration>;<audio cue id>:(<text>|%<action>)
[<offset>;<duration>;<audio cue id>:(<text>|%<action>)]] ...

...
```

Kde bloky označené `<` a `>` jsou bloky hodnot, bloky označené `[` a `]` jsou nepovinné bloky a bloky ve tvaru `( A | B )` představují možnost alternativy (A nebo B).

> TODO: Popsat syntax slovně

Významy bloků jsou uvedeny v tabulce:

Název bloku | Funkce bloku
--- | ---
`<groupname>` | Název skupiny
`<offset>` | Časové odsazení od předchozího úseku v sekundách
`<duration>` | Doba trvání daného časového úseku v sekundách
`<audio cue id>` | Identifikátor zvukového úseku
`<text>` | Text úseku (přepis zvukového úseku)
`<action>` | Činnost, která se má v úseku provést

Pro lepší představu je přiložen krátký úryvek *STXT* souboru z aplikace, na kterém lze snadněji vidět jeho praktické použití.

```
#intro
0;0;0:%showlogo
0;2.5;0:Vítejte v herně Virtualnirealita.cz!
0;3.2;0:Tato krátká výuka vás provede vstupem do virtuální reality.
0;0;0:%hidelogo

#skippable
0;0;1:%showskiptxt
0.5;6.9;1:Pokud s virtuální realitou již máte zkušenosti a výuku\nchcete..
0;0;1:%hideskiptxt

#playarea1
2;2;2:Rozhlédněte se kolem sebe a na podlahu.
0;7.5;2:Ohraničení, které můžete vidět na zemi je místo, ve kterém se ...

...```

Činnosti jsou již však narozdíl od textů a časování pevně určené, protože jsou daleko komplexnější a mnohem méně parametrizovatelné. Pro referenci je tak uvedena kompletní tabulka všech použitelných činností.

Název činnosti | Popis činnosti
--- | ---
`%showlogo` | Zobrazí před hráčem logo herny.
`%hidelogo` | Skryje logo herny.
`%showskiptxt` | Zobrazí informaci o možnosti přeskočit výuku.
`%hideskiptxt` | Skryje informaci o možnosti přeskočit výuku.
`%waitforuserraise` | Pozastaví se a čeká, dokud uživatel nezvedne ruce před sebe.
`%highlighttrigger` | Zvýrazní na ovladači tlačítko spouště.
`%givelaser` | Přidá uživateli možnost používat laserové ukazovátko.
`%waitforusertargethit` | Pozastaví se a čeká, dokud uživatel netrefí laserovým paprskem terč.
`%highlightside` | Zvýrazní boční tlačítko na ovladači.
`%waitforside` | Pozastaví se a čeká, dokud uživatel nestiskne boční tlačítko.
`%highlighttouchpad` | Zvýrazní na ovladači dotykovou plochu.
`%waitforusercolor` | Pozastaví se a čeká, dokud uživatel nezvolí na ovladači barvu.
`%highlightmenu` | Zvýrazní menu tlačítko na ovladači.
`%highlightsystem` | Zvýrazní systémové tlačítko na ovladači.
`%gotolibrary` | Zobrazí spouštěč.
`%skip` | Přeskočí výuku.

### Generování uživatelského rozhraní

### Voice-over

> TODO: target 19kC
