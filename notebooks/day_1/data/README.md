# Day 1 data

Download and unzip into `notebooks/day_1/`, so the files end up here in
`notebooks/day_1/data/`:

**[day1_inputs.zip](https://github.com/scverse/202609_workshop_GSCN/releases/download/data-v1/day1_inputs.zip)** (399 MB)

| File | Used by | Origin |
|---|---|---|
| `filtered_feature_bc_matrix/` | nb1 | [10k Human PBMCs, 3' v3.1, Chromium X, with intronic reads](https://www.10xgenomics.com/datasets/10k-human-pbmcs-3-v3-1-chromium-x-with-intronic-reads-3-1-high) (10x Genomics) |
| `HALLMARK_G2M_CHECKPOINT.v2023.2.Hs.grp` | nb2 | [MSigDB hallmark gene set](https://www.gsea-msigdb.org/gsea/msigdb/human/geneset/HALLMARK_G2M_CHECKPOINT.html) |
| `b1_exprs.txt`, `b1_celltype.txt`, `b2_exprs.txt`, `b2_celltype.txt` | nb4 | PBMC dataset 5 from the batch-correction benchmark of [Tran et al. 2020](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-019-1850-9), distributed at [JinmiaoChenLab/Batch-effect-removal-benchmarking](https://github.com/JinmiaoChenLab/Batch-effect-removal-benchmarking) |
| `human_cd34_bm_rep1.h5ad` | nb5 | CD34+ bone marrow from [Setty et al. 2019](https://www.nature.com/articles/s41587-019-0068-4), distributed with [dpeerlab/Palantir](https://github.com/dpeerlab/Palantir) |

nb3 and nb6 download their own data and need nothing from here.

## If you fall behind

nb2 reads `data/processed/processed_data.h5ad`, which nb1 writes. If nb1 did not
finish, get that file from
**[day1_processed.zip](https://github.com/scverse/202609_workshop_GSCN/releases/download/data-v1/day1_processed.zip)**
(159 MB) and carry on.
