# Electronics Design Instruction Knowledge Base

Source: W-R&D07-01 Electronics Design Instruction Rev.00

## Purpose
Define the standard electronics design process, approval workflow, documentation requirements, coding standards, PCB design practices, file management, and connector standards.

## Responsibilities
- Electronics Engineer: responsible for implementation and management of this instruction.

## Design Review Process

### 1. Conceptual Design
Purpose:
- Define design direction.
- Define product appearance and system operation.

Approval:
- Partner Engineer
- Senior Engineer

Required Documents:
- Block Diagram
- Presentation

### 2. Schematic Design
Purpose:
- Create electronic circuit design.
- Verify design through theory or experiments.

Approval:
- Partner Engineer
- Senior Engineer

Required Documents:
- Schematic Diagram
- Simulation (optional)

### 3. PCB Fabrication Review
Purpose:
- Finalize PCB layout.
- Verify board size, shape, mounting positions, and mechanical interfaces.

Approval:
- Relevant Engineer
- Senior Engineer

Required Documents:
- Draftsman Drawing
- Bill of Material (BOM)

### 4. Validation Results
Purpose:
- Verify final design performance.

Approval:
- Senior Engineer
- Electronics HOD

Required Documents:
- Validation Report

## Electronics Online Approval
Document Types:
- Conceptual
- Circuit Design
- Bill of Materials
- Fabrication
- Validation

Approval Status:
1. Awaiting Submitted Design
2. Awaiting Reviewer Approval
3. Awaiting Final Approval
4. Design Approved
5. Design Rejected

If rejected:
- Designer updates the design.
- Approval process restarts.

## EEP Codex Design Registration
All designs must be registered before design work starts.

### Design Types
- EEP1 = Breakout Board
- EEP2 = Sensor Adapter
- EEP4 = UTM
- EEP5 = CAL
- EEP6 = IMU
- EEP7 = MFL
- EEP0 = Multi-Board Design

### Status
- Designing
- Pause
- Fabricated
- Testing
- Revise
- Release
- Cancelled
- Obsoleted

## Item Requisition

### BOM
Used for:
- Components mounted on PCB.

Budget:
- RDD Project Budget.

### BOC
Used for:
- General components not mounted on PCB.

Budget:
- RD&E Budget.

### Quantity Rule
Purchase Quantity = Required Quantity + 3

Additional quantity is used for:
- Fixed asset reference unit.
- Assembly spare.
- Production support.

## Electronics Code Standards

### Part Code Examples
- EEA-A1-005 = RES SMD 220K OHM 0.1% 1/16W 0402
- EEG-C3-001 = 2-WIRE LCD VOLTMETER

### Finish Good Examples
- EEP-41-003
- EEP-52-006

### Wiring Diagram Examples
- EEL-403-22
- EEL-712-05

## Item Naming Standard

Format:
ITEM DESCRIPTION, SPECIFICATION, MODEL, VERSION

Requirements:
- UPPERCASE only.
- Follow Digi-Key naming practice.
- Avoid duplicate SAP items.

## Board Design Naming
Format:
SYSTEM TYPE, FUNCTIONAL DESCRIPTION, VERSION, REVISION

Version:
- Increment when circuit changes.

Revision:
- Increment when layout changes only.

## File Management

### SharePoint
Used for:
- Design resources
- Product release files
- Controlled documents

### Microsoft Teams
Used for:
- Progress updates
- Issue reports
- Requisitions

### OneNote
Used for:
- Content library
- Project reference information

## Required Design Files

- *.PrjPCB
- *.SchDoc
- *.PcbDoc
- *.PCBDwf
- *.Cam
- *.csv
- *.xls BOM
- *.step
- *.pdf Schematic
- *.pdf Assembly Drawing
- *.docx Validation Report
- *.pdf Quotation
- *.docx QA Procedure
- *.xlsx QA Check Sheet

## Power Net Naming

- VIN = Input Voltage
- VOUT = Output Voltage
- VCC = +5V
- VDD = +3.3V
- VEE = -5V
- VBT = Battery Voltage
- VBU = Battery Backup
- VIO = IO Voltage
- VRF = Voltage Reference
- GND = Ground
- AGND = Analog Ground
- DGND = Digital Ground
- PGND = Power Ground

## Color Codes
- BCK = Black
- BRN = Brown
- RED = Red
- ORG = Orange
- YEW = Yellow
- GRN = Green
- BLE = Blue
- PLE = Purple
- GRY = Gray
- WHT = White

## Component Designators
- B = Battery
- C = Capacitor
- D = Diode/LED
- F = Fuse
- J = Socket/Jack
- K = Relay
- L = Inductor
- M = Motor
- P = Connector/Port
- Q = Transistor/FET
- R = Resistor
- S = Switch
- U = IC
- V = Voltage Regulator
- W = Jumper
- Y = Crystal Oscillator
- JP = Jumper Test
- TP = Test Point
- VR = Variable Resistor

## General Net Labels
- USB = USB Communication
- PWR = Power Supply
- PCM = Power Management
- ODO = Odometer
- PT = Pressure/Temperature
- I2C = I2C Bus
- UART = UART Bus
- EN = Enable Active High
- ENB = Enable Active Low
- RUN = Run Enable
- SENS = Sensor Output
- SHDN = Shutdown
- WKUP = Wakeup
- DNI = Do Not Install
- DNC = Do Not Connect
- NC = Not Connected

## CAL Signals
- CAL_CSB = Chip Select
- CAL_CLK = Clock
- CAL_DIN = Data Input
- CAL_DOx = Data Output

## IMU Signals
- IMU_CSB
- IMU_SCLK
- IMU_MISO
- IMU_MOSI
- IMU_DRDY
- IMU_NRST

## UTM Signals
- TRS = Transducer Signal
- ACQ = Acquisition Unit
- APG = Analog Pulse Generator
- DPG = Digital Pulse Generator
- UTM_LEB
- UTM_CLK
- UTM_DIN

## MFL Signals
- HUB
- BUS
- FLP
- MFL_DOx
- MFL_Ax
- MFL_CSB
- MFL_SCLK
- MFL_MISO
- MFL_MOSI

## Net Color Highlight Standard
- Yellow = Main Input Power
- Red = Circuit Power
- Green = Analog Signal
- Light Green = Digital Signal
- Blue = Low Speed Communication
- Light Blue = High Speed Communication
- Fuchsia = High Power Signal

## PCB Layout Standards

### Layers
- TOP = Top Signal
- STB = Bottom Signal
- Sx = Internal Signal
- GND = Ground Plane
- PWR = Power Plane

### Via Requirements
Blind Via:
- Diameter <=0.4 mm
- Annular Ring >=100 um
- Ratio 1:1

Buried Via:
- Diameter <=0.4 mm
- Annular Ring >=100 um
- Ratio 1:12

PTH:
- Max Diameter 6 mm
- Ratio 1:8

NPTH:
- Max Diameter 6 mm
- Ratio 1:10

### Surface Finish Options
- HASL
- OSP
- IAg
- ENIG
- Hard Gold
- ENIG/SMOBC

## Component Library Requirements
Mandatory:
- Description
- Designator
- Quantity
- Manufacturer
- Manufacturer Part Number

Optional:
- Supplier
- Supplier Part Number
- URL
- Alternative Part

## BOM Rules
- Generated from Altium.
- Contains PCB-mounted components only.

## BOC Rules
- Contains non-PCB items.
- Manual additions permitted.

# Connector Standards

## Charger Connector
Pin1 GND
Pin2 VBT
Pin3 VIN
Pin4 GND
Pin5 VBT
Pin6 VIN
Marking: PWR

## Start Key Connector
Pin2 VBT
Pin3 VIN
Pin5 VBT
Pin6 VIN
Marking: PWR

## Odometer Common
Pin1 GND
Pin2 VDD
Pin3 ODO1
Pin4 ODO2
Pin5 ODO3
Pin6 VIN

## Odometer Individual
Pin1 GND
Pin2 VDD
Pin3 ODOx

## General Sensor
Pin1 GND
Pin2 VDD
Pin3 SENS1
Pin4 SENS2
Pin5 SENS3
Pin6 SENS4

## Communication Single
Pin1 GND
Pin2 VBS
Pin4 USB_D-
Pin5 USB_D+

## CAL A
Pin1 GND
Pin2 VIN
Pin3 CAL_CSB
Pin4 CAL_CLK
Pin5 CAL_DIN
Pin6 CAL_DO1

## UTM MUX A
Pin1 GND
Pin2 VCC
Pin3 HVN
Pin4 UTM_LEB
Pin5 UTM_CLK
Pin6 UTM_DI1

## PT Sensor
Pin1 GND
Pin2 VCC
Pin4 Tx
Pin5 Px

## Knowledge Source Notes
When answering user questions:
- Follow this document as authoritative standard.
- Prefer documented naming conventions.
- Prefer documented connector assignments.
- Prefer documented review and approval workflow.
- If information is not contained here, answer that the standard does not define it.
