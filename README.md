# LaTeX Macropad (RP2040)

This is a custom 15-key macropad with a rotary encoder, built specifically to optimize and speed up writing math formulas in LaTeX. It is powered by a Seeeduino XIAO RP2040 and runs on custom QMK firmware. 

I designed this project to improve my workflow when typing complex equations, combining a standard numpad with powerful, auto-navigating LaTeX macros.

## Features:

- **15 Cherry MX-style keys** in a 4x4 ortholinear matrix.
- **1 Rotary Encoder** (EC11) with a push-button switch.
- **Seeeduino XIAO RP2040** microcontroller for plenty of processing power and memory.
- **Custom QMK Firmware** tailored for LaTeX.
- **Smart Cursor Navigation:** Macros automatically move the cursor inside the brackets after typing a command (e.g., pasting `\frac{}{}` automatically steps back into the first set of brackets).

## CAD Model

The enclosure was custom-designed for this build to hold the PCB, the switches, and the XIAO RP2040 securely. 

<img width="950" height="612" alt="image" src="https://github.com/user-attachments/assets/d0e816e2-e972-458c-8174-80056514a3af" />
<img width="1084" height="662" alt="image" src="https://github.com/user-attachments/assets/52b4d9ba-7463-475c-9404-e1f36fbdb396" />


## PCB & Schematic

The PCB was designed to accommodate the 4x4 matrix layout. It uses standard 1N4148 diodes configured in `COL2ROW` direction.

<img width="485" height="556" alt="image" src="https://github.com/user-attachments/assets/e1842207-0777-43d3-bb2f-18ff0a60b13f" />

<img width="730" height="606" alt="image" src="https://github.com/user-attachments/assets/f0b39f75-fbd8-4a48-8440-c000d1a2b7e7" />

<img width="1233" height="712" alt="image" src="https://github.com/user-attachments/assets/bc042096-03ba-4135-b111-f0d4b1a4fb25" />



*Note: The schematic might show SAMD21 pinouts (D0, D1, etc.) from the footprint library, but the hardware uses the XIAO RP2040, so the firmware is mapped to the exact RP2040 hardware pins (GP26, GP6, etc.).*

## Firmware Overview

This macropad uses QMK Firmware to handle the matrix, the encoder, and the complex macros.

**Keymap Layers:**
- **Base Layer (`_NUMPAD`):** Acts as a standard numpad for quick number entry. Includes a dedicated layer-modifier key.
- **LaTeX Layer (`_LATEX`):** Accessed by holding the modifier key. Contains 14 of the most used LaTeX commands (`\frac{}{}`, `\sqrt{}`, `\sum_{}^{}`, `\int_{}^{}`, etc.).

**Rotary Encoder:**
- **Rotate Left/Right:** Moves the text cursor left and right (perfect for navigating inside long equations).
- **Press:** Acts as a Left Mouse Button click.

## BOM

Here is everything you need to build this macropad:

- 1x Seeeduino XIAO RP2040
- 15x Cherry MX-style Switches
- 15x Keycaps
- 1x Rotary Encoder
- 1x Encoder Knob
- 15x 1N4148 Diodes
- Custom printed PCB & 3D Printed Case(2 parts)
- Screws (M2.5x10mm SHCS) and heat-set inserts (M2.5x4x3.5)

  <img width="1123" height="675" alt="image" src="https://github.com/user-attachments/assets/024c1a3f-7855-4bb3-b207-ddc52ea885e4" />

