# Gypsy

ESP32 + Raspberry Pi dual-target development scaffold.

## Layout

- `firmware/` – ESP32 (ESP-IDF) firmware projects
- `host/` – Raspberry Pi host-side test harnesses
- `drivers/` – portable device logic (shared between targets)
- `tools/` – utilities (I2C/SPI smoke tests, bring-up scripts)
- `docs/` – notes, pinouts, and design docs

## Quick start (ESP32)

1. Install VS Code + Espressif ESP-IDF extension
2. Open `firmware/esp32/app`
3. Build/flash:
   - `idf.py build`
   - `idf.py -p COMx flash monitor`

## Quick start (Pi)

1. `sudo apt install -y build-essential cmake ninja-build`
2. Build:
   - `cd host/pi`
   - `mkdir -p build && cd build`
   - `cmake -G Ninja ..`
   - `ninja`
