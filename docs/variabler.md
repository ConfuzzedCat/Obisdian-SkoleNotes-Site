---
slug: variables
---


## Hvad er variabler?
Variabler er en måde for at holder på noget værdi, som kan læse eller ændre på senere.
For eksemple hvis man tager en bil, så kan en variable for det være antal af hjul. Hvis en bil mister et hjul, ville bilHjul variablen gå fra 4 til 3.
```java
int bilHjul = 4;

// et hjul bliver taget af.
bilHjul = bilHjul - 1;

println(bilHjul); //Dette ville skrive 3 i consolen.
```
### Forskellen mellem variabler og datatyper
En variable består af en datatype, navn og en værdi. Hvor datatype bare er hvilken type af data man ville gemme i sin variable f.eks.
```java
//Datatype | Variable navn  | Værdi |
  int        antalStudenter =  36; // Denne linje er hele variablen.
```

## Datatyper
Der findes flere forskellige datatyper, fra tal til tekst. De mest normal/mest brugte er:
```java
int heleNummer = 20;
float decimalNummer = 1.32; 
char bogstav = 'c';
boolean bool = true;
String tekst = "Noget tekst man gerne ville gemme.";
``` 
{.language-java}
#### int
Kan holde tal fra `-2.147.483.648` til `2.147.483.647`, men ingen decimal tal.
Int står for Integer. Nogle sprog (som c og c++) bliver det også kaldet int32.
Størrelsen på en int i hukommelsen er 4 bytes.

#### float
Kan holde decimal tal med cirka 6-7 tal decimal cifre.
En hvis du ville fortælle sproget eller kompileren(f.eks. java eller processing) at et tal er en float, kan man sættes `f` efter tallet f.eks. `2.31f`.
Størrelsen på en float i hukommelsen er 4 bytes.

#### char
Kan holde et tegn eller bogstav.
Når man ville fortælle sproget eller kompileren at man har med en char at gøre, sætter man `''` rundt om tegnet eller bogstavet, f.eks. `'g'`.
Hvis man ville gemme et backslash`\` som en char, skal man skrive det to gange f.eks. `\\`. Begrundelse for dette er at backslash bliver også brugt som et `escape character`, hvilket ville sige at man kan f.eks. lave en ny line med `\n` eller et backspace med `\b` osv.
char står for character. 
Størrelsen på en char i hukommelsen er 2 bytes.

#### boolean
Kan holde `true` (sandt) eller `false` (falsk). 
Det har ikke et rigtig et dansk navn.
boolean bliver også nogle gang forkortet til `bool`.
Størrelsen på en boolean i hukommelsen er 1 bit. (Note: Dette gælder ikke for alle sprog!).

#### String
Kan holde 1 eller flere tegn. 
En string er også en linje af tegn/bogstaver (Den får sit navn fra: "A `String` of characters").
Når man ville fortælle sproget eller kompileren at man har med en string at gøre, sætter man `""` omkring sin tekst, f.eks. `"Dette er et eksemple."`.
Størrelsen på en string i hukommelsen kan varier, men i java bruges der 2 bytes per tegn.

## Andre datatyper
Udover de grundlæggende datatyper nævnt over, findes der også andre. Disse inkludere f.eks. double, men også andre som short og long.
```java
byte _byte = 120;
short _short = 25565;
long _long = 2226372016824775807;
double _double = 213.277817288291;
```
#### byte
Kan holde hele nummer fra `-128` til `127`.
En byte består af 8 bits, f.eks. 121 i binary er  `0111 1001`. Bits kan kun holde `1` eller `0`, men hvis man putter flere samme, kan man give være bit et tal, så ved en byte holder hver maks disse tal `(128)(64)(32)(16) (8)(4)(2)(1)`. For det meste læses bytes fra højre mod venstre. Noget andet er den sidste byte holder `128`, men en byte går ikke op til `128`. Dette har noget at gøre om byte'en er `signed` eller `unsigned`. Kommer ind på det senere.
Størrelsen på en byte i hukommelsen er 1 byte.

#### short
Kan holde hele nummer fra `-32.768` til `32.767`. 
Short bliver også kaldet int16 i sprog som c og c++, hvilket kommer fra at det er datatype der kan holde hele tal og består af 16 bits. Tidligere skrev jeg også at int kunne blive kaldet int32 og det er samme grund, altså at den består af 32 bits.
Størrelsen på en short i hukommelsen er 2 bytes.

#### long
Kan holde hele nummer fra `-9.223.372.036.854.775.808` til `9.223.372.036.854.775.807`.
Ligesom short og int, bliver long også kaldet int64. Da den som de short og består af 64 bits.
Long er den primitiv datatype der kan holde den størreste værdi.
Størrelsen på en short i hukommelsen er 8 bytes.

#### double
Kan holde decimal tal med cirka 15 tal decimal cifre.
Double får sit navn fra at være dobbel så stor i hukommelsen som en float.
Størrelsen på en short i hukommelsen er 8 bytes.

## Array
De overstående datatyper (udover string) er alle primitiv datatyper (i java). Men derudover er der også andre type man kan bruge. En er hvad man kan en array.
En array er and samle række/list med en given størrelse (gives når man erklærer den).
Alle datatyper kan bruges til at lave et array, f.eks. hvis man gemme en list af hele nummer, kan man lave en int array.
```java
int[] nummerArray1 = new int[]{0, 1, 2, 3, 4, 5, 6, 7, 8, 9};
int[] nummerArray2 = new int[10];
nummerArray2[5] = 192;
```
Som vist ovenover, kan en array erklæres på to måder, først datatypen fulgt af en åben og lukket squarebrackets (`[]`), derefter (lige som en anden variable) gives variables navn. Men efter ligehedstegnet adskiller den sig fra andre datatyper, da vi skal bruge keyword'et `new` efterfulgt af datatypen og squarebrackets. Som sagt tidligere er der to måde at eklære array på, den ene hvis man ved både størrelse, man ville have og hvilke værdier man ville give den. Den anden er hvis man kun ved hvor stort man ville have array. Hvis ikke man ved hvor stor en array man skal bruge, kan man bare lave et stort array og kun fulde den man skal bruge.
### Index
Hvert værdi i en array, har et række nummer, men andreleds end når man normalt tæller en række, starter det fra 0 og går opad. f.eks.
```java
Index nummer  | 0 | 1 | 2 | 3 | 4 | 5 |
new int[]     { 1 , 2 , 3 , 4 , 5 , 6 };
```

### Multi dimensional array
Udover normale array, kan man også eklære multi dimensional array. Personligt har jeg ikke selv kommet udfor en usecase for det, men det eklæres såleds
```java
int[][] 2dArray = new int[][]{ { 1, 2, 3, 4, 5, 6 }, { 21, 3, 2, 4, 5, 6 } , { 1, 3, 556, 6, 2, 1 }, { 6, 87, 2, 14, 6, 9 } };
```

## Classes
Den sidste og mest brugt udover primitiv datatyper er `classes`. 
Læs mere om classes [[Classes | Her]] (ikke lavet endnu).

Hvis en class ikke er static, kan den eklæres som en datatype således
```java
class Bil{
	public int årsTal {get; set;}
	public String bilProducent {get; set;}
	public String nummerPlade {get; set;}
	public String farve {get; set;}
	public String bilEjer {get; set;}
}

//Inde i noget kode
Bil nyBil = new Bil(){
	årsTal = 2013;
	bilProducent = "BMW";
	nummerPlade = "XX 12345";
	farve = "Rød";
	bilEjer = "Jørgen";
};

// Du kan nu bruge variabler inde i class'en således.
println(nyBil.farve); 

```