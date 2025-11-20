# Dark Matter and Galactic Rotation Curves

This directory contains a Jupyter notebook that demonstrates how changing the
properties of a dark matter halo affects a galactic rotation curve.

The notebook shows:

- A top-down view of the galaxy (stellar disc + dark matter halo).
- The corresponding rotation curve, with separate disc and halo contributions.
- Interactive sliders to change the halo and disc parameters.
- Observed rotation-curve data overlaid for “by-eye” fitting.

If you downloaded this as a zip file from QMPlus, **unzip the archive first**
and keep the folder structure intact (e.g. `data/` stays next to the notebook).

---

## Contents

- `dm_rotation_widget.ipynb` – main notebook with theory, widgets, and questions.
- `data/` – example rotation-curve data files used in the notebook (if provided).
- `load_gaxies.py` - script to load up galaxy data.
- `README.md` – this file.

---

## Google Colab

You can open this notebook in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](
https://colab.research.google.com/github/ajw278/dm_rotation_lab/blob/main/dm_rotation_lab.ipynb
)

This is the easiest if you're not familiar with notebooks. Otherwise the following requirements are needed.

## Requirements

You need:

- Python **3.9+** (3.10–3.12 recommended)
- **JupyterLab** or classic Jupyter Notebook
- The following Python packages:
  - `numpy`
  - `matplotlib`
  - `ipywidgets`

You do **not** need `%matplotlib widget` for this notebook – it uses standard
inline plots with `ipywidgets` sliders.

---

## Option A: Setup using conda (recommended)

```bash
conda create -n dm_widget_env python=3.11 -c conda-forge \
    jupyterlab ipywidgets matplotlib numpy
conda activate dm_widget_env
```

## Option B: Setup using pip + venv

```bash 
python -m venv dm_widget_env
# On macOS / Linux:
source dm_widget_env/bin/activate
# On Windows:
# dm_widget_env\Scripts\activate

pip install jupyterlab ipywidgets matplotlib numpy
```

## Launch the notebook

From the directory containing the notebook:

```bash
# Activate the environment first
conda activate dm_widget_env        # or: source dm_widget_env/bin/activate

# Then start Jupyter
jupyter lab                         # or: jupyter notebook
```

Then in your browser:
1. Open `dm_rotation_widget.ipynb`.
2. Run the cells from top to bottom (e.g. Kernel -> Restart & Run All).
3. Use the sliders at the bottom to explore how the halo and disc affect the
rotation curve and answer the questions in the notebook.

If widgets do not appear (no sliders), check that:
`ipywidgets` is installed in the same environment as the notebook kernel, and
you restarted Jupyter after installing new packages.

