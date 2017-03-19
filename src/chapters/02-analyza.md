# Analýza

Jak je zvykem u organizovaného vývoje softwaru -- implementací a prototypování předchází analýza, pro stanovení požadavků uživatelů softwaru a upřesnění funkcionalit aplikace.

Následující kapitola se takovou analýzou bude zabývat. Analyzuji existující řešení, co požadují hráči docházející do herny, co požadují zaměstnanci pracující v herně a jaké požadavky jsou prakticky realizovatelné.

# Analýza existujících řešení výuky

Výukové aplikace pro seznámení s virtuální realitou již existují. Nicméně většina z nich trpí špatnou přístupností. Systémy jsou navrhovány tak, aby po absolvování takové výuky již nebyly výukové aplikace jednoduše dostuné a tudíž spustitelné pro návštěvníky herny. 

Takové aplikace jsou spíše určené pro toho, kdo jako první systém konfiguruje a je jímž prvním uživatelem. Nově příchozí k nakonfigurovanému systému není tutoriál nabídnut a jsou přímo uvedeni do prostředí, ve kterém se již očekává, že uživatel systém důvěrně zná.

## SteamVR Tutorial 

Pro totožnou platformu, pro kterou je aplikace této závěrečné práce určena -- **HTC Vive**, existuje oficiální výuková aplikace vytvořená přímo autory samotné platformy -- společnosti Valve. 

![](http://1u88jj3r4db2x4txp44yqfj1.wpengine.netdna-cdn.com/wp-content/uploads/2016/03/Walkthrough-of-SteamVRs-new-tutorial_17-930x523.jpg)  
*fig.1 Výuková aplikace SteamVR setup*

Aplikace se nejprve uvede vizuálně poutavým úvodem, který spočívá v sestavení výukové scény animací obklopující hráče. Hráči je tak názorně ukázana možnost rozhlížet se kolem sebe a prozkoumávat prostředí.

### Průběh výuky

Následně je uživateli představena postava (*Virtual Reality Assistance and Education Core*) ze hry Portal 2, která s hráčem komunikuje a provádí ho výukou -- stává se tak *průvodcem*. Monolog je dabovaný a v místech, kde se nachází průvodce lze číst titulky, které jsou lokalizovány do nepřeberného množství jazyků (je k dispozici i Čeština). 

Příjemným bonusem je pro hráče hry Portal 2 familiarita postavy, která může zvýšit hráčovu pozornost a pro hráče, kteří si hru Portal 2 v minulosti oblíbili tak tutoriál navozuje na obličejích úsměv.

Jako první je uživateli představena plocha, tzv. *Play area*, ve které se VR zážitky budou odehrávat. Neprodleně jsou pak představeny tzv. *Chaperone bounds*, které upozorňují hráče na skutečnost, že opouštějí hranice *play area* a jsou vystaveni limitacím fyzické místnosti, ve které se nacházejí. Protože je tato funkcionalita důležitá v zájmu uživatele, pro jeho bezpečnost, je na ni ve výuce kladen důraz a je proto požádán, aby se ke kraji místnosti pomalu přiblížil a následně to stejné zopakoval na druhé straně místnosti.

Dále je uživatel požádán, aby se podíval na ovladače, které drží v ruce a provedl s nimi libovolné pohyby pro vyzkoušení manipulace s nimi. Poté, co se seznámí s pohyby s ovladačem jsou mu postupně představena všechna tlačítka, která se nacházejí na ovladači a je požádán, aby každé stiskl a vyzkoušel si tak, kde se nacházejí a jakou mají zpětnou odezvu.

Výuková aplikace je pojatá spíše komicky a každé tlačítko velmi chytře vyvolává různé destrukční, hlasité a nečekané události, které se průvodci nelíbí. Průvodce hráče žádá aby přestal, hráč však může mít nutkání tyto tlačítka mačkat opakovaně, aby průvodce rozčílil a dělal nepořádek. Tím se s tlačítky seznámí o to více.

Hráč není informován o tom, která tlačítka mají jakou funkci, logicky z toho důvodu, že každá VR hra a aplikace má své pojetí smyslu těchto tlačítek. Ovšem k tlačítkům *Menu* a *System* je uživateli řečeno, k čemu se nejčastěji používají.

Ke stisknutí tlačítka *System* je vzápětí požádáno, což vede k otevření *SteamVR Dashboard*. Lze si povšimnout, že se hra nepozastaví při otevření *Dashboardu* a probíhá tak stále instruktáž, jak se lze ve *SteamVR Dashboard* pohybovat a k čemu je určena.

Tím je výuka u konce, uživatel je instruován k otevření *Dashboardu* a výběrem VR hry či aplikace. Stále ovšem může v aplikaci zůstat a dále zkoušet práci s ovladači, nebo zhlédnout závěrečnou animaci, kdy průvodce komicky odvezou pryč ze scény.

### Zhodnocení

![](http://i.imgur.com/dHgOC1S.png)  
*fig.2 Přístup k aplikaci je skryt ve SteamVR nabídce, která je přístupna jen z monitoru počítače*

> TODO: ^ Nahradit tuten obrázek vlastním

## Oculus Home

# Analýza existujících řešení spouštěčů