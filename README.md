# Data access and execution

## 1. Install the dependencies

Use Python 3.12. Open a terminal in the project folder and run:

```powershell
py -3.12 -m venv .venv
.venv\Scripts\python -m pip install -r requirements.txt
```

On macOS/Linux, use `python3.12` instead of `py -3.12` and `.venv/bin/python` instead of `.venv\Scripts\python`.

## 2. Import the data

The first model cell automatically downloads the original training and test CSV files into `data/`. An internet connection is required for this first download.

To download the data manually, create a `data` folder inside the project folder and save these files with the names shown:

| Download | Save as |
|---|---|
| [training.csv](https://raw.githubusercontent.com/LuisM78/Appliances-energy-prediction-data/master/training.csv) | `data/author_training.csv` |
| [testing.csv](https://raw.githubusercontent.com/LuisM78/Appliances-energy-prediction-data/master/testing.csv) | `data/author_testing.csv` |

Keep the downloaded files unchanged. The notebook checks their hashes before loading them.

## 3. Run the notebook

From the project folder, run:

```powershell
.venv\Scripts\python -m notebook appliance_energy.ipynb
```

In Jupyter, select **Kernel → Restart Kernel and Run All Cells**. Keep `study_support.py` and `rebuild_report.py` in the same folder as the notebook.

Let all ten model cells finish. The final cell generates the report figures and tables from the new results. Numerical outputs are saved in `results/run_01/` through `results/run_10/`; figures and tables are saved in `latex/figures/` and `latex/tables/`.

To run one configuration, execute its model cell. Run the final report-generation cell only after all ten configurations have completed.
