# Montagem Básica com LEDs
## Descrição
O programa faz com que os LEDs conectados aos pinos 4, 5 e 6 acendam de forma sequencial, com cada LED permanecendo aceso por 1 segundo. Após o terceiro LED acender, o ciclo se reinicia, repetindo indefinidamente.

## Materiais Necessários
+ Arduino Uno

+ 3 LEDs

+ 3 resistores de 220Ω (para limitar a corrente dos LEDs)

+ Fios de conexão (jumpers)

+ Protoboard

## Montagem do Circuito


**1.Conecte os LEDs:**

* Conecte o anodo do primeiro LED ao pino digital 4 do Arduino através de um resistor de 220Ω, e o cátodo ao GND.

* Conecte o anodo do segundo LED ao pino digital 5 do Arduino através de um resistor de 220Ω, e o cátodo ao GND.

* Conecte o anodo do terceiro LED ao pino digital 6 do Arduino através de um resistor de 220Ω, e o cátodo ao GND.

**2.Montagem na Protoboard:**


* Utilize a protoboard para organizar as conexões dos LEDs, resistores e fios ao Arduino.

* Os fios de conexão (jumpers) podem ser usados para ligar os pinos do Arduino aos LEDs montados na protoboard.
```
const int ledPin1 = 4;
const int ledPin2 = 5;
const int ledPin3 = 6;

void setup() {
pinMode(ledPin1, OUTPUT);
pinMode(ledPin2, OUTPUT);
pinMode(ledPin3, OUTPUT);
}

void loop() {
digitalWrite(ledPin1, HIGH);
delay(1000);
digitalWrite(ledPin1, LOW);


digitalWrite(ledPin2, HIGH);
delay(1000);
digitalWrite(ledPin2, LOW);


digitalWrite(ledPin3, HIGH);
delay(1000);
digitalWrite(ledPin3, LOW);
}
```
![Figura](https://github.com/user-attachments/assets/24bc438a-783c-4db5-b29f-fe2760251634)
