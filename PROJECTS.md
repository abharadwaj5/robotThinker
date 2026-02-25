# Projects

## Cattle Health Monitoring System

### Summary
Currently leading end-to-end development of an IoT-based cattle health monitoring platform, owning the hardware lifecycle from early requirements through **production-ready deployment**. The system is being designed to reliably capture physiological and behavioral signals in the field, transmit device data for analysis, and support early detection of health issues through data-driven insights.

### What I Am Doing
- **Defining System Architecture:** Translating product requirements into a complete system design, covering sensing, power, processing, data storage, and connectivity.
- **Managing PCB Development End-to-End:** Driving the board from schematic and component selection through layout, prototyping, bring-up, and iterative improvements toward manufacturable hardware.
- **Building For Production-Ready Deployment:** Making design decisions that account for real-world constraints such as robustness, power efficiency, and repeatable production/testing workflows.
- **Enabling Data Pipelines For Analytics:** Structuring device data outputs to support downstream analysis and model training.

### Machine Learning and Health Insights
- Applying **machine learning techniques** to device data to extract meaningful patterns related to cattle health and activity.
- Generating **actionable insights** (e.g., abnormal behavior indicators, trend deviations) to support system decision-making and potential early intervention workflows.

### Current Focus / Direction
- Advancing the platform toward a reliable field-ready design while connecting embedded telemetry to ML-driven interpretation, turning raw signals into practical health indicators.

---

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

## Smart Irrigation and Soil Analysis Using Raspberry Pi and IoT

### Summary
Developed an IoT-based smart irrigation and soil monitoring system using a **Raspberry Pi** as the central processing and control unit. The system continuously measured key environmental and soil parameters and used those readings to automate irrigation, while also generating cloud-hosted datasets that can help infer **soil characteristics** and support data-driven agricultural decisions.

### System Goals
- **Smart Irrigation Automation:** Irrigate only when needed based on soil moisture and surrounding conditions.
- **Soil Understanding Through Data:** Use multi-sensor trends (before/after irrigation, environmental changes) to better understand soil behavior and potential soil type indicators.
- **Decision Support For Farmers:** Enable cloud-based reporting that could be shared with agricultural departments to guide farmers on **crop suitability**, irrigation scheduling, and soil management.

### Sensors and Hardware
- **Soil Moisture Sensor:** Primary driver for irrigation decisions.
- **Temperature Sensor:** Tracks ambient conditions influencing evapotranspiration.
- **Humidity Sensor:** Adds environmental context for moisture loss and irrigation timing.
- **Raspberry Pi:** Sensor acquisition, decision logic, and actuator control.

### Cloud Data Pipeline
- Integrated with a **MATLAB-based ThingSpeak module (ThingSpeak UTI)** to upload and visualize sensor data on the cloud.
- Created time-series datasets (sensor readings before/after irrigation events) to support analysis of:
  - **Moisture Retention Behavior**
  - **Environmental Influence (Temperature/Humidity)**
  - **Irrigation Response Patterns** relevant to soil characterization

### Irrigation and Actuation Logic
- Implemented irrigation using **Timed Relay Actuation**, enabling controlled water delivery based on sensor thresholds and predefined time windows.
- Coordinated irrigation events with sensor logging to reduce overwatering and improve repeatability in collected data.

### Integrated Fertigation Feature (Irrigation + Fertilizer In One System)
- Extended the same irrigation hardware (Relays + Pipelines) to also deliver **Fertilizer** without requiring a separate system.
- When fertilization was needed, the system automatically mixed **Water + Fertilizer** at a **60:40 ratio** using calibrated relay timing.
- The mixed solution was then delivered through the **Same Relays** and **Same Irrigation Pipelines**, enabling fertilization to occur as part of the normal irrigation cycle.

### Impact, Use Case, and Future Extensions
This project demonstrates how low-cost sensing + cloud monitoring can be used not only for automated irrigation, but also for **Soil Behavior Profiling**. By sharing the collected datasets with agricultural departments or advisory services, farmers can receive guidance on:
- **Crop Suitability** for local soil conditions
- **Irrigation Frequency Recommendations**
- **Soil Management Strategies** based on measured trends

A natural next step is integrating additional soil-quality sensors such as an **NPK Sensor (Nitrogen, Phosphorus, Potassium)** to better quantify nutrient availability and further improve soil classification and crop planning recommendations.

---

