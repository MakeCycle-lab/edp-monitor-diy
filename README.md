# eDP Monitor DIY

Everything you need to bring an **eDP panel** back to life — driver boards + device adapters.

All iPad screens are eDP panels (directly compatible with a DisplayPort signal), so this repository also covers turning salvaged iPad screens into external monitors.

## 🧩 How It Works

Modular design, three parts:

| Part | Role | Where |
| :--- | :--- | :--- |
| **Mainboard** | The reusable driver board (video in → eDP out) | This repo, top level |
| **Device Adapter** | The private connector part for a specific device | [`adapters/`](adapters/) |
| **Touch Controller** | Optional, shared across all mainboards | [touch-controllers](https://github.com/MakeCycle-lab/touch-controllers) repo |

**Assembly**: pick your device → find its adapter in [`adapters/`](adapters/) → the adapter's readme tells you which mainboard to use → download production files from the linked Release.

## 🖥️ Mainboard Matrix

| Mainboard | Input → Output | Panel Connection | Status |
| :--- | :--- | :--- | :--- |
| **[dptoipad-lite](dptoipad-lite/)** | DP → eDP (direct) | Any eDP panel via 40-pin FPC adapter (ready-made adapters for salvaged iPad screens) | ✅ Released |
| **dptoipad-pro** | DP → eDP (direct) | Any eDP panel via 40-pin FPC adapter | 📄 Docs pending |
| **NCS8803** | HDMI → eDP | generic eDP panels | 🚧 Planned |
| **CS5801** | HDMI → eDP | generic eDP panels | 🚧 Planned |
| **LDR6023** | USB-C → eDP | generic eDP panels | 🚧 Planned |
| **PD-MCU board** | USB-C → eDP | generic eDP panels | 🚧 Planned |

> **ℹ️ Whether a panel lights up is decided by the source ↔ panel handshake, not by this table.**
> eDP *is* DisplayPort. The mainboards are transparent bridges and add **no** restrictions on the video source. If your source device (PC GPU, laptop, SBC…) can output the panel's native resolution and timing over DP, it will work directly — many GPUs drive an eDP panel out of the box once the driver is installed, while some sources need the correct resolution/timing configured. The adapters listed above exist because devices like iPads use a **non-standard panel connector** — they solve the connector problem, and are not a whitelist of supported sources.

## 📱 iPad Adapter Compatibility

See [`adapters/readme.md`](adapters/readme.md) for the full model table (iPad 3/4, Air, mini, Pro — most models share the same panel hardware across Wi-Fi/Cellular variants).
