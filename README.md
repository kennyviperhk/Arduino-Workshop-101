# CFSS-Arduino-Workshop-101

## p5 Example

- [p5.serialcontrol App](https://github.com/p5-serial/p5.serialcontrol/releases/download/0.0.7/p5.serialcontrol-win32-x64.zip)

- p5 Serial Arduino Code:
```
void setup() {
 Serial.begin(9600); // initialize serial communications
}

void loop() {
 int potentiometer = analogRead(A0);                  // read the input pin
 int mappedPot = map(potentiometer, 0, 1023, 0, 255); // remap the pot value to fit in 1 byte
 Serial.write(mappedPot);                             // print it out the serial port
 delay(1);                                            // slight delay to stabilize the ADC
}
```

- [p5 Serial Communication Example](https://editor.p5js.org/kennyviperhk/sketches/H136aX7b4)
