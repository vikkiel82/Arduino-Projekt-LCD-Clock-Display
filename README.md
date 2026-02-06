# Arduino LCD Clock & Thermometer

Dieses Projekt zeigt Datum, Uhrzeit und Temperatur auf einem LCD1602 Display an. [cite_start]Die Zeit wird über ein DS3231 RTC-Modul gehalten und kann über den Seriellen Monitor eingestellt werden[cite: 12, 318].

## Hardware Material
[cite_start]Liste basierend auf der Dokumentation[cite: 19]:
* 1x Arduino Uno (Rev3)
* 1x DS3231 RTC Modul
* 1x LCD1602 Display
* 1x 10kΩ Potentiometer (für LCD Kontrast)
* 1x 220 Ohm Resistor
* Breadboard und Jumper-Kabel

## Bibliotheken
[cite_start]Folgende Bibliotheken müssen in der Arduino IDE installiert sein[cite: 101, 102, 103]:
* `DS3231.h`
* `Wire.h`
* `LiquidCrystal.h`

## Verkabelung (Pinout)

### [cite_start]LCD1602 Verbindungen [cite: 65-81]
| LCD Pin | Arduino Pin / Power |
|:-------:|:-------------------:|
| VSS     | GND                 |
| VDD     | +5V                 |
| VO      | Potentiometer Output|
| RS      | D12                 |
| RW      | GND                 |
| E       | D11                 |
| D4      | D5                  |
| D5      | D4                  |
| D6      | D3                  |
| D7      | D2                  |
| A       | 220Ω -> +5V         |
| K       | GND                 |

### [cite_start]DS3231 Verbindungen [cite: 82-92]
| DS3231 Pin | Arduino Pin |
|:----------:|:-----------:|
| SCL        | A5          |
| SDA        | A4          |
| VCC        | +5V         |
| GND        | GND         |

## Zeit einstellen
Öffne den Seriellen Monitor (9600 Baud) und sende das Format:
`Jahr Monat Tag Wochentag Stunde Minute Sekunde`
[cite_start]Beispiel: `16 5 20 3 0 33 30` [cite: 134]
