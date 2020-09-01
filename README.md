# Push-button-LED
The pushbutton is a component that connects two points in a circuit when you press it. The example turns on an LED when you press the button. We connect three wires to the Arduino board. The first goes from one leg of the pushbutton through a pull-up resistor (here 220O ohm) to the 5 volt supply.


int Button = 0;

void setup()
{
  pinMode(9, INPUT);
  pinMode(6, OUTPUT);
}

void loop()
{
  Button = digitalRead(9);
  if (Button == HIGH) {
    digitalWrite(6, HIGH);
  } else {
    digitalWrite(6, LOW);
  }
  delay(10); // Delay a little bit to improve simulation performance
}
