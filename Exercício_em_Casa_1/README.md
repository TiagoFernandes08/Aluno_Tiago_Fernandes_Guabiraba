# Ligar e desligar o LED com o botão.


## Descrição


Este projeto demonstra como controlar um LED usando um botão conectado a um Arduino. Ao pressionar o botão, o LED integrado no pino 13 da placa Arduino será ligado. A configuração utiliza um resistor pull-up de 10 kΩ para garantir que a entrada digital seja lida corretamente pelo Arduino.

## Funcionamento


+ **Botão não pressionado**: Quando o botão não está pressionado, o pino 2 da placa Arduino é conectado à terra através do resistor pull-up, fazendo com que a entrada seja LOW (0V). O LED permanece desligado.
+ **Botão pressionado**: Quando o botão é pressionado, a entrada digital se torna HIGH (5V), e o LED é ligado.


Além disso, é possível inverter o circuito, utilizando um resistor pull-down para manter a entrada HIGH por padrão e torná-la LOW quando o botão é pressionado, invertendo assim o comportamento do LED.

## Materiais Necessários
+ Arduino Uno
+ 1 Botão de pressão
+ 1 Resistor de 10 kΩ (pull-up)
+ Fios de conexão (jumpers)
+ Protoboard
## Diagrama de Montagem

```
const int buttonPin = 2;
const int ledPin = 13 ;

int buttonState = 0;

void setup() {
 
 pinMode(ledPin, OUTPUT);

 pinMode(buttonPin, INPUT);
}

void loop() {
buttonState = digitalRead(buttonPin);


if (buttonState == HIGH) {
 digitalWrite(ledPin, HIGH) ;
} else {
  digitalWrite(ledPin,LOW);
}

```

![Figura](https://github.com/user-attachments/assets/97785591-5a9c-4034-b3de-900e08e79e9a)


## Montagem do Circuito
### Conecte o Botão:

+ Conecte um terminal do botão ao pino digital 2 do Arduino.

+ Conecte o outro terminal do botão a uma fonte de 5V.

+ Conecte um resistor de 10 kΩ entre o pino 2 e o GND para configurar o resistor pull-up.

### Protoboard e Fios de Conexão:


+ Use a protoboard para montar o circuito e organizar as conexões.
+ Utilize fios de conexão (jumpers) para ligar os componentes ao Arduino.
