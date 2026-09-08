# Day-2 spatial data

Everything the spatial notebooks read lives in this folder.

## Raw data

| File | Used by | Size |
|---|---|---|
| [visium_2.1.0_2_io_subset.zip](https://s3.embl.de/spatialdata/raw_data/workshop/visium_2.1.0_2_io_subset.zip) | beginner/nb1 | 67 MB |
| [visium_hd_3.0.0_io_subset.zip](https://s3.embl.de/spatialdata/raw_data/workshop/visium_hd_3.0.0_io_subset.zip) | beginner/nb1 | 228 MB |
| [xenium_2.0.0_io_subset.zip](https://s3.embl.de/spatialdata/raw_data/workshop/xenium_2.0.0_io_subset.zip) | beginner/nb1 | 786 MB |
| [mouse_liver_spatialdata_0.7.1.zip](https://s3.embl.de/spatialdata/spatialdata-sandbox/mouse_liver_spatialdata_0.7.1.zip) | advanced/transformations | 66 MB |

Unzip all four here. The mouse liver archive unpacks to `data.zarr`; rename it to
`mouse_liver.zarr`.

## Zarr stores

`beginner/nb1_spatialdata_objects.ipynb` converts the three 10x folders into
`visium.zarr`, `visium_hd.zarr` and `xenium.zarr`, which every other spatial
notebook reads. Run nb1 first, or unzip pre-built stores here.

nb1 also shortens the coordinate-system names: spatialdata-io names them after
the dataset (`CytAssist_..._downscaled_hires`), while the notebooks refer to
`downscaled_hires` and `global`.
