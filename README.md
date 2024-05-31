# Arduino-IR_Sensor ![arduinoThumb](https://github.com/ICAREMAKER/Arduino-IR_Sensor/assets/107696317/f8b31aa9-3747-432c-bea6-bcdc31f9c2c8) ![C++-Logo wine](https://github.com/ICAREMAKER/Arduino-IR_Sensor/assets/107696317/738f3b9a-94b0-45e7-99e6-5a4880131bd2)

## Preview
![Line-Following-Robot](https://github.com/ICAREMAKER/Arduino-IR_Sensor/assets/107696317/f18775b7-7a0d-43e3-9724-44e8b01d98b5)

## Code
```C
void setup() {
    pinMode(A0, INPUT); // Entrée analogique du capteur gauche sur A0
    pinMode(A1, INPUT); // Entrée analogique du capteur droit sur A1

}

void loop() {

  int GAUCHE_IR = digitalRead(A0);
  int DROITE_IR = digitalRead(A1);

if(DROITE_IR==0 && GAUCHE_IR==0) {
    AVANCE(); 
}

  else if(DROITE_IR==0 && GAUCHE_IR==1) {
    DROITE(); 
 }

  else if(DROITE_IR==1 && GAUCHE_IR==0) {
    GAUCHE(); 
}

  else if(DROITE_IR==1 && GAUCHE_IR==1) {
    STOP();  
 }
}
```




