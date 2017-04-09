# Návrh

## Návrh průběhu výuky

Před konkrétním návrhem přesného scénáře výuky se v této kapitole budu nejdříve zabývat hrubým a obecnějším návrhem průběhu celé výuky. Samotnou výuku rozdělím do tzv. momentů, které si i označím identifikátory, pro snazší pozdější referenci v textu. Výsledný průběh pak dále zpracuji ve formě storyboards.

## Momenty výuky

Seznam klíčových momentů průběhu výuky v chronologickém pořadí:

 - M1 Uživatel je uvítán do herny, kterou navštívil.
 - M2 Uživateli je vysvětleno, jaký bude průběh výuky.
 - M3 Uživateli je umožněno výuku přeskočit.
 - M4 Uživateli je představena play area a chaperone bounds.
 - M5 Uživatel je požádán, aby prozkoumal ovladače systému.
 - M6 Uživateli je představeno každé tlačítko na ovladači a je požádán aby je stiskl.
 - M7 Uživateli je vysvětleno, k čemu je určen spouštěč, který je mu zobrazen po skončení výuky.
 
### M1 Uvítání herny

Jako první moment je herně posktynut velmi krátký prostor na její prezentaci. Návštěvník herny je uvítán jménem herny do virtuální reality. Zároveň je mu na krátký moment zobrazeno logo herny. Díky tomuto prvku je aplikace blíže svázána s hernou a jedná se tak i o jistou formu brandingu. 

Díky tomuto prvku mohou mít o aplikaci zájem i jiné firmy provozující herny virtuální reality, jelikož prozatím neexistuje žádná jednoduše dostupná aplikace pro virtuální realitu, která by vhodným způsobem prezentovala hernu, kterou uživatel právě navštívil.

### M2 Vysvětlení průběhu výuky

Aby byl uživatel připravený a věděl, co jej čeká, je mu velmi stručně přiblížen průběh výuky. Zároveň se tak může lépe v následujícím momentu rozhodnout, zda-li bude výuku přeskakovat, či nikoliv.

### M3 Možnost přeskočení výuky

Protože někteří uživatelé jsou již systému HTC Vive znalí, je jim umožněno takovou výuku přeskočit a jsou rovnou uvedeni do spouštěče.

Přeskočení výuky lze provést stisknutím kombinace tlačítek na ovladači. Na obou ovladačích bude uživatel nucen stisknout tlačítko spouště a tlačítko nabídky. Tato kombinace bude uživateli představena a jde o takovou kombinaci tlačítek, kterou neznalý uživatel omylem nestiskne.

Stisknutí těchto dvou tlačítek není úplně přirozené. Při běžném držení má uživatel palec spíše v oblasti nad dotykovou plochou, nebo mírně pod ní. Tlačítko nabídky se nachází nad dotykovou plochou. Zároveň stisknutí obou tlačítek zároveň je mírně nepřirozené (je nepravděpodobné, že by tato dvě tlačítka uživatel stiskl omylem, např. nevhodným úchopem ovladače), ale zároveň ne nemožné, či obtížně stisknutelné.

Původním záměrem bylo instruovat uživatele k této kombinaci tlačítek pouze slovy a textem -- tím by bylo zajištěno, že uživatel, který tlačítka a jejich pojmenování nezná, nebude schopen tato tlačítka najít a stisknout. V závěru jsem však došel k tomu, že je naprosto v kompetenci uživatele, aby se rozhodl, jestli chce výuku spustit, či nikoliv, a tedy pokud se rozhodne výuku nepodstoupit i za předpokladu, že tlačítka nezná, je to jeho volba, která bude respektována. Zároveň může dojít i k jazykovým nepřesnostem a uživatel může z jiných zdrojů znát tlačítka pod jinými názvy, nebo jejich pojmenování znát pouze ve specifické anglické mutaci (mnohem pravděpodobnější).

### M4 Představení Play area a Chaperone Bounds

Jelikož bezpečnost zákazníka a majetku herny je prioritní, jsou uživateli vysvětleny pravidla pohybování se v play area jako první.

Uživateli se na podlaze zobrazí ohraničení odpovídající velikosti a pozici nastavené play area. Je mu vysvětleno, k čemu play area slouží. Následně jsou mu představeny chaperone bounds. Uživatel je požádán, aby k nim přistoupil, aby si jejich funkcionalitu vyzkoušel.

![](http://icdn9.digitaltrends.com/image/chaperone-beginner-1500x1000.png)
*fig. 1 Chaperone bounds a jejich možnosti v nastavení OpenVR*

Tento přístup je tak inspirován výukou v aplikaci *SteamVR Tutorial*, nicméně je zkrácena o jedno opakování, aby tato část nebyla příliš dlouhá. Ač jsem výše poznamenal, že je žádoucí, aby byl na tuto část kladen důraz, domnívám se, že jedno přistoupení k mřížce uživateli stačí k tomu, aby intuitivně funkci pochopil a na zobrazení mřížky v budoucnu reagoval.

### M5 Prozkoumání ovladače

Uživatel je požádán, aby si prohlédl ovladač. V aplikaci bude vykreslován velmi přesný model ovladače, takže uživatel může pohodlně prozkoumat, jak ovladač vypadá, pokusit se nalézt tlačítka a najít správný úchop pro vlastní komfort.

Délka této části je dynamická a uživateli je tady poskytnut libovolný prostor pro jeho vlastní zkoumání. Důvod je prostý -- každému z uživatelů bude průzkum ovladačů trvat různou dobu, odvíjející se i od důkladnosti prozkoumávání. Zde by mělo být kompletně na jeho uvážení, zda-li si chce a potřebuje ovladače prohlédnout skutečně důkladně, nebo mu stačí jen letmý pohled na jejich vzhled a přibližnou polohu tlačítek.

Pokud se uživatel rozhodne pro druhou volbu, neznamená to, že by se nedosáhlo na potřebnou kvalitu výuky. Seznámení s tlačítky zajistí moment *M6*, takže se nestane, že by s ovladači po skončení výuky nebyl seznámen pouze proto, že si ovladače v této části neprohlédl důkladně.

Uživatel je pak požádán, aby ve chvíli, kdy bude připraven pokračovat ve výuce dále, si stoupl do středu místnosti a zvedl své ovladače před sebe tak, aby na ně viděl.

Skriptově nebude podmíněno, aby si uživatel stoupl do středu místnosti. Instrukce slouží spíše k úpravě pozice uživatele. Poslední jeho poloha je totiž u kraje místnosti, kde právě před chvílí zkoumal Chaperone bounds. Ač mají Chaperone bounds od reálně vyměřené velikosti místnosti určitý odstup, stále se může stát, že uživatel ve chvíli, kdy je požádán, aby zvedl natažené ruce před sebe, natáhne ruce příliš a může ovladačemi praštit do stěny, která je před ním.

### M6 Představení tlačítek

Každé tlačítko je uživateli postupně představeno, zvýrazněno se zobrazením titulku názvu tlačítka a je požádán aby tlačítko stiskl, nebo s ním provedl nějakou interakci v následujícím pořadí:

 - Tlačítko spouště
 - Boční tlačítka
 - Dotyková plocha
 - Tlačítko nabídky a systémové tlačítko

Po každém požádání o stisk tlačítka je uživatel jen přibližně seznámen s tím, k čemu se tlačítko běžně používá. Je však nutné u návrhu scénáře dát pozor, aby takové informace nebyly zavádějící, protože jak jsem již v analýze zmínil, tlačítka si VR aplikace mapují podle vlastního uvážení a každá aplikace tak tlačítka používá k různě jiným činnostem.

![](http://i.imgur.com/5rTX05h.png)
*fig. 2 Náčrt ovladače HTC Vive*

> TODO: Nahradit tento obrázek jiným, pravděpodobně nejsou práva na použití!

Protože je tlačítko spouště důležité, je do výuky přidán prvek laserového ukazovátka, pomocí kterého se uživatel naučí s ovladačem mířit a spouští vybírat. Mělo by to tak podvědomě utvrdit často VR aplikacemi využívaný koncept navigace v nabídkách -- ukázáním a výběrem spouští.

Následně je uživatel požádán, aby tlačítko spouště stiskl, což vyvolá akci ve formě zesílení laserového paprsku a vypalování tmavých stop do okolí po tomto paprsku. Uživatel je požádán, aby namířil na terč, který bude pro účely tohoto kroku do scény umístěn a stiskl spoušť. Je tak v rychlosti uveden do schopnosti mířit ovladačem a zároveň provést akci.

Protože laserový paprsek vypaluje do okolí stopy, uživatel může být podvědomě podnícen práci se spouští procvičit více a to tak, že začne do okolí vypalovat další stopy. Ač je hned následně pobídnut, aby stiskl boční tlačítko, může tak stále činit a dále používat tlačítko spouště s laserovým paprskem.

Poté, co uživatel stikne boční tlačítko, je mu představena dotyková plocha. Je důležité, aby uživatel pochopil, že má dvě funkce. Pohyb prstem přes plochu a její stisknutí. Na ovladači přes dotykovou plochu se zobrazí barevný kruh a uživatel je požádán, aby přes plochu přejížděl prstem, vybral si barvu a dotykovou plochu stiskl. Výběrem barvy a stikem dotykového tlačítka je uživateli změněna barva laserového ukazovátka. Opět jej to může podpořit v další spontánní činností s ovladači.

Jako poslední jsou mu představena tlačítko nabídky a systémové tlačítko. Tady uživatel výjimečně není požádán o stisk těchto tlačítek, jelikož systémové tlačítko otevírá *SteamVR Dashboard*, který záměrně uživateli představit nechceme. V rámci konzistence pak nechceme uživatele žádat o stisk tlačítka nabídky.

Nicméně uživateli je vysvětlena funkce obou tlačítek a nedochází ve výuce ke snaze přesvědčit jej, aby systémové tlačítko nemačkal. Místo toho je mu vysvětleno, k čemu slouží, co se po stisku stane a velmi mírně s dobrou volbou slov doporučíme procházení *SteamVR Dashboard* pouze zkušenějším uživatelům. Chceme však toto tlačítko vysvětlit i uživatelům neznalým, aby při stisku tohoto tlačítka nepanikařili a vzpomněli si na výuku, která je naučila stisk tohoto tlačítka v případě, že nějakou systémovou nabídku otevřeli omylem.

### M7 Představení spouštěče

Po skončení výuky je uživateli oznámeno, že je to vše, co o systému potřebuje vědět a je mu vysvětleno, co se bude dále dít.

Krátce je mu představeno, co před sebou vidí, k čemu je spouštěč určen a jak může spustit svůj první VR zážitek.

## Návrh výuky

Poté, co jsem specifikoval hrubý návrh scénáře výuky a její momenty, lze z těchto momentů sestavit konkrétní podobu výuky.

### Návrh scénáře

První část návrhu výuky je sestavení scénáře, který pak lze velmi efektivně využít pro skriptování průběhu, zobrazení přepisu a samotnému dabování mluveného slova.

Ve scénáři jsou specifikovány identifikátory momentů. Ty označují části, které vycházejí ze zmíněných momentů.

---

*[M1] Zobrazí se logo herny.*

*Průvodce:* Vítejte v herně Virtualnirealita.cz.

*[M2] Průvodce:* Tato krátká výuka vás provede vstupem do virtuální reality.

*[M3] Průvodce:* Pokud s virtuální realitou již máte zkušenosti a výuku chcete přeskočit, stiskněte kombinaci tlačítek menu a spouště.

*Zobrazí se instrukce pro přeskočení výuky na obrazovce.*

*- krátká pauza -*

*[M4] Play area se zvýrazní.*

*Průvodce:* Rozhlédněte se kolem sebe a na podlahu. Ohraničení, které můžete vidět na zemi je místo, ve kterém se můžete volnbě pohybovat v průběhu svých zážitků ve virtuální realitě.

*Průvodce:* Toto ohraničení však není vidět vždy, proto se zobrazuje pomocná mřížka, která vás na tyto hranice upozorní, pokud se je pokusíte překročit. Nyní se zkuste pomalu k hranici přiblížit, abyste si vyzkoušeli, jak to funguje. Za tuto hranici dále nechoďte.

*[M5] Průvodce:* Prozkoumejte ohraničení a dále se krátce podívejte na ovladače, které máte v ruce. Až budete připraveni, vraťte se doprostřed místnosti a zvedněte obě ruce před sebe. Řekneme si něco více k ovladačům.

*Výuka nyní čeká na uživatelův vstup: zvednutí obou rukou před sebe...*

*[M6] Průvodce:* Toto jsou ovladače systému HTC Vive. Nyní vám představíme všechna tlačítka, která se na ovladači nacházejí. Budou zvýrazněny a můžete ovladačem libovolně otáčet.

*Zvýrazní se tlačítko spouště.*

*Průvodce:* Toto je tlačítko spouště. Slouží ve hrách většinou jako tlačítko pro výstřel, nebo výběr položky v menu. Namiřte laserové ukazovátko na terč a stiskněte spoušť.

*V pozadí se zobrazí terč a z ovladače začne zářit slabý laserový paprsek. Po stisknutí spouště se zvýší výkon laserového paprsku a začne vypalovat do objektů stopy. Dále se zvýrazní boční tlačítko.*

*Průvodce:* Skvělé. Toto je boční tlačítko, které lze stisknout z libovolné strany. Slouží jako alternativní funkce, například pro přebíjení zbraně. Stiskněte jej.

*Po stisku tlačítka se zvýrazní dotyková část ovladače, na které se zobrazí barevný kruh.*

*Průvodce:* Výborně. Toto je dotyková část ovladače. Můžete po ní přejíždět prstem nebo ji i stisknout. Přejížděním prstu vyberte barvu a stisknutím dotykové plochy vyberte barvu svého laserového ukazovátka.

*Po výběru barvy uživatelem se zvýrazní tlačítka Menu a Systém s odpovídajícími popisky.*

*Průvodce:* Dobře. Zbývají nám dvě tlačítka. Menu tlačítko a systémové tlačítko. Menu tlačítko slouží většinou k vyvolání nabídky ve hře, kterou můžete používat pro pozastavení hry, nebo jiné činnosti. Systémové tlačítko pak otevírá nástěnku systému Steam. Pokud jste s platformou Steam seznámeni, můžete toto tlačítko používat pro navigaci platformou a výběru jiných VR aplikací. Stejným tlačítkem tuto nástěnku i můžete zavřít.

*- krátká pauza -*

*[M7] Průvodce:* Nyní jste připraveni spustit svůj první zážitek ve virtuální realitě. Před sebou vidíte knihovnu dostupných aplikací naší herny. Vyberte si, o který zážitek máte zájem, namiřte na něj a stiskněte spoušť.

---

### Storyboards

Pro lepší vizualizaci je k podrobnému konkrétnímu scénáři i ilustrován průběh výuky ve formě storyboards.

## Návrh spouštěče

Spouštěč je funkcionalita aplikace navazující po výuce. Je určen k tomu, aby nahradil stávající řešení výběru VR aplikací skrze *SteamVR Dashboard*, které se ukázalo být nevhodné pro použití v prostředí herny.

Podle funkčních požadavků a v kontrastu s existujícími řešení v podobě *SteamVR Dashboard* a *Oculus Home* chceme vytvořit takový spouštěč, který bude pro uživatele jednoduchý, bude brát v potaz fakt, že uživatel může být v systému virtuální reality stále nováček a že nemusí znát tituly podle jejich názvu. Nechceme uživatele zatěžovat v herně nerelevantními komunitními funkcemi a nechceme uživateli jednoduše dovolit prohlížet obchod a nakupovat tituly na účtu herny.

### Návrh rozhraní

Pro rozhraní lze využít celý prostor kolem uživatele. Nebude se jednat o rozhraní, které můžeme vidět u *SteamVR Dashboard* -- ploché dvourozměrné rozhraní vykreslované na malou plochu před uživatelem.

Základní myšlenka rozhraní je přímý přístup k výběru VR aplikací jako hlavní primární obrazovka spouštěče. Oba zkoumané existující řešení zmíněné výše mají výběr VR aplikací ukrytý pod tlačíkem "Library". 

Jako první bude uvádět rozhraní velký nadpis vyzývající uživatele k činnosti: "Vyberte si VR aplikaci". Pod ním bude zobrazen název aktuálně otevřené kategorie s šipkou evokující známý dropdown prvek, kterým může uživatel změnit aktuálně zobrazenou kategorii. Pod výběřem kategorií se nachází již samotná mřížka s aplikacemi. Mřížka má na výšku čtyři prvky a na šířku počet sloupců dynamický, podle velikosti místnosti takový, že vyplní bannery pokud možno kruh okolo uživatele.

![](http://i.imgur.com/EEyrMmf.png)  
*fig. 3 Rozložení prvků rozhraní kolem uživatele*

VR aplikace budou v mřížce zobrazovány velmi podobně, jako jsou zobrazovány v existujících spouštěčích -- vizuální obdélníkový banner s vizuálem hry. Velký rozdíl se však bude projevovat při ukázání ukazatelem na takový banner. Hra zobrazí svůj rychlý detail. Místo vizuálního banneru zaujme krátké video pořízené ze hry (tzv. in-game gameplay), které se bude opakovat. Nepůjde tedy o vizuál autorů aplikace, ani o trailer, ale čistě realistický záznam přímo ze hry. Uživatel tak bude schopen velmi přesně odhadnout, o čem aplikace je, jaká je její vizuální úroveň a přibližně i hratelnost a celkový dojem z aplikace, ještě dřív, než ji spustí. Napravo od videa bude pak doplněno celým názvem titulu, krátkým popisem a kategorizací podle žánru a intenzity. Pokud se bude jednat o často spouštěnou aplikaci, bude automaticky označena jako oblíbená. Celý tento blok detailu hry bude k uživateli mírně přiblížen a ostatní prvky se stanou částečně průhledné a budou mírně potlačeny do pozadí. 

![](http://i.imgur.com/W7i1O7H.png)  
*fig. 4 Základní stav aplikace spouštěče*

Mřížka těchto bannerů se bude zobrazovat v kruhu okolo uživatele. Hlavní mřížka aplikací bude zarovnána k pravému "virtuálnímu okraji", za kterým budou dva sloupce dalších bannerů, označených jako "Naše herna doporučuje". Tyto bannery bude volit herna jako doporučené hry pro své zákazníky a bude obsahovat maximální počet 8 aplikací. Pravý "virtuální okraj" se bude nacházet po pravé ruce uživatele a hlavní mřížka aplikace se bude podle počtu zobrazených aplikací rozšiřovat proti směru hodinových ručiček o obvodu kruhu, na kterém se mřížka zobrazuje. Pokud počet aplikací bude větší, než prostor k zobrazení bannerů na mřížce, zobrazí se pod mřížkou přepínač stránek.

![](http://i.imgur.com/K37enUq.png)  
*fig. 5 Detail hry po ukázání na jeho položku v mřížce*

Po výběru prvku pro změnu kategorie se potlačí pozadí stejným způsobem, jako při práci s detailem hry. Do popředí se pak zobrazí velmi jednoduchá nabídka v podobě seznamu dostupných kategorií, ze kterých může uživatel vybírat. První oddělená položka této nabídky bude tlačítko pro návrat nazvané "Zpět".

![](http://i.imgur.com/49YOKw4.png)  
*fig. 6 Výběr kategorie po kliknutí na prvek výběru kategorie*

Rozhraní by tak mělo být velmi přehledné a především jednoduché. Uživatel se v rozhraní nemá kde ztratit, rozhraní nemá přechod na jiné obrazovky či stavy s vyjímkou možnosti třídění her.

