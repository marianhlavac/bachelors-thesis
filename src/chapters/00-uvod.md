# Úvod

Virtuální realita (často zkracována na VR) je bezesporu novým trendem v oblasti informačních technologií. Protože je tato technologie běžným lidem méně dostupná, vznikly ve větších městech nové podniky, které zprostředkovávají zážitky ve virtuální realitě za zlomek ceny celého systému, bez nutnosti znalosti systémů virtuální reality a jejich specifikací, zajištění dostatečného výpočetního výkonu pro takové systémy, nutnosti výběru a nákupu her pro virtuální realitu kompatibilní s konkrétním systémem a konfigurace virtuální reality.

Takovým podnikům a jejich návštěvníkům však vznikají určité požadavky, na které systémy virtuální reality nejsou v současné době příliš připraveny. Uživatelské rozhraní softwaru je spíše soustředěno na jednoho dlouhodobého uživatele, který měl prostor systému porozumět, což je nevhodné v prostředí, kde se uživatel s virtuální realitou setkává poprvé a v omezeném čase, po který mu byl systém zapůjčen.

## Co je virtuální realita

Pojem virtuální realita označuje technologii prezentace prostředí pomocí replikace lidských smyslů pro simulaci přítomnosti uživatele v takovém prostředí. Často se virtuální realitou označuje i samotné virtuální prostředí. Technologie tak vytvářejí iluzi reálného alternativního světa.

Konkértní častou definici virtuální reality v angličtině -- "a realistic and immersive simulation of a three-dimensional 360-degree environment, created using interactive software and hardware, and experienced or controlled by movement of the body", můžeme volně přeložit jako "realitiská a pohlcující simulace trojrozměrného 360 stupňového prostředí tvořeného pomocí interaktivního softwaru a hardwaru ovládaného pohybem lidského těla".

Uživatel virtuální reality se může v prostředí typicky rozhlížet, procházet se (v různě omezené míře) a interagovat s vyzobrazenými objekty. Virtuální realita nalézá uplatnění v průmyslu, lékařství, sportu, armádě a pro koncové uživatele především v zábavním průmyslu.

Počátky virtuální reality sahají až do 50. let 18. století, kdy se experimentovalo s různými stereoskopickými displeji a klamání lidských smyslů. Jako nejranější známý příklad virtuální reality je přístroj zvaný *Sensorama*, který byl schopen zobrazovat trojrozměrné stereoskopické obrázky, přehrávat zvuk prostředí a vypouštět aromatické látky, pro pohlcující zážitek.

Na počátku 20. století se objevily další příklady pohlcujících zážitků virtuální reality. Za zmínku stojí projekt projekční místnosti *The Cave*, mezi koncové uživatele nikdy nerozšířený *Sega VR Headset*, či *Virtual Boy* od společnosti *Nintendo*.

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Virtual-Boy-Set.jpg/800px-Virtual-Boy-Set.jpg)  
*fig. 1 Virtuální realita z roku 1995 -- Virtual Boy*

> TODO: Nebude asi právo na použití ^ (i když... je to z wikicommons možná, takže 🤔 ) Stejně je to spíš nevhodná fotka, moc vysoká.

## Virtuální realita v současnosti

V současnosti je virtuální realita tvořena typicky pomocí počítačem generované trojrozměrné grafiky a zvuku, snímání pohybu a snímání polohy lidského těla. Uživateli je zážitek zprostředkován pomocí náhlavních souprav, které vykreslují obraz, přenášejí zvuk a snímají polohu hlavy uživatele.

V rámci této technologie tak vznikají celé systémy virtuální reality, které disponují různými vlastnotmi, technologiemi simulace a kvalitou simulace. Některé systémy míru a kvalitu simulace doplňují snímáním celého lidského těla, či částí jejich končetin, např. ovladačů pro ruce. Snímány jsou i polohy fyzických předmětů, či různých jiných ovladačů. Některé systémy disponují různou technologií snímání. Některé používají infračervené světlo a kamery, jiné systémy zase laserové snímání.

Velkou roli v této technologii hrají kvalitní a rychlé gyroskopy a počítačový výkon. Právě kvůli virtuální realitě v poslední době začal převažovat trend nových "VR ready" grafických karet, které jsou přizpůsobeny k výpočtu obrazu z dvou úhlů pro stereoskopii.

![](https://static3.wareable.com/media/imager/14526-b104d0dee746b81605d5ab3bc0b9c2de.jpg)  
*fig. 2 Systémy virtuální reality současnosti*

> TODO: Tohle ^ definitivně přijde nahradit vlastní fotkou, chci tam vive, oculus a psvr pohromadě. Navíc tenhle nelze použít, nejsou práva asi.

### Systém HTC Vive

V této práci se zaměřím především na systém *HTC Vive*, pro který bude aplikace navržena. Systém *Vive* vyvinutý společností *HTC* ve spolupráci se společností *Valve* je jedním z nejoblíbenějších systémů virtuální reality v současnosti. Koncovým zákazníkům se stal dostupným v dubnu roku 2016.

Skládá se z náhlavní soupravy s OLED displejem o rozlišení 2160x1200 a dvou ovladačů do ruky s gyroskopem, pěti tlačítky a haptickou odezvou. Díky laserovému snímání je možné velmi přesně snímat velký prostor v místnosti, ve kterém se může uživatel volně pohybovat. V České republice je k aktuálnímu datu systém dostupný za přibližně 24 tisíc korun.

![](https://upload.wikimedia.org/wikipedia/commons/7/7a/Vive_pre.jpeg)  
*fig.3 Systém virtuální reality HTC Vive a jeho ovladače*

## Platforma Steam a SteamVR

Protože se na vývoji systému *HTC Vive* podílela společnost *Valve*, která je známá především svou platformou *Steam*, určenou pro digitální distribuci her, je více než logické, že *Vive* je úzce spjat s touto platformou.

Hry a aplikace určené pro tento systém jsou primárně distribuovány skrze platformu *Steam*. Aplikace *Steam* pak obsahuje specializovanou platformu *SteamVR* určenou pro práci se systémy virtuální reality a jejich komunikaci s počítačem. V současné době podporuje jen systém *HTC Vive* a v nedávné době byla přidána experimentální podpora systému *Oculus Rift*.

Platforma *SteamVR* má na starosti spojení všech ovladačů a jejich rozpoznání a umožňuje systém z počítače ovládat (provést restart či nastavení). V prostředí s nasazeným systémem na hlavě pak poskytuje rozhraní pro ovládání systému, zajišťuje, abyste neopustili vyhrazený prostor pro hraní (tzv. *Chaperone bounds*) a další podpůrné funkce důležité pro zážitky ve virtuální realitě tohoto systému.

## OpenVR

OpenVR je API rozhraní vyvíjené společností Steam, které umožňuje snadný a rychlý přístup k hardware systémů virtuální reality různých výrobců. Poskytuje určitou míru abstrakce k tomu, aby vývojáři měli přístup k jednotnému rozhraní bez závilosti na tom, jaký konkrétní systém jakého výrobce právě používají.

> TODO: target 1200w
