# Emulation strategies for Bayesian inference of regional left ventricle material parameters

The repository is organised by research purpose. It includes code for emulator training and testing, Gaussian-process modelling, experimental design, synthetic disease scenarios, analysis of a clinical volunteer case, left-ventricular mesh visualisation, and preparation of manuscript figures.

The repository also retains exploratory files that were important during model development, even where their results were not included in the final manuscript.

## Repository structure

### Path Description

- `5.2/`  Results and supporting analyses for Section 5.2 of the JRSSC manuscript, where the candidate emulators were assessed and an emulator was selected for subsequent inference. 
- `ACase/`  Data, results, and analysis for a clinical example. 
- `CheckPoint/`  Saved parameters and checkpoint files for trained emulator models. 
- `DiseaseScenarios/`  Data and results for the simulated local disease scenarios used in the manuscript. These files contain the synthetic regional stiffening examples and their associated analyses. 
- `FinalPlots/`  Final or near-final figures produced for manuscript visualisation. 
- `GP_functions/`  Gaussian-process model implementations and supporting code for model construction, training, prediction, and related utilities. 
- `LVmeshV/`  Data and code used to visualise the left-ventricular geometry and mesh structure. 
- `PythonFile/`  Python scripts used on the computing server to train, test, and compare emulator models. 
- `SimulationData/`  Finite-element simulation data generated from the Abaqus implementation of the left-ventricular Holzapfel–Ogden constitutive model. These data were used to train and test the emulators. 
- `TestFiles/`  Exploratory analyses and model-development experiments. Most of these results do not appear directly in the manuscript, but they contributed to the development, validation, and refinement of the analysis pipeline. 

## Notebooks


- `Data.ipynb`  Experimental-design code used to construct or prepare the parameter samples for simulation and emulator development. 
- `Delete_tiff.ipynb`  Utility notebook used during file and image management. 
- `Docu.ipynb`  Early documentation of the analysis strategy and approximate workflow. It records how many of the main code components were intended to be used during the initial stages of the project. 
- `LocalDisease_submission_figures.ipynb`  Analysis and visualisation code for the simulated local disease scenarios and the corresponding submission figures. 
- `lv_ed_reference_visualization.ipynb`  Code for visualising and analysing the end-diastolic left-ventricular reference geometry.
- `Plot.ipynb`  Earlier plotting and figure-development code used during preliminary analysis.


## Software dependencies


- Python 3 and Jupyter
- PyTorch, GPyTorch and Pyro
- NumPy, pandas, SciPy, scikit-learn, and joblib
- Matplotlib, seaborn, statsmodels, ArviZ, and tqdm
- PyVista and Pillow for the LV mesh visualisation notebooks

Abaqus was used to generate the finite-element simulation data stored in `SimulationData/`.


## Path and reproducibility note

The repository was reorganised by research purpose without changing the contents of existing code, notebooks, data, results, checkpoints, or logs. Consequently, some historical scripts still contain paths that refer to the former directory layout or assume a particular working directory.

## Path and reproducibility note

The repository was reorganised by research purpose without changing the contents of existing code, notebooks, data, results, checkpoints, or logs. Consequently, some historical scripts still contain paths that refer to the former directory layout or assume a particular working directory.

Some data-loading paths are therefore no longer valid without modification. Before running an archived script or notebook, update its input and output paths to match the current repository structure.

The model definitions and reusable modelling functions remain available for direct import. For example, code in `GP_functions/` can be imported after adding the repository root to the Python path or installing the repository as a local package.

Large `.pth`, `.pt`, and `.pkl` files are saved model, posterior, or intermediate analysis artifacts rather than source code. Their interpretation depends on the model architecture, preprocessing steps, and object definitions used when they were created.

## Citation

The complete article citation and DOI will be added here if the manuscript is accepted and published.

