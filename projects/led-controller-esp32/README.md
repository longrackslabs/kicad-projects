# LED Controller ESP32

General-purpose ESP32-based LED controller PCB.  
Compatible with **WLED**, **ESPHome (NeoPixelBus RMT)**, or **FastLED/Arduino**.  
Designed to drive 5 V addressable LEDs (WS2812B, SK6812, etc.).

---

## Project structure# LED Controller ESP32

General-purpose ESP32-based LED controller PCB.  
Compatible with **WLED**, **ESPHome (NeoPixelBus RMT)**, and **FastLED/Arduino**.  
Designed for 5 V addressable LEDs (WS2812B, SK6812, etc.).

## Project structure
led-controller-esp32/  
  led-controller-esp32.kicad_pro ← open this  
  led-controller-esp32.kicad_sch  
  led-controller-esp32.kicad_pcb  
  sym-lib-table (project-specific symbols)  
  fp-lib-table (project-specific footprints)  
  docs/  
  fabrication/ (gerbers/BOM/PNP; ignored by git)

## Libraries
- Project uses **relative paths** so it’s portable.
- Shared repos paths:
  - ../../libs/ → custom symbols & footprints
  - ../../step/ → 3D models

## How to open
1) Open `led-controller-esp32.kicad_pro` in KiCad.  
2) Edit schematic or PCB as usual.  
3) Generate fab outputs into `fabrication/` when ready to manufacture.

## Firmware options
- WLED (set LED pin to your chosen GPIO, e.g., 5)  
- ESPHome (NeoPixelBus, method: esp32_rmt)  
- FastLED (e.g., `#define DATA_PIN 5`)

## Notes / best practices
- Common ground between ESP32 and LED power.  
- 330 Ω series resistor on DATA; ≥1000 µF across 5 V/GND at LED input.  
- Avoid ESP32 boot-strap pins (0/2/12/15) for LED data.
