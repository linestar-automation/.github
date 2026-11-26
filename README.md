<p align="center">
  <img src="https://raw.githubusercontent.com/linestarlabs/.github/main/assets/banner.png" alt="Linestar Labs: industrial automation and controls, PLC and motion systems, and industrial and distributed power software. Austin, TX" width="100%">
</p>

# Linestar Labs

**Industrial automation and controls engineering from Austin, Texas.** Linestar Labs is the software side of **[Linestar Automation](https://linestarautomation.com)**, a design-build shop that engineers the electrical and control side of custom machines for manufacturers and mechanical-engineering firms.

Linestar was founded by **Frank Zeiler**, its President & Principal Engineer. Frank has a BS in Mechanical Engineering from UT Austin and more than 40 years in machine design, motion control and power control. He is also President of the **[ISA Bluebonnet Section](https://connect.isa.org/communities/community-home?CommunityKey=1d16157a-fa10-41cc-8525-a17aaec80501)** of the International Society of Automation, which covers Central Texas.

## What we build

| Capability | What it means on your machine |
|---|---|
| 🎛️ **Control systems & PLC/HMI** | PLC programming, touchscreen operator interfaces and machine-to-machine communication |
| ⚙️ **Motion control** | Multi-axis servo and robot control, from precision stages to 6-axis robots (Beckhoff / EtherCAT) |
| 🔌 **Electrical panels & power distribution** | Control enclosures, switchgear and fail-safe power distribution, up to 400 A / 480 V three-phase |
| 🛑 **Safety systems** | Emergency stops and automated safety systems that help keep lines OSHA-compliant |
| 📈 **Data logging** | Production-rate and fault logging, so you always know what the machine is doing |
| 🛠️ **Prototype → install** | Design, prototyping, build and installation, usually in **3 to 6 months** |

<p align="center">
  <img src="https://raw.githubusercontent.com/linestarlabs/.github/main/assets/demo.gif" alt="Animation: how Linestar's controls, machines, edge software and power systems connect" width="85%">
</p>

---

## Selected projects

- **Concrete 3D-printing robot.** Linestar built the control system, power distribution and motion control (6-axis robot, EtherCAT on a Beckhoff controller) for a concrete-structure 3D printer in 2017. ICON and New Story named Linestar Automation as a partner on the **Vulcan** printer that printed the first permitted 3D-printed home in Austin (2018).
- **Holographic imaging for U.S. military mapping.** One of Linestar's first big jobs: power, laser and motion control for a high-precision optomechanical holographic imaging machine.
- **High-pressure drill-bit tester (Houston).** PLC control of a 20,000 PSI test chamber with a 100 kW servo and 400 A / 480 V three-phase power distribution.
- **Laser notching and wire winding (San Marcos, TX).** Motion control, touchscreen HMI, power distribution and safety systems for a precision electrical-component maker.
- **Data-center HPC robotics.** Motion control, safety and power distribution for a compact high-performance-computing system that swaps servers robotically, plus process control for 2-phase liquid cooling.
- **Cobot electronics testing.** Portable cobot cells that test digital multimeters, with six built for one client.
- **Automated Magnet Mover.** An API-driven machine that replaced a manual magnetic-wand process. It is controlled by [linestar-py](https://github.com/linestarlabs/linestar-py).
- **Energy storage and microgrids.** A 12 kWh industrial UPS (Linestar's first energy-storage system) and, per Linestar, an energy switch for the U.S. Department of Energy's SunShot program.

See all case studies at **[linestarautomation.com/projects](https://linestarautomation.com/projects)**.

## Our story

| When | Milestone |
|------|-----------|
| 1980–2007 | Frank Zeiler earns a BS in Mechanical Engineering from UT Austin, then holds engineering roles at APV / Invensys, Advanced System Integration and Zebra Imaging |
| 2008–2010 | Linestar starts in Austin, with an early holographic-imaging machine for U.S. military applications |
| 2012 | Builds its first energy-storage system, a 12 kWh industrial UPS |
| 2013–2015 | Builds laser-notching and wire-winding controls, robotic assembly, UV curing and electro-optical inspection cells. LSA Labs LLC is formed (2013) |
| 2014–2016 | Adds microgrid control systems, including the DOE SunShot energy switch |
| 2017–2018 | Builds the drill-bit test system and the Beckhoff / EtherCAT control system for the concrete 3D printer, and is named an ICON / New Story Vulcan partner |
| 2019–2020 | Builds data-center HPC robotics and cooling controls, plus cobot test cells |
| 2022 | Adds home microgrids and the Linestar Power Server, along with blockchain-backed machine data logging, and starts this GitHub org |
| 2023 | Releases the Automated Magnet Mover with an API, Python and C++ PLC clients, Yaskawa MP3300 work and an IEC 61131-3 runtime |
| 2024 → today | Continues custom controls work and expands distributed-power software R&D |

---

## 1 · 🏭 Industrial automation & PLC control

Software for commanding the PLC-controlled machines we build and for running PLC programs on commodity hardware.

| Repo | Stack | What it does |
|------|-------|--------------|
| [**linestar-py**](https://github.com/linestarlabs/linestar-py) | Python | `PLCMagnetMover` client (pycomm3 / EtherNet/IP), Click CLI and Flask-RESTX API: wake, home, go to position, and report location and errors |
| [**linestar-cpp**](https://github.com/linestarlabs/linestar-cpp) | C++17 | Pistache REST controller and Boost CLI skeleton for the same machine operations (work in progress) |
| [**ReactInnovations**](https://github.com/linestarlabs/ReactInnovations) | Yaskawa | Yaskawa MP3300 PLC controller logic, API and client software (placeholder) |
| [**echidna**](https://github.com/linestarlabs/echidna) | C | Fork of [61131/echidna](https://github.com/61131/echidna), an IEC 61131-3 compiler and VM runtime (runs on a Raspberry Pi with PiFace I/O) |

## 2 · ⚡ Distributed power & microgrid R&D

**Active, exploratory software.** This work grows out of Linestar's industrial UPS and microgrid-controls projects. It includes a Raspberry Pi power server, a Go microgrid controller, EcoFlow device tooling, and cloud APIs and apps for monitoring local grids of batteries, solar, generators and loads. Expect prototypes and moving interfaces.

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

## 3 · 🌐 Web products & dashboards

| Repo | Stack | What it does |
|------|-------|--------------|
| [**linestarautomation.com-react**](https://github.com/linestarlabs/linestarautomation.com-react) | JavaScript | The Linestar Automation website: services, case studies and blog |
| [**linestar.tech-nodejs**](https://github.com/linestarlabs/linestar.tech-nodejs) | TypeScript | Hapi API for products, machine events, a home-power dashboard, Prometheus metrics and on-chain machine telemetry |
| [**linestar.tech-react**](https://github.com/linestarlabs/linestar.tech-react) | JavaScript | Dashboard for the Home Power System and Linestar products |
| [**modernize-admin-dashboard**](https://github.com/linestarlabs/modernize-admin-dashboard) | TypeScript | Next.js 14 + MUI admin template kept as a dashboard starter |

---

## Quick starts

```bash
# Drive a PLC Magnet Mover from Python (EtherNet/IP)
git clone https://github.com/linestarlabs/linestar-py && cd linestar-py
pip install -r requirements.txt
ETHERNET_IP_ADDRESS=192.168.1.100 python plc_magnet_mover.py

# Microgrid controller on macOS (R&D)
brew tap linestarlabs/microgrid && brew install microgrid
```

## Work with Linestar

Have a machine that needs controls, a panel, motion or safety work? Get in touch.

🌐 [linestarautomation.com](https://linestarautomation.com) · 📍 8711 Burnet Rd, Suite B-31, Austin, TX 78757 · ☎️ +1 (512) 963-0939 · ✉️ [FZeiler@LineStarAutomation.com](mailto:FZeiler@LineStarAutomation.com)

<sub>Each repo's README includes a banner, a demo animation and setup instructions. Issues and pull requests are welcome.</sub>
