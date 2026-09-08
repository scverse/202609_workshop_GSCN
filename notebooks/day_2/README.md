# Day 2: Advanced Single-cell Analysis and Spatial Omics

Welcome to Day 2 of the workshop! Today we'll focus on advanced single-cell analysis techniques and spatial omics using various tools from the scverse ecosystem.

## Notebooks

### Morning Session: Advanced Single-cell Analysis

1. [Ligand-Receptor Interactions](nb1_ligand_recepter_interactions.ipynb)
   - Learn how to analyze cell-cell communication
   - Identify significant ligand-receptor pairs
   - Visualize and interpret interaction networks

2. [Differential Cellular Abundance](nb2_differential_cellular_abundance_pertpy_implementation.ipynb)
   - Understand methods for comparing cell type proportions
   - Learn statistical approaches for differential abundance
   - Add contrasts to compare specific groups
   - Visualize and interpret changes in cell populations

   **This is the notebook to use.** It runs Milo through pertpy in pure Python,
   so it works under `environment.yml` like everything else.

   [An R variant](nb2_differential_cellular_abundance.ipynb) drives the original
   miloR through rpy2. It covers the same ground and is kept for reference, but
   it needs R, rpy2 and miloR, none of which are in `environment.yml` - so it
   will not run for participants who followed the setup instructions.

### Afternoon Session: Spatial Analysis

3. [Spatial Analysis](spatialdata/README.md)
   - Introduction to spatial transcriptomics concepts
   - Learn how to process and analyze spatial data
   - Explore spatial patterns and interactions
   - Apply advanced spatial analysis techniques 

4. [Spatial structure](spatial_domain_and_niche.ipynb)
   - Learn the difference between clustering of dissociated data and spatial data 
   - Learn the computational definition of a niche
   - Apply methods to characterize spatial niches
## Data

`spatialdata/data/README.md` covers the afternoon; everything there is public.

The two morning-session datasets are the presenters' own and are not public.
Put them in `notebooks/day_2/data/`:

| File | Used by |
|---|---|
| `clean_myeloid.h5ad` | `nb2_differential_cellular_abundance*.ipynb` |
| `xenium_mouse_ad_annotated_rotated_domain.h5ad` | `spatial_domain_and_niche.ipynb` |

Without `clean_myeloid.h5ad` both nb2 notebooks fall back to Haber et al. 2017
(mouse small intestine, the dataset the Milo paper uses), remapped onto the same
column names, so they still run end to end.

`spatial_domain_and_niche.ipynb` has no fallback and stops with a clear message
until the Xenium file is in place. Its `scvi_model/` and `autok_l3` artifacts are
optional - the notebook trains and saves them if they are missing.
