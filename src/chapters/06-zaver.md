# Závěr

Cílem této práce bylo vytvořit aplikaci pro usnadnění seznámení s virtuální realitou návštěvníkům herny a jejich obsluhu zaměstnancům herny.

Byly provedeny analýzy existujících řešení výuky a spouštěčů a pozorováno chování zákazníků a obsluhy v herně virtuální reality. Výsledkem analytické části bylo mimo jiné i stanovení funkčních a nefunkčních požadavků.

Na základě výsledků analýzy pak byla navržena aplikace pro virtuální realitu, skládající se z dvou částí -- z výuky ovládání systému a spouštěče VR aplikací.

Implementaci navržené aplikace předcházelo ověření korektnosti navržených funkcionalit principem Proof of Concept, který poukázal na budoucí komplikace. Jako nejzásadnější komplikací se ukázalo odchýlení od rozsahu implementace v podobě nutnosti přidat další komponentu, a to malý program, tzv. agent, mající na starosti zobrazení spouštěče po ukončení cizí VR aplikace.

Samotná aplikace byla implementována v jazyce C# s využitím herního engine Unity. Součástí implementace bylo zpracování vizuálu, tvorba prostředí, nadabování průvodce a programování logiky aplikace.

Nakonec byla aplikace otestována v reálném prostředí herny virtuální reality. Testování dopadlo ... Z testování vyplynulo několik důležitých nedostatků. Šlo o návrat k výuce při výměně uživatelů na jednom systému, či o ...

*fig Snímek obrazovky zobrazující kompletní výsledky celé realizační fáze*

Realizaci aplikaci lze označit za zdárnou, nicméně lze na ní spatřit následky časové limitace. Velmi omezující byla také nemožnost spouštět aplikaci na VR systému okamžitě. Vlastní headset je pro studenta finančně velmi náročná záležitost a tak bylo nutné aplikaci testovat pouze nárazově způsobem, kdy byla do herny přinesena zkompilovaná binárka aplikace, otestována, a chyby zaznamenány a posléze opraveny.

## Možnosti dalšího vývoje

Až v průběhu realizace se naskytly zajímavé možnosti a nápady, jak aplikaci rozšířit. Bohužel kvůli časovým možnostem nejsou součástí této závěrečné práce, proto jsou uvedeny v závěru jako příležitosti, jak aplikaci dále rozšířit a vyvinout.

Knihovna OpenVR je mnohem mocnější, než je na několik prvních pohledů zjevné. Za vinu to ovšem lze klást špatné dokumentaci, která je nekompletní, nepřehledná a práce s ní není příjemná. Pokud by se s knihovnou pracovalo na hlubší úrovni a doplnila se dokumentace, bylo by teoreticky možné vyřešit několik problémů, na které se v práci narazilo. 

Především by mělo být možné nahradit celý *SteamVR Dashboard* a nedovolit tak zákazníkům přístup k platformě Steam, což by mohlo být pro herny bezpečnější a systém virtuální reality by tak mohl pracovat v jakémsi "kiosk módu". Dále je z nezdokumentovaného kódu zjevné, že v knihovně existují některé metody pro stahování nainstalovaných VR aplikací v počítači. Znamenalo by to tak možnost zobrazit instalované hry nejen z platformy Steam, ale například i z platformy Oculus, či Viveport. Pro účely této závěrečné práce lze však konstatovat, že výsledek nebyl o nic připraven, jelikož se na platformě Oculus nenacházejí žádné aplikace určené pro systém HTC Vive a platforma Viveport není v Evropě příliš populární, je cílena spíše na asijský trh.

Další zajímavou funkcí by mohlo být jednodušší navázání hry pro více hráčů. V herně se nacházejí dva systémy HTC Vive a mezi návštěvníky je oblíbená i hra se spoluhráčem. Také mřížka her by mohla být vylepšena o doplnění řazení, kupříkladu podle oblíbenosti, určené podle doby, kterou zákazníci s hrou strávili.

Více návrhů na vylepšení aplikace by mohlo vzniknout v každodenním používáním v herně, po produkčním nasazení.

