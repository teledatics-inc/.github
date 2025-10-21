# Teledatics Incorporated

Ultra‑long‑range, low‑power **Wi‑Fi HaLow™ (IEEE 802.11ah)** modules, dev kits, drivers, and open tooling for connecting intelligent systems—drones & rovers, ag‑tech, industrial control, off‑grid comms, and more.

---
![World Record Link](profile/images/WiFi_Halow_Record_2024_Mount_Greylock_Peak.jpg)

## World Record Wi-FI HaLow Link
- **Mount Greylock to Mount Wachusett in Massacusetts, USA**
- **106 kilometer / 66 mile link**
- - **White Paper** → https://github.com/teledatics-inc/.github/tree/main/profile/docs/Teledatics_WiFi_HaLow_Distance_Record_White_Paper_July2024.pdf
-  **Teledatics 1W HaloMax 902-928 MHz module**

---

## What we build

- **Modules & Dev Kits**
  - **HaloMax™**: high‑power Wi‑Fi HaLow module and M.2 card (NRC7394‑based), plus the **TD‑WRLS** development platform.
  - **TD‑XPAH**: open‑hardware, open‑source 802.11ah experimenter board (NRC7292‑based).

- **Drivers, SDKs & Packaging**
  - Linux **FTDI‑SPI** kernel driver for USB‑to‑SPI control paths.
  - **Newracom** host‑mode and standalone SDK packages, plus DKMS packaging for quick Raspberry Pi and Linux installs.

- **Open Hardware & Example Apps**
  - Open daughterboards (“hATs”) for gateway, Ethernet, sensors, GPS, battery/solar.
  - Example projects for **mobile HaLow hotspots**, **AI drone & rover control**, and more.

---

## Quick links

- **Docs** → https://teledatics.com/docs  
- **GitHub org** → https://github.com/teledatics  
- **TD‑XPAH (open HW)** → https://github.com/teledatics/TD-XPAH  
- **FTDI‑SPI Linux driver** → https://github.com/teledatics/ftdi-spi-linux  
- **Newracom NRC7292 host pkg (fork)** → https://github.com/teledatics/nrc7292_sw_pkg  
- **Newracom NRC7292 standalone SDK (fork)** → https://github.com/teledatics/nrc7292_sdk  
- **DKMS packaging** → https://github.com/teledatics/nrc-dkms  
- **Mobile HaloMax™ hotspot (how‑to)** → https://github.com/teledatics/mobile_halomax_hotspot  
- **TD‑WRLS daughterboards (open HW)** → https://github.com/teledatics/TD-WRLS_Hats  
- **AI drone & rover control** → https://github.com/teledatics/ai-drone-control  

> Community: Join the Teledatics [Discord Server](https://discord.gg/WpguKNMR7H) (linked from product pages) to ask questions, collaborate, and share field results.

---

## Choose your path

### 1) HaloMax™ / TD‑WRLS (NRC7394)

**Use cases**: high‑power, extreme‑range HaLow links; M.2 “Key‑E” cards; mobile hotspots; Raspberry Pi 4/5 and Radxa Rock 5A devkits.

**Fast start**
1. Set up a Raspberry Pi 4/5 (64‑bit OS recommended).
2. Install HaLow host‑mode SW for NRC7394 (see Newracom `nrc7394_sw_pkg`) and the Teledatics FTDI‑SPI driver if you’re using a USB‑SPI control path.
3. Try the **mobile hotspot** example:
   - Repo: https://github.com/teledatics/mobile_halomax_hotspot  
   - Build the portable hotspot and verify AP/STA or mesh connectivity.
4. Explore open daughterboards for Ethernet, Wi‑Fi, GPS/RTK, battery/solar, and sensors:
   - https://github.com/teledatics/TD-WRLS_Hats

### 2) TD‑XPAH (NRC7292)

**Use cases**: open hardware dev board, host mode (USB dongle) or standalone FreeRTOS mode.

**Fast start**
1. Read the **TD‑XPAH** docs: https://teledatics.com/docs/introduction/
2. **Host mode** (Linux):
   - Install the NRC7292 host package (fork): https://github.com/teledatics/nrc7292_sw_pkg
   - Install DKMS package for the kernel driver: https://github.com/teledatics/nrc-dkms
   - Install the FTDI‑SPI driver if your setup uses USB‑SPI: https://github.com/teledatics/ftdi-spi-linux
3. **Standalone mode** (FreeRTOS):
   - Use the NRC7292 standalone SDK (fork): https://github.com/teledatics/nrc7292_sdk
4. Configure **AP**, **client (STA)**, or **802.11s mesh** modes per docs.

---

## Repository map

| Area | Repository | What it is |
|---|---|---|
| Open hardware board | `TD-XPAH` | Schematics for the 802.11ah experimenter board + accessory hATs |
| Linux USB‑SPI | `ftdi-spi-linux` | FT232H/FT4232H SPI driver used with NRC host paths |
| NRC7292 host pkg | `nrc7292_sw_pkg` | Newracom host‑mode package (fork) |
| NRC7292 SDK | `nrc7292_sdk` | Newracom standalone SDK (fork) |
| DKMS | `nrc-dkms` | Debian DKMS packaging for the NRC driver |
| How‑to | `mobile_halomax_hotspot` | Build a long‑range HaloMax™ mobile hotspot |
| Open HW daughterboards | `TD-WRLS_Hats` | Open designs for Ethernet, Wi‑Fi GW, GPS/RTK, sensors, battery/solar |
| Example / research | `ai-drone-control` | AI and CV components for drone/rover scenarios |

> Each repo includes its own README and LICENSE. Hardware vs. software may differ (MIT/GPL/Apache, etc.).

---

## Getting help

- **Docs**: https://teledatics.com/docs  
- **Issues**: Use the relevant repo’s **Issues** tab for bugs and feature requests.  
- **Discussions / Community**: Join the [Discord Server](https://discord.gg/WpguKNMR7H) linked from the product pages for setup questions, RF tuning tips, and field reports.  
- **Commercial & certification**: Contact Teledatics for enterprise support, module certification questions, or custom builds.

---

## Contributing

We ❤ contributions in the form of bug reports, docs, tests, drivers, example apps, and daughterboard designs.

1. Fork the relevant repo, create a feature branch, and open a PR.
2. Follow code style:
   - **C / kernel**: match upstream driver style.
   - **Python**: PEP 8; **Markdown**: wrap at ~100 chars; add diagrams with Mermaid when helpful.
3. Use **Conventional Commits** (e.g., `feat:`, `fix:`, `docs:`).
4. Add tests and docs where applicable.
5. Sign your commits if your employer requires DCO/CLA.

> See `CONTRIBUTING.md` (per‑repo). If it’s missing, open an issue and we’ll add one.

---

## Security & responsible disclosure

Please **do not** open public issues for vulnerabilities. Instead, use **GitHub Security Advisories** or contact our security point of contact (see the repo’s `SECURITY.md`). We’ll coordinate a fix and credit reporters.

---

## Compliance & regulatory notes

- Wi‑Fi HaLow operates in sub‑GHz ISM bands. Frequency allocations and transmit‑power limits vary by region.  
- You are responsible for operating within **local regulations** and ensuring proper **antenna selection**, **EIRP**, and **certifications** for your deployment.

---

## Trademarks

**Wi‑Fi HaLow™** is a trademark or certification mark of the Wi‑Fi Alliance. Other names and marks are the property of their respective owners.

---

## About Teledatics

Teledatics builds modules, boards, and software to make **secure, long‑range Wi‑Fi HaLow** practical in the real world—from edge AI and robotics to agriculture and industrial telemetry.

- Org: https://github.com/teledatics  
- Website: https://teledatics.com
