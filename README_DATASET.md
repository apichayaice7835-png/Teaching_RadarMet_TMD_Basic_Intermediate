# Canonical TMD Radar Teaching Dataset v1

This dataset was prepared for the course:

**TMD Weather Radar Processing with Open-Source Python**

## Purpose

The dataset freezes the common inputs required by Notebook 01–13 so
students do not need to download external environmental and geospatial
sources independently during class.

## Teaching radar

- Site: Phitsanulok (PHS)
- Latitude: 16.775408
- Longitude: 100.217964
- Altitude: 72.0 m MSL
- Maximum range in the teaching file: 240.5 km
- UTM CRS used by the course: EPSG:32647

## Radar files

- `01_data/radar/uf/PHS240@201807201000.uf`
- `01_data/radar/uf/PHS240@201807201030.uf`

Source repository used by the instructor builder:

`nattaponm/train_tmd_radar_basic_1day`

The source filenames use a `.uf.bz2` suffix, but the builder does
not assume that the byte stream is bzip2. It inspects magic bytes and
supports true bzip2, gzip, or already-uncompressed radar binary before
materializing a canonical `.uf` file.

The instructor builder then verifies that both canonical UF volumes can
be opened by Py-ART and checks for the radar fields required by the course.

## DEM

Canonical file:

`01_data/dem/raw/wrl_dem_phk1.tif`

Source repository:

`nattaponm/Beam_blockage_radar_Thai`

The builder checks raster readability, CRS, valid pixels, and whether
the PHS radar location falls inside the DEM extent.

## Sounding

Raw canonical file:

`01_data/sounding/raw/sounding_cm.txt`

Source repository:

`nattaponm/Python_sounding_Sharppy_Wyomming`

Important limitation:

The Chiang Mai sounding is a pedagogical profile and is NOT collocated
in time or space with the PHS radar event. It is retained because the
existing polarimetric lesson uses it to demonstrate temperature-profile
mapping and isotherm levels.

Do not use this profile to describe the true environmental state of the
20 July 2018 PHS radar event.

## Administrative boundaries

Thailand ADM1 was retrieved through the geoBoundaries gbOpen API.
The API metadata used during the build are stored in:

`01_data/metadata/geoboundaries_adm1_source_metadata.json`

A Phitsanulok amphoe layer is additionally frozen from
`prasertcbs/thailand_gis` to preserve compatibility with legacy lessons.

## HydroBASINS

The instructor builder downloads HydroBASINS Asia level
7 and retains only polygons intersecting the PHS radar
domain in the canonical student dataset.

Canonical file:

`01_data/gis/subbasins_phs/phs_subbasins_hybas07.gpkg`

## Reproducibility

See:

- `01_data/metadata/data_provenance.csv`
- `01_data/metadata/source_download_log.csv`
- `01_data/metadata/radar_file_summary.csv`
- `01_data/metadata/radar_field_inventory.csv`
- `01_data/metadata/dem_qc.csv`
- `01_data/metadata/spatial_dataset_qc.csv`
- `01_data/metadata/acceptance_test.csv`
- `00_config/dataset_manifest.csv`

## Student-use principle

Students should start with Notebook `00B`, which downloads the frozen
course packages from the course GitHub repository, verifies SHA256,
installs the dataset into:

`/content/drive/MyDrive/tmd_radar_course`

and creates `setup_status.json`.

Notebook 01–13 should not re-download these external source datasets.

## Redistribution and attribution

Before publicly redistributing the packages, review the current license
and data-use conditions of every original source. Technical preparation
by 00A is not a substitute for permission to redistribute third-party data.
