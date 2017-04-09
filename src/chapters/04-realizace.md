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

**Ukázka syntaxe jazyka C#**

```csharp
using UnityEngine;
using System.Collections;

public class ExampleSyntax : MonoBehaviour
{
    int myInt = 5;
    
    int MyFunction (int number)
    {
        int ret = myInt * number;
        return ret;
    }
}
```

**Ukázka syntaxe jazyka JavaScript (UnityScript)**

```javascript
#pragma strict

var myInt : int = 5;

function MyFunction (number : int) : int
{
    var ret = myInt * number;
    return ret;
}
```

## Proof of Concept

V aplikaci lze rozlišit klíčové funkce, které jsou poněkud specifické a charakteristické pro danou aplikaci. Ač je snadné navrhnout způsob řešení implementace takových funkcí, je nutné tyto funkce podrobit principem **Proof of Concept** — rychlou implementací konkrétních funkcí nezávisle na zasazení do koncové aplikace.

Na základě takové implementace je pak možné potvrdit, zda-li je návrh implementace klíčových funkcí, na kterých aplikace stojí, realizovatelný.

Jednou z takových funkcí je zobrazení her, které vlastní herna na svém účtu platformy *Steam*. Aby bylo možné zobrazení provést, je nutné o hrách stáhnout informace, podle požadavku *F-C02*. Taková data jsou přístupná pomocí některého z API rozhraní služby *Steam*. Předmětem POC bude takový zdroj dat nalézt a implementovat práci s takovým zdrojem do enginu *Unity*.

Další funkcí, kterou je nutné podrobit POC je samotný spouštěč her a to konkrétně funkci spuštění a opouštění VR aplikací, podle požadavků *F-C03* a *F-C04*. Je nutné vyzkoušet, jak z aplikace vytvořené v *Unity* spouštět aplikace nainstalované skrz platformu *Steam* a jak detekovat jejich ukončení a vyvolání spouštěče opět do popředí.

> TODO: Výsledky POC

## Postup implementace

...

## Prototypování uživatelského rozhraní

...

> TODO: target 2600w