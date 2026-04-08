Esse sistema possui um LED RGB e três potenciômetros. Cada potenciômetro controla a intensidade de uma cor no LED.
<p align="center">
  <img src="arduino-led-rgb.png" width="50%">
</p>

Código escrito do projeto:

```bash
// C++ code
//
int pote_a2 = 0;

int pote_a3 = 0;

int pote_a4 = 0;

void setup()
{
  pinMode(A2, INPUT);
  pinMode(A3, INPUT);
  pinMode(A4, INPUT);
  pinMode(3, OUTPUT);
  pinMode(5, OUTPUT);
  pinMode(6, OUTPUT);
}

void loop()
{
  pote_a2 = analogRead(A2);
  pote_a3 = analogRead(A3);
  pote_a4 = analogRead(A4);
  analogWrite(3, map(pote_a2, 0, 1023, 0, 255));
  analogWrite(5, map(pote_a3, 0, 1023, 0, 255));
  analogWrite(6, map(pote_a4, 0, 1023, 0, 255));
  delay(10); // Delay a little bit to improve simulation performance
}
```
Código em blocos:
<p align="center">
<img width="524" height="459" alt="image" src="https://github.com/user-attachments/assets/e1659c38-a768-40fb-9711-7ec2b2c9f14e" />
</p>

O potenciômetro ligado na porta A2 controla a intensidade de vermelho no LED.
O potenciômetro ligado na porta A3 controla a intensidade de azul no LED.
O potenciômetro ligado na porta A4 controla a intensidade de verde no LED.


