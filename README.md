# AL117-99 Beacon Firmware

This firmware is for the **ESP32 DevKit V4.1** and connects to analog radios via a 3.5mm TRRS cable.

It turns your ESP32 + walkie-talkie into a **smart APRS audio relay node** that:
- **Listens for incoming APRS AFSK1200 audio**
- **Forwards only packets containing `w1-1`**
- **Beacon every 45–60 minutes** with rotating custom messages
- **No LoRa or internet required**
- **GPIO PTT control** (not VOX)

---

## Technical Specs

- **Platform:** ESP32 DevKit (V4.1 or similar)
- **TX Audio (DAC):** GPIO 25
- **RX Audio (ADC):** GPIO 34
- **PTT Control:** GPIO 14 (active LOW)
- **AFSK 1200 Baud** modem logic
- **Beacon messages rotate hourly**

---

## Sample Beacon Messages

```
Hello from AL117-99
AL117-99 is everywhere and watching
AL117-99 just got DOWN!
Overwatch active. Node AL117-99
You can't outrun AL117-99
```

---

## Flashing Instructions

1. Use [https://web.esphome.io](https://web.esphome.io) or `esptool.py` to flash the `.bin` file to your ESP32.
2. Connect TRRS cable to your radio (mic/speaker + PTT)
3. Power it up and monitor APRS frequency for beacons or responses.

---

## License

MIT — free to use, modify, and remix.
