# ST7032_AQM0802
forked by `ST7032_asukiaaa`

# Usage

## Hello world
See [HelloWorld](./examples/HelloWorld/HelloWorld.ino).

```c
#include <ST7032_asukiaaa.h>

ST7032_asukiaaa lcd;

void setup() {
  lcd.begin(16, 2); // LCD columns and rows.
  lcd.setContrast(40);
  // If lcd become black, reduced value for contrast
  // lcd.setContrast(10);
  lcd.print("hello, world!");
}

void loop() {
  lcd.setCursor(0, 1);
  lcd.print(millis()/1000);
}
```

## Set slave address
You can specify slave address for a LCD.

```c
ST7032_asukiaaa lcd(0x3E);
```

## Set wire
You can set customized wire.(See [setWire](./examples/setWire/setWire.ino))

```c
#if defined(ESP32)
  Wire.begin(25, 26); // SDA, SCL
  lcd.setWire(&Wire);
#endif
```

See [examples](./examples) to know other usage.

# License
MIT

# References
- [asukiaaa/ST7032_asukiaaa](https://github.com/asukiaaa/ST7032_asukiaaa)
