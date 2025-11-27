# Attested (Reference Repository)

![DRG4FOOD](https://img.shields.io/badge/DRG4FOOD-project-green)
![Status](https://img.shields.io/badge/status-reference-lightgrey)
![License](https://img.shields.io/badge/license-MIT-brightgreen)

Attested is a DRG4FOOD Open Call project delivering an open traceability platform for cooperative food systems, enabling verifiable field-to-fork data capture and presentation. Developed by Commonslab, Valdibella and FiBL and carried out from **My 2024 to April 2025**. 

This repository serves as the official DRG4FOOD Toolbox reference for Attested providing links to its open-source ESP32 firmware, FIWARE bridge module, consumer UI, and KiCAD hardware design files. All source code and hardware designs remain hosted in the Attested GitLab space; this page provides a structured overview and direct links to those resources.

---

## Overview

Attested is a traceability platform that brings transparency, accountability, and autonomy to food supply chains. Designed for small cooperatives and conscious consumers, it offers a practical, privacy-respecting way to document and share every step of a product's journey - from field to fork - using verifiable data.

At its core lies a modular hardware-software stack that combines handheld RFID/QR scanners, environmental sensors, and a FIWARE-based backend. Producers use it to record cultivation, processing, and transport events, while consumers can scan a QR label to access an interactive webpage showing where, when, and under what conditions a product was made.

The architecture supports local or cooperative-owned hosting, giving small producers full control of their data and reducing dependency on proprietary, data-extractive traceability platforms.

---

## About the solution

Attested demonstrates how open, affordable digital tools can make food traceability both ethical and accessible for small actors:

- **In the field** - Handheld QR/RFID scanners and IoT sensors capture key events (harvest, storage, transport) and environmental conditions (e.g. temperature, humidity).  
- **In processing and logistics** - Products are re-scanned at each processing or packing step, building a complete digital footprint linked to a unique identifier.  
- **At the point of sale and beyond** - Each unit carries a QR code that opens a consumer-facing webpage, turning raw traceability data into a clear, human-readable story about origin, handling, and conditions.

By combining an ESP32-based device firmware, a FIWARE Orion bridge, a consumer UI, and open hardware designs for a handheld scanner, Attested provides an end-to-end reference implementation for digitally responsible traceability.

---

## Open-source components

The Attested stack is developed and maintained in the Attested GitLab space. The main components are:

### Consumer WebUI (Flask)
A flask-based python program that implements a web interface visualizing the data gathered for a specific product, for the consumer-facing webUI thia shows the data previously collected using the hand-held QR/RFID scanners.
https://gitlab.com/commonslabgr/attested/consumer-webui

### Bridge Module (Orion - SQL)
A python script to fetch changes from the Orion FIWARE Context Broker and insert them into an SQL database.
https://gitlab.com/commonslabgr/attested/orion-sql-bridge

### QRFID scanner firmware (ESP32)
Firmware intended to run on the Espressif ESP32 Wrover-E embedded in the hand-held data-collection device. Makes use of the Arduino framework.
https://gitlab.com/commonslabgr/attested/qrfid-scanner-fw

### QRFID Scanner Hardware (KiCAD)
Hardware design files for producing the printed circuit board (PCB) as well as the casing of the ATTESTED hand-held scanner for QR-codes and RFID tags. 
https://gitlab.com/commonslabgr/attested/qrfid-scanner-hw

---

## How you can use it

Attested’s components are designed to be reusable and adaptable across different short food supply chains.

### For producers and cooperatives

- Capture real-time data on cultivation, processing, and transport using handheld scanners and field sensors.  
- Host the backend locally or on cooperative-controlled servers to maintain data sovereignty.  
- Use cooperative dashboards (built on FIWARE) to monitor key conditions (e.g. temperature, humidity, timing) across the production chain.

### For distributors and retailers

- Link each product’s QR code to a dynamic digital page that shows verified origin, handling steps, and environmental conditions.  
- Use the same verified data for both in-store communication and compliance reporting.

### For consumers

- Scan a product’s QR code to see where, when, and under what conditions it was produced, processed, and transported.  
- Access transparent stories about cooperatives and their members, backed by verifiable data rather than generic claims.

### For developers and open innovation partners

- Reuse and extend the firmware, bridge, UI, and hardware designs under open licenses (AGPLv3 / CC for hardware).  
- Integrate Attested with other traceability tools or digital product passport initiatives using FIWARE-compatible interfaces.  
- Fork and adapt the stack for new cooperatives, regions, or product lines.

---

## Contribution to the DRG4FOOD Toolbox

Attested contributes to the DRG4FOOD Toolbox by providing:

- **Open-source hardware toolkit** for environmental and logistics sensing (handheld QR/RFID scanners, IoT sensor nodes, PCB designs, and bills of materials).  
- **Firmware and backend services** built on FIWARE Orion, supporting data minimisation, local hosting, and strong privacy-by-design principles.  
- **Consumer and cooperative-facing interfaces** that translate complex traceability data into clear, human-readable stories.  
- **A reference architecture for digital responsibility** in short food supply chains, operationalising DRG4FOOD goals such as privacy, data fairness, transparency, and human agency.

These components offer a replicable model for accessible, inclusive, and digitally responsible traceability across Europe’s evolving food ecosystem.

---

## License

Unless otherwise noted in the individual component repositories, Attested software is released under the **GNU Affero General Public License v3.0 (AGPL-3.0)** or later.

Please refer to the specific LICENSE files in:

- the firmware repository  
- the bridge module repository  
- the consumer UI repository  
- the hardware design repository (for hardware and documentation licenses)
