### Lexar Kjøgx - Gruppe 4 - 6 medlemmer - (Daniel, Magnus, Sebastian, Lexar, André og jacob)

# Opgave 1 - Base - Milepælsopgave


 
 # hvad lærte jeg i fagene?

 ## programmering
 i programmering der har vi lært en masse om hvordan c++ generelt virker og lært det grundlæggende af hvad man kan gøre i c++. VI har lært hvordan vi opsætter et miljø i visual studio code vi kan arbejde i med alle mulige projekter og især med vores ESP-32. vi har lært en mase om hvordan man kommunikere med en ESP-32 og hvordan vi definere de fysiske pins på ESP'en i vores kode. Vi kan nu give dem forskellige definitioner og bestemme hvilke pins der styre de forskellige motorere i vores kode. 

 Vi kan styre mængden af strøm der bliver sendt ud igennem de pins og se hvordan det påvirker DC-motorerne. vi kan i koden nu styre 4 individuelle DC-motorer og vi har lært hvordan vi kan få roveren til køre langsomt, hurtigt, til højre og til venstre. 
 
 Der er blevet undersøgt hvordan vi får sensorerne sat op, som der gav udfordringer til at starte med da der er 2 typer pins sensorerne skal bruge. Time-of-flight sensorere skal bruge en SDA pin og en SCL pin, og dem er der kun 2 af på vores ESP-32. Der er derfor blevet lagt meget tid i at få flere sensorere sat op ved at bruge XSHUT pins, som der gør at vi kan give vores sensorere unikke adresser så ESP'en kan differenciere mellem sensorerne som har gjort at vi kan bruge de 3 sensorere individuelt af hinanden i forskellige funktioner. derfor har vi nu funktioner der bruger vores sensorere til at måle hvad afstanden, og så efter de afstandsparametre vi har sat så starter den forskellige funktioner alt efter hvilke parametre der bliver opfyldt. 

 nu vil jeg gerne undersøge hvordan vi kan få vores kode til roveren kogt ned, gjort pænt og om der er nogen bedre funktioner i c++ som vi kan bruge, istedet for dem som vi bruger ligenu. 

## Elektronik og indlejrede systemer

vi har arbejdet med de forskellige komponenter som f.eks. modstande, kondensatorere, kapacitator og H-broer. 
H-broer har vi lært hvordan fungere ved først at bgge et kredsløb med knapper der bruger det samme koncept som en H-bro er bygget efter, der har vi bagefter koblet kredsløbet til vores DC-motorerne og testet det. Den information har vi derefter brugt til at koble vores H-broer op til vores motorere og til vores ESP-32 som kan styre dem lidt ligesom vi gjorde med knapperne, så vores base nu kunne køre frem og tilbage. 

Efter vi havde gjort det, prøvede vi at forbinde en sensor, som var problematisk men vi fik den ene sensor til at virke, så prøvede vi at forbinde 2 mere til, som tog ekstremt lang tid at få at til at virke efter vi havde skrevet en kode vi vidste ville virke da den var blevet testet uden roveren kørte.Vi fejlsøgte i koden i rigtig lang tid. vi fandt derefter frem til at koden slet ikke var problemet, men at vi efterhånden havde så mange ting på roveren, at der bare ikke var strøm nok til de kunne virke i mens at motorerne også var tændt, som vi løste ved at tilføje en ekstern strømforsyning. 

Det har medført at elektronikken på basen nu virker og at det er blevet muligt at koble lygter på foran og bagved. 

## projekt 

i projekt har vi arbejdet med de 4 forskellige faser inden for projekt arbejde, idé og målsætning, analyse og planlægning, gennemførelse med overgang til drift, samt evaluering og læring. 

vi har brugt mindmaps og brainstorming til at opbygge en generel ide om hvad det er vi gerne vil opnå i milepæl 1, vi har efter de ideer sat os nogen mål vi rigtig gerne ville have opfyldt, derefter har vi haft nogen forskellige arbejdsopgaver som alle sammen er blevet udfyldt som har gjort vi har opnået de mål vi har sat for os selv. Bagefter har vi sat flere ting på for at udfordre os selv og komme lidt på forkant i næste milepæl. 

## Komponentliste

* base
* 2x H-bro
* 1x Fumlebræt med 2 røde LED'er(bak lys)
* 1x Fumlebræt med 2 hvide LED'er(for lys)
* 1x Fumlebræt med styring 
* 1x ESP-32
* 4x DC-motorer
* 3x Time-of-flight sensor
* 39x jumpers


### Beskrivelse af basen
Basen er opbygget sådan at der er to H-broer som styrer DC-motorerne, altså hjulene, de er sat op sådan at motorerne i venstre side sidder i en H-bro og at motorerne i højre side sidder i den anden H-bro. Vi har valgt at gøre sådan fordi at det mener vi giver den bedste styring til når roveren skal dreje og generelt er mere overskueligt at styre. foran der har vi en time-of-flight sensor sådan at roveren "kan se" når den er ved at køre ind i noget, det styrer vi gennem vores ESP-32.
Det samme gør vi med vores to andre time-of-flight sensorer, hvor der en sidder en på venstre side og en på højre side. 
På basen der har vi også 3 fumlebræt med, et til bag lygter, et til for lygter og en til generel styring med ESP-32.
vi har så skrevet en kode der gør at ESP'en tænder og slukker motorerne alt efter hvad sensorerne læser, sådan at hvis den er tæt på noget i højre side drejer den til venstre, og det modsatte i den anden side, hvis den ser noget tæt på foran, så bakker den og drejer en lille smule indtil den er fri fra det der er foran den. 
#

Det har været udfordrende at få startet op på at bygge basen og sammensætte delene korrekt i samarbejde med koden. Der er blevet brugt meget tid på fejlfinding. Som jeg helt klart finder mest udfordrende da det er helt nye emner vi arbejder med så derfor skal man lære mens man fejlfinder. Vvis man starter sin fejlfinding det forkerte sted er det allerede der svært at finde fejlen hurtigt. vi har haft en udfordring med at vi ikke har haft strøm til at trække hele roveren med en forsyning, så det tog lidt ekstra tid at regne ud hvorfor roveren ikke gjorde som vi havde bedt den om i koden.  

# 
Vores rover fungere nu ret godt med at den kan køre selv uden at kører ind i noget, jeg er stolt af at på en  måned der har vi lært hvordan programmeringen skal sættes op men også at vi kan bygge basen op fra bunden med motorer, H-broer og styring, og at vi har fået det hele til at spille sammen med vores ESP-32, især sensorene har været en udfodring så det er jeg meget stolt over der virker ikke bare med én sensor, men med tre sensorere der kan bruges. 