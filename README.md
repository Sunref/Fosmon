# 👾 Tamagotchi Foston FS-66

Transforming a classic 2006 generic Foston MP3 Player into a pocket-sized virtual pet (Tamagotchi). This is a bare-metal development and reverse engineering project tailored for legacy 8-bit architectures. The objective of this project is to replace the original firmware (or inject a custom binary) of a **Foston FS-66** MP3 Player (Batch: 2006/11), converting its music playback interface into a real-time virtual pet game running directly on the original hardware.

---

## Technical Specifications
* **Device:** Foston FS-66 (2006/11 Batch)
* **Microcontroller (MCU):** Actions Semiconductor **ATJ2085 / ATJ2091**
* **CPU Architecture:** 8-bit Z80 / 24-bit DSP core
* **Display:** Monochromatic OLED (Dual color: Yellow/Blue) - $128 \times 32$ pixels resolution
* **Storage:** Integrated NAND Flash (Typically 512MB / 1GB)

---

## Repository Structure (Planned)

* `/firmware_dumps`: Original firmware dumps extracted for backup and reverse engineering.
* `/tools`: Scripts for extraction, disassembly, and injection via USB (ADFU Mode).
* `/src`: C source code (targeted for the SDCC compiler) and Z80 Assembly.
* `/assets`: Virtual pet sprites converted into byte arrays (`16x16` bitmaps).

---

## Toolchain & Environment (Linux/Debian)

* **Compiler:** `SDCC` (Small Device C Compiler) configured for the Z80 architecture.
* **Reverse Engineering:** `Ghidra` or `IDA Pro` for binary analysis.
* **USB Communication:** `lsusb` and open-source utilities to interact with the device in ADFU (Actions Device Firmware Update) mode.

---

## Control Mapping (Proposed)
Due to the FS-66's minimal physical layout, the Tamagotchi controls have been streamlined:
* **Next Button:** Navigate through menu options (Feed, Status, Clean).
* **Prev Button:** Confirm / Execute the selected action.
* **Menu Button:** Open the pet's status screen (Age, Hunger, Happiness).
