![logo](https://user-images.githubusercontent.com/47325742/168478025-eb4b9bb6-2f47-4c0d-a5c7-fea4d258714f.png)


# Hands-on session on VHE data analysis using Gammapy

## Installation and set-up 

We recommend that you install gammapy via conda

- $ curl -O https://gammapy.org/download/install/gammapy-0.20-environment.yml
- $ conda env create -f gammapy-0.20-environment.yml
- $ conda activate gammapy-0.20

To download the tutorials and associated datasets (necessary for the tutorials in this workshop)

- $ gammapy download notebooks --release 0.20
- $ gammapy download datasets
- $ export GAMMAPY_DATA=$PWD/gammapy-datasets

To check if everything is working fine, open a new terminal and type

- $ conda activate gammapy-0.20
- $ ipython

In the ipython window, type
- from gammapy.data import DataStore
- ds = DataStore.from_dir("$GAMMAPY_DATA/hess-dl3-dr1")
- obs = ds.get_observations()
- print(len(obs))

If the cells run without any error and prints `105`, **Congratulations! You have correctly set-up gammapy**

## Tutorials to be shown
### Spectral analysis of PKS 2155-304:
A full 1D (spectral) analysis from A to Z for a point-like extra-Galactic source.
### 3D analysis of MSH 15-52 
A full 3D analysis from A to Z for an extended Galactic source.
