### Lexar Kjøgx - Gruppe 4 - 5 medlemmer - (Daniel, Magnus, Sebastian, Lexar og André)
 
## Hvad lærte jeg i fagene?
### Programmering 
 
I programmering der har vi haft om structs som gør det muligt at strukturere koden og bygge objekter i den.
Vi har også haft om at lave classes i koden, der gør at vi kan gøre vores programmering mere objektorienteret da vi her kan sætte et objekt op som vi kan tilskrive egenskaber og funktioner, det har vi oprettet i en header. Det gør at vi med en class som f.eks. "Class arm" kan lave en kommando der tilskriver arm en forward funktion som vi selv har skrevet og besluttet hvad gør.
### Elektronik - indlejrede systemer
#### buck converters
en buck converter er et meget praktisk værktøj til at kontrollere hvor meget spænding der kommer igennem vores kredsløb men også til at sikre vi ikke brænder noget af, vi bruger en step down converter fra vores serie forbundede batterier til at gå fra 11.1v til 6v. Buck converteren består af en masse små komponenter, hovedsageligt en diode, switch, mosfet, variabel modstand og kapacitatorer som i samarbejde gør at vi kan styre vores udgangsspænding.
 
#### PWM
PWM er forkortelsen for pulse width modulation som er noget vi bruger til at styre de forskellige slags motorer, det giver en fordel i forhold til strøm forbrug og varmen som de producere da de ikke vil være tændt konstant. Vi får også muligheden for at styre hastigheden på vores DC-motorer, som gør vi kan lave mere avancerede køre funktioner. På servomotorerne bruger vi det til at styre positionen de holder sig på, et kort signal får os tættere på 0 og et langt signal tætttere på 180 grader.
### servo motorer 
en servo motor minder lidt om DC-motor, men i stedet for en hastighed der ændre sig efter PWM, så er det ændring af servo motorens position PWM'en bestemmer, sådan at hvis der er ingen strøm er servo motoren i 0, og hvis PWM'en er sat til 255 vil servo motoren sædde i 180 som er dens maks position. servo motorerne bruger vi på armen til at styre bevægelserne på armen.
#### kirchhoffs lov
kirchhoffs lov kogt helt ned i det simple siger egentlig bare at hvis jeg står ved et knudepunkt med 3 komponenter, så på den anden side af komponenterne hvor de 3 mødes vil min samlede strømstyrke på den anden side være det samme som min samlede strømstyrke da jeg gik ind i knudepunktet.
 
### Projekt
 
I projekt har vi haft om læserskæring og 3D-tegning samt at printe 3D objekter, vi har lært at bruge prusaslicer, inkscape og fusion 360. inkscape bruger man til at tegne 2D tegninger man efterfølgende kan skære ud på MDF i 3 eller 6 milimeter, eller i plexiglas. Det har vi brugt til at lave f.eks. 2 plader til vores rover. Fusion 360 har vi brugt til at lave f.eks. en batteriholder til vores rover som kan tages af og på ved brug af velkro tape, det gør at vi kan flytte vores batterier frem og tilbage fra rover til rover.  Prusaslicer skal man bruge til at få lavet koden som 3D-printeren printer efter, her kan man også lave små ændringer som farveskift igennem printet.
### netværk 
det eneste vi har haft om i netværk der kan anbringes på roveren er at vi har lært hvordan man sætter en web-server op på roveren der kan kontrollere GPIO pins trådløst.
 
## Opgave 2 - Arm - Milepælsopgave
 
### Komponentliste

rover fra milepæls opgave 1
4x servomotor
3D-printet arm
12x Jumpers
 
### Beskrivelse af armen
 
Armen er bygget ud af plastik og printet nede i FABlab, det gør at vi selv har kunne bestemme hvor meget fyld der skal være inde i delene til armen sådan at de dele der er belastede kan være mere holdbare end de dele der ikke bliver tungt belastede. Derefter har vi samlet armen og påsæt 4 servo motorer, til at styre armen frem og tilbage. En til at dreje hele armen rundt og en til at åbne og lukke den griber der taget fat om objekter, alle motorerne er begrænsede til kun at kan dreje 180 grader.
 
# 
 
Vi har haft nogen udfordringer angående vores arm da vi har 3 forskellige rovers og vi har skiftet i mellem dem som gør at der altid er noget der skal ændres og skiftes over. De første par 3D-print vi lavede havde også nogen små fejl som satte os en anelse bagud. Der har også været issues angående vores servomotorere, vi har generelt brugt meget tid på at få kontrol på styringen til dem hvilket vi ikke skulle have gjort da det automatisk styring på dem er irrelevant da vi kun skal styre dem via Joystick.
# 
Er personligt ret stolt over at vi har nået så meget på armen, vi startede med at tro vi var bagud men har nu fået samlet ret godt op igen som gør at vi faktisk ikke længere er bagud.
 

