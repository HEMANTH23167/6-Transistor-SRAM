# 6-Transistor SRAM

A repository dedicated to the design, simulation, and implementation of 6-Transistor Static Random-Access Memory (6T-SRAM) cells and arrays.

## Overview

This project focuses on the development and optimization of 6-transistor SRAM (6T-SRAM), a fundamental building block in modern digital memory systems. The 6T-SRAM cell is one of the most widely used memory cell architectures in microprocessor caches and embedded memory applications due to its excellent trade-offs between density, speed, and power consumption.

## Features

- **Core 6T-SRAM Cell Design**: Standard 6-transistor cell configuration with two cross-coupled inverters and access transistors
- **Memory Array Architecture**: Multi-bit word organization with row/column selection circuitry
- **Read/Write Operations**: Complete control logic for memory access operations
- **Simulation & Verification**: Comprehensive testing and validation of memory functionality
- **Performance Analysis**: Timing, power consumption, and noise margin characterization

## What is 6T-SRAM?

The 6-transistor SRAM cell consists of:
- **2 Cross-coupled inverters** (4 transistors) - store the bit value
- **2 Access transistors** (2 transistors) - control read/write operations

### Key Characteristics:
- **Static**: Retains data as long as power is supplied
- **Volatile**: Data is lost when power is removed
- **Fast Access**: Sub-nanosecond read/write times
- **Low Power**: Minimal leakage and dynamic power consumption
- **Scalable**: Can be easily integrated into large memory arrays

## Applications

- CPU L1/L2/L3 Cache Memory
- GPU Register Files
- Embedded Microcontroller Memory
- Mobile Device RAM
- High-Speed Buffer Memory

## Getting Started

### Prerequisites
- SPICE simulator (ngspice, Cadence Spectre, or equivalent)
- Verilog/VHDL simulator (optional, for higher-level modeling)
- Digital design tools and CAD software

### Basic Usage

1. **Clone the repository**
   ```bash
   git clone https://github.com/HEMANTH23167/6-Transistor-SRAM.git
   cd 6-Transistor-SRAM
   ```

2. **Review the design files** - Navigate through the project structure to understand the cell design and architecture

3. **Run simulations** - Execute simulation scripts to verify functionality

## Project Structure

```
6-Transistor-SRAM/
├── README.md
├── designs/              # SRAM cell and array designs
├── simulations/          # Simulation files and test benches
├── verification/         # Test cases and verification scripts
├── documentation/        # Technical documentation and specifications
└── results/             # Simulation results and analysis
```

## Design Considerations

### Read Operation
- Bit lines are precharged to VDD
- Word line is asserted
- Storage nodes discharge through access transistors
- Sense amplifier detects the voltage difference

### Write Operation
- Bit lines are driven to desired levels
- Word line is asserted
- Strong drive from bit lines forces cell to desired state

### Key Metrics
- **Access Time**: Time from word line assertion to data valid
- **Cycle Time**: Minimum time between successive operations
- **Power Consumption**: Static and dynamic power
- **Noise Margins**: Robustness to environmental variations
- **Cell Area**: Layout density

## Features & Optimizations

- Standard 6T configuration for proven reliability
- Optimized transistor sizing for balanced performance
- Read stability and write ability analysis
- Temperature and supply voltage variations
- Process variation tolerance

## Contributing

Contributions are welcome! Please feel free to:
- Report issues and bugs
- Suggest improvements and optimizations
- Submit design enhancements
- Improve documentation

## References

- Weste, N. H. E., & Harris, D. M. (2010). *CMOS VLSI Design: A Circuits and Systems Perspective* (4th ed.)
- Rabaey, J. M., Chandrakasan, A., & Nicolic, B. (2003). *Digital Integrated Circuits* (2nd ed.)
- International Roadmap for Devices and Systems (IRDS)
- IEEE Standards for Microelectronic Design and Manufacturing

## License

This project is open source and available under the MIT License. See LICENSE file for details.

## Author

**HEMANTH23167**

## Support & Contact

For questions, issues, or collaborations, please open an issue on the GitHub repository or contact the project maintainer.

---

**Last Updated**: May 17, 2026

