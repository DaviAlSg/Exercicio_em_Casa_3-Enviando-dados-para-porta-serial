# Exercicio_em_Casa_3-Enviando-dados-para-porta-serial
-
-
# Arduino feito no Tinkercad
![image](https://github.com/user-attachments/assets/47eae7e9-22ea-42b0-b326-15d0d9faf104)

-
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
