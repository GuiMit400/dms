
int Temp = 0;
int celsius = 0;
int vibration = 0;
float voltage = 0;
float electric_current = 0;

void setup() {
  Serial.begin(9600);
  pinMode(A0, INPUT);
  pinMode(A1, INPUT);
  pinMode(A2, INPUT);
}

void loop() {

  Temp = 40;
  celsius = map(((analogRead(A0) - 20) * 3.04), 0, 1023, -40, 125);
  
  voltage = map((analogRead(A2)), 0, 1023, 0, 5);
  voltage = (analogRead(A2) / 1023.0) * 5;
  electric_current = (voltage/2.6);
  
  vibration = map((analogRead(A1)), 0, 1023, 100, 0);
  if (vibration == 0) {
  Serial.print("vibration:||  ");
}
    if (vibration > 0 and vibration<=27) {
  Serial.print("vibration:||||  ");
}
    if (vibration >27) {
  Serial.print("vibration:||||||  ");
}

  Serial.print(celsius);
  Serial.print("C    ");
  Serial.print(voltage);
  Serial.print("V    ");
  Serial.print(electric_current);
  Serial.println("A    ");
  delay(1000);
}
