 # PhaseSpaceTOPAS-Visualization

## Project Overview
This repository is made in order to analyze and visualyze the phase space data from TOPAS Monte Carlo Simulation using python.

## Folder Structure
    The folder is made within this structure
       * PhaseSpaceTOPAS-Visualization
            * data
                * parameter
                    put the topas code here
                * input
                    put the `.phsp` file here
                * output
                    store the output from `PhaseSpaceVisualization.ipynb`
            * src
                code `PhaseSpaceVisualization.ipynb`

  ## Nomenclature for the `.phsp` Files
        Particle in orginal history: XXX
            Proton
            Photon 
            Electron 
        
        Energy of the original history:
            XXX-XXX = 123,456
                note:     
                    MeV for charged particle
                    MV for photon
  
        Material of PHSP:
            Example: 
            Udara
            Air (Water)

  
        Position Z of PHSP from 0,0,0 of the geometry (cm):
            Positive Z direction: (+XX_XX)
            Negative Z direction: (-XX_XX)
  
        BeforeAfter:
            Before = if the phase space is used to analyze the beam before a component
            After = if the phase space is used to analyze the beam after a component

        Component:
            Naming based on the component name
  
        The size of PHSP:
            Size of PHSP in X.Y (cm)
            Example 30x30=3030
  
  Example:
  Proton beam with 67.5 MeV scored in a PHSP, the material is air, in the position Z= -13.35cm before water phantom
  Proton_67,5MeV_Udara_(-13_35)_Before-Before_WaterPhantom_Defult_3030
  
## How to Use
1. Place the `.phsp` files in the `data/input/` folder. Note that the name of the `.phsp` files should be suitable with the nomenclature guideline
2. Run the `PhaseSpaceVisualization.ipynb` notebook in the `src` folder.
3. Processed results will appear in the `data/output/` folder.
4. More detail of manual instruction in Bahasa is available in [here](https://github.com/alfiafazimah/PhaseSpaceTOPAS-Visualization/blob/main/manual/Manual.md)

## Requirements
- Python 3.9 or later
- Libraries: `topas2numpy`, `pandas`, `numpy`, `matplotlip`, `plotly`