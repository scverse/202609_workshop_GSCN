# Day 1: Introduction to Single-cell RNA-seq Analysis

All notebooks use the single `scverse-workshop` environment - see the
[setup instructions](https://scverse.org/gscn2026/setup/).

## Data

Notebooks 3 and 6 download their data themselves. The others read from a local
`data_day1/` folder; the download link is announced on Zulip before the workshop.

## Notebooks

### First hands-on session: Preprocessing and DGE

1. [Quality Control and Normalization](nb1_qc_normalization.ipynb)
   - Learn how to perform quality control on single-cell RNA-seq data
   - Understand and apply different normalization techniques
   - Identify and filter out low-quality cells

2. [Preprocessing](nb2_preprocessing.ipynb)
   - Explore data preprocessing steps including feature selection
   - Learn about dimensionality reduction techniques
   - Understand how to handle technical artifacts

3. [Downstream Analysis](nb3_downstream_analysis.ipynb)
   - Perform clustering and cell type annotation
   - Conduct differential expression analysis
   - Visualize and interpret results

### Second hands-on session: Advanced Analysis

4. [Batch Correction](nb4_batch_correction.ipynb)
   - Learn about batch effects in single-cell data
   - Apply different batch correction methods
   - Evaluate the effectiveness of batch correction

5. [Trajectory Inference](nb5_trajectory_inference.ipynb)
   - Learn about trajectory inference methods
   - Apply trajectory analysis to understand cell differentiation
   - Visualize and interpret developmental trajectories

6. [Fate probability](nb6_cell_rank.ipynb)
   - Infer fate probability using CellRank

