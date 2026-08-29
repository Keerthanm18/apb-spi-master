# APB-SPI Master

## 📌 Project Overview

This project implements an **APB-controlled SPI Master** using **Verilog HDL**.

The design provides an interface between an **APB bus** and an **SPI Master**, enabling APB transactions to control SPI data transfer.

The project focuses on **RTL design, modular implementation, simulation, verification, and waveform-based debugging**.

---

## 🎯 Objectives

- Design an APB interface for controlling the SPI Master
- Implement SPI Master functionality using Verilog
- Generate the SPI serial clock
- Control the SPI Slave Select signal
- Perform serial data transmission through MOSI
- Implement serial data shifting
- Validate APB-controlled SPI transactions
- Perform simulation and waveform-based debugging

---

## 🏗️ RTL Modules

The design is organized into multiple Verilog modules:

| Module | Description |
|---|---|
| `spi_core.v` | Core SPI control and data-transfer logic |
| `spi_apb_interface.v` | Handles APB interface transactions |
| `spi_shifter.v` | Handles serial data shifting |
| `spi_slave_select.v` | Controls the SPI Slave Select signal |
| `spi_baud_generator.v` | Generates the SPI serial clock |

---

## 🔌 Interfaces

### APB Interface

The design uses APB signals for controlling and communicating with the SPI Master:

- `PCLK`
- `PRESET_n`
- `PADDR`
- `PWRITE`
- `PSEL`
- `PENABLE`
- `PWDATA`
- `PRDATA`
- `PREADY`
- `PSLVERR`

### SPI Interface

The SPI Master provides:

- `SCLK` – SPI serial clock
- `MOSI` – Master Out Slave In
- `MISO` – Master In Slave Out
- `SS` – Slave Select

> **Note:** This project focuses on the SPI Master logic. MISO is hardcoded for simulation/testing of the master-side functionality. A separate SPI Slave RTL implementation is not included.

---

## ⚙️ Key Features

- APB-controlled SPI Master
- Verilog RTL implementation
- Modular RTL architecture
- APB transaction handling
- SPI serial clock generation
- Slave Select control
- Serial data shifting
- 8-bit SPI data transfer
- MOSI data transmission
- Module-level verification
- Simulation and waveform debugging

---

## 🧪 Verification

The individual RTL modules were verified using **Verilog-based testbenches**.

### Testbenches

- `spi_core_tb.v`
- `spi_shifter_tb.v`
- `spi_slave_select_tb.v`
- `spi_baud_generator_tb.v`
- `spi_apb_interface_tb.v`

### Verification Focus

- APB write transactions
- APB control and data handling
- SPI transaction initiation
- Slave Select behavior
- SPI clock generation
- Serial data shifting
- MOSI data transmission
- 8-bit data transfer
- Reset behavior
- Waveform analysis and debugging

---

## 📊 Simulation Waveform

The waveform below demonstrates an APB-controlled SPI transaction and the resulting SPI activity.

![APB-SPI Master Waveform](simulation/apb_spi_master_waveform.png)

The waveform demonstrates:

- APB clock and reset
- APB address and write data
- APB control signals
- SPI Slave Select activity
- SPI serial clock generation
- MOSI data transmission
- Transfer counter progression

---

## 🛠️ Tools & Technologies

**HDL**
- Verilog

**Design**
- RTL Design
- APB Interface
- SPI Master
- Modular Digital Design

**Verification**
- Verilog Testbench
- Simulation
- Waveform Analysis
- RTL Debugging

**EDA Tools**
- ModelSim

---

## 📁 Repository Structure

```text
apb-spi-master/
│
├── rtl/
│   ├── spi_core.v
│   ├── spi_apb_interface.v
│   ├── spi_shifter.v
│   ├── spi_slave_select.v
│   └── spi_baud_generator.v
│
├── tb/
│   ├── spi_core_tb.v
│   ├── spi_shifter_tb.v
│   ├── spi_slave_select_tb.v
│   ├── spi_baud_generator_tb.v
│   └── spi_apb_interface_tb.v
│
├── simulation/
│   └── apb_spi_master_waveform.png
│
└── README.md
```

---

## 🧠 Skills Demonstrated

- Verilog HDL
- RTL Design
- APB Interface
- SPI Master Design
- Serial Data Transfer
- Clock Generation
- Modular RTL Design
- Testbench Development
- Simulation
- Waveform Analysis
- RTL Debugging

---

## 📚 Learning Outcomes

Through this project, I gained practical experience in:

- Translating protocol requirements into RTL
- Designing modular digital systems
- Implementing APB-controlled functionality
- Understanding SPI Master data transfer
- Developing module-level testbenches
- Debugging RTL using simulation waveforms
- Analyzing control and data-transfer behavior

---

## ✅ Project Status

**Completed**

---

## 👤 Author

**Keerthan M**

📧 mailmekeerthanm@gmail.com

🔗 LinkedIn: www.linkedin.com/in/keerthan-m-b26689316

---

### Design • Verify • Debug • Deliver
