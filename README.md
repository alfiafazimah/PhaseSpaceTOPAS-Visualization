 # PhaseSpaceTOPAS-Visualization

## Project Overview
This repository is made in order to analyze and visualyze the phase space data from TOPAS Monte Carlo Simulation using python.

## Folder Structure
The folder is made within this structure
    PhaseSpaceTOPAS-Visualization
        data
            parameter
                put the topas code here
            input
                put the `.phsp` file here
            output
                store the output from `PhaseSpaceVisualization.ipynb`
        src
            code `PhaseSpaceVisualization.ipynb`

  ## Nomenclature for the `.phsp` Files
        Particle in orginal history: XXX
            Proton = 1 0 0
            Photon = 0 2 0
            Electron = 0 0 3
        
        Energy of the original history:
            XXX-XXX = 123,456
                note:     
                    MeV for 1 3 (Proton dn Electron)
                    MV for 2 (photon)
  
        Material of PHSP:
            MATX = MAT_KodeMaterial
            Kode Material Voxel:
            1 = Udara
            2 = Air (Water)
            3 = Metal
            4 = Spesifik material
            5 = Spesifik material
  
        Position Z of PHSP from 0,0,0 of the geometry (cm):
            Positive Z direction: (+XX_XX)
            Negative Z direction: (-XX_XX)
  
        Location of PHSP within a beamline component:
            (Phsp is placed after these component)
            XXXX = component code
            If not within the beamline component = XXXX
            The XXXX will be adjusted by the beamline component in the model
  
        The size of PHSP:
            Ukuran PHSP dalam X.Y
            Contoh 30x30=3030
  
  Example:
  Proton beam with 67.5 MeV scored in a PHSP, the material is air, in the position Z= -13.35cm 
  100_067-500_1-0_MAT1_-13_35-BFWP3030
  
## How to Use
1. Place the `.phsp` files in the `data/input/` folder. Note that the name of the `.phsp` files should be suitable with the nomenclature guideline
2. Run the `PhaseSpaceVisualization.ipynb` notebook in the `src` folder.
3. Processed results will appear in the `data/output/` folder.

## Requirements
- Python 3.9 or later
- Libraries: `topas2numpy`, `pandas`, `numpy`