# STM32 RedBoard

Custom STM32F103C8T6 development board designed with KiCad, featuring USB-C, Micro-USB, CAN, Micro-SD, SWD and GPIO interfaces.

## Project Overview

The **STM32 RedBoard** is a versatile open-source hardware development platform built around the ARM Cortex-M3-based STM32F103C8T6 microcontroller. This board integrates multiple connectivity and interface options, making it suitable for embedded systems prototyping, IoT applications, and educational purposes. The entire design is implemented using KiCad 10.0, ensuring compatibility with modern PCB design workflows.

## Main Features

- **ARM Cortex-M3 Microcontroller**: STM32F103C8T6 with 64 KB SRAM and 256 KB Flash memory
- **Dual USB Connectivity**: USB Type-C (primary) and Micro-USB (secondary) interfaces
- **CAN Bus Support**: Full CAN 2.0B protocol support for vehicular and industrial applications
- **Micro-SD Card Interface**: SD/SDIO interface for mass storage and data logging
- **SWD Programming & Debugging**: Serial Wire Debug interface for development and troubleshooting
- **GPIO Expansion**: Extensive General-Purpose Input/Output pins for sensor integration
- **Professional PCB Design**: Schematic and layout designed in KiCad 10.0
- **Open-Source Hardware**: Full design files available for customization and adaptation

## Hardware Specifications

| Specification | Details |
|---|---|
| **Microcontroller** | STM32F103C8T6 (ARM Cortex-M3, 72 MHz) |
| **Flash Memory** | 256 KB |
| **SRAM** | 64 KB |
| **Supply Voltage** | 3.3V (USB derived or external) |
| **GPIO Pins** | Multiple configurable I/O ports |
| **Interfaces** | USB-C, Micro-USB, CAN, SWD, Micro-SD |
| **EDA Tool** | KiCad 10.0 (version 20260306) |
| **PCB Design Standard** | A4 paper reference |

## Interfaces and Connectivity

### USB-C (Primary Interface)
- **Type**: USB Type-C Receptacle (USB 2.0)
- **Configuration**: 16-pin receptacle
- **Function**: Primary power supply and data communication
- **Features**: Reversible plug orientation, robust mechanical connection
- **Status**: ✅ Schematic definition verified

### Micro-USB (Secondary Interface)
- **Type**: USB Micro Type-B Connector
- **Pins**: 5-pin configuration (VBUS, D-, D+, ID, GND, Shield)
- **Function**: Alternative power and communication interface
- **Use Case**: Legacy compatibility and alternative charging
- **Status**: ✅ Schematic definition verified

### CAN Bus
- **Protocol**: CAN 2.0B (standard and extended frames)
- **Application**: Vehicle diagnostics, industrial automation, real-time control systems
- **Signal Lines**: CAN_H and CAN_L (differential signaling)
- **Transceiver Model**: *To be verified in PCB layout*
- **Status**: ⚠️ Transceiver specifications pending validation

### Micro-SD Card Interface
- **Type**: Micro SD Card Socket
- **Pins**: 8-pin configuration (DAT2, DAT3/CD, CMD, VDD, CLK, VSS, DAT0, DAT1, SHIELD)
- **Protocol**: SDIO/SPI mode
- **Function**: Data storage, firmware updates, data logging
- **Reference**: [Würth Elektronik Micro-SD Connector Datasheet](https://www.we-online.com/components/products/datasheet/693072010801.pdf)
- **Status**: ✅ Schematic definition verified

### SWD (Serial Wire Debug)
- **Protocol**: ARM Serial Wire Debug (SWD)
- **Pins**: SWDCLK, SWDIO, GND, 3.3V (standard configuration)
- **Function**: Real-time debugging, firmware upload, on-chip debugging
- **Compatible Debuggers**: ST-LINK/V2, Segger J-Link, OpenOCD-compatible devices
- **Use Case**: Development, firmware flashing, runtime inspection
- **Status**: ✅ Schematic definition verified

### GPIO Expansion
- **Source**: STM32F103C8T6 GPIO ports (multiple I/O pins)
- **Voltage Levels**: 3.3V logic (5V tolerant on selected pins)
- **Capabilities**: Digital I/O, PWM, analog input (ADC), timer functions
- **Applications**: Sensor interfacing, LED control, button input, relay driving
- **Status**: ⚠️ Detailed pinout to be documented

## PCB Design and Schematic

The STM32 RedBoard is fully designed using **KiCad 10.0**, a professional-grade, open-source electronic design automation (EDA) suite.

### Key Features
- **Cross-platform compatibility**: Windows, macOS, Linux
- **Version control friendly**: Text-based design files
- **Community ecosystem**: Extensive libraries and documentation

### Design Files

| File | Description |
|---|---|
| `Stm32_Red_Board.kicad_sch` | Main schematic with all component connections and interfaces |
| `Block_Diagram.kicad_sch` | High-level system architecture overview |
| `Stm32_Red_Board.kicad_pcb` | PCB layout, routing, and component placement |

### Design Status

| Aspect | Status |
|---|---|
| Schematic symbols | ✅ Defined for all major interfaces |
| Component connections | ✅ Verified in kicad_sch files |
| PCB layout | ⚠️ To be verified |
| Trace routing | ⚠️ To be verified |
| Manufacturing files | ⚠️ Pending validation |
| Functional testing | ⚠️ Not yet conducted |

## Repository Contents and File Structure

```
stm32-RedBoard/
├── README.md                           # Project documentation
├── LICENSE                             # MIT License
├── Stm32_Red_Board.kicad_sch          # Main schematic file
├── Stm32_Red_Board.kicad_pcb          # PCB layout file
├── Block_Diagram.kicad_sch            # System block diagram
├── images/                             # Design documentation and screenshots
│   ├── 1.png                          # Schematic visualization
│   ├── 2.png                          # Interface details
│   ├── 3.png                          # PCB layout preview
│   └── 7.png                          # Additional design images
└── _restore_backup_*/                 # Version control backups
```

## Hardware Requirements and Compatibility

### Required Software (Development)
- **KiCad 10.0 or later** (free, open-source)
  - [KiCad Official Website](https://www.kicad.org)
  - Includes: Schematic editor, PCB designer, 3D viewer

### Programming & Debugging Tools
- **ST-LINK/V2** - Official STMicroelectronics debugger
- **Segger J-Link** - Universal JTAG/SWD debugger
- **OpenOCD** - Open-source debugging protocol

### Integrated Development Environments
- **STM32CubeMX** - Configuration and code generation
- **STM32CubeIDE** - Official integrated development environment
- **PlatformIO** - Cross-platform embedded development
- **VSCode + ARM Toolchain** - Open-source workflow

### Compatibility
- **Operating Systems**: Windows, macOS, Linux
- **EDA Versions**: KiCad 9.0+ recommended for compatibility
- **Design Format**: Standard FR-4 substrate

## Getting Started

### 1. Opening the Project in KiCad

1. **Install KiCad 10.0** (or latest stable version)
   - Download from [kicad.org](https://www.kicad.org)

2. **Clone or download this repository**
   ```bash
   git clone https://github.com/EJ-JATIMohammed/stm32-RedBoard.git
   cd stm32-RedBoard
   ```

3. **Open in KiCad**
   - Launch KiCad
   - Select **File** → **Open Project**
   - Navigate to `Stm32_Red_Board.kicad_sch`

4. **Explore the Design**
   - **Schematic view**: Examine all connections and component values
   - **PCB view**: Review layout, trace routing, and layer assignments
   - **Block diagram**: See `Block_Diagram.kicad_sch` for system overview

### 2. Schematic Navigation

- **Zoom**: Use mouse wheel or View menu
- **Search**: Ctrl+F to find components or signals
- **Properties**: Right-click components to view datasheets and values
- **Hierarchical design**: Navigate between schematic pages (if present)

### 3. PCB Layout View

- **3D visualization**: View → 3D Viewer for mechanical design review
- **Design rules check**: Tools → Design Rules Checker (DRC)
- **Electrical rules check**: Tools → Electrical Rules Checker (ERC)
- **Manufacturing files**: File → Plot to generate Gerber files

### 4. Customization and Adaptation

The design is modular and supports customization:

- **Add components**: Extend GPIO or add shields
- **Remove interfaces**: Disable unused features (CAN, Micro-SD)
- **Modify power distribution**: Adjust supply voltage and filtering
- **Update component footprints**: Select alternatives from KiCad libraries
- **Adapt for variants**: Create sub-designs for specific applications

## Programming and Debugging Overview

### Development Workflows

**Workflow 1: STMicroelectronics Official Tools**
```
STM32CubeMX (config) → STM32CubeIDE (code) → ST-LINK/V2 (program/debug)
```

**Workflow 2: Open-Source Stack**
```
VSCode + ARM Toolchain → OpenOCD → SWD Debugger (program/debug)
```

**Workflow 3: Online Editors**
```
STM32CubeIDE Web → Built-in compiler → Debug via IDE
```

### Key Debugging Capabilities

- **Breakpoints**: Suspend execution at specific code locations
- **Watch variables**: Inspect register and memory contents in real-time
- **Single-stepping**: Execute code line-by-line
- **Call stack**: View function call hierarchy and return addresses
- **Memory inspection**: Read/write SRAM, Flash, and peripheral registers

### Typical Development Cycle

1. **Configure MCU**: Use STM32CubeMX to define pins, clocks, peripherals
2. **Generate code**: CubeMX creates HAL initialization code
3. **Add application logic**: Write firmware in STM32CubeIDE or preferred IDE
4. **Compile**: Build project to generate ELF/HEX files
5. **Flash**: Use ST-LINK/V2 or J-Link to program Flash memory
6. **Debug**: Connect debugger, set breakpoints, inspect state

## Design Images

The following images provide visual documentation of the board design:

| Image | Content |
|---|---|
| `images/1.png` | Schematic overview or block diagram |
| `images/2.png` | Interface connectivity details |
| `images/3.png` | PCB layout preview |
| `images/7.png` | Additional design documentation |

*Images can be viewed directly in the repository or by opening files in an image viewer.*

## Future Improvements and Enhancements

The following items are planned or under consideration:

- [ ] **Manufacturing & Testing**
  - Prototype fabrication and functional validation
  - Assembly and test procedures

- [ ] **Documentation**
  - Detailed pinout and signal assignment tables
  - Schematic annotations and design rationale
  - Bill of Materials (BOM) with supplier information
  - Assembly guide and hardware setup instructions

- [ ] **Firmware & Examples**
  - STM32 HAL initialization code
  - USB communication drivers
  - CAN bus example applications
  - Micro-SD file system integration
  - GPIO and ADC sample projects

- [ ] **Hardware Variants**
  - Ultra-low-power variant
  - High-performance alternative
  - Industrial temperature range version

- [ ] **Accessories & Shields**
  - Motor control shield
  - Wireless communication modules
  - Sensor array expansion board

- [ ] **Design Enhancements**
  - 3D STEP models for mechanical integration
  - EMC/EMI optimization review
  - Power distribution improvements
  - Thermal management analysis

- [ ] **Community & Quality**
  - Design review feedback incorporation
  - Automated test suite
  - Performance benchmarking

## License

This project is released under the **MIT License**. See [LICENSE](LICENSE) for complete terms.

### Open-Source Hardware Notice

The MIT License covers all software, documentation, and design files in this repository. However, open-source hardware licensing involves additional considerations:

- This license grants permission to use, modify, and distribute the design files
- Hardware manufacturing and commercialization may involve patent implications
- Refer to the [Open Source Hardware Association (OSHWA)](https://www.oshwa.org/) for additional guidance
- For commercial use or manufacturing inquiries, contact the project author

## Author and Acknowledgments

**Author**: EJ-JATI Mohammed  
**Project Created**: August 2026  
**Repository**: [github.com/EJ-JATIMohammed/stm32-RedBoard](https://github.com/EJ-JATIMohammed/stm32-RedBoard)

### Credits and Resources

- **KiCad** – Open-source EDA suite
- **STMicroelectronics** – STM32 microcontroller family and documentation
- **Würth Elektronik** – Component reference designs and datasheets
- **ARM Holdings** – Cortex-M3 architecture specification
- **Open Source Hardware Association** – OSHWA standards and guidelines

## Contributing

Contributions, feedback, and suggestions are welcome! To contribute:

1. **Open an Issue** – Report bugs or suggest improvements
2. **Submit a Pull Request** – Share design enhancements or documentation improvements
3. **Provide Feedback** – Help improve the design and documentation

## Status

🔧 **Development Status**: Schematic design complete, PCB layout in progress  
📋 **Documentation Status**: Active development  
🧪 **Testing Status**: Pending prototype fabrication  

---

**Last Updated**: October 2026  
**KiCad Version**: 10.0 (version 20260306)

For questions or support, please open an issue on the GitHub repository.
