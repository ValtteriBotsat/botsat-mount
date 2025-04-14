# BotSat Mount

A parameterized 3D printable mount designed for the [Val1 BotSat project](https://www.k-si.com/projects/botsat/). This mount is specifically designed to fit inside a Fanta Exotic 1.5L bottle and securely hold a perfboard for the BotSat electronics.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ValtteriBotsat/botsat-mount/HEAD?urlpath=lab/tree/botsat.ipynb)

## Features

- Parameterized design that can be adjusted for different bottle sizes
- Threaded holes for M4 screws to secure the mount to the bottle
- Central hole to reduce weight
- Flat bottom with mounting points for perfboard
- Reinforced mounting points with flat surfaces for better load distribution

## Usage

The mount is created using CadQuery and can be customized by modifying the parameters in the Jupyter notebook:

- `bottle_dia`: Diameter of the bottle (default: 89mm)
- `wall_height`: Height of the mount walls (default: 20mm)
- `wall_thickness`: Thickness of the mount walls (default: 5mm)
- `perfboard_dim`: Dimensions of the perfboard (default: 46x66mm)
- `perfboard_padding`: Padding around the perfboard (default: 7mm)
- `central_hole_dia`: Diameter of the central hole (default: bottle_dia/1.5)

## Running the Notebook

You have several options to run the notebook:

### Option 1: Run Online (Recommended)
Click the "launch binder" badge above or paste this link into your browser

https://mybinder.org/v2/gh/ValtteriBotsat/botsat-mount/HEAD?urlpath=lab/tree/botsat.ipynb

to run the notebook in your browser for free using MyBinder.org. No installation required!

### Option 2: Local Installation
1. Install the dependencies from `environment.yml`:
   ```bash
   conda env create -f environment.yml
   conda activate jupyter-cadquery
   ```
2. Start Jupyter Lab:
   ```bash
   jupyter lab
   ```

### Option 3: Using repo2docker
1. Install repo2docker:
   ```bash
   pipx install jupyter-repo2docker
   ```
2. Build and run the container:
   ```bash
   jupyter-repo2docker .
   ```

## Requirements

- Python 3.10+
- CadQuery 2.2
- Jupyter CadQuery 3.5.2
- cq_warehouse (for standard parts)

## Getting Started

1. Open `botsat.ipynb` in Jupyter Lab
2. Adjust the parameters to match your bottle and perfboard dimensions
3. Run the notebook to generate the 3D model
4. Export the model as an STL file for 3D printing

## Hardware Requirements

- M4 screws for securing the mount to the bottle
- Perfboard (default size: 46x66mm)
- Fanta Exotic 1.5L bottle (or similar diameter bottle)

See www.k-si.com/projects/botsat for more info.

## License

This project is open source and available under the MIT License.
