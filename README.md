# SCD4x Library

This is a library to interface with the Sensirion SCD4x in Arduino using the I2C protocol.

## Features
- use multiple I2C Busses -> scd4x.begin(Wire1);
- no extra dependencies
- only implements necessary functions
- uses doubles (64bit floating point numbers) for proper accurate data calculations

## Warnings
- not all functions are implemented
- not compatible with other SCD4x arduino libraries
- only tested with the esp32
- under active development

### Setup
```c++
#include "scd4x.h"
scd4x scd4x;
double CO2 = 0, temperature = 0, humidity = 0;


Wire.begin();
scd4x.begin(Wire);
scd4x.startPeriodicMeasurement();
```
### Loop
```c++
while (scd4x.isDataReady() == false) {
	vTaskDelay(50 / portTICK_PERIOD_MS);
}

if (scd4x.readMeasurement(CO2, temperature, humidity) == 0) {
	Serial.printf("%4.0f,%2.1f,%1.0f\n", CO2, temperature, humidity);
}
vTaskDelay(4750 / portTICK_PERIOD_MS);
```

## 🖼️ Schematic
![Schematic](/images/schematic.png)

# License

See [LICENSE](LICENSE).
