## Descrição
O programa Blink é um dos exemplos mais básicos e tradicionais para quem está começando a trabalhar com microcontroladores, como o Arduino. Ele faz com que um LED pisque (ou "blink") repetidamente, ligando e desligando em intervalos regulares. Este exemplo é útil para testar se o ambiente de desenvolvimento e o hardware estão funcionando corretamente.

## Circuito a ser montado
## código
```
void setup() {

pinMode(LED_BUILTIN, OUTPUT);
}


void loop() {
digitalWrite(LED_BUILTIN, HIGH); 
delay(1000); // espera por um segundo
digitalWrite(LED_BUILTIN, LOW); 
delay(1000); // espera por um segundo
}
```




![Figura](https://github.com/user-attachments/assets/e43f4321-18c8-464e-aea4-54e1703bfaae)

## Objetivo
Demonstrar como controlar um pino de saída digital no Arduino para acionar um LED. O código alterna o estado do LED, ligando-o e desligando-o a cada segundo.

## Funcionamento
O código faz o LED embutido (geralmente conectado ao pino 13) ou um LED externo conectado a um pino digital piscar com intervalos de 1 segundo (1000 milissegundos). O ciclo de funcionamento é simples:

1.O LED é ligado.

2.Aguarda-se 1 segundo.

3.O LED é desligado.

4.Aguarda-se mais 1 segundo.

Este ciclo se repete indefinidamente enquanto o programa estiver em execução.

