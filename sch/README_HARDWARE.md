# StarMiner BitaxeGamma601a V1.0 Hardware Design Documentation

## Project Introduction

This directory contains the hardware design resources for the StarMiner BitaxeGamma601a V1.0 DC 12V board. The hardware design files are released under the CERN-OHL-S-2 open hardware license.

The current hardware package provides native PADS schematic and PCB source files, an updated schematic PDF preview dated 2026-06-30, and Gerber manufacturing outputs.

## Design Software

This hardware design is developed with the PADS VX series EDA toolchain, not KiCad.

The CERN-OHL-S-2 license does not require a specific EDA application. Its key requirement is that the editable design source files needed for study, modification, and reproduction are provided. For this release, the editable native sources are the PADS `.sch` and `.pcb` files in this directory.

## Hardware File Inventory

```text
sch/
|-- README_HARDWARE.md
|-- bitaxeGamma601a_V1.0.sch          # Editable PADS schematic source
|-- bitaxeGamma601a_V1.0.pcb          # Editable PADS PCB layout source
|-- bitaxeGamma601a_V1.0_20260630.pdf # Static schematic preview for the DC 12V design
`-- gerbers/                          # PCB fabrication outputs exported from the PADS design
    |-- Routing-Top.pho
    |-- Routing-Bottom.pho
    |-- Routing-POWER.pho
    |-- Routing-GND.pho
    |-- Solder-Top.pho
    |-- Solder-Bottom.pho
    |-- Paste-Top.pho
    |-- Paste-Bottom.pho
    |-- Silkscreen-Top.pho
    |-- Silkscreen-Bottom.pho
    |-- Drill.pho
    |-- NC Drill.drl
    |-- NC Drill.lst
    `-- *.rep
```

## Design Notes

- Target board: StarMiner BitaxeGamma601a V1.0.
- Power input: DC 12V board design.
- Main ASIC family referenced by the source files: BM1370.
- Controller module referenced by the source files: ESP32-S3-WROOM-1.
- Main power stage referenced by the source files: TPS546D24ARVFR.
- The PDF file is only a static preview and is not a substitute for the editable PADS source files.
- The Gerber files are manufacturing outputs generated from the PADS PCB design. Verify stackup, drill data, panelization, and fabrication requirements with the PCB vendor before production.

## CERN-OHL-S-2 Compliance Statement

1. The editable hardware sources for the current design are provided as native PADS files: `bitaxeGamma601a_V1.0.sch` and `bitaxeGamma601a_V1.0.pcb`.
2. The exported PDF is provided only for quick browsing and review. It is not an editable source file.
3. The `gerbers/` directory contains fabrication outputs and related report files. These files help manufacture the board but do not replace the editable source files.
4. Anyone modifying and distributing derivative hardware based on this design must comply with the CERN-OHL-S-2 license terms, including disclosure of the corresponding source files.

## Resource Links

- Full hardware repository: https://github.com/awxhw/StarMiner
- Schematic PDF preview: https://github.com/awxhw/StarMiner/blob/master/sch/bitaxeGamma601a_V1.0_20260630.pdf

## Important Notes

1. Use PADS VX series software to open and edit the `.sch` and `.pcb` source files.
2. Treat `bitaxeGamma601a_V1.0.sch` and `bitaxeGamma601a_V1.0.pcb` as the authoritative editable design sources for this hardware release.
3. Treat the PDF as a preview document only; do not use it as the source for derivative hardware work.
4. Review all manufacturing outputs in `gerbers/` before ordering PCBs.
5. If you have questions about license compliance, source completeness, or hardware design files, please open an issue in this repository.