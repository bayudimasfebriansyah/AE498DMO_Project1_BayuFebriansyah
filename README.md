## Setup

Use Python 3.12. Open a terminal in the repository folder and install the required packages:

```bash
python -m pip install numpy pandas scikit-learn torch matplotlib threadpoolctl ipython notebook
```

## Data

The dataset is not included in the repository. The notebook automatically downloads the original training and test files into `data/` when a model cell is first executed. Internet access is required for this download.

For offline use, download the files below and save them at these paths without modifying their contents:

- [training.csv](https://raw.githubusercontent.com/LuisM78/Appliances-energy-prediction-data/master/training.csv) → `data/author_training.csv`
- [testing.csv](https://raw.githubusercontent.com/LuisM78/Appliances-energy-prediction-data/master/testing.csv) → `data/author_testing.csv`

## Run the code

From the repository folder, open the notebook:

```bash
python -m notebook Project1_BayuFebriansyah_Code.ipynb
```

Select **Kernel → Restart Kernel and Run All Cells** to run all ten configurations. Each model cell can also be executed independently.

Results appear below each code cell and are saved in `results/run_01/` through `results/run_10/`. A summary of all ten configurations appears at the end of the notebook.
