# Exercicio_em_Casa_3-Enviando-dados-para-porta-serial
-
-
# Arduino feito no Tinkercad
![image](https://github.com/user-attachments/assets/47eae7e9-22ea-42b0-b326-15d0d9faf104)
-
-Conecte um botão entre o pino de 5V e o pino digital D2 do Arduino, com um resistor de 10kΩ ao GND. O ânodo de um LED deve ser ligado ao pino D12, e o cátodo a um resistor de 220Ω, que se conecta ao GND.
Este circuito permite enviar dados à porta serial do Arduino, utilizando o botão como sinalizador e o LED como indicador visual. Ao pressionar o botão, o Arduino registra a ação e transmite informações pela porta serial.
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
