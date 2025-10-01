# TZ-OSeMOSYS-STEEL

TZ-OSeMOSYS-STEEL is an open-source energy systems model of Japan’s steel sector developed by TransitionZero. The model optimises the capacity expansion and operation of steel assets in Japan to meet steel production demand at least cost while adhering to a set of resource constraints and policy targets.

TZ-OSeMOSYS-STEEL is designed to be replicable in other countries and regions; scalable to different spatial resolutions from asset- to national-level. Therefore, it can increase transparency and accessibility of system modelling for the global steel sector, a significant source of emissions.

The model framework underpinning TZ-OSeMOSYS-STEEL is [TZ-OSeMOSYS](https://github.com/transition-zero/tz-osemosys). It is a modern, open-source energy systems modelling framework designed for long-run analysis and planning. Developed by TransitionZero as a pip-installable Python package, it is a re-built version of the [original OSeMOSYS (Open Source Energy Modelling System)](https://github.com/OSeMOSYS/OSeMOSYS).

TZ-OSeMOSYS-STEEL is available under an AGPL open-source license. It was developed based on work done by [Anthea Lam](https://www.linkedin.com/in/anthealamiweng/) during her [MSc thesis at TransitionZero for Imperial College London during the summer of 2024](https://www.imperial.ac.uk/energy-futures-lab/study/annual-conference/sustainable-energy-futures-annual-conference-2024/research-themes/decarbonising-industry/). We are grateful for her work and will continue to build on it. Please note that this repository will not be continuously maintained until additional funding is secured to adequately resource it. 

## Overview

TZ-OSeMOSYS-STEEL is a modeling framework for optimizing steelmaking pathways in Japan up to 2060, supporting decarbonization goals based on least-cost and climate constraints.

## Repository Structure

- `config/`: Scenario configuration files (YAML) for different decarbonization pathways.
- `*.csv`: Input data files (emissions, capacities, costs, etc.).
- `*.ipynb`: Jupyter notebooks for data processing, scenario analysis, and visualization.
- `README.md`: This file.

## Prerequisites

- Python 3.8+
- [pip](https://pip.pypa.io/en/stable/)
- [Jupyter Notebook](https://jupyter.org/)
- Recommended: Create a virtual environment

## Installation

1. **Clone the repository:**
   ```sh
   git clone https://github.com/transitionzero/tz-osemosys-steel.git
   cd tz-osemosys-steel
   ```

2. **(Optional) Create and activate a virtual environment:**
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```sh
   pip install tz-osemosys pandas numpy jupyter matplotlib pyyaml highspy
   ```

## Usage

### 1. Prepare Data

Ensure all required CSV files are present in the root directory. Scenario configurations are in `config/japan/<scenario>/description.yaml`.

### 2. Run Jupyter Notebooks

Start Jupyter Notebook:
```sh
jupyter notebook
```
Open and run the notebook:
- `test_model.ipynb`

These notebooks guide you through data preparation, scenario setup, and model execution.

### 3. Modify or Add Scenarios

Edit or add scenario YAML files in `config/japan/` as needed. Each scenario folder (e.g., `high-lc`, `medium-nz-scope3`) contains a `description.yaml` file describing the scenario.

### 4. Analyze Results

Model outputs and processed data are saved as CSV files in the root directory. Use the provided notebooks to visualize and analyze results.

## Support

For questions or issues, please open an issue on the [GitHub repository](https://github.com/transitionzero/tz-osemosys-steel).

## License

See `LICENSE` file for details.
