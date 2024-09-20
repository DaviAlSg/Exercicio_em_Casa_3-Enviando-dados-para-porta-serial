# Exercicio em Casa 3 Enviando dados para porta serial
-
-
# Arduino feito no Tinkercad
![image](https://github.com/user-attachments/assets/2504bd33-9fef-47c8-a0f3-d046ff47abdf)

-
-Conecte um botão entre o pino de 5V e o pino digital D2 do Arduino, com um resistor de 10kΩ ao GND.
Este circuito permite enviar dados à porta serial do Arduino, utilizando o botão como sinalizador. Ao pressionar o botão,
o Arduino registra a ação e transmite informações pela porta serial.
-
# Materiais
1 Fio de 10 k ohm,
1 Fio de 220 ohm,
1 Led,
1 Protobord,
1 Botão.

# Código
int pushButton = 2;

void setup() {
  Serial.begin(9600);
  pinMode(pushButton, INPUT);
}

void loop() {
  int buttonState = digitalRead(pushButton);
  Serial.println(buttonState);
  delay(100);
}
