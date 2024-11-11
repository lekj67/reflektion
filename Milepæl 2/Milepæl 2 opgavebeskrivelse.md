### Lexar Kjøgx - Gruppe 4 - 5 medlemmer - (Daniel, Magnus, Sebastian, Lexar og André)

## Hvad lærte jeg i fagene?
### Programmering 

structs 
I programmering der har vi haft om structs som gør det muligt at strukturere koden
classes
Vi har også haft om at lave classes i koden, der gør at vi kan gøre vores programmering mere objektorienteret da vi her kan sætte et objekt op som vi kan tilskrive egenskaber og funktioner, det har vi oprettet i en header. Det gør at vi med en class som f.eks. "Class arm" kan lave en kommando der tilskriver arm en forward funktion som vi selv har skrevet og besluttet hvad gør. 
### Elektronik - indlejrede systemer
buck converters
En Buck converter også kendt som et "step down modul" er en lille elektronisk del man kan bruge til at tage et input på f.eks. 12volt, til at blive f.eks. 8 volt.Det virker ved at strømmen kører igennem en modstand der består af en lille ring, en skrue og en pin der kører rundt på ringen og kør modstanden enten størrere eller mindre alt efter hvilken vej du drejer skruen. 
PWM
PWM er forkortelsen for pulse width modulation som er noget vi bruger til at styre de forskellige slags motorer, det giver en fordel i forhold til strøm forbrug og varmen som de producere da de ikke vil være tændt konstant. Vi får også muligheden for at styre hastigheden på vores DC-motorer, som gør vi kan lave mere avancerede køre funktioner. På servomotorerne bruger vi det til at styre positionen de holder sig på, et småt signal får os tættere på 0 og et stort signal tætttere på 180 grader.
servo motorer 
en servo motor minder lidt om DC-motor, men istedet for en hastighed der ændre sig efter PWM, så er det ændring af servo motorens position PWM'en bestemmer, sådan at hvis der er ingen strøm er servo motoren i 0, og hvis PWM'en er sat til 255 vil servo motoren sædde i 180 som er dens maks position. servo motorerne bruger vi på armen til at styre bevægelserne på armen.
kirchhoffs lov
udstyr i E-lab(oscilloscope, triple channel DC power supply, digit multimeter)

### Projekt

I projekt har vi haft om læserskæring og 3D-tegning samt at printe 3D objekter, vi har lært at bruge prusaslicer, inkscape og fusion 360. inkscape bruger man til at tegne 2D tegninger man efterfølgende kan skære ud på MDF i 3 eller 6 milimeter, eller i plexiglas. Det har vi brugt til at lave f.eks. 2 plader til vores rover. Fusion 360 har vi brugt til at lave f.eks. en batteriholder til vores rover som kan tages af og på ved brug af velkro tape, det gør at vi kan flytte vores batterier frem og tilbage fra rover til rover.  Prusaslicer skal man bruge til at få lavet koden som 3D-printeren printer efter, her kan man også lave små ændringer som farveskift igennem printet. 

## Opgave 2 - Arm - Milepælsopgave

### Komponentliste

rover fra opgave 1
4x servomotorer
3D-printet arm
12x Jumpers


### Beskrivelse af armen

Armen er bygget ud af plastik og printet nede i FABlab, det gør at vi selv har kunne bestemme hvor meget fyld der skal være inde i delene til armen sådan at de dele der er belastede kan være mere holdbare end de dele der ikke bliver tungt belastede. Derefter har vi samlet armen og påsæt 4 servo motorer, til at styre armen frem og tilbage. En til at dreje hele armen rundt og en til at åbne og lukke den griber der taget fat om objekter, alle motorerne er begrænsede til kun at kan dreje 180 grader. 