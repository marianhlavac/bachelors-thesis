# Analýza

Jak je zvykem u organizovaného vývoje softwaru -- implementací a prototypování předchází analýza, pro stanovení požadavků uživatelů softwaru a upřesnění funkcionalit aplikace.

Následující kapitola se takovou analýzou bude zabývat. Analyzuji existující řešení, co požadují hráči navštěvující hernu, co požadují zaměstnanci pracující v herně a jaké požadavky jsou realizovatelné.

## Analýza a porovnání existujících řešení výuky

Výukové aplikace pro seznámení s virtuální realitou již existují. Nicméně většina z nich trpí špatnou přístupností. Systémy jsou navrhovány tak, aby po absolvování takové výuky již nebyly výukové aplikace jednoduše dostupné. V našem případě jsou tak obtížně spustitelné pro návštěvníky herny.

Takové aplikace jsou spíše určené pro toho, kdo jako první systém konfiguruje a je jímž prvním uživatelem. Nově příchozímu k nakonfigurovanému systému není tutoriál nabídnut a jsou přímo uvedeni do prostředí, ve kterém se již očekává, že uživatel systém důvěrně zná.

Součásti analýzy je i porovnání jednotlivých existujících řešení, pro které jsem si stanovil následující metriky k porovnání:

  - jednoduchost přístupu k výukové aplikaci
  - rychlost a svižnost výuky
  - zábavnost
  - výstižnost
  - srozumitelnost

### SteamVR Tutorial

Pro totožnou platformu, pro kterou je aplikace této závěrečné práce určena -- **HTC Vive**, existuje oficiální výuková aplikace vytvořená přímo autory samotné platformy -- společnosti Valve.

#### Průběh výuky

Aplikace se nejprve uvede vizuálně poutavým úvodem, který spočívá v sestavení výukové scény animací obklopující hráče. Hráči je tak názorně ukázana možnost rozhlížet se kolem sebe a prozkoumávat prostředí.

Následně je uživateli představena postava (*Virtual Reality Assistance and Education Core*) ze hry Portal 2, která s hráčem komunikuje a provádí ho výukou -- stává se tak *průvodcem*. Monolog je dabovaný a v místech, kde se nachází průvodce lze číst titulky, které jsou lokalizovány do nepřeberného množství jazyků (je k dispozici i Čeština).

Příjemným bonusem je pro hráče hry Portal 2 familiarita postavy, která může zvýšit hráčovu pozornost a pro hráče, kteří si hru Portal 2 v minulosti oblíbili tak tutoriál navozuje na obličejích úsměv.

![](http://1u88jj3r4db2x4txp44yqfj1.wpengine.netdna-cdn.com/wp-content/uploads/2016/03/Walkthrough-of-SteamVRs-new-tutorial_17-930x523.jpg)  
*fig.1 Výuková aplikace SteamVR Tutorial*

Jako první je uživateli představena plocha, tzv. *Play area*, ve které se VR zážitky budou odehrávat. Neprodleně jsou pak představeny tzv. *Chaperone bounds*, které upozorňují hráče na skutečnost, že opouštějí hranice *play area* a jsou vystaveni limitacím fyzické místnosti, ve které se nacházejí. Protože je tato funkcionalita důležitá v zájmu uživatele, pro jeho bezpečnost, je na ni ve výuce kladen důraz a je proto požádán, aby se ke kraji místnosti pomalu přiblížil a následně to stejné zopakoval na druhé straně místnosti.

Dále je uživatel požádán, aby se podíval na ovladače, které drží v ruce a provedl s nimi libovolné pohyby pro vyzkoušení manipulace s nimi. Poté, co se seznámí s pohyby s ovladačem jsou mu postupně představena všechna tlačítka, která se nacházejí na ovladači a je požádán, aby každé stiskl a vyzkoušel si tak, kde se nacházejí a jakou mají zpětnou odezvu.

Výuková aplikace je pojatá spíše komicky a každé tlačítko velmi chytře vyvolává různé destrukční, hlasité a nečekané události, které se průvodci nelíbí. Průvodce hráče žádá aby přestal, hráč však může mít nutkání tyto tlačítka mačkat opakovaně, aby průvodce rozčílil a dělal nepořádek. Tím se s tlačítky seznámí o to více.

Hráč není informován o tom, která tlačítka mají jakou funkci, logicky z toho důvodu, že každá VR aplikace má své vlastní pojetí smyslu těchto tlačítek. Ovšem k tlačítkům *Menu* a *System* je uživateli řečeno, k čemu se nejčastěji používají.

Ke stisknutí tlačítka *System* je vzápětí požádáno, což vede k otevření *SteamVR Dashboard*. Lze si povšimnout, že se hra nepozastaví při otevření *Dashboardu* a probíhá tak stále instruktáž, jak se lze ve *SteamVR Dashboard* pohybovat a k čemu je určena.

Tím je výuka u konce, uživatel je instruován k otevření *Dashboardu* a výběrem VR aplikace. Stále ovšem může v aplikaci zůstat a dále zkoušet práci s ovladači, nebo zhlédnout závěrečnou animaci, kdy průvodce komicky odvezou pryč ze scény.

#### Zhodnocení

SteamVR Tutorial je relativně dobrým příkladem výukové aplikace. Je kvalitně navržena, s objektivně sic strohým, ale kvalitním vizuálním a zvukovým zpracováním.

Pro účely herny je však shledán nevhodným, jelikož je návštěvníkům herny takový tutoriál prakticky nepřístupný. Obsluha je nucena jej spustit manuálně a také se návštěvníka herny zeptat, jestli už tutoriál absolvoval a zdali jej chce skutečně absolvovat. Návštěvník nemá možnost takovou výuku zopakovat, nebo alespoň získat nějaký závěrečný přehled, pro zopakování toho, co se naučil.

![](http://i.imgur.com/dHgOC1S.png)  
*fig.2 Přístup k aplikaci je skryt ve SteamVR nabídce, která je přístupna jen z monitoru počítače*

Další nevýhodou je délka tutoriálu, která se běžně pohybuje kolem 7-12 minut. To představuje v prostředí, kde se běžně systém zapůjčuje na jednu hodinu, velkou část takového času.

### Oculus Touch Tutorial & Oculus First Contact

Pro konkurenční systém **Oculus Rift** a jeho platformu je určena aplikace *Oculus First Contact*, která je spojena s předcházející krátkou výukou ovladačů *Oculus Touch*, které jsou k systému *Oculus Rift* prodávány odděleně.

Bez těchto ovladačů tuto výuku nelze spustit.

#### Průběh výuky

Uživatel je zasazen do čistého prostředí, bez předmětů, zobrazující pouze ovladače v ruce. Před ním se pak zobrazuje přepis (titulky) hlasu průvodkyně, která není vizuálně zpracována, lze slyšet pouze hlas.

Jako první je požádán, aby se podíval na podlahu a zpozoroval obrys prostoru, ve kterém se může uživatel pohybovat -- *the play area*. Následně je požádán, aby se podíval na své ruce a ovladače, které v nich právě drží a osahal si všechna tlačítka, která se mu podaří nalézt. Následně jsou mu všechna tlačítka jedno po druhém představeny, jsou zvýrazněny a je požádán, aby tato tlačítka stiskl.

![](http://i.imgur.com/pLGppB7.png)  
*fig.3 Výuková aplikace Oculus Touch Tutorial*

Pokud uživatel provádí stisky tlačítek svižně, lze tuto část projít relativně velmi rychle. Výuka nezdržuje dlouhým monologem, nebo pauzami, jde o krátké věty a díky tomu může působit velmi svižně.

Vzápětí jsou uživateli ovladače vizuálně z rukou odstraněny a je požádán, aby znovu vyzkoušel mačkat tlačítka a zvedat z nich prsty tak, aby pochopil přibližnou reprezentaci přirozeného pohybu rukou a prstů. Je požádán, aby mačkal specifické kombinace tlačítek tak, aby vytvářel gesta rukou jako je například gesto uzavření v pěst nebo míření na objekty ukazováčkem.

Uživateli není vysvětlen účel tlačítek, z dříve zmíněných důvodů. Pokud však předpokládáme, že všechny VR aplikace a hry budou implementovat systém gest ruky, které byly vysvětleny v třetí části výuky, uživatel je schopen odvodit účel tlačítek sám, což lze považovat za nespornou výhodu.

Překvapující je absence objasnění smyslu tlačítek *Oculus* a *Menu*, které téměř ve všech VR aplikacích fungují totožně.

Tím výuka končí a je uživateli spuštěna aplikace *Oculus First Contact*, která je určena k prohloubení seznámení s virtuální realitou a slouží jako úvodní zábavný zážitek, který je srovnatelně kvalitní a zábavný jako jiné herní tituly pro virtuální realitu. Tím tak lze považovat výuku jako dokončenou a aplikací *Oculus First Contact* začíná "zábava".

![](http://i.imgur.com/Ly6t8mi.png)  
*fig.4 Aplikace Oculus First Contact*

#### Zhodnocení

Oculus má výukovou aplikaci zpracovanou do podstatně rychlejšího tempa, než SteamVR. Přispívá tomu i jednoznačné rozdělení práce od zábavy. Nejprve přichází rychlý a strohý úvod do ovládání, který trvá přibližně 4-5 minut, až následně po tomto úvodu následuje zábavný prvek ve formě plnohodnotného VR zážitku. Vidíme tak zásadní rozdíl vůči SteamVR, který tyto dva prvky míchá do jednoho průběhu.

## Analýza existujících řešení spouštěčů

Po skončení výuky můžeme předpokládat, že návštěvník herny je se systémem do určité míry seznámen a dále je nutné mu nějakým způsobem nabídnout výběr VR zážitků. O VR aplikacích může vědět a jít do herny za účelem takovou aplikaci vyzkoušet, nebo může hernu navštívit z obecnějšího důvodu -- protože chce vyzkoušet virtuální realitu.

Dvě v předchozí kapitole zmíněné platformy (SteamVR a Oculus) mají vlastní software pro spouštění VR aplikací, které blíže analyzuji.

### SteamVR Dashboard

*SteamVR Dashboard* je pouze malou modifikací již existujícího rozhraní *Steam Big Picture*, který je určen k použití *Steam* platformy z pohodlí gauče s použitím herního ovladače.

Díky tomu má *SteamVR Dashboard* nespornou výhodu v tom, že většina hráčů počítačových her se s platformou *Steam* již setkala a setkala se dokonce i s rozhraním *Big Picture*, které část hráčů dokonce používá jako primární rozhraní pro práci s platformou *Steam*.

Na druhou stranu lze však považovat jako nevýhodu ten fakt, že fakticky *Steam Big Picture* nebyl původně navržen pro použití s VR. Hráč tak pracuje s malým oknem na virtualizovaném monitoru.

![](https://cdn0.vox-cdn.com/thumbor/Lei26JXsB0zMdW_jkshawf3t29o=/0x205:839x677/1600x900/cdn0.vox-cdn.com/uploads/chorus_image/image/49240909/ViveTheaterModeTop.0.0.jpg)
*fig.5 SteamVR Dashboard*

Z tohoto rozhraní lze procházet knihovnu her, prohlížet elektronický obchod s hrami a hry také nakupovat, prohlížet komunitní profily, stránky her, sledovat průběh aktuální ho stahování, používat webový prohlížeč a přistupovat k omezenému nastavení.

Pokud budeme hodnotit *SteamVR Dashboard* z pohledu návštěvníka herny, je takové rozhraní naprosto nevyhovující. Pro návštěvníka, který nemá s platformou *Steam* zkušenosti je rozhraní spíše matoucí a může vyžadovat nějakou dobu, než se s ním seznámí. V rozhraní se také nacházejí sociální a komunitní funkce, které pro použití v herně nemají žádný význam a jsou tak dalším matoucím prvkem pro návštěvníka. Zákazník herny má nadále plný přístup k obchodu a mohl by tak na účet herny libovolně nakupovat hry, není mu v tom nikterak zabráněno.

Seznam a výběr her je pro použití v herně taktéž spíše nevhodný. Seznam se skládá z mřížky 3x4 grafických bannerů, které o dané hře vypovídají jen málo. Je totiž spíše na vývojářích, či v takovém banneru zobrazí pouze logo hry, obrázek ze hry či obojí. Lze tak velmi obtížně odhadnout o jaký žánr hry jde, zda je zábavná, zda je subjektivně návštěvníkovi herny vizuálně přitažlivá, jaké ovládání podporuje, či zda způsobuje závratě a kinetózu.

### Oculus Home

*Oculus Home* je plnohodnotným rozhraním pro virtuální realitu od společnosti Oculus pro svou stejnojmennou platformu.

Skrze toto rozhraní lze procházet knihovnu her a nakupovat hry v obchodě. Uživatel může vidět i minimální komunitní funkce, jako je seznam hráčů a notifikace (a to i systémové).

Rozhraní je vizuálně velmi přitažlivé, zobrazuje se jako výchozí prostor při nasazení headsetu na hlavu bez spuštěné hry, což oproti platformě SteamVR, kde se zobrazuje prázdná šedá místnost s mřížkou, může působit příjemně.

![](https://i.ytimg.com/vi/kWJvFR04xyM/maxresdefault.jpg)
*fig.6 Oculus Home*

Jelikož je rozhraní navržené specificky pro použití s hrami pro virtuální realitu, k hrám lze nalézt informaci o tom, jaké ovládání podporuje a lze je řadit podle míry "komfortu". Nekomfortní hry jsou pak označeny jako takové, které mohou způsobovat kinetózu a lidé, kterým se z intenzivnějších her dělá nevolno, se takovým hrám mohou snadno vyhnout.

Pro hernu je však *Oculus Home* také nevyhovující. Přístup k obchodu a komunitní funkce jsou opět irelevantní a nejsou určeny návštěvníkům herny.

## Pozorování v herně

Ke konci března roku 2017 jsem měl příležitost stát se na jeden den obsluhou v herně *Virtualnirealita.cz* v pražských Dejvicích. Tuto příležitost jsem využil v prospěch analýzy jako předmět pozorování a bližšího pochopení požadavků jak hráčů tak obsluhy herny.

Jako obsluha jsem měl povinnost seznámit zákazníky s pronajatým systémem a pokud s virtuální realitou neměli dosud zkušenost, nebo se nedoslechli o žádné konkrétní hře, či aplikaci, kterou by si přišli vyzkoušet, byl jsem dále pověřen doporučením nějaké hry na základě jejich preferencí.

Protože jsem se ptal na přirozené otázky, abych byl schopen lépe s lidmi pracovat a také jim doporučit správnou hru, vznikla mi tak miniaturní analýza z malého vzorku lidí, kteří ten den do herny dorazili.

Dotazování zákazníků se tak běžně skládalo z otázek:
  - "Už jste u nás někdy byli?"
  - "Máte zkušenosti s VR?"
  - "Hrajete počítačové hry?"
  - "Jaký žánr her rádi hrajete?"

Za daný den navštívilo hernu **15 zákazníků**, z toho **10 mužů**. Většina -- **12 zákazníků** hraje počítačové hry, ale pouze **2 z nich** v minulosti hernu navštívili, nebo měli s VR zkušenost. Většina z nich byla mládež (v rozmezí 15-30 let), výjimku tvořili **2 děti** (< 15) a **2 dospělí** (> 30). U jednoho z návštěvníků se projevila *kinetóza*.

Pouze **4 z nich** odpověděli, že jim nepřišly ovladače systému HTC Vive obtížné na seznámení, stejně tak tito lidé odpověděli, že by se obešli bez pomoci obsluhy. Dva z těchto čtyř byli ti, kteří již s VR měli zkušenost.

![Imgur](http://i.imgur.com/lEo1Fkh.jpg)  
*fig.3 Na jeden den jsem změnil svou pracovní roli*

Občasným jevem bylo několikanásobné vystřídání zákazníků na jednom systému za dobu zapůjčení. To je důležitá informace, protože výuková aplikace musí s takovým jevem počítat.

Rychlost seznámení se systémem byla převážně ovlivněna zákazníkovou zkušenosti s počítačovými hrami.

## Aplikování bodů použitelnosti podle Nielsena

Před stanovením požadavků jsem se pokusil aplikovat body použitelnosti podle *Jakoba Nielsena*, které jsem v minulosti úspěšně použil pro návrh uživatelského rozhraní pro webové aplikace.

*Jakob Nielsen* je významným odborníkem v oblasti tvorby uživatelského rozhraní, specializující se především na webová rozhraní. Jeho klíčovým dílem je kniha *Designing Web Usability* z roku 1999, ve které popisuje veškeré své znalosti a zkušenosti z oboru.

Na základě svých zkušeností sestavil **deset bodů použitelnosti**, které se používají pro heuristickou analýzu uživatelských rozhraní. Jedná se o tyto body:

1. Viditelnost stavu systému
2. Propojení systému a reálného světa
3. Uživatelská kontrola a svoboda
4. Standardizace a konzistence
5. Prevence chyb
6. Rozpoznání namísto vzpomínání
7. Flexibilní a efektivní použití
8. Estetický a minimalistický
9. Pomoc uživatelů pochopit, poznat a vzpamatovat se z chyb
10. Nápověda a návody

Nielsenovy body použitelnosti pravděpodobně nebudou plně vhodné pro jejich použití na aplikaci virtuální reality, jelikož jsou primárně určeny pro analýzu webových rozhraní. V této kapitole jsem vybral ty z nich, které nejsou vhodné a upravil je tak, aby byly aplikovatelné.

Všechny tyto body jsem pak použil pro sestavení dodatečných požadavků na aplikaci, které lze nalézt v následující kapitole.

### Bod č. 2 -- Propojení systému a reálného světa

Druhý z Nielsenových bodů použitelnosti ukazuje na to, jak by mělo uživatelské rozhraní reflektovat známé jevy a souvislosti reálného světa. Typickým příkladem je ikona složky vyzobrazená v rozhraní. Podle tohoto bodu je žádoucí, aby se taková ikona opravdu podobala složce a při přetažení objektů na takovou ikonu se provedla očekávatelná akce -- přesunutí objektu do této složky.

Ve virtuální realitě je nutné tyto vztahy ještě více utvrdit. Z přednášky na americké konferenci GCD 2016 hovoří *Kimberly Voll* ze společnosti *Riot Games* o konceptu takzvaného *fidelity contract* (volně přeloženo -- kontraktu věrnosti) a popisuje jej jako mechanismus splnění očekávání chování virtuálního světa shodným s chováním reálného světa.

> TODO: Dopsat k tomuto tématu více.

### Bod č. 10 -- Nápověda a návody

Vzhledem k tomu, že samotná aplikace slouží k výuce a je ji tak možné považovat jako nápovědu, je tento bod pro daný typ aplikace neaplikovatelný.

> TODO: Tohle zvážit a případně přepsat.

## Funkční požadavky návštěvníků herny

Z pozorování v herně a analýzy existujících řešení plynou následující požadavky vztahující se k návštěvníkům herny.

**F-A01 Uživatel se chce seznámit se základními pravidly systému virtuální reality**  
Uživatel chce vědět, jak se používá headset systému virtuální reality, jak se může v *play area* pohybovat, kam se nesmí vydat a jak je na to upozorněn. Funkční požadavek je klíčový z hlediska bezpečí návštěvníka herny a ochrany majetku herny.

**F-A02 Uživatel se chce seznámit s ovladači a jejich tlačítky**  
Uživatel chce vědět, jak vypadají ovladače, jakými tlačítky disponují a k čemu slouží. V závislosti na této znalosti je pak uživateli usnadněno pochopení ovládání v konkrétních VR aplikacích.

**F-A03 Uživatel se chce seznámit s funkcemi na tlačítcích pro konkrétní hru**  
Uživatel chce vědět, jak se ovládá konkrétní VR aplikace.

**F-A04 Uživatel si chce vybrat VR aplikaci podle žánru**  
Uživatel si chce zvolit VR zážitek takového žánru, který mu vyhovuje. Do herny docházejí různé věkové a zájmové skupiny. Často záleží i na pohlaví. Ženy většinou rády hrají méně intenzivnější zážitky, vyhýbají se hororovým hrám a střílečkám a více ocení vizuálně atraktivní aplikace.

**F-A05 Uživatel si chce vybrat VR aplikaci podle intenzity**  
Uživatel, u kterého se projevuje kinetóza, si chce vybrat takovou aplikaci, aby nebyla příliš intenzivní a jeho zážitek z VR byl pozitivní. Ač může být toto kritérium velmi subjektivní, lze aplikace rozdělit alespoň do dvou kategorií, jako intenzivní a klidné, kde pod klidné aplikace spadají všechny aplikace, které mají implementovány mechanismy zabraňující kinetóze, nebo nezahrnují pohyb kamery kinetózu způsobující.

**F-A06 Uživatel si chce vybrat VR aplikaci podle vizuálního zpracování**  
Uživatel si chce vybrat takovou aplikaci, která bude pro něj vizuálně atraktivní. Spousta uživatelů upřednostňuje určité aplikace z jednoduchého důvodu -- líbí se jim.

**F-A07 Uživatel chce výuku kdykoliv přeskočit, nebo informace zopakovat znova**
Pokud uživatel shledá výuku subjektivně příliš jednoduchou, či zdlouhavou, měl by mít možnost její průběh minimálně urychlit. Naopak, pokud je pro něj výuka příliš rychlá, měl by mít na konci výuky možnost si informace zopakovat, či zopakovat celou výuku znova.

**F-A08 Uživatel chce, aby byla výuka časově efektivní**  
Protože má návštěvník herny omezený čas, po který je mu zapůjčen systém virtuální reality, je pro něj důležité, aby ho výuka o tento čas připravila v co nejmenší míře.

## Funkční požadavky obsluhy herny

Požadavky obsluhy se velkou částí kryje s požadavky zákazníka, jen z jiného úhlu pohledu.

**F-B01 Obsluha chce zákazníka seznámit s pravidly používání systému virtuální reality**  
Aby uživatel používal systém správně, obsluha se potřebuje ujistit, že zákazník ví, jak se systém používá, aby nedošlo k jeho poškození nesprávným použitím a zákazník nebyl vystaven nebezpečí.

**F-B02 Obsluha chce zákazníka seznámi s ovladači systému**  
Aby uživatel byl se zážitkem spokojený, obsluha potřebuje, aby zákazník byl schopen používat ovladače systému. Taková znalost pak zákazníkovi usnadní pochopení ovládání konkrétních aplikací a je tak logicky více spokojený.

**F-B03 Obsluha chce zákazníkovi vybrat VR aplikaci pro něj vhodnou**  
Zákazníci velmi často přicházejí do herny pouze za účele vyzkoušení virtuální reality. Zřídkakdy se stává, že by zákazník věděl o jakou konkrétní VR aplikaci má zájem a chce si ji vyzkoušet. Obsluha je tak povinna zjistit, co bude zákazníkovi vyhovovat a vybrat mu tak nějakou aplikaci či herní titul pro něj vhodný.

**F-B04 Obsluha chce zákazníka upozornit na blížící se konec vypůjčení systému**  
Přibližně pět minut před koncem doby zápůjčky obsluha žádá zákazníka, aby si na moment sundal sluchátka a mohla jej upozornit na blížící se konec.

## Funkční požadavky obecné

Požadavky nekategorizovatelné jako požadavek návštěvníka či obsluhy herny. Valná většina z nich se týká fukncionality spouštěče.

**F-C01 Aplikace chce zobrazit uživateli seznam VR aplikací a umožnit mu výběr**  
Základní funkce spouštěče je zobrazení seznamu VR aplikací, ze kterých může uživatel provést výběr. Takový seznam by měl poskytovat možnost vyhledávat přímo podle názvu, dále podle žánru, intenzity i podle vizuálu.

**F-C02 Aplikace chce stáhnout data o VR aplikaci**  
Aby mohla aplikace splnit požadavek *F-C01*, je nutné taková data o hrách získat. Většina požadavkem zmíněných dat je dostupná přes veřejná API. Více se získáním dat bude zabývat návrh.

**F-C03 Aplikace spustí uživatelem vybranou VR aplikaci**  
Poté, co uživatel provede výběr aplikace, je tato aplikace spuštěna a funkce spouštěče jsou pozastaveny či ukončeny.

**F-C04 Po ukončení VR aplikace je uživateli znovu nabídnut přehled her**  
Po ukončení práce s VR aplikací, kterou uživatel spustil, je mu opět nabídnut výběr spouštěče (pokračováním v činnosti či opětovým spuštěním).

## Nefunkční požadavky

**N-01 Aplikace je navržena pro systém HTC Vive**  
Ze zadání plyne soustředění aplikace na jednu platformu a její konkrétní ovladače.

**N-02 Aplikace je vizuálně atraktivní**  
Aby byl uživatelův dojem z aplikace pozitivní a příjemný, měla by aplikace splňovat alespoň nějakou základní úroveň kvality vizuálního zpracování.

**N-03 Výukou je uživatel prováděn mluvenou řečí**  
Jelikož je kvůli disperzi krajů obrazu, omezenému rozlišení a obtížně proveditelnému umístění psaného textu ve virtuální realitě, je nutné kromě titulků ve formě takového textu, uživatele navigovat i prostřednictvím mluveného slova. Požadavek na primární jazyk mluveného slvoa je Čeština.

**N-04 Výuka je časově efektivní**  
Protože je návštěvník herny časově omezen dobou zapůjčení systému, je nutné, aby taková výuka trvala co nejkratší možnou dobu.

**N-05 Aplikace bude jednoduchá na použití**
