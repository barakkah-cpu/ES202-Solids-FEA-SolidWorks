# ES202 — Solids FEA & SolidWorks

Structural analysis of a real STOP sign on the ERAU Daytona Beach campus — from physical measurements and wind load estimation to pole design, material selection, and FEA validation in SolidWorks. Completed as part of ES 202, Mechanics of Materials (Honors) Coursework, Spring 2026.

## Project Overview
The goal was to treat a campus STOP sign as a real engineering design problem: measure it, load it, design the support pole to survive it, and validate the design with finite element analysis. Every decision from material choice, wind load method, to factor of safety is justified against engineering standards.

## Deliverables
### 1. STOP Sign Measurements & Wind Load Estimation
**Folder:** `stopsign-wind-load-calculations/`

A STOP sign on campus was physically measured and modelled in SolidWorks. Wind loading was estimated using two independent methods and compared:

| Method | Result |
|--------|--------|
| Bluff Body Drag Equation | 273.3 lb |
| ASCE 7 Standard | 164.2 lb |
| Percentage Difference | ~50% |

**Design load chosen: 164 lb (ASCE 7)** — selected because it accounts for boundary layer effects, wind directionality (Kd = 0.85), and gust response, making it more physically realistic than the bluff body approximation.

Compliance with City of Daytona Beach engineering standards was also verified:
- Sign shape, material, and thickness per MUTCD Note 2 ✓
- Pole diameter (measured at 3 in) per Note 4 ✓
- Clearance from pavement edge (measured at 8 ft, minimum 6 ft) per Note 6 ✓
- Wind load capacity per Note 7 ✓

### 2. Pole Design & FEA Validation
**Folder:** `stopsign-pole-design/`

Using the ASCE 7 wind load as the design input, the support pole was fully specified:

**Material:** ASTM B221 6061-T6 Aluminum
- Yield strength: 35,000 psi
- Ultimate tensile strength: 42,000 psi
- Selected for corrosion resistance in Daytona Beach's coastal environment

**Factor of Safety:** FS = 2 applied to yield strength (permanent deformation is the failure condition, not fracture.)

**Outcome:** Minimum required wall thickness calculated, then matched to a commercially available 2.5" OD aluminum tube sourced from McMaster-Carr.

### 3. SolidWorks Model
**Folder:** `solidworks-model/`

3D solid model and 2D engineering drawing of the STOP sign system built in SolidWorks. Includes critical dimensions and compliance annotations.

> **Note:** `.SLDPRT` and `.SLDDRW` files require SolidWorks to open. Screenshots of the model and FEA results are not included in this repo.

## Repository Structure
```
ES202-Solids-FEA-SolidWorks/
├── stopsign-wind-load-calculations/
│   └── ES202_HON_Mini_Project_2A_Measurement_and_Load_Estimation.pptx
├── stopsign-pole-design/
│   └── miniproject_2b.pptx
├── solidworks-model/
│   ├── Miniproject_2a.SLDPRT
│   └── Miniproject_2a.SLDDRW
└── README.md
```
## Tools Used
- SolidWorks (3D modelling, FEA simulation)
- ASCE 7 wind load standard
- Hand calculations (bending stress, factor of safety, wall thickness)

## Author
**Barakkah Ibishomi**  
Aerospace Engineering, Embry-Riddle Aeronautical University  
ES 202 — Mechanics of Materials (Honors), Spring 2026
