<p align="center">
  <img src="https://raw.githubusercontent.com/linestarlabs/.github/main/assets/banner.png" alt="Linestar Labs: microgrid & power-server software, industrial PLC automation, and web products" width="100%">
</p>

# Linestar Labs

**Linestar, LLC · Austin, Texas.** We build the software that runs **home and site microgrids**, **automates industrial machines**, and powers the **web products** people use to buy, monitor and control them.

Our stack goes from the hardware up: a Raspberry Pi power server and a Go microgrid controller at the edge, Python and C++ clients for PLC-driven machinery, an IEC 61131-3 PLC runtime, and TypeScript APIs and dashboards in the cloud.

<p align="center">
  <img src="https://raw.githubusercontent.com/linestarlabs/.github/main/assets/demo.gif" alt="Animation: how Linestar's power server, microgrid controller, store, PLC machines, PLC runtime and web products connect" width="85%">
</p>

---

## ⚡ Microgrid & Power Server platform

Software for running a local power grid of batteries, solar/generators and loads, and managing it from the cloud.

| Repo | Stack | What it does |
|------|-------|--------------|
| [**power-server-brain-pi**](https://github.com/linestarlabs/power-server-brain-pi) | Rust | Software for the Linestar Central Power Server on Raspberry Pi. Currently an AMQP/RabbitMQ prototype, with Wi-Fi onboarding, GPIO and Matter on the roadmap |
| [**microgrid**](https://github.com/linestarlabs/microgrid) | Go | Controller daemon (`start`/`stop`/`status`) plus Hub WebSocket server, shipped as a `.deb` with systemd for `apt.microgridstore.com` |
| [**microgrid-cli**](https://github.com/linestarlabs/microgrid-cli) | Go | Cobra CLI scaffold for grids, batteries, consumers and event subscriptions |
| [**homebrew-microgrid**](https://github.com/linestarlabs/homebrew-microgrid) | Ruby | `brew tap linestarlabs/microgrid && brew install microgrid` |
| [**ecoflow-ts**](https://github.com/linestarlabs/ecoflow-ts) | TypeScript | HMAC-SHA256 request signing for the EcoFlow IoT Open API (power stations as grid batteries) |
| [**api.microgridstore.com**](https://github.com/linestarlabs/api.microgridstore.com) | TypeScript | Hapi + Prisma/PostgreSQL API for grids, batteries, generators and consumers, with RabbitMQ events and WebSocket streams |
| [**app.microgridstore.com**](https://github.com/linestarlabs/app.microgridstore.com) | TypeScript | Next.js app that visualises microgrids as D3 force graphs |
| [**myhomegrid-app**](https://github.com/linestarlabs/myhomegrid-app) | JavaScript | Expo / React Native MyHomeGrid mobile app (UI prototype) |
| [**linestarpower.com**](https://github.com/linestarlabs/linestarpower.com) | TypeScript | Next.js site and account portal for Linestar Power, with Supabase auth |

## 🏭 Industrial PLC automation & machine control

Software for commanding PLC-controlled machines such as the Linestar **PLC Magnet Mover**, and for running PLC programs on commodity hardware.

| Repo | Stack | What it does |
|------|-------|--------------|
| [**linestar-py**](https://github.com/linestarlabs/linestar-py) | Python | `PLCMagnetMover` client (pycomm3 / EtherNet/IP), Click CLI and Flask-RESTX API: wake, home, go-to-position, report location and error |
| [**linestar-cpp**](https://github.com/linestarlabs/linestar-cpp) | C++17 | Pistache REST controller and Boost CLI skeleton for the same machine operations (work in progress) |
| [**ReactInnovations**](https://github.com/linestarlabs/ReactInnovations) | Yaskawa | Placeholder for Yaskawa MP3300 PLC controller logic, API and client software |
| [**echidna**](https://github.com/linestarlabs/echidna) | C | Fork of [61131/echidna](https://github.com/61131/echidna), an IEC 61131-3 compiler and VM runtime (runs on a Raspberry Pi with PiFace I/O) |

## 🌐 Web products, backends & dashboards

| Repo | Stack | What it does |
|------|-------|--------------|
| [**linestar.tech-nodejs**](https://github.com/linestarlabs/linestar.tech-nodejs) | TypeScript | Hapi API for linestar.tech: products, machine events, home-power dashboard, Prometheus metrics and on-chain (BSV) telemetry posting |
| [**linestar.tech-react**](https://github.com/linestarlabs/linestar.tech-react) | JavaScript | linestar.tech dashboard (Home Power System, Linestar Products) on Soft UI Dashboard PRO |
| [**linestarautomation.com-react**](https://github.com/linestarlabs/linestarautomation.com-react) | JavaScript | Marketing site for Linestar Automation's custom automation services (Vercel) |
| [**modernize-admin-dashboard**](https://github.com/linestarlabs/modernize-admin-dashboard) | TypeScript | Modernize Next.js 14 + MUI admin template kept as a dashboard starter |

---

## Quick starts

```bash
# Microgrid controller on macOS
brew tap linestarlabs/microgrid && brew install microgrid

# Microgrid controller on Debian/Ubuntu
curl https://apt.microgridstore.com/install.sh | bash

# Drive a PLC Magnet Mover from Python
git clone https://github.com/linestarlabs/linestar-py && cd linestar-py
pip install -r requirements.txt
ETHERNET_IP_ADDRESS=192.168.1.100 python plc_magnet_mover.py
```

## Find us

🌐 [linestarautomation.com](https://linestarautomation.com) · [linestar.tech](https://linestar.tech) · [microgridstore.com](https://app.microgridstore.com) · ✉️ ops@21e8.tech

<sub>Every repo's README has a banner, a demo animation and setup instructions. Issues and pull requests are welcome.</sub>
