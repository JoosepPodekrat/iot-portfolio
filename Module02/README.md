# Module 2

We are going to show here notes for Task 1, 2, 3, 4, and 5 to prove

## Fading LED
Wiring itself was pretty easy, the code worked 1 for 1 from an example on how PWD works, just had to swap in the correct pin number we wired it to.
```
#include <Arduino.h>
int myFunction(int, int);
#define LED_PIN D8
void setup() {
  pinMode(LED_PIN, OUTPUT);
}
int brightness = 0;
int brightnessChange = 5;
void loop() {
  analogWrite(LED_PIN, brightness);
  brightness = brightness + brightnessChange;
  if (brightness <= 0 || brightness >= 255) {
    brightnessChange = -brightnessChange;
  }
  delay(30);
}
```

## Voltage splitter
Wiring the splitter itself was relatively easy, from our understanding it just gives 2 routes for the electricity to move, and depending on the resistances of the resistors, more or less electrical energy moves along a certain path, with everything else moving to the other path.

```
#include <Arduino.h>

const int analogPin = A0; 
const float R1 = 330;
const float R2 = 330;
const float refVoltage = 1.0;
void setup() {
  Serial.begin(9600);
}

void loop() {
  int analogValue = analogRead(analogPin);
  float voltage = (analogValue / 1023.0) * refVoltage; 
  float actualVoltage = voltage * ((R1 + R2) / R2);

  Serial.print("ADC Value: ");
  Serial.print(analogValue);
  Serial.print(" | Voltage: ");
  Serial.print(actualVoltage, 2);
  Serial.println(" V");

  delay(1000);
}
```

## Touch sensor
We wired the touch sensor on the breadboard, ran this code and then got it working. Couldn't figure out what the numbers meant for a while but it's actually which of the pins on the chip was being touched at the time, our fingers were just too big so they were always touching one of the pins while trying to touch the chip we thought was the sensor.
![image](https://github.com/user-attachments/assets/50ad6e7a-049c-42f9-9cda-4c6f640c47b6)
## Bomb defusal
Tried building the bomb defusal circuit, got stuck not knowing how to power the LED strip. Asked both partner and teacher for help, turns out we were missing the charger so couldn't finish building it. I think the rest of the circuit was fine, used the blueprint from the class.
It is [here](https://github.com/partner/iot-portfolio/Module02/Readme.md#task-2).

## Reflection 2
Do in the mornin
[Reflection 2](/Reflections/ref02.md)

## Reflection 3
[Reflection 3](/Reflections/ref03.md)


