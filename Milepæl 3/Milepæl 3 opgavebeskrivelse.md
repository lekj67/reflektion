## Opgave 3 - Joystick og fjernstyring - Milepælsopgave

## Hvad lærte jeg i fagene?
### Programmering 

### elektronik

### projekt 


### Komponentliste
2x joystick 
1x pcb board
2x SMD capacitor
2x SMD resistor 
1x liligo T-display
6x jumper wires
2x Knapper


### Beskrivelse af joystick samt fjernstyring
Basen af joysticket er et PCB som er konstruet sådan at der kan være et joystick i venstre side og et joystick i venstre side samt et styk SMD kapacitor og et styk SMD resistor for at fjerne elektrisk støv.Der er på PCB'en lavet sådan at vi kan lodde vores liligo fast og bruge den til at sende koden. Koden er opbygget med en reciever kode som er den ESP-32 der sidder på vores rover, den er sat til at modtage data som vi bruger til at styre de forskellige funktioner vores rover har. Koden er opbygget i tasks for at kan maximere processor kraften på vores ESP-32 og så gør det at koden er mere responsive og at vi kan styre forskellige funktioner ved at skifte task, og ikke vente på koden er kommet til det punkt.Den anden del af koden er vores sender kode som vi bruger til at sende info fra vores joystick til vores ESP-32. Infoen der bliver sendt er aflæsninger fra joystickkene som vi bruger til at kontrollere både køre funktioner og arm funktioner, der bliver også sendt information om de 4 knapper som der sidder på PCB'en, der er 2 integrerede knapper i joysticket og 2 knapper vi selv har monteret som alle 4 bliver brugt til at skifte mellem forskellige funktioner på roveren. 


# 
Vi har haft nogen udfordringer med at få vores rover til at styre armen smooth sådan at den ikke hakker rundt i de positioner vi gerne vil have den skal køre over i, samt udfordringer med at få integreret knapperne da vores styring af knap værdierne ikke har været som det skulle så at i starten skiftede de kun fra true til false når vi holdte knappen inde. 

#
jeg er personligt ret stolt af at vores rover nu kan styres 100% trådløst og køre helt efter planen, samt at vi nu kan skifte mellem at styre armen og at den skal køre. 