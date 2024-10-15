# Montagem Básica com LEDs
## Descrição
Este projeto demonstra uma montagem básica utilizando um Arduino Uno e dois LEDs. O objetivo é aprender como controlar LEDs através do Arduino, ligando e desligando-os de forma sequencial simulando luzes de sinalizaçao de garagem.

## Materiais Necessários
+ Arduino Uno

+ 2 LEDs

+ 2 Resistores de 220Ω (para limitar a corrente dos LEDs)

+ Fios de conexão (jumpers)

+ Protoboard

## Montagem do Circuito

**1.Conecte os LEDs:**

+ O primeiro LED deve ter o anodo (terminal positivo) conectado ao pino digital 2 do Arduino, e o cátodo (terminal negativo) conectado a um resistor de 220Ω.

+ O segundo LED deve ter o anodo conectado ao pino digital 3 do Arduino, e o cátodo conectado a outro resistor de 220Ω.

+ Os outros terminais dos resistores devem ser conectados ao GND no Arduino.

**2.Conexões com a Protoboard:**

+ Use a protoboard para facilitar as conexões entre os LEDs, resistores e o Arduino.


Utilize os fios de conexão (jumpers) para ligar os pinos do Arduino aos componentes montados na protoboard.

```
// Define os pinos dos LEDs
const int ledPin1 = 13;
const int ledPin2 = 9;

// Intervalo de tempo (em milissegundos) para piscar os LEDs
const int interval = 500;

void setup() {
// Inicializa a comunicação serial
Serial.begin(9600);

// Define os pinos dos LEDs como saída
pinMode(ledPin1, OUTPUT);
pinMode(ledPin2, OUTPUT);

// Exibe os pinos dos LEDs na porta serial
Serial.print("LED 1 está conectado ao pino ");
Serial.println(ledPin1);
Serial.print("LED 2 está conectado ao pino ");
Serial.println(ledPin2);
}

void loop() {
    // Acende o LED 1 e apaga o LED 2
       digitalWrite(ledPin1, HIGH); 
       digitalWrite(ledPin2, LOW);
        Serial.println("LED 1 aceso, LED 2 apagado");
    // Espera pelo intervalo
       delay(interval);
    // Apaga o LED 1 e acende o LED 2
       digitalWrite(ledPin1, LOW);
       digitalWrite(ledPin2, HIGH);
       Serial.println("LED 1 apagado, LED 2 aceso");
    // Espera pelo intervalo
       delay(interval);
  }
```

+ ![Figura](https://github.com/user-attachments/assets/faa4167d-cc3b-4587-bd64-24a5f8646cf4)
