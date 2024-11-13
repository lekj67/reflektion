## Styring af roverarm og servoer

---

## PWM recap


---

## Duty cycle rent matematisk

- Time On, $T_{on}$ , er tiden signalet er **on** eller 1 (altså pulsbredden)
- Time Off, $T_{off}$, er tiden signalet er **off** eller 0.
- Total cycle time, $T_{cycle}$, er summen af  $T_{on}$  og  $T_{off}$ 
$$ DutyCycle = \frac{T_{on}}{T_{on}+{T_off}} \times 100 \%  $$
---
## Periode

Indikerer tiden (typisk i miliseekunder) for hver del af cyklen. 
Indicates the amount of time (usually in milliseconds) for each part of the cycle. 

"Cycle time" er så den totale periode for PWM, eller $T_{on}+T_{off}$.

Frekvensen er så det inverse af perioden:
$$Frequency = \frac{1}{Period}$$
---
## Periode eksempel

Et PWM signal med total cycle time på 20ms har en frekvens på 50hz. Altså fuldfører signalet 50 komplette cykler hvert sekund.

---
## PWM og servoers rotation

* Servoer roterer mellem 0 - 180 grader (sjældent 360)
* Én puls bestemmer rotation
* Pulser af den samme bredde skal sendes hele tiden for at den bliver i positionen

---

## Længere forklaring på rotation

> *Most servos fixedly rotate between 0° and 180° - starting and ending at fixed points relative to the motor. They accept pulses within a fixed range commonly between 500 and 2500us. To put it all together, say we send a 500us width pulse to a servo accepting pulses between 500us and 2500us. The servo will rotate its arm to the 0° position in response - no matter which position the arm was in before. It will respond with appropriate increments when the pulse width is increased up until 2500us, then it will stop moving.*

---

## Visualisering af pulsbredder og servos rotation (givent 1ms - 2ms pulsbredde)

![[Vault attachments/Pasted image 20241105163505.png]]

---
## Animation af servos roation og pulsbredde

![](https://cdn.getmidnight.com/84f7b02a8128f5f5775611244c24b941/2023/02/ServoGif.gif)

---

## Pins og anbefalet spændingsniveau samt frekvens

![[Vault attachments/Pasted image 20241106145340.png]]

---
## Øvelse 0: Start servo


* Tilføj følgende bibliotek til jeres Platform.io-projekt: ESP32Servo https://registry.platformio.org/libraries/madhephaestus/ESP32Servo 
* Kobl op som sidste slide anviser.
* Brug bibliotekets eksempler eller følgende 2 slides til at prøve at én servo kan dreje.
---

## Minimal PWM Servo kode - Setup

```cpp
#include <ESP32Servo.h> 
Servo servo;
int pos = 0; // Til at gemme position
int servoPin = 17;
void setup() { 
	// Allow allocation of all timers 
	ESP32PWM::allocateTimer(0); 
	ESP32PWM::allocateTimer(1); 
	ESP32PWM::allocateTimer(2); 
	ESP32PWM::allocateTimer(3); 
	servo.setPeriodHertz(50); // standard 50 hz servo 
	servo.attach(servoPin, 1000, 2000); // 1ms - 2ms pulse width
```

---
## Minimal PWM Servo kode - Loop

```cpp
void loop() { 
	for (pos = 0; pos <= 180; pos += 1) {
	// goes from 0 degrees to 180 degrees in steps of 1 degree 
		myservo.write(pos); // tell servo to go to position in variable 'pos' 
		delay(15); // waits 15ms for the servo to reach the position 
		}
	for (pos = 180; pos >= 0; pos -= 1) { // goes from 180 degrees to 0 degrees
		myservo.write(pos); // tell servo to go to position in variable 'pos' 
		delay(15); // waits 15ms for the servo to reach the position 
		} 
}
```

---
## Øvelse 1: Find pulsbredde minimum og maks for jeres servoer

* Der kan være en margen i hvor stor en rækkevidde af pulsbredder jeres servomotorer kan bruge af.
* Ved at eksperimentere med pulsbredder, lad os sige start på 1.2 ms til 1.8 ms, se hvor de roterer hen.
* Prøv at udvide rækkevidden indtil i finder maks pulsbredden jeres servo responderer på.

---
## ESP32Servo library, video

* Anbefalet video at se: https://www.youtube.com/watch?v=qJC1nt_eJZs
* ESP32Servo library https://registry.platformio.org/libraries/madhephaestus/ESP32Servo - lidt flere indstillingsmuligheder end `Servo.h`


---

## Pintabel

| **ESP**    | **Pin Name** | **Description**                |
| ---------- | ------------ | ------------------------------ |
| Gnd        | Gnd          | Ground terminal                |
| VIN        | +5v          | Positive supply terminal       |
| Analog pin | VRx          | Voltage proportional to X axis |
| Analog pin | VRy          | Voltage proportional to Y axis |
| GPIO pin   | SW           | Switch                         |

---

## Forklaring

* Eneste nye er analog pins - kig efter `ADC` i jeres pinout for disse
* Digital er 0 og 1, analog er alle heltal mellem 0 og et maksimum, f.eks. 1023.
* Dette er muligt med en variabel spænding (vekselstrøm), hvor vores ADC pin så måler spændingen, f.eks. 2.43 volt, og oversætter det til et heltal.

---
## Minimalt kodeeksempel:

```cpp
const int joyXPin = A0; // X-axis of joystick 
const int joyYPin = A1; // Y-axis of joystick 
void loop() { 
	int xValue = analogRead(joyXPin); // Read X-axis value 
	int yValue = analogRead(joyYPin); // Read Y-axis value
	Serial.print(xValue);
	Serial.print(yValue);
}
```

---

## Øvelse 2 - Joystick og målinger

* Idéen er at vi skal kunne styre servo med joystick.
* Først målinger - så kobl til, og prøv det minimale kodeeksempel.
* Se hvornår (ved hvilken vinkel) at joystickmålingerne ændrer værdi

---
## Joystick med map()

```cpp
const int joyXPin = A0; // X-axis of joystick 
const int joyYPin = A1; // Y-axis of joystick 
void loop() { 
	int xValue = analogRead(joyXPin); // Read X-axis value 
	int yValue = analogRead(joyYPin); // Read Y-axis value 
	// Map joystick values from [0,1023] to [0,180] 
	int angle1 = map(xValue, 0, 1023, 0, 180); 
	int angle2 = map(yValue, 0, 1023, 0, 180); 
	// Write mapped values to servos 
	servo1.write(angle1); 
	servo2.write(angle2); 
	delay(15); // Short delay for stability
}
```

---

## Øvelse 3

* `map()` oversætter fra 0 - 1023 (joystick målinger) til 0 - 180 (servopositioner).
* MEN, joystick går ikke lineært fra 0 - 1023. I skal nu "kalibrere" så i kan bevæge positioner som i vil have det med joystick.