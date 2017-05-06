# Realizace

Pro realizaci aplikace bude použit herní engine *Unity*. *Unity* je multi-platformní herní engine napsaný v C a C++ určený k vývoji her pro PC, konzole a mobilní zařízení. Je to v současnosti jeden z nejvhodnějších a nejpopulárnějších nástrojů na vývoj her pro virtuální realitu.

Ač jde o nástroj pro tvorbu her, je vhodným nástrojem i pro tvorbu aplikace určené pro virtuální realitu, jelikož aplikace pro virtuální realitu jsou vykreslovány stereoskopicky a trojrozměrně. Předmětem tvorby této aplikace by neměla být tvorba takového vykreslovacího jádra, ale spíše samotné aplikace. Proto je využito herního enginu, abych čas strávený tvorbou vykreslovacího jádra byl využit spíše pro tvorbu samotné aplikace.

## Jazyk implementace

Herní engine *Unity* podporuje několik programovacích jazyků, ve kterých můžou být vytvořeny skripty pro ovládání logiky aplikace. Jsou to jazyky *C#*, *JavaScript* a *Boo*. Tato kapitola se bude zabývat volbou jednoho z těchto jazyků, ovšem výhradně v souvislosti s použitím v enginu *Unity*.

Výběr jazyku budou ovlivňovat i mé předchozí zkušenosti. V *Unity* jsem doposud napsal několik skriptů pouze v jazyce *C#*. Na druhou stranu mám s jazykem *JavaScript* mnohem hlubší zkušenosti a znalosti, ovšem mimo herní vývoj -- především ve webovém prostředí.

Po rešerši na nepřeberném množství internetových diskuzních fór jsem z různorodých názorů vývojářů vyderivoval následující doporučení, týkající se výběru jazyka pro *Unity*:

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

V aplikaci lze rozlišit klíčové funkce, které jsou poněkud specifické a charakteristické pro danou aplikaci. Ač je snadné navrhnout způsob řešení implementace takových funkcí, je nutné tyto funkce podrobit principem **Proof of Concept** — rychlou implementací konkrétních funkcí nezávisle na zasazení do koncové aplikace.

Na základě takové implementace je pak možné potvrdit, zda-li je návrh implementace klíčových funkcí, na kterých aplikace stojí, realizovatelný.

Jednou z takových funkcí je zobrazení her, které vlastní herna na svém účtu platformy *Steam*. Aby bylo možné zobrazení provést, je nutné o hrách stáhnout informace, podle požadavku *F-C02*. Taková data jsou přístupná pomocí některého z API rozhraní služby *Steam*. Předmětem POC bude takový zdroj dat nalézt a implementovat práci s takovým zdrojem do enginu *Unity*.

Další funkcí, kterou je nutné podrobit POC je samotný spouštěč her a to konkrétně funkci spuštění a opouštění VR aplikací, podle požadavků *F-C03* a *F-C04*. Je nutné vyzkoušet, jak z aplikace vytvořené v *Unity* spouštět aplikace nainstalované skrz platformu *Steam* a jak detekovat jejich ukončení a vyvolání spouštěče opět do popředí.

### Stahování informací o aplikacích

Aby došlo ke splnění požadavku *F-C02*, je nutné získat následující informace:

 - Jaké aplikace jsou zakoupené na účtě herny platformy Steam
 - Které z nich jsou nainstalovány na konkrétním počítači
 - Název aplikace, její krátký oficiální popis od výrobce, obrázek aplikace 
 
Mezi informace nepatří navržené krátké video ze hry, či popis úrovně intenzity, jelikož platforma Steam není zdrojem takových dat. Předmětem zíkáním těchto dat se bude zabývat jedna z následujících kapitol.

Steam nabízí více API rozhraní pro komunikaci, specifická pro různá použití, jako je např. přístup k různorodým API v rámci partnerského progrmu *Steamworks*, které by dávalo smysl použít, jelikož je běžně používáno pro aplikace a hry distribuované skrz platformu Steam, které jsou s platformou integrovány a pracují s ní, což se velmi podobá aplikací této závěrečné práce (minimálně splňuje podmínku práce s platformou Steam). *Steamworks SDK* je ovšem dostupné pouze pro partnery společnosti, což nejeví problém, partnerství je možné získat, jde však o mírně zdlouhavý proces a pro účely stažení informací by šlo o neefektivní postup.

Ideálním API rozhraním se tak ukázalo *Steam Web API*, které ač, jak je z názvu patrné, je určeno pro použití webovými službami, je ideálním a snadno přístupným zdrojem informací, které jsou nutné pro splnění požadavku. Rozhraní disponuje několika endpointy, nabízejícími různá data, pro nás zajímavým endpointem je však *GetOwnedGames-v0001*, který vrací seznam všech her, které vlastní specifikovaný účet platformy Steam.

Situace se však komplikuje ve dvou bodech -- viditelností dat a autentizací:

Pro stažení takových dat z účtu pomocí tohoto API, je nutné, aby daný účet měl v nastavení účtu platformy Steam povolen veřejný přístup k datům, jako je např. seznam her, který přesně potřebujeme. V naší situaci by to neměl být problém za předpokladu, že herna nemá důvod chtít skrývat seznam her, který vlastní na svých účtech. V případě, že herna z libovolného důvodu nebude chtít zveřejnit svůj seznam her na platformě Steam, tento postup tak selhává a není možné herně nabídnout takovou aplikaci bez toho, aniž by se využilo jiného API rozhraní služby Steam.

Další, tentokrát už mnohem méně závažnější komplikací, je způsob autentizace pro použití *Steam Web API*. Steam nabízí dva způsoby -- vygenerováním statického klíče na jejich stránkách a jeho použitím při vytváření požadavků na API, nebo implementací OpenID přihlašování. Vzhledem k tomu, že je aplikace z podstaty zadání učená pro použití (resp. konfiguraci) jedním subjektem (či malým počtem subjektů), vygenerování klíče je velmi jednoduché a v ideálním případě je nutné takový proces provést jen jednou, je z důvodu časové efektivity a jednoduchosti implementace použita autorizace pomocí klíče.

Získáním takových dat z tohoto API rozhraní jsou však splněny pouze dva z tří výše zmíněných bodů -- jaké aplikace jsou zakoupené a jaké jsou jejich názvy, krátké popisy a obrázky aplikací. Chybí informace o tom, zda-li jsou na systému nainstalovány a připraveny ke spuštění.

Pokud na chvíli odběhneme do následující kapitoly zabývající se spouštěním aplikací, zjistíme, že lze aplikace výhodně a jednoduše spouštět pomocí systémového protokolu `steam://` a jeho akce `steam://run/<appid>`. Tato akce se chová tak, že pokud je v systému aplikace nainstalovaná, provede její spuštění. V opačném případě se zahájí proces instalace a provede uživatele procesem stažení a nainstalování takové aplikace. Z pohledu návštěvníka herny je však takové chování nežádoucí. Potřebujeme tedy vědět, které aplikace jsou nainstalovány a ty, které nainstalovány nejsou je nutné ze spouštěče vyřadit, aby nebyly uživatelům nabízeny, pokud nejsou připraveny ke spuštění.

Detekce připravenosti aplikace se však ukázala jako potenciálně problémová. Podle dostupných zdrojů v současné chvíli Steam neexponuje žádné rozhraní pro detekci instalovaných aplikacích na konkrétním systému. Takovou detekci je tak nutné provádět ručně. Ze zkušeností ostatních vývojářů, kteří se o detekci nainstalovaných her pokusili plyne, že ruční sken složek není tak jednoduchý. Většina her splňuje tu podmínku, že se v jejich složkách nachází soubor `steam_appid.txt`, který jednoznačně složku se hrou identifikuje, ovšem to není pravidlem a ve vyjímečných případech může dojít k tomu, že se tam soubor nebude nacházet a tím pádem ruční detekce označí takovou hru jako nenainstalovanou i přesto, že nainstalovaná je. To může způsobovat problémy se spouštěčem.

Jiné řešení však podle dostupných zdrojů neexistuje. Nabízí se tak motivace přidat do konfigurace aplikace možnost zobrazení všech titulů ve spouštěči a obsluha herny pak bude zodpovědná za udržení všech her nainstalovaých a připravených ke spuštění. Což dává v herně smysl -- herna bude chtít svým návštěvníkům nabídnout všechny hry, které zakoupila. Neměl by z toho tak plynout žádný zásadní problém.

### Spouštění aplikací

Požadavky *F-C03* a *F-C04* jsou nezbytnou součástí spouštěče aplikací. Hry je nutné na uživatelův pokyn spouštět a po jeho ukončení práce se spuštěnou aplikací je nutné uživateli znova zobrazit předešlý výběr aplikací.

Spouštění aplikace se díky systémového protokolu `steam://` stává velmi jednoduchým úkonem. Zde je krátký výpis z dokumentace systémového protokolu a činnosti `run`, kterou lze pro účel spouštěče použít:

> `steam://run/<id>`  
> Runs an application. It will be installed if necessary.

Z popsaného chování v dokumentaci plyne, že se tímto příkazem spustí hra, a pokud je to nutné, tak se spustí instalační proces.

## Postup implementace

...


> TODO: target 19kC
