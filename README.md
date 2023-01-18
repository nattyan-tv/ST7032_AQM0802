# ST7032_AQM0802
forked by `ST7032_asukiaaa`

# Usage

Include `ST7032_AQM0802.h`.

## Examle

```c
#include <ST7032_AQM0802.h>

ST7032_AQM0802 lcd;

void setup() {
  lcd.begin();
  // If lcd become black, reduced value for contrast
  // Default value is 30.
  lcd.print("TIME:");
}

void loop() {
  lcd.setCursor(0, 1);
  lcd.print(millis()/1000);
}
```

See [examples](./examples) to know other usage.

# License
MIT

# References
- [asukiaaa/ST7032_asukiaaa](https://github.com/asukiaaa/ST7032_asukiaaa)
