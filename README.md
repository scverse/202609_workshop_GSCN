# scverse x GSCN workshop

Notebooks for **"Computational single-cell genomics for stem cell biologists"**.

Schedule, venue and full setup instructions live on the workshop site:
**https://scverse.org/gscn2026/**

## Setup, in short

Full step-by-step instructions, including how to install Anaconda on your operating
system, are at **https://scverse.org/gscn2026/setup/**. If you already have a working
conda, this is all of it:

```
conda env create -f environment.yml
conda activate scverse-workshop
python -m ipykernel install --user --name scverse-workshop
```

One environment covers both days and every notebook in this repository. Start work with:

```
conda activate scverse-workshop
jupyter lab
```

and make sure the kernel shown in the top right of each notebook is
**scverse-workshop**.

### Or, with pixi

`pixi.toml` / `pixi.lock` pin the same environment exactly, which is what the
notebooks were last run against. It needs no conda:

```
pixi run lab
```

That installs the environment if needed, registers the `scverse-workshop`
kernel into it, builds miloR on first run, and starts JupyterLab. If you already
have a *user-level* kernel of that name from an older environment it will shadow
this one - check with `pixi run jupyter kernelspec list`.

## Data

Day 2 needs three files, downloaded before the workshop and unzipped into
`notebooks/day_2/spatialdata/data/`:

- [Visium](https://s3.embl.de/spatialdata/raw_data/workshop/visium_2.1.0_2_io_subset.zip) (67 MB)
- [Visium HD](https://s3.embl.de/spatialdata/raw_data/workshop/visium_hd_3.0.0_io_subset.zip) (228 MB)
- [Xenium](https://s3.embl.de/spatialdata/raw_data/workshop/xenium_2.0.0_io_subset.zip) (786 MB)

Day 1 data: see [notebooks/day_1/README.md](notebooks/day_1/README.md).

## Contents

- [Day 1](notebooks/day_1/README.md) — QC, preprocessing, downstream analysis, batch
  correction, trajectory inference, fate probabilities
- [Day 2](notebooks/day_2/README.md) — ligand-receptor interactions, differential
  abundance, spatial data, spatial domains and niches
- [misc/pre-workshop](misc/pre-workshop/pre_workshop_session.ipynb) — Python refresher

## Reusing this for the next edition

Nothing here is dated: the environment is called `scverse-workshop`, the kernel matches,
and `environment.yml` is unpinned so a fresh `conda env create` picks up the current
scverse stack. Fork, update the data links, run the notebooks through once.
