# Projects

## SkillForAction (Horizon 2020)
**Virtual Driver Model** for harvesting scenarios and prediction of fuel consumption and CO2 emissions  
Website: https://etnskillforaction.com/

### Summary
Built and integrated discrete-event simulation components as part of an experimentable digital twin environment for forestry operations.

### What I did
- Designed discrete-event simulations of harvesting tasks, including individual harvester operation.
- Integrated real machine data (CAN-bus, positional data, joystick logs) for accurate time synchronization.
- Built a modular simulation testbed with interacting machine, forest, and terrain models.
- Ran scenarios and extracted metrics to support estimation/validation of fuel and emissions models.

### Digital Twin Components
- **Forest Digital Twin (FDT):** tree dimensions/species + geo-location
- **Terrain Digital Twin (TDT):** terrain models (DTM), slope, soil type/moisture
- **Machine Digital Twin (MDT):** operational logic + telemetry (rpm, fuel usage, torque)

### Publications
- **Virtual reality and Digital Twins for the Simulation of Forestry Operations:** Abhay Bharadwaj, Arthur Wahl, Juergen Rossmann, Translated to Italian by Stefano Grigolato for Sherwood - Foreste Ed Alberi Oggi, March - April, 2023 | 263
**https://www.rivistasherwood.it**
- **Prediction of Fuel Consumption in Forest Machines with the Application of Experimentable Digital Twins:** Abhay Bharadwaj, Michael Schluse, Arthur Wahl, Juergen Rossmann, ESM (European Simulation and Modelling Conference), October 2023 
**https://doi.org/10.5281/zenodo.16737969**


---

## OUTREACH
Website: https://www.mmi.rwth-aachen.de/projekt/outreach/

### Summary
Coordination of heterogeneous forestry machines (e.g., harvesters with different crane arm lengths) operating in the same environment, aiming to reduce overlap and improve efficiency.

### What I did
- Reconstructed a realistic simulation of a harvested forest site.
- Designed experiments with two harvesters with varied reach capabilities.
- Modeled coordination logic for task allocation and spatial positioning.
- Evaluated efficiency using travel time and task distribution metrics.

---

## Clean Room Calibration of PM Sensor for Pollution Monitoring (Embedded Systems + Sensor Fusion)

### Summary
Designed and built a stand-alone particulate matter (PM) sensing system to evaluate and calibrate **low-cost PM sensors** across controlled and real-world conditions. I initially benchmarked two affordable options, **Shinyei PPD2NS** and **Sensirion SPS30**. After comparative testing, **SPS30 demonstrated stronger performance and more consistent outputs**, so I selected it as the primary sensor for calibration and validation against **Particle Technology dust/reference measurements**.

### Embedded System Design
- Implemented the sensing platform using an **Arduino Uno (ATmega microcontroller)** as the main acquisition and control unit.
- Developed **register-level firmware** (beyond high-level libraries) to achieve deterministic timing and reliable sampling.
- Built a repeatable logging workflow to capture stable datasets suitable for calibration experiments.

### Sensor Fusion and Data Handling
- Acquired readings from multiple PM sensors during the evaluation phase and used **register-level, timing-aligned sampling** to compare them under identical conditions.
- Applied firmware-side filtering and fusion-style processing to reduce noise and improve repeatability during data capture.
- Analyzed calibration datasets using **OriginLab**, deriving **Gaussian curves** and performing curve fitting to extract fitting characteristics and calibration parameters that supported the final accuracy results.

### Calibration Methodology
1. **Sensor Evaluation (Low-cost selection)**
   - Tested and compared **PPD2NS vs SPS30** to identify the more stable and accurate sensor for calibration work.
2. **Cleanroom Calibration**
   - Calibrated the **SPS30** in a cleanroom environment to establish a controlled baseline and reduce environmental variability.
3. **Vacuum Desiccator Calibration (Regular Environment)**
   - Performed additional calibration inside a **vacuum desiccator** to study sensor behavior under controlled humidity/particle conditions while reflecting practical operating environments.
4. **Reference Comparison**
   - Compared calibrated outputs against **Particle Technology** dust/reference measurements to quantify accuracy.

### Validation and Results
- Achieved approximately **~95% match** between cleanroom-calibrated SPS30 data and **Particle Technology** certified reference data.
- Reported **>90% calibration accuracy** across calibration scenarios after applying calibration + fitting.

### Key Takeaways
- Demonstrated how **embedded firmware choices** (register-level control and deterministic sampling) directly improve measurement quality.
- Showed that selecting the right low-cost sensor (SPS30) and combining **multi-environment calibration** with **Gaussian fitting in OriginLab** leads to robust, validated PM monitoring performance.

---

## Analog Devices Projects

### Storage Devices (Process Development)
- Optimized 8-inch wafer manufacturing via experimentation with chemical compositions.
- Achieved smoother material deposition and improved packaging outcomes through controlled process changes.

### Isolator (Cost Reduction via Layout Improvements)
- Reduced die spacing on wafers through design changes.
- Resulted in **~15% cost reduction**.

### DNA Sensor (Design + Tape-out)
- Led design and tape-out of a wafer-level DNA sensor using **Cadence Virtuoso**.
- Focused on via design for intermetallic connections.
- Contributed to development of commercial wafer output.

---

## Bachelor Thesis: Smart Irrigation using Raspberry Pi and IoT
### Summary
Built an irrigation system using soil moisture, temperature, and pH sensors, with relay-based automation through a Raspberry Pi and cloud-based monitoring.

### Notable Feature
Mixed “water” and “medicine” in a **60:40 ratio** using timing across two relay-controlled flows.
