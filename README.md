
---

## Notebook 1: Colab – 3D reconstruction from images

**Purpose**  
Runs DUSt3R / MASt3R-based multi-view reconstruction from input images and exports sparse colored point clouds.

**Platform**  
Google Colab (GPU required)

**How to run**
1. Open `colab_dust3r_mast3r_reconstruction.ipynb` in Google Colab.
2. Set runtime to **GPU**.
3. Run cells in order.
4. Upload input images when prompted.
5. The notebook exports one or more `.ply` point cloud files.

**Main outputs**
- Sparse colored PLY point cloud
- Optional interactive visualizations

---

## Notebook 2: Kaggle – Sonar alignment and quantitative evaluation

**Purpose**  
Aligns the reconstructed MASt3R point cloud to sonar data using ICP and computes quantitative error metrics.

**Platform**  
Kaggle Notebook (GPU recommended)

**How to run**
1. Create a new Kaggle notebook.
2. Upload `kaggle_mast3r_sonar_evaluation.ipynb`.
3. Attach required Kaggle datasets:
   - MASt3R reconstruction output (PLY or OBJ)
   - Sonar TXT file
4. Enable GPU.
5. Run cells sequentially.

**Main steps**
- Load and preprocess sonar data
- Load MASt3R point cloud
- Voxel downsampling
- ICP registration
- Error computation and visualization

**Evaluation metrics**
- Mean and median point-to-point error
- RMSE and MAE
- Percentile statistics (90th, 95th, 99th)
- Absolute relative depth error
- Hausdorff distance
- Chamfer distance (L1 and L2)

---

## Requirements (high level)

- Python 3.x
- PyTorch with CUDA 11.8
- MASt3R / DUSt3R
- NumPy < 2
- SciPy
- Open3D
- Matplotlib
- Plotly

All dependencies are installed directly inside the notebooks.

---

## Notes

- GPU acceleration is required for reconstruction and strongly recommended for alignment.
- Paths to datasets may need to be updated depending on the Kaggle environment.
- The notebooks are intended to be run top-to-bottom without skipping cells.
