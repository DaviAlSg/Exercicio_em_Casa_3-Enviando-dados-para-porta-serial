# Exercicio_em_Casa_3-Enviando-dados-para-porta-serial
-
-
# Arduino feito no Tinkercad
![image](https://github.com/user-attachments/assets/47eae7e9-22ea-42b0-b326-15d0d9faf104)
-
-Para montar o circuito, conecte o botão na protoboard, ligando uma de suas extremidades ao 5V e a outra ao pino digital D2 do Arduino, além de um resistor de 10kΩ que vai ao GND para funcionar como um pull-down.
Em seguida, posicione o LED, conectando o anodo (perna positiva) à porta digital D13 e o catodo (perna negativa) a um resistor de 220Ω, que vai ao GND.
Por fim, conecte os pinos de 5V e GND do Arduino à protoboard para alimentar o circuito. Quando o botão for pressionado, o Arduino poderá controlar o LED com base no estado do botão.
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
