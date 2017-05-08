# Úvod

Virtuální realita (často zkracována na VR) je bezesporu novým trendem v oblasti informačních technologií.@ Protože je tato technologie běžným lidem méně dostupná, vznikly ve větších městech nové podniky, které zprostředkovávají zážitky ve virtuální realitě za zlomek ceny celého systému bez nutnosti znalosti systémů virtuální reality, zajištění dostatečného výpočetního výkonu, výběru a nákupu her pro virtuální realitu kompatibilní s konkrétním systémem a konfigurace virtuální reality. Tyto podniky se označují jako *herny virtuální reality*.@

Návštěvníci pak kladou na takové podniky jisté požadavky, na které systémy virtuální reality nejsou v současné době plně připraveny. Uživatelské rozhraní softwaru je navrženo spíše na jednoho dlouhodobého uživatele, který měl prostor systému porozumět, což je nevhodné v prostředí, kde se uživatel s virtuální realitou setkává poprvé a v omezeném čase, po který mu byl systém zapůjčen.

## Co je virtuální realita

Pojem virtuální realita označuje technologii prezentace prostředí pomocí replikace lidských smyslů tak, aby simulovala přítomnost uživatele v takovém prostředí. Často se virtuální realitou označuje i samotné prostředí. Technologie tak vytváří iluzi reálného alternativního světa.

Konkrétní definici virtuální reality v angličtině: "a realistic and immersive simulation of a three-dimensional 360-degree environment, created using interactive software and hardware, and experienced or controlled by movement of the body" lze přeložit jako "realistická a pohlcující simulace trojrozměrného 360 stupňového prostředí tvořeného pomocí interaktivního softwaru a hardwaru ovládaného pohybem lidského těla".@

Uživatel virtuální reality se může v prostředí typicky rozhlížet, procházet se (v různě omezené míře) a interagovat s vyzobrazenými objekty. Virtuální realita nalézá uplatnění v průmyslu, lékařství, sportu, armádě a především i v zábavním průmyslu.

Počátky virtuální reality sahají až do 50. let 18. století, kdy se experimentovalo s různými stereoskopickými displeji a zprostředkováním jevů ostatních lidských smyslů. Jako nejranější známý příklad virtuální reality je přístroj zvaný *Sensorama*, který byl schopen zobrazovat trojrozměrné stereoskopické obrázky, přehrávat zvuk prostředí a vypouštět aromatické látky pro pohlcující zážitek.@

Na počátku 20. století se objevily další příklady pohlcujících zážitků virtuální reality. Za zmínku stojí projekční místnost *The Cave*@, mezi koncové uživatele nikdy nerozšířený *Sega VR Headset*@, či stejně nepříliš úspěšný *Virtual Boy* od společnosti *Nintendo*.@

![](https://upload.wikimedia.org/wikipedia/commons/c/ce/Virtual-Boy-wController.jpg)  
*fig. 1 Virtuální realita z roku 1995 -- Virtual Boy*

## Virtuální realita v současnosti

V současnosti je virtuální realita tvořena typicky pomocí počítačem generované trojrozměrné grafiky a zvuku, snímání pohybu a snímání polohy lidského těla. Uživateli je zážitek zprostředkován pomocí náhlavní soupravy, které vykreslují obraz, přenášejí zvuk a snímají polohu hlavy uživatele.

V rámci této technologie tak vznikají celé systémy virtuální reality, které disponují různými vlastnotmi, různými technologiemi simulace a různou kvalitou simulace. Některé systémy míru a kvalitu simulace doplňují snímáním celého lidského těla, či částí jejich končetin, např. ovladačů pro ruce. Snímány mohou být i polohy fyzických předmětů, či různých jiných ovladačů. Systémy se mohou lišit i technologií snímání. Některé používají infračervené světlo a kamery, jiné zase laserové snímání. Virtuální realita pro některá mobilní zařízení například využívá pouze gyroskopických senzorů.

Velkou roli v této technologii hraje, mimo kvalitní a rychlé gyroskopy, také počítačový výkon. Právě kvůli virtuální realitě začal v poslední době převažovat trend nových "VR ready" grafických karet, které jsou přizpůsobeny k výpočtu obrazu z dvou úhlů pro efekt stereoskopie.

![](https://static3.wareable.com/media/imager/14526-b104d0dee746b81605d5ab3bc0b9c2de.jpg)  
*fig. 2 Systémy virtuální reality současnosti*

> TODO: Tohle ^ definitivně přijde nahradit vlastní fotkou, chci tam vive, oculus a psvr pohromadě. Navíc tenhle nelze použít, nejsou práva asi.

### Systém HTC Vive

Systém *Vive* vyvinutý společností *HTC* je jedním z nejoblíbenějších systémů virtuální reality v současnosti. Současně s *HTC* se na vývoji podílela společnost *Valve*. Tato společnost stojí za jednou z největších platforem pro digitální distribuci počítačových her -- *Steam*. S touto službou je úzce spjatá technologie *SteamVR*. O těchto technologiích více pojednávají kapitoly níže.

Systém *HTC Vive* se skládá z náhlavní soupravy s OLED displejem o rozlišení 2160x1200 a dvou ovladačů do ruky s gyroskopickými senzory, senzory detekce pozice v prostoru, pěti tlačítky, dotykovou plochou a haptickou odezvou. Díky laserovému snímání je možné velmi přesně snímat relativně velký prostor v místnosti, ve které se může uživatel volně pohybovat. V České republice je k současnému datu systém dostupný za přibližně 24 tisíc korun. Koncovým zákazníkům se stal dostupným v dubnu roku 2016. Pro tento systém bude navržena aplikace této závěrečné práce.

![](https://upload.wikimedia.org/wikipedia/commons/7/7a/Vive_pre.jpeg)  
*fig.3 Systém virtuální reality HTC Vive a jeho ovladače*

## Platforma Steam a SteamVR

Protože se na vývoji systému *HTC Vive* podílela společnost *Valve*, je více než logické, že *HTC Vive* je úzce spjat s touto platformou.

Hry a aplikace určené pro tento systém jsou primárně distribuovány skrze platformu *Steam*. VR aplikace určené pro systém *HTC Vive* jsou pak podpořeny specializovanou platformou *SteamVR*. Ta je určena pro práci s hardwarem virtuální reality a jeho komunikaci s počítačem. Je založena na open-source knihovně *OpenVR*. V současné době podporuje primárně jen systém *HTC Vive* a v nedávné době byla přidána experimentální podpora systémů *Oculus Rift* a *OSVR*.

*SteamVR* má na starosti spojení všech ovladačů a jejich rozpoznání, a umožňuje systém z počítače ovládat (provést restart či nastavení). V prostředí virtuální reality pak poskytuje možnost konfigurace systému, zajišťuje, aby uživatel neopustil vyhrazený prostor pro pohyb a další podpůrné funkce důležité pro nerušené zážitky ve virtuální realitě.

## OpenVR

OpenVR je multi-platformní API rozhraní vyvíjené společností Steam, které umožňuje snadný a rychlý přístup k hardware virtuální reality různých výrobců. Poskytuje určitou míru abstrakce k tomu, aby vývojáři měli přístup k jednotnému rozhraní bez závilosti na tom, jakého výrobce systém právě používají.
