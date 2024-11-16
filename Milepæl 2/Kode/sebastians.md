## Opgave 2 - Arm - Milepælsopgave

Gruppe 4 - Magnus, Lex, André, Daniel & Sebastian

Fortsættelse på milepælsopgave 1 - Basen.

# Opgavebeskrivelse 
Introduktion

I skal aflevere et refleksionsdokument i Markdown (.md) baseret på dokumenteti arbejdede med i sidste milepæl (altså skriv videre på den).

Besvarelsen er med udgangspunkt i fagene indlejrede elektronik, programmering,og projekt.Det forventes at i bruger feedback fra sidste gang til at forbedre/rette det iafleverede sidst, samt tilføjer eventuelle mangler fra sidst.I skal redegøre for de emner i har haft om siden sidste aflevering.

Dernæst skal i ligesom sidste gang forklare hvordan i har brugt det i har lærtsiden sidst, men denne gang til at forklare hvordan i har designet, konstrueret,og programmeret armen til roveren. I skal besvare og aflevere individuelt.  Gruppenr.  og gruppemedlemmer skal noteres så det er tydeligt hvilken gruppe i er i.

I afleverer én Markdownfil (.md) på ItsLearning. Maksimalt 5 normalsider (2400tegn per side inklusive symboler og mellemrum), intet minimum.

### Komponentliste

* 4x Servomotorer
* Fumlebræt
* 3D printet arm
* 3D printet base
* ESP32

### Beskrivelse af armen
 
Armen er 3D printet efter vi har haft undervisning i 3D print og lasercutting. Vi har brugt undervisningen til at kigge på forskelle formfaktorer til vores arm. Vi har lavet ændringer på den nuværende base ud fra de mål der er blevet brugt til armen. Vi har arbejdet med flere forskellige versioner af armen for at se hvad der passer os og de forestillinger vi har bedst. 

# Indlejret systemer
I indlejret systemer har vi lært om b.la. Buck converter. Dette kan bruges senere til at sætte det hele sammen, så vi kan styre hvor meget spænding de individuelle komponenter skal have. Vi har også arbejdet med servomotorer så vi kan ændre på PWM i forhold til funktionalitet af armen samt hvordan den skal styres. 
Vi har haft en gennemgang af forskellige apparater som f.eks. oscilloskop, digitalt multimeter og triple channel power supply, så vi kan teste og afprøve teorier uden at dette nødvendigvis ødelægger noget på roveren. 

# Programmering
I programmering har vi siden sidst fokuseret mere på opsætning af selve koden. Dette har hjulpet med at skabe noget overblik i koden, samt hvordan vi kan forberede ved hjælp af classes så det bliver lettere at tilføje noget til den nuværende kode senere. 
Vi har arbejdet med PWM i kodning og hvordan man "oversætter" dette fra afrekvens til grader, så vi kan sikre at vores servomotorer ikke brænder sammen. 

# Projekt
I projekt har vi primært arbejdet med at 3D printe, så vi kan tilføje komponenter til roveren der er mere specifikke. Vi har indtil videre brugt dette til at printe vores egen arm, en batteriholder og en nummerplade.
Projekt bruges ligeledes som beskrevet i milepælsopgave 1, til at løbende evaluere på vores tidsplan for at se om vores ideer kan blive udført indenfor den tidsfrist der er stillet. 

# Netværk
Netværk har indtil videre ikke været en stor del af rover-projektet. Vi har kort haft om ESP32 og den hvordan vi kan sætte et trådløst interface op, der kan styres fra telefonen eller en computer. Dette kan muligvis senere bruges til nogle funktionaliter på roveren. 

## Udfordringer undervejs
Der har siden vi afleveret milepælsopgave 1, været en række udfordringer. Vi er nu nået så langt i de individuelle fag at der begynder at komme et naturligt overlap. Dette har givet udfordringer i koden, da den skulle tilpasses og sættes op i classes, hvilket har medført at vi skulle ændre på mange af de structs vi havde lavet indtil nu. 

i indlejret systemer begynder der nu at være mange komponenter når vi sætter armen sammen med basen. Dette betyder at de forskellige dele ikke nødvændigvis skal have den samme spænding. Der er blevet brugt mange timer på fumlebræt og med lodning for at finde løsninger der ikke kræver meget plads, men som kan bruges til flere komponenter. 