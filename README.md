# Mic
----
### نام ازمایش : جهت یابی با جوی استیک
---
### هدف : جهت یابی درمسیرهای مختلف و نشان دادن ان 
#### ابزار : جوی استیک،اردینو،بردبوردوسیم 
### شرح ازمایش :
استيك را به پين A1 آردوينو متصل مي‌كنيم.

برای تشخیص اینکه دسته جوی استیک فشرده شده است یا نه، پين SW جوي استيك را به پين ديجيتال D8 آردوينو متصل مي‌كنيم. علاوه بر این، براي تغذيه ماژول جوي استيك، پين VCC و GND آن را به ترتيب به ترمينال 5 ولت و زمين آردوينو متصل مي‌ نماييم



```cpp

  const int SW_pin = 8; // digital pin connected to switch output
const int X_pin = 0; // analog pin connected to X output
const int Y_pin = 1; // analog pin connected to Y output
 
void setup() {
  pinMode(SW_pin, INPUT);
  digitalWrite(SW_pin, HIGH);
  Serial.begin(9600);
}
 
void loop() {
  Serial.print("Switch:  ");
  Serial.print(digitalRead(SW_pin));
  Serial.print(" | ");
  Serial.print("X-axis: ");
  Serial.print(analogRead(X_pin));
  Serial.print(" | ");
  Serial.print("Y-axis: ");
  Serial.print(analogRead(Y_pin));
  Serial.println(" | ");
  delay(200);
}
```
 
