# 🗓️ {{DATE}} – Vaisala Sensor Log

## 🧪 Sensor Info
- **Device**: Temp & RH% Transmitter
- **Model**: {{e.g., HMD60Y, HMT120}}
- **Channels**: {{e.g., 2 – T + RH}}
- **System Location**: {{e.g., Cleanroom Monitoring Island}}

## ⚠️ Reported Issue
- Transmitter blinks **3 times** on shutdown
- Suspected: {{Wrong polarity? Short circuit? Internal fault?}}

## 🛠️ Actions Taken
- [x] Power-off and visual inspection
- [x] Suspected fault not confirmed due to shared supply
- [x] Swapped sensor with new Vaisala model: {{Model}}
- [ ] Wiring completed
- [ ] SCADA / signal mapping update pending

## 🔍 Risk Notes
- System connected to shared 24 V island — short could affect:
  - [ ] Other transmitters
  - [ ] Fuse
  - [ ] Central power unit

## 🔄 Next Steps
- [ ] Observe wiring procedure with senior tech
- [ ] Review model compatibility
- [ ] Check output (e.g., 4–20 mA, voltage, digital)
- [ ] Confirm scaling in SCADA

## 🧠 Notes
- Documented model difference: {{Input/output, pinout, config file}}
- Risk mitigation: Used identical voltage range
- Recommended: Add procedure for sensor swap in SOP
