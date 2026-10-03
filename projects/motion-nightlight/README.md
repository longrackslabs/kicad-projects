# Motion Nightlight

Motion-activated nightlight built into a Nest Protect housing. ESP32 firmware, custom PCB, 3D printed enclosure and diffuser.

## Related files

| What | Where |
|------|-------|
| Design artifacts (DIYLC, FreeCAD, STLs, docs) | `Dropbox/Projects/Nest DIY Nightlight/` |
| Firmware | `~/src/platformio-projects/nest_night_light` |

---

## TODO

### PCB Changes

- [ ] Remote LDR — 2-pin JST header instead of THT so it can be positioned anywhere
- [ ] Right-angle JST on J1 and LED1
- [ ] Populate all MPNs in KiCad — needed for AI design review to catch pinout issues
- [ ] Fix C3 symbol — non-polarized ceramic
- [ ] Fix U2 lib_id — 74HC08 not 74LS08
- [ ] Add 47-100Ω resistor between U1 pin 10 and D1 anode
- [ ] Add Rev B silkscreen marking
- [ ] Fix RV1/RV2 3D model absolute paths

### Power

- [ ] Build single supply pigtail — splits one 5V to both V_LED+ and V_CONTROL on J1

### Enclosure

- [ ] Custom enclosure in FreeCAD — proper LED and LDR positioning
- [ ] Custom diffuser — Nest lens doesn't align with custom LED positions
- [ ] Access holes for RV1/RV2 trim pot adjustment

### Assembly

- [ ] First hot air reflow attempt with SAG-55 and Chipquik paste
- [ ] Build second board using incremental gate plan

### Stretch

- [ ] Replace discrete logic with ATtiny for more flexibility
- [ ] PWM dimming on Q2
- [ ] Battery level indicator
