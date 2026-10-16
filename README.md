# VirtualEphysAnalysis

Browser-based analysis notebooks for **Visual Neuron Lab**, the simulated electrophysiology teaching rig in [VirtualEphysRig](https://github.com/PJendritza/VirtualEphysRig).

The notebooks run in your browser using JupyterLite and Python (Pyodide). Students need **no software installation and no Google, GitHub, or ChatGPT account**. An internet connection is needed to load the environment and its Python packages.

## Open the teaching materials

- [Visual Neuron Lab — record an experiment](https://patrickjendritza.com/VirtualEphysRig/dist/)
- [Analysis 1 — Orientation tuning](https://patrickjendritza.com/VirtualEphysAnalysis/notebooks/?path=Analysis_Exercise1_OrientationTuning.ipynb)
- [Analysis 2 — Spatial receptive-field mapping](https://patrickjendritza.com/VirtualEphysAnalysis/notebooks/?path=Analysis_Exercise2_SpatialRF.ipynb)

These links open a single notebook in the clean Notebook interface, without the JupyterLab file-browser sidebar.

**Analysis 1** explores raw voltage, high-pass filtering, negative-threshold event detection, trial-aligned rasters, and an orientation tuning curve.

**Analysis 2** detects events, compares responses across stimulus positions, and builds measured and interpolated spatial response maps. These analysis exercise numbers are separate from the experiment numbers inside the rig.

## Student workflow

1. Open Visual Neuron Lab and record an orientation-tuning or spatial-mapping experiment.
2. Stop recording and **download the recording ZIP**. Leave it zipped.
3. Open the matching analysis notebook above. Select **Python (Pyodide)** if asked for a kernel.
4. Run the first code cell with **Shift+Enter**. On first use, it downloads the required packages into browser Python; wait for the upload button, then use it to select your recording ZIP.
5. Once the recording is loaded, continue through the notebook in order using Shift+Enter. Read the questions and explore the plots as you go.
6. **Download your edited notebook to preserve your work** using **File → Download**. Browser-local storage is not a backup and may be cleared.

When changing recordings, restart the kernel, run the upload cell, select the new ZIP, and rerun the remaining cells in order so old analysis variables are not reused.

The complete voltage recording remains available for inspection. Experimental trial comparisons use only grating presentations marked `source == 'protocol'`; manual exploration and a stimulus already displayed when recording began are not treated as protocol trials. Spatial coordinates are rounded to six decimal places for consistent grouping without modifying the original log.

## Maintaining the course notebooks

The teaching notebooks live in **`content/`**. Edit those files, not duplicate copies in the repository root. The GitHub Actions workflow copies this README into `content/`, builds the JupyterLite site, and publishes the generated `dist/` artifact through GitHub Pages. Pages must use **GitHub Actions** as its source.

The template examples and dependencies remain available. There is no server-side Python service: computations and uploaded recordings stay in the browser. Do not rely on browser storage alone; download recordings and edited notebooks you want to keep.

## Attribution and status

Based on the [JupyterLite demo template](https://github.com/jupyterlite/demo). See the retained [LICENSE](LICENSE) and [JupyterLite documentation](https://jupyterlite.readthedocs.io/en/stable/).

Teaching materials for the 2026 IMPRS Methods Course. **Ongoing work**: notebooks and instructions may continue to change.


