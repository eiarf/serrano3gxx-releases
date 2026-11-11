# LineageOS 21.0 (Android 14 Go) for Samsung Galaxy S4 Mini 3G (`serrano3gxx`)

Unofficial, experimental port of **LineageOS 21.0 (Android 14 Go Edition)** based on Linux kernel 3.4 for the **Samsung Galaxy S4 Mini 3G (GT-I9190 / `serrano3gxx`)**.

> [!NOTE]
> **AI / LLM Development Disclosure**:
> This porting project, device tree adaptations, userspace shim fixes, and kernel debugging were researched, engineered, and diagnosed in close collaboration with an **AI / Large Language Model (Google Antigravity / DeepMind)** paired with the maintainer.

---

## 📱 Device Specifications

| Feature | Specification |
| :--- | :--- |
| **Model** | Samsung Galaxy S4 Mini 3G (GT-I9190) |
| **Codename** | `serrano3gxx` / `serrano3g` |
| **Chipset** | Qualcomm MSM8230 Snapdragon 400 (Dual-core Krait 1.7 GHz) |
| **GPU** | Adreno 305 |
| **RAM** | 1.5 GB |
| **Kernel** | Linux 3.4.113 |
| **OS** | Android 14 (LineageOS 21.0 Go Edition) |

---

## ⚡ Current Status

* **Boot & System**: Working (Android 14 Go launcher and core services responsive).
* **Display & Graphics**: Working (Software fallback / Adreno 305 GLES threaded renderengine).
* **Touchscreen & Keys**: Working (Atmel mXT / Synaptics touch and touchkeys).
* **Audio & Loudspeaker**: **Working** (WCD9306 differential Line Out into hardware speaker amplifier gated via PM8917 PMIC GPIO 14 / GPIO 165 with `CONFIG_EXT_SPK_AMP=y`).
* **Camera**: **Working** (HALv1 legacy camera stack with defensive bounds checking and memory isolation in `CameraWrapper.cpp`).
* **Telephony & RIL**: **Working** (Samsung Qualcomm RIL daemon using `libsec-ril.so` via `vendor.rild.libpath`).
* **Wi-Fi & Wireless ADB**: Working.

---

## 📦 Releases & Downloads

Pre-built flashable ROM `.zip` packages will be published in the [Releases](../../releases) tab.

### Installation Instructions
1. Ensure your device is GT-I9190 (`serrano3gxx`).
2. Boot into custom recovery (TWRP recommended).
3. Back up all important data.
4. Wipe `System`, `Data`, `Cache`, and `Dalvik / ART Cache`.
5. Flash the ROM zip file.
6. Reboot to system.

---

## 🙏 Credits & Acknowledgments

This project stands on the shoulders of the open-source community:

* **LineageOS Project** & upstream CyanogenMod maintainers:
  * For the Android 14 base and foundational platform code.
* **[Sherif Mo Shalaby (@SherifMoShalaby)](https://github.com/SherifMoShalaby)**:
  * For the inspiring work on the `LineageOS-UL` 21.0 bringup for Samsung MSM8930 platforms (`melius` / Galaxy Mega 6.3).
* **arco68 & Simon (sombree)**:
  * For the original Serrano kernel and device tree development.
* **Google Antigravity AI**:
  * For pairing on kernel driver debugging, HALv1 memory-safe wrapping, logcat telemetry analysis, and single-module build pipelines.

---

## ⚖️ Disclaimer

```text
This software is provided "as is", without warranty of any kind, express or implied.
Use at your own risk. The authors and contributors are not responsible for bricked devices,
dead SD cards, or any other damages resulting from flashing this software.
```
