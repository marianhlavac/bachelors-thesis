# Analýza

Jak je zvykem u organizovaného vývoje softwaru -- implementací a prototypování předchází analýza, pro stanovení požadavků uživatelů softwaru a upřesnění funkcionalit aplikace.

Následující kapitola se takovou analýzou bude zabývat. Analyzuji existující řešení, co požadují hráči docházející do herny, co požadují zaměstnanci pracující v herně a jaké požadavky jsou prakticky realizovatelné.

## Analýza existujících řešení výuky

Výukové aplikace pro seznámení s virtuální realitou již existují. Nicméně většina z nich trpí špatnou přístupností. Systémy jsou navrhovány tak, aby po absolvování takové výuky již nebyly výukové aplikace jednoduše dostuné a tudíž spustitelné pro návštěvníky herny. 

Takové aplikace jsou spíše určené pro toho, kdo jako první systém konfiguruje a je jímž prvním uživatelem. Nově příchozí k nakonfigurovanému systému není tutoriál nabídnut a jsou přímo uvedeni do prostředí, ve kterém se již očekává, že uživatel systém důvěrně zná.

### SteamVR Tutorial 

Pro totožnou platformu, pro kterou je aplikace této závěrečné práce určena -- **HTC Vive**, existuje oficiální výuková aplikace vytvořená přímo autory samotné platformy -- společnosti Valve. 

![](http://1u88jj3r4db2x4txp44yqfj1.wpengine.netdna-cdn.com/wp-content/uploads/2016/03/Walkthrough-of-SteamVRs-new-tutorial_17-930x523.jpg)  
*fig.1 Výuková aplikace SteamVR Tutorial*

#### Průběh výuky

Aplikace se nejprve uvede vizuálně poutavým úvodem, který spočívá v sestavení výukové scény animací obklopující hráče. Hráči je tak názorně ukázana možnost rozhlížet se kolem sebe a prozkoumávat prostředí.

Následně je uživateli představena postava (*Virtual Reality Assistance and Education Core*) ze hry Portal 2, která s hráčem komunikuje a provádí ho výukou -- stává se tak *průvodcem*. Monolog je dabovaný a v místech, kde se nachází průvodce lze číst titulky, které jsou lokalizovány do nepřeberného množství jazyků (je k dispozici i Čeština). 

Příjemným bonusem je pro hráče hry Portal 2 familiarita postavy, která může zvýšit hráčovu pozornost a pro hráče, kteří si hru Portal 2 v minulosti oblíbili tak tutoriál navozuje na obličejích úsměv.

Jako první je uživateli představena plocha, tzv. *Play area*, ve které se VR zážitky budou odehrávat. Neprodleně jsou pak představeny tzv. *Chaperone bounds*, které upozorňují hráče na skutečnost, že opouštějí hranice *play area* a jsou vystaveni limitacím fyzické místnosti, ve které se nacházejí. Protože je tato funkcionalita důležitá v zájmu uživatele, pro jeho bezpečnost, je na ni ve výuce kladen důraz a je proto požádán, aby se ke kraji místnosti pomalu přiblížil a následně to stejné zopakoval na druhé straně místnosti.

Dále je uživatel požádán, aby se podíval na ovladače, které drží v ruce a provedl s nimi libovolné pohyby pro vyzkoušení manipulace s nimi. Poté, co se seznámí s pohyby s ovladačem jsou mu postupně představena všechna tlačítka, která se nacházejí na ovladači a je požádán, aby každé stiskl a vyzkoušel si tak, kde se nacházejí a jakou mají zpětnou odezvu.

Výuková aplikace je pojatá spíše komicky a každé tlačítko velmi chytře vyvolává různé destrukční, hlasité a nečekané události, které se průvodci nelíbí. Průvodce hráče žádá aby přestal, hráč však může mít nutkání tyto tlačítka mačkat opakovaně, aby průvodce rozčílil a dělal nepořádek. Tím se s tlačítky seznámí o to více.

Hráč není informován o tom, která tlačítka mají jakou funkci, logicky z toho důvodu, že každá VR aplikace má své vlastní pojetí smyslu těchto tlačítek. Ovšem k tlačítkům *Menu* a *System* je uživateli řečeno, k čemu se nejčastěji používají.

Ke stisknutí tlačítka *System* je vzápětí požádáno, což vede k otevření *SteamVR Dashboard*. Lze si povšimnout, že se hra nepozastaví při otevření *Dashboardu* a probíhá tak stále instruktáž, jak se lze ve *SteamVR Dashboard* pohybovat a k čemu je určena.

Tím je výuka u konce, uživatel je instruován k otevření *Dashboardu* a výběrem VR aplikace. Stále ovšem může v aplikaci zůstat a dále zkoušet práci s ovladači, nebo zhlédnout závěrečnou animaci, kdy průvodce komicky odvezou pryč ze scény.

#### Zhodnocení

...

![](http://i.imgur.com/dHgOC1S.png)  
*fig.2 Přístup k aplikaci je skryt ve SteamVR nabídce, která je přístupna jen z monitoru počítače*

> TODO: ^ Nahradit tuten obrázek vlastním

...

### Oculus Home

...

## Kvalitativní porovnání existujících řešení výuky

...

### Metriky porovnávání

Lorem ipsum dolor sit amet.

| Metrika | Popis |
| ------- | ----- |
| Seznámení se s *play area* | dfo kasdp ofkapso kfpaosk fdpoask df |
| Seznámení se s ovladači | sdmf asndf njf ndsf asdf jasiodj fiosaj |

...

## Analýza existujících řešení spouštěčů

...

## Pozorování v herně

Ke konci března roku 2017 jsem měl příležitost stát se na jeden den obsluhou v herně *Virtualnirealita.cz* v pražských Dejvicích. Tuto příležitost jsem využil v prospěch analýzy jako předmět pozorování a bližšího pochopení požadavků jak hráčů tak obsluhy herny.

Jako obsluha jsem měl povinnost seznámit zákazníky s pronajatým systémem a pokud s virtuální realitou neměli dosud zkušenost, nebo se nedoslechli o žádné konkrétní hře, či aplikaci, kterou by si přišli vyzkoušet, byl jsem dále pověřen doporučením nějaké hry na základě jejich preferencí.

Protože jsem se ptal na přirozené otázky, abych byl schopen lépe s lidmi pracovat a také jim doporučit správnou hru, vznikla mi tak miniaturní analýza z malého vzorku lidí, kteří ten den do herny dorazili.

Za daný den navštívilo hernu **15 zákazníků**, z toho **10 mužů**. Většina -- **12 zákazníků** hraje počítačové hry, ale pouze **2 z nich** v minulosti hernu navštívili, nebo měli s VR zkušenost. Většina z nich byla mládež (v rozmezí 15-30 let), výjimku tvořili **2 děti** (< 15) a **2 dospělí** (> 30). U jednoho z návštěvníků se projevila *kinetóza*.

Pouze **4 z nich** odpověděli, že jim nepřišly ovladače systému HTC Vive obtížné na seznámení, stejně tak tito lidé odpověděli, že by se obešli bez pomoci obsluhy. Dva z těchto čtyř byli ti, kteří již s VR měli zkušenost.

![Imgur](http://i.imgur.com/lEo1Fkh.jpg)  
*fig.3 Na jeden den jsem změnil svou pracovní roli*

Občasným jevem bylo několikanásobné vystřídání zákazníků na jednom systému za dobu zapůjčení. To je důležitá informace, protože výuková aplikace musí s takovým jevem počítat.

Rychlost seznámení se systémem byla převážně ovlivněna zákazníkovou zkušenosti s počítačovými hrami.

...
