<p align="center">
  <img src="https://raw.githubusercontent.com/linestarlabs/.github/main/assets/banner.png" alt="Linestar Labs: industrial automation, PLC machine control, microgrid and power-server software" width="100%">
</p>

# Linestar Labs

**The software arm of [Linestar Automation](https://linestarautomation.com), an industrial automation and controls shop in Austin, Texas.**

Linestar was founded by **Frank Zeiler**, a UT Austin mechanical engineer with four decades in machine design, motion control and power control. Frank is Linestar's President & Principal Engineer and President of the [ISA Bluebonnet Section](https://connect.isa.org/communities/community-home?CommunityKey=1d16157a-fa10-41cc-8525-a17aaec80501) (International Society of Automation, Central Texas). Linestar designs and builds the electrical side of custom machines: **control systems, PLC/HMI and touchscreen interfaces, motion control, power distribution, safety systems and data logging**. It works mostly for mechanical-engineering firms and manufacturers, and most jobs take 3 to 6 months from first call to installation.

This org holds the code that grew out of that shop floor: clients for PLC-driven machines, an IEC 61131-3 runtime, the microgrid and Power Server platform, and the websites and dashboards around them.

<p align="center">
  <img src="https://raw.githubusercontent.com/linestarlabs/.github/main/assets/demo.gif" alt="Animation: how Linestar's power server, microgrid controller, store, PLC machines, PLC runtime and web products connect" width="85%">
</p>

---

## Our story

| When | Milestone |
|------|-----------|
| 1980–2007 | Frank Zeiler earns a BS in Mechanical Engineering from UT Austin, then holds engineering roles at APV / Invensys, Advanced System Integration and Zebra Imaging |
| 2008–2010 | Linestar starts in Austin. One of its first big jobs is power, laser and motion control for a high-precision holographic imaging machine for U.S. military mapping |
| 2012 | Builds its first energy-storage system, a 12 kWh industrial UPS for a factory |
| 2013–2015 | Builds controls for laser-notching and wire-winding lines (San Marcos, TX), plus robotic assembly, UV curing and electro-optical inspection cells. LSA Labs LLC is formed (2013) |
| 2014–2016 | Moves into microgrids, including an energy switch for the U.S. Department of Energy's **SunShot** program (10 kW, 10 kWh battery) |
| 2017 | Builds a 20,000 PSI drill-bit test system (Houston) and the 6-axis **Beckhoff / EtherCAT control system** for a concrete 3D printer |
| 2018 | ICON and New Story name Linestar Automation as a partner on the **Vulcan** printer that printed the first permitted 3D-printed home in Austin |
| 2019–2020 | Builds robotic server swapping and 2-phase liquid-cooling controls for data-center HPC, plus cobot cells for testing electronics (six units for one client) |
| 2022 | Launches home microgrids (nanogrid, Sol-Ark, Growatt) and the palm-sized **Linestar Power Server**, adds blockchain-backed machine data logging, and starts the `linestarlabs` GitHub org |
| 2023 | Releases an API-driven **Automated Magnet Mover**, Python and C++ PLC clients, Yaskawa MP3300 work and an IEC 61131-3 runtime |
| 2024 → today | Builds the microgrid platform: a Raspberry Pi power server, a Go microgrid controller, the Microgrid Store API and app, an EcoFlow client and the MyHomeGrid mobile app |

Industries served include military, manufacturing, electro-optics, oil field, construction, medical, data centers and renewable energy. More than 20 case studies are at **[linestarautomation.com/projects](https://linestarautomation.com/projects)**.

---

## 🏭 Industrial automation & PLC control

Software for commanding PLC-controlled machines such as the Linestar **Automated Magnet Mover**, and for running PLC programs on commodity hardware.

| Repo | Stack | What it does |
|------|-------|--------------|
| [**linestar-py**](https://github.com/linestarlabs/linestar-py) | Python | `PLCMagnetMover` client (pycomm3 / EtherNet/IP), Click CLI and Flask-RESTX API: wake, home, go to position, and report location and errors |
| [**linestar-cpp**](https://github.com/linestarlabs/linestar-cpp) | C++17 | Pistache REST controller and Boost CLI skeleton for the same machine operations (work in progress) |
| [**ReactInnovations**](https://github.com/linestarlabs/ReactInnovations) | Yaskawa | Yaskawa MP3300 PLC controller logic, API and client software (placeholder) |
| [**echidna**](https://github.com/linestarlabs/echidna) | C | Fork of [61131/echidna](https://github.com/61131/echidna), an IEC 61131-3 compiler and VM runtime (runs on a Raspberry Pi with PiFace I/O) |

## ⚡ Microgrid & Power Server platform

This software follows Linestar's hardware path from industrial UPS systems through the DOE SunShot energy switch to home microgrids. It runs a local grid of batteries, solar, generators and loads, and manages it from the cloud.

| Repo | Stack | What it does |
|------|-------|--------------|
| [**power-server-brain-pi**](https://github.com/linestarlabs/power-server-brain-pi) | Rust | Software for the Linestar Central Power Server on a Raspberry Pi |
| [**microgrid**](https://github.com/linestarlabs/microgrid) | Go | Controller daemon plus a Hub WebSocket server, shipped as a `.deb` with systemd |
| [**microgrid-cli**](https://github.com/linestarlabs/microgrid-cli) | Go | CLI for grids, batteries, consumers and event subscriptions |
| [**homebrew-microgrid**](https://github.com/linestarlabs/homebrew-microgrid) | Ruby | `brew tap linestarlabs/microgrid && brew install microgrid` |
| [**ecoflow-ts**](https://github.com/linestarlabs/ecoflow-ts) | TypeScript | Signed client for the EcoFlow IoT Open API (power stations used as grid batteries) |
| [**api.microgridstore.com**](https://github.com/linestarlabs/api.microgridstore.com) | TypeScript | Hapi + Prisma/PostgreSQL API for grids, batteries, generators and consumers, with RabbitMQ events and WebSocket streams |
| [**app.microgridstore.com**](https://github.com/linestarlabs/app.microgridstore.com) | TypeScript | Next.js app that shows microgrids as D3 force graphs |
| [**myhomegrid-app**](https://github.com/linestarlabs/myhomegrid-app) | JavaScript | Expo / React Native MyHomeGrid mobile app (UI prototype) |
| [**linestarpower.com**](https://github.com/linestarlabs/linestarpower.com) | TypeScript | Next.js site and account portal for Linestar Power, with Supabase auth |

## 🌐 Web products & dashboards

| Repo | Stack | What it does |
|------|-------|--------------|
| [**linestarautomation.com-react**](https://github.com/linestarlabs/linestarautomation.com-react) | JavaScript | The Linestar Automation website: services, case studies and blog |
| [**linestar.tech-nodejs**](https://github.com/linestarlabs/linestar.tech-nodejs) | TypeScript | Hapi API for products, machine events, a home-power dashboard, Prometheus metrics and on-chain machine telemetry |
| [**linestar.tech-react**](https://github.com/linestarlabs/linestar.tech-react) | JavaScript | Dashboard for the Home Power System and Linestar products |
| [**modernize-admin-dashboard**](https://github.com/linestarlabs/modernize-admin-dashboard) | TypeScript | Next.js 14 + MUI admin template kept as a dashboard starter |

---

## Quick starts

```bash
# Microgrid controller on macOS
brew tap linestarlabs/microgrid && brew install microgrid

# Drive a PLC Magnet Mover from Python
git clone https://github.com/linestarlabs/linestar-py && cd linestar-py
pip install -r requirements.txt
ETHERNET_IP_ADDRESS=192.168.1.100 python plc_magnet_mover.py
```

## Work with Linestar

🌐 [linestarautomation.com](https://linestarautomation.com) · 📍 8711 Burnet Rd, Suite B-31, Austin, TX 78757 · ☎️ +1 (512) 963-0939 · ✉️ [FZeiler@LineStarAutomation.com](mailto:FZeiler@LineStarAutomation.com)

<sub>Each repo's README includes a banner, a demo animation and setup instructions. Issues and pull requests are welcome.</sub>
