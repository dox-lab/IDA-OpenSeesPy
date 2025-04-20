# Incremental Dynamic Analysis with OpenSees

This repository contains the implementation and results of an Incremental Dynamic Analysis (IDA) conducted using [OpenSees](https://opensees.berkeley.edu/) through Python (OpenSeesPy). The project focuses on analyzing the nonlinear seismic behavior of an 8-story structural model.

> ⚠️ **Disclaimer**: This repository is intended purely for educational and theoretical purposes. A real-world IDA requires in-depth studies in diferent areas like structural modeling, ground motion selection and scaling, and site condition. Use this repository as a learning tool — not for design or professional decision-making.

## 📘 Project Structure

```
IDA-OpenSees/
├── csv_data/                   ← Converted data from TXT to CSV (Excel-friendly)
├── data/                       
│   ├── elCentro.AT2            ← Ground motion record (PEER format)
│   └── model_3d.dxf            ← 3D structural model (DXF format)
│
├── notebooks/
│   └── IDA.ipynb               ← Jupyter notebook with modeling, analysis, and results
│
├── processed_results/          ← Processed data (IDA curves, summary tables, plots)
├── raw_results/                ← Raw output files from OpenSees (.txt format)
│
├── LICENSE                     ← License for the repository
├── README.md                   ← This file
└── requirements.txt            ← Python dependencies
```

## 🚀 Getting Started

To reproduce the analysis and results, follow these steps:

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/IDA-OpenSees.git
cd IDA-OpenSees
```

### 2. Install Requirements

Before running the notebook, ensure you have:

1. Input Data (place these in the `data/` folder):

    - `model_3d.dxf`: 3D structural model in DXF format  
    - `elCentro.AT2`: Ground motion record in PEER format (in this case, the El Centro earthquake record)

2. Python Packages:

    ```bash
    pip install -r requirements.txt
    ```

### 3. Run the Notebook

Launch Jupyter or VS Code and open `notebooks/IDA.ipynb`. Execute the cells to reproduce the full analysis.

## 📊 IDA Summary

The IDA was performed by scaling the ground motion from **0.1g to 8.0g**, with an increment step of **0.1g**, resulting in **80 dynamic analyses** in total.

- **Total runtime**: approximately **800 minutes** (~13 hours and 20 minutes), depending on hardware.

## 📁 Data Description

- **raw_results/**: Contains raw OpenSees output files for different intensity levels.
- **csv_data/**: Structured CSV files converted from raw outputs for easier analysis.
- **processed_results/**: Includes summary tables, plots of IDA curves, and interstory drift profiles.

## 🛠 Dependencies

The notebook requires Python 3.8+ and the following packages:
- **Core analysis**:
    - `openseespy`
    - `opsvis` (OpenSees Visualization)
    - `ezdxf` (CAD integration)
- **Data processing**:
    - `numpy`
    - `pandas`
- **Utilities**:
    - `tqdm` (progress bars)
    - `pathlib`, `os` (file handling)

See `requirements.txt` for complete dependency information.

## 📄 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

## ✍️ Author

Daniel Medina Quispe — [LinkedIn](https://www.linkedin.com/in/daniel-medina-quispe-3b63b5174/) — [GitHub](https://github.com/dox-lab)
