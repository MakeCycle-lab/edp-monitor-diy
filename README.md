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
> eDP *is* DisplayPort. Whether a given source can drive a given panel depends on the link negotiation between them — specifically whether the source accepts the panel's **EDID** (including EDID forwarded through a converter chip). The adapters listed above exist because devices like iPads use a **non-standard panel connector** — they solve the connector problem, not source compatibility.

## 📱 iPad Adapter Compatibility

See [`adapters/readme.md`](adapters/readme.md) for the full model table (iPad 3/4, Air, mini, Pro — most models share the same panel hardware across Wi-Fi/Cellular variants).
