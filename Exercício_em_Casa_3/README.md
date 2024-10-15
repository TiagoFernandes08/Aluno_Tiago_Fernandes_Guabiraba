# Enviando dados para porta serial
## Descrição
A porta serial pode ser usada para exibir o estatuto das entradas da placa Arduino. Neste Código , ao pressionar o botão liga o LED integrado no pino 13 da placa Arduino.

## Código

```
int pushButton = 2;  

void setup() {
  Serial.begin(9600);  
  pinMode(pushButton, INPUT);  
}

void loop() {
  int buttonState = digitalRead(pushButton); 
  Serial.println(buttonState);  
  delay(500);  
}
```

![Figura](https://github.com/user-attachments/assets/4a681359-1e03-46c8-8603-4fcd3bae2ecf)
