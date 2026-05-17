# 6T SRAM Cell Design using Cadence Virtuoso

## Project Overview

This project presents the design and analysis of a 6T SRAM (Static Random Access Memory) Cell using Cadence Virtuoso. The complete design flow includes schematic creation, simulation, layout verification, parasitic extraction, and performance evaluation.

The project focuses on:

* SRAM cell functionality
* Read and write stability
* Power and delay analysis
* Physical verification using industry-standard EDA tools

---

# Tools & Technologies

* Cadence Virtuoso
* Cadence Spectre
* Cadence Assura / Calibre
* Cadence Quantus
* Technology Node: 45nm

---

# 6T SRAM Architecture

The SRAM cell consists of:

* 2 PMOS transistors
* 4 NMOS transistors

  * Two cross-coupled CMOS inverters
  * Two access transistors controlled by the Word Line (WL)

The design stores one bit of data using bistable latch operation.

---

# SRAM Operations

## Hold Mode

* WL = 0
* Access transistors remain OFF
* Stored data is retained through cross-coupled inverters

## Write Operation

1. WL is enabled
2. Data applied on BL and BL̅
3. Internal nodes switch according to input data
4. WL disabled after successful write

Example:

* BL = 1, BL̅ = 0 → Stores logic ‘1’
* BL = 0, BL̅ = 1 → Stores logic ‘0’

## Read Operation

1. BL and BL̅ are precharged
2. WL enabled
3. Stored node discharges corresponding bitline
4. Sense amplifier detects voltage difference

---

# Design Flow

## 1. Schematic Design

* Designed the SRAM cell using Virtuoso Schematic Editor
* Implemented transistor-level connectivity

## 2. Simulation & Testbench

* Created testbench for Read/Write verification
* Performed transient analysis using Spectre

## 3. Layout Design

* Custom layout designed following 45nm design rules
* Optimized transistor placement and routing

## 4. DRC Verification

* Verified layout against fabrication design rules

## 5. LVS Verification

* Confirmed layout matches schematic connectivity

## 6. RC Extraction

* Extracted parasitic resistance and capacitance
* Evaluated impact on timing and power

## 7. Performance Analysis

Analyzed:

* Read Delay
* Write Delay
* Power Consumption
* Stability Margins

---

# Repository Structure

```bash
📦 6T-SRAM-Cell
├── schematic/        # SRAM schematic design
├── layout/           # Layout files
├── testbench/        # Simulation testbench
├── drc_lvs/          # DRC & LVS reports
├── extraction/       # RC extraction data
├── analysis/         # Timing and power analysis
├── results/          # Output waveforms/screenshots
└── README.md
```

---

# Simulation Procedure

1. Open Cadence Virtuoso
2. Load SRAM schematic/layout
3. Open testbench setup
4. Apply Read/Write stimulus
5. Run Spectre transient analysis
6. Perform DRC and LVS checks
7. Run RC extraction and analyze results

---

# Key Features

* Full Custom 6T SRAM Design
* DRC/LVS Clean Layout
* RC Extracted Analysis
* Low-Power Optimization
* Read/Write Stability Verification

---

# Future Enhancements

* Multi-Port SRAM Architecture
* Advanced Low-Power Techniques
* Bitline Optimization
* Sense Amplifier Integration
* FinFET-Based SRAM Design

---

# Author

HEMANTH B R

Email: [hemanthhrh23167@gmail.com](mailto:hemanthhrh23167@gmail.com)
GitHub: github.com/HEMANTH23167
LinkedIn: linkedin.com/in/hemanthbr23167/
