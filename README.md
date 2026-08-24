# Teaching Radar Meteorology with TMD Weather Radar Data
## Basic–Intermediate Weather Radar Processing for Environmental Science, Geography, and Geoinformatics

[![Open in Google Colab](https://img.shields.io/badge/Google%20Colab-Ready-F9AB00?logo=googlecolab&logoColor=white)](https://colab.research.google.com/)
[![Py-ART](https://img.shields.io/badge/Py--ART-Weather%20Radar-0A7BBB)](https://arm-doe.github.io/pyart/)
[![wradlib](https://img.shields.io/badge/wradlib-Radar%20Processing-2E8B57)](https://docs.wradlib.org/)
[![GeoPandas](https://img.shields.io/badge/GeoPandas-Geospatial-139C5A)](https://geopandas.org/)
[![Cartopy](https://img.shields.io/badge/Cartopy-Maps-4C78A8)](https://scitools.org.uk/cartopy/docs/latest/)
[![MetPy](https://img.shields.io/badge/MetPy-Meteorology-3366CC)](https://unidata.github.io/MetPy/latest/)
[![Rasterio](https://img.shields.io/badge/Rasterio-Raster%20GIS-6A5ACD)](https://rasterio.readthedocs.io/)
[![GitHub](https://img.shields.io/badge/GitHub-Course%20Repository-181717?logo=github)](https://github.com/nattaponm/Teaching_RadarMet_TMD_Basic_Intermediate)

Repository นี้จัดทำขึ้นเพื่อใช้ในการเรียนการสอน **การใช้ข้อมูลเรดาร์ตรวจอากาศของกรมอุตุนิยมวิทยา (TMD)** ด้วย Python และไลบรารีรหัสเปิด โดยเน้นการเชื่อมโยงระหว่าง **Radar Meteorology + Environmental Science + Geography + Geoinformatics**

เหมาะสำหรับนิสิตระดับ:

- ปริญญาตรี ชั้นปีที่ 3–4
- ปริญญาโท
- ผู้เรียนด้านสิ่งแวดล้อม ภูมิศาสตร์ ภูมิสารสนเทศ อุตุนิยมวิทยา และสาขาที่เกี่ยวข้อง

หลักสูตรใช้ **Google Colab + Google Drive** เป็นสภาพแวดล้อมหลัก เพื่อให้นิสิตสามารถเรียนรู้ได้โดยไม่ต้องติดตั้ง Python environment บนเครื่องส่วนตัว

> **แนวคิดของหลักสูตร**
>
> `Radar physics → Radar data structure → PPI → QC → Doppler → 3-D geometry → CAPPI/RHI → GIS → QPE → Basin analysis → Polarimetric radar → Advanced radar products`

---

# Start Here — เริ่มใช้งานจากตรงนี้

สำหรับนิสิต ให้เริ่มจาก:

**00B — Student Dataset Installer**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teaching_RadarMet_TMD_Basic_Intermediate/blob/main/00B_get_radar_course_dataset_from_GitHub.ipynb)

00B จะดาวน์โหลด canonical teaching dataset จาก GitHub ตรวจ SHA256 แตก ZIP ตรวจไฟล์เรดาร์ DEM GIS และ sounding จากนั้นติดตั้งทั้งหมดไว้ที่:

```text
/content/drive/MyDrive/tmd_radar_course
```

เมื่อขึ้น:

```text
TMD RADAR COURSE DATA READY
```

จึงเริ่ม Notebook 01–13 ได้โดยตรง

---

# Course Architecture

```text
External radar / DEM / GIS / sounding sources
                  ↓
     00A Instructor Dataset Builder
                  ↓
      QC + Validation + Packaging
                  ↓
      Canonical Teaching Dataset v1
                  ↓
             GitHub Repository
                  ↓
      00B Student Dataset Installer
                  ↓
      MyDrive/tmd_radar_course/
                  ↓
     01 → 02 → 03 → ... → 13
```

---

# Notebook Sequence

| Notebook | Topic | Level | Colab |
|---|---|---|---|
| **00A** | Build and validate canonical teaching dataset | Instructor | [Open](https://colab.research.google.com/github/nattaponm/Teaching_RadarMet_TMD_Basic_Intermediate/blob/main/00A_build_and_validate_radar_course_dataset.ipynb) |
| **00B** | Download and install course dataset from GitHub | Student setup | [Open](https://colab.research.google.com/github/nattaponm/Teaching_RadarMet_TMD_Basic_Intermediate/blob/main/00B_get_radar_course_dataset_from_GitHub.ipynb) |
| **01** | Radar reflectivity: Z, dBZ and Z–R relationships | Foundation | [Open](https://colab.research.google.com/github/nattaponm/Teaching_RadarMet_TMD_Basic_Intermediate/blob/main/01_lesson_z_Z_dBZ_ZR.ipynb) |
| **02** | Py-ART radar object, sweep/ray/gate and basic PPI | Foundation | [Open](https://colab.research.google.com/github/nattaponm/Teaching_RadarMet_TMD_Basic_Intermediate/blob/main/02_lesson_pyart_basic_PPI.ipynb) |
| **03** | GateFilter, masking and radar quality control | Core | [Open](https://colab.research.google.com/github/nattaponm/Teaching_RadarMet_TMD_Basic_Intermediate/blob/main/03_lesson_gate_filter_masking.ipynb) |
| **04** | Gridding, interpolation and CAPPI | Core | [Open](https://colab.research.google.com/github/nattaponm/Teaching_RadarMet_TMD_Basic_Intermediate/blob/main/04_lesson_gridding_interpolation.ipynb) |
| **05** | Cross-section, pseudo-RHI and vertical storm structure | Core | [Open](https://colab.research.google.com/github/nattaponm/Teaching_RadarMet_TMD_Basic_Intermediate/blob/main/05_lesson_cross_section_RHI.ipynb) |
| **06** | Geographic maps, CRS, UTM and GeoTIFF | GIS core | [Open](https://colab.research.google.com/github/nattaponm/Teaching_RadarMet_TMD_Basic_Intermediate/blob/main/06_lesson_maps_geographic_UTM_geotiff.ipynb) |
| **07** | Polarimetric QC, KDP, attenuation correction and HID | Advanced | [Open](https://colab.research.google.com/github/nattaponm/Teaching_RadarMet_TMD_Basic_Intermediate/blob/main/07_lesson_polarimetric_QC_KDP_attenuation_HID.ipynb) |
| **08** | QPE, rain rate and rainfall accumulation | Intermediate | [Open](https://colab.research.google.com/github/nattaponm/Teaching_RadarMet_TMD_Basic_Intermediate/blob/main/08_lesson_QPE_rainrate_accumulation.ipynb) |
| **09** | Doppler velocity and dealiasing | Intermediate | [Open](https://colab.research.google.com/github/nattaponm/Teaching_RadarMet_TMD_Basic_Intermediate/blob/main/09_lesson_doppler_dealiasing.ipynb) |
| **10** | Scan strategy, beam geometry and DEM | Intermediate | [Open](https://colab.research.google.com/github/nattaponm/Teaching_RadarMet_TMD_Basic_Intermediate/blob/main/10_lesson_scan_strategy_beam_geometry_DEM.ipynb) |
| **11** | Beam blockage with DEM | Intermediate | [Open](https://colab.research.google.com/github/nattaponm/Teaching_RadarMet_TMD_Basic_Intermediate/blob/main/11_lesson_beam_blockage_DEM.ipynb) |
| **12** | Capstone: basin zonal statistics and rainfall-input analysis | Capstone | [Open](https://colab.research.google.com/github/nattaponm/Teaching_RadarMet_TMD_Basic_Intermediate/blob/main/12_lesson_capstone_zonal_statistics.ipynb) |
| **13** | Spectrum width, turbulence proxy and EDR/PyTDA | Advanced/Research | [Open](https://colab.research.google.com/github/nattaponm/Teaching_RadarMet_TMD_Basic_Intermediate/blob/main/13_lesson_spectrum_width_turbulence_EDR_PyTDA.ipynb) |

> หาก GitHub แสดงชื่อไฟล์ 07, 10 หรือ 13 แบบตัดท้ายในหน้าเว็บ ให้ตรวจชื่อไฟล์จริงก่อนแก้ลิงก์ Colab หากมีการ rename ภายหลัง

---

# Learning Objectives

เมื่อเรียนครบชุด ผู้เรียนควรสามารถ:

1. อธิบายหลักการพื้นฐานของ weather radar
2. เข้าใจ reflectivity factor \(Z\), logarithmic reflectivity \(dBZ\) และความสัมพันธ์ Z–R
3. อ่านไฟล์เรดาร์ TMD ด้วย Py-ART
4. เข้าใจ radar volume, sweep, ray, gate, range, azimuth และ elevation
5. สร้างและอ่าน PPI
6. แยก radar measurement ออกจาก derived product
7. ใช้ GateFilter และ masking เพื่อ QC
8. เข้าใจบทบาทของ SNR, RHOHV, texture และ threshold-based QC
9. เข้าใจ radial Doppler velocity และ velocity folding
10. ทำ Doppler dealiasing และตรวจผล
11. เข้าใจ scan strategy และ beam geometry
12. คำนวณ beam height
13. วิเคราะห์ terrain interaction และ beam blockage
14. สร้าง 3-D radar grid และ CAPPI
15. วิเคราะห์ cross-section และ pseudo-RHI
16. เชื่อม radar data กับ GIS
17. เข้าใจ latitude/longitude, CRS และ UTM
18. export radar product เป็น GeoTIFF
19. ประมาณ rainfall rate จาก reflectivity
20. คำนวณ rainfall accumulation แบบเบื้องต้น
21. วิเคราะห์ rainfall by basin ด้วย zonal statistics
22. เข้าใจ dual-polarization variables เช่น ZDR, ΦDP, KDP และ ρHV
23. ทำ polarimetric QC และ hydrometeor classification ในระดับการสอน
24. เข้าใจ spectrum width และข้อจำกัดในการใช้เป็น turbulence proxy
25. วิเคราะห์ uncertainty และข้อจำกัดของ radar-derived products
26. ใช้ workflow เดิมไปพัฒนาต่อในงานสิ่งแวดล้อม GIS hydrology และ severe-weather research

---

# Teaching Data

Canonical dataset รุ่นปัจจุบันคือ:

```text
v1
```

และถูกแบ่งเป็น 3 packages:

```text
TMD_Radar_Core_v1.zip
TMD_Radar_Metadata_v1.zip
TMD_Radar_Spatial_v1.zip
```

พร้อมไฟล์ตรวจสอบ:

```text
dataset_packages.csv
dataset_packages.sha256
dataset_manifest.csv
build_acceptance_test.csv
final_acceptance_test.csv
final_build_summary.csv
data_provenance.csv
README_DATASET.md
```

รายละเอียด dataset โดยเฉพาะดูที่:

[`README_DATASET.md`](./README_DATASET.md)

---

# Radar Data

ข้อมูลหลักเป็นตัวอย่างจาก **Phitsanulok (PHS) weather radar** จำนวนอย่างน้อย 2 volume:

```text
PHS240@201807201000.uf
PHS240@201807201030.uf
```

ใช้สำหรับการสอนตั้งแต่ PPI, QC, gridding, QPE, Doppler, beam geometry ไปจนถึง advanced products

00A และ 00B ตรวจสอบว่าไฟล์สามารถเปิดด้วย Py-ART และมี field ที่บทเรียนต้องใช้ เช่น:

```text
reflectivity
velocity
spectrum_width
corrected_reflectivity
corrected_differential_reflectivity
differential_phase
cross_correlation_ratio
```

---

# Supporting Environmental and GIS Data

นอกจาก radar course ยังใช้:

```text
DEM
Thailand administrative boundaries
Phitsanulok amphoe boundary
HydroBASINS sub-basins
Radar-site point
Radar-domain polygon
50 / 100 / 150 / 200 km range rings
Raw sounding profile
```

ข้อมูลเหล่านี้ทำให้หลักสูตรไม่หยุดเพียงการดู radar PPI แต่สามารถเชื่อมไปยัง:

```text
Radar Meteorology
+
Physical Geography
+
GIS
+
Hydrology
+
Environmental Analysis
```

---

# Google Drive Structure

หลังรัน 00B สำเร็จ:

```text
MyDrive/
└── tmd_radar_course/
    │
    ├── 00_config/
    │   ├── course_config.json
    │   ├── dataset_manifest.csv
    │   ├── requirements_colab.txt
    │   └── setup_status.json
    │
    ├── 01_data/
    │   ├── radar/
    │   ├── dem/
    │   ├── sounding/
    │   ├── gis/
    │   └── metadata/
    │
    ├── 02_outputs/
    ├── 03_exercises/
    ├── 04_exports/
    ├── 99_logs/
    │
    ├── 1results/
    │   ├── lesson01/
    │   ├── lesson02/
    │   └── ...
    │
    └── 9config/
        └── course_paths.py
```

Notebook 01–13 ใช้ root เดิม:

```text
/content/drive/MyDrive/tmd_radar_course
```

---

# Core Python Libraries

## Py-ART

**Python ARM Radar Toolkit**

https://arm-doe.github.io/pyart/

ใช้สำหรับ:

```text
radar I/O
Radar object
PPI
GateFilter
gridding
Doppler velocity
dealiasing
polarimetric processing
radar visualization
```

Py-ART เป็น library หลักของ course

---

## wradlib

https://docs.wradlib.org/

ใช้สำหรับแนวคิดและเครื่องมือด้าน weather-radar processing เช่น:

```text
georeferencing
beam geometry
radar data processing
hydrometeorological radar applications
```

---

## GeoPandas

https://geopandas.org/

ใช้สำหรับ:

```text
vector GIS
province / amphoe / basin layers
spatial operations
GeoDataFrame
```

---

## Cartopy

https://scitools.org.uk/cartopy/docs/latest/

ใช้สำหรับ:

```text
map projection
geographic plotting
coastlines
coordinate-aware visualization
```

---

## Rasterio

https://rasterio.readthedocs.io/

ใช้สำหรับ:

```text
DEM
raster GIS
GeoTIFF
CRS
affine transform
```

---

## MetPy

https://unidata.github.io/MetPy/latest/

ใช้สำหรับ meteorological calculations และ thermodynamic support โดยเฉพาะส่วนที่เชื่อมกับ sounding และ atmospheric interpretation

---

## Additional Libraries

```text
NumPy
Pandas
Matplotlib
Shapely
PyProj
Pyogrio
SciPy
netCDF4
cmweather
```

---

# Recommended Learning Path

สำหรับ **ปริญญาตรี ปี 3–4** แนะนำให้เน้น:

```text
00B
↓
01
↓
02
↓
03
↓
04
↓
05
↓
06
↓
08
↓
09
↓
10
↓
11
↓
12
```

Notebook 07 และ 13 สามารถใช้เป็น advanced exercise หรือ demonstration

สำหรับ **ปริญญาโท** แนะนำเรียนครบ 01–13 และเพิ่มการอภิปราย:

```text
algorithm assumptions
parameter sensitivity
uncertainty
validation
research reproducibility
```

---

# Lesson 01 — Z, dBZ and Z–R

หัวใจคือทำความเข้าใจว่า radar **ไม่ได้วัด rainfall rate โดยตรง**

แนวคิด:

\[
dBZ = 10 \log_{10} Z
\]

และ:

\[
Z = aR^b
\]

ดังนั้น:

```text
electromagnetic backscatter
→ reflectivity factor
→ dBZ
→ empirical rainfall estimate
```

ผู้เรียนควรเข้าใจว่า Z–R coefficients แตกต่างตาม precipitation regime และควรตรวจสอบกับ observations ก่อนใช้เป็น operational QPE

---

# Lesson 02 — Radar Object and PPI

ผู้เรียนจะรู้จัก:

```text
Radar volume
Sweep
Ray
Gate
Range
Azimuth
Elevation
Field
```

และสร้าง PPI ด้วย Py-ART

แนวคิดสำคัญ:

> PPI เป็นการแสดงผลบน elevation angle ที่กำหนด ไม่ใช่แผนที่ของบรรยากาศที่ระดับความสูงคงที่

---

# Lesson 03 — Radar Quality Control

หัวข้อ:

```text
GateFilter
masking
RHOHV
SNR
texture
threshold sensitivity
```

ควรตีความ QC indicators อย่างระมัดระวัง

เช่น low ρHV ไม่ได้หมายถึง ground clutter เสมอไป แต่อาจสัมพันธ์กับ:

```text
nonmeteorological targets
biological targets
noise
mixed phase
hail
melting layer
nonuniform beam filling
```

---

# Lesson 04 — Gridding and CAPPI

จาก polar radar coordinates ไปสู่ Cartesian 3-D grid

แนวคิด:

```text
Radar gates
↓
interpolation
↓
Cartesian grid
↓
CAPPI
```

หลักสำคัญ:

> **Interpolation does not create observations.**

ผู้เรียนควรแยก:

```text
observed
interpolated
unsupported
```

---

# Lesson 05 — Cross-section and Vertical Structure

หัวข้อ:

```text
pseudo-RHI
cross-section
vertical reflectivity structure
echo top
vertical profiles
```

Deep echo สามารถบ่งชี้ deep convection ได้ แต่ไม่ควรใช้ echo-top height เพียงตัวเดียวเพื่อสรุป storm severity

---

# Lesson 06 — Radar GIS

นี่เป็นส่วนสำคัญสำหรับ Geography / Geoinformatics

```text
Radar polar coordinates
↓
Cartesian coordinates
↓
Latitude / Longitude
↓
CRS
↓
UTM
↓
GIS
↓
GeoTIFF
```

ผู้เรียนจะเห็นว่า radar product สามารถนำเข้าสู่ GIS workflow ได้อย่างไร

---

# Lesson 07 — Polarimetric Radar

หัวข้อขั้นสูง:

```text
ZH
ZDR
ρHV
ΦDP
KDP
attenuation correction
temperature profile
HID
```

บทนี้เหมาะกับ ป.โท และผู้เรียนระดับ advanced

### Sounding limitation

sounding ที่มากับ teaching dataset ใช้เพื่อสาธิต workflow เท่านั้น และไม่ได้ตรงเวลา/สถานที่กับ PHS radar event

จึงไม่ควรใช้เป็น environmental verification ของเหตุการณ์จริง

---

# Lesson 08 — QPE

จาก reflectivity ไปสู่ rainfall-rate estimate

```text
Reflectivity
↓
Z–R
↓
Rain rate
↓
Time integration
↓
Rainfall accumulation
```

ข้อควรระวัง:

radar-derived rainfall เป็น **estimate**

ควรพิจารณา:

```text
beam height
attenuation
bright band
drop-size distribution
orography
distance from radar
Z–R uncertainty
gauge validation
```

---

# Lesson 09 — Doppler Velocity

Radar Doppler วัด:

\[
V_r
\]

หรือ **radial velocity**

ไม่ใช่ horizontal wind vector โดยตรง

หัวข้อ:

```text
Nyquist velocity
velocity folding
dealiasing
inbound / outbound
diagnostics
```

ผล dealiasing ควรตรวจเชิงกายภาพ ไม่ควรถือว่าทุก gate คือ true wind โดยอัตโนมัติ

---

# Lesson 10 — Beam Geometry

ผู้เรียนจะเข้าใจว่า:

```text
distance from radar increases
↓
beam height changes
↓
sampling altitude changes
```

รวมถึง:

```text
Earth curvature
standard 4/3-Earth approximation
elevation angle
beamwidth
terrain profile
```

---

# Lesson 11 — Beam Blockage

ใช้ DEM วิเคราะห์:

```text
Partial Beam Blocking
Cumulative Beam Blocking
```

ซึ่งมีผลต่อคุณภาพข้อมูล radar โดยเฉพาะในพื้นที่ภูเขา

สำคัญ:

```text
NoData ≠ zero blockage
```

---

# Lesson 12 — Basin Capstone

เชื่อม:

```text
Radar rainfall
+
GIS basin polygon
↓
Zonal statistics
↓
Rainfall input by basin
```

ปริมาตรจาก:

```text
rainfall depth × basin area
```

ควรเรียกว่า **rainfall input volume**

ไม่ใช่ runoff volume โดยตรง เพราะ runoff ต้องพิจารณากระบวนการทางอุทกวิทยาเพิ่มเติม

---

# Lesson 13 — Spectrum Width and Turbulence

หัวข้อขั้นสูง:

```text
spectrum width
velocity variability
turbulence proxy
EDR concepts
PyTDA-related workflow
```

Spectrum width สูงอาจสัมพันธ์กับ turbulence แต่ยังได้รับผลจาก:

```text
wind shear
beam broadening
antenna motion
velocity gradient
signal quality
nonmeteorological targets
```

จึงควรตีความเป็น **candidate enhanced-spectrum-width region** มากกว่าการสรุป turbulence โดยตรงหากยังไม่มี validation

---

# Reproducibility

หลักสูตรนี้ใช้แนวคิด:

```text
Source data
↓
Instructor validation
↓
Canonical dataset
↓
SHA256
↓
Student installer
↓
Fixed Drive structure
↓
Reproducible lessons
```

การวิเคราะห์ควรบันทึก:

```text
dataset version
radar file
time
field
sweep
QC thresholds
grid resolution
ROI
CRS
Z–R coefficients
algorithm parameters
software/library versions
```

---

# Important Scientific Cautions

## Radar reflectivity ≠ rainfall truth

Reflectivity เป็น radar measurement ส่วน rainfall rate เป็น derived estimate

## Radial velocity ≠ full wind vector

Doppler radar วัดองค์ประกอบตามแนวลำแสง

## Low ρHV ≠ clutter automatically

ต้องพิจารณาบริบทและ field อื่นร่วมด้วย

## CAPPI ≠ direct observation everywhere

CAPPI มี interpolation และ range-dependent sampling

## 2-km radar field ≠ surface rainfall automatically

ต้องพิจารณา vertical precipitation processes

## Echo top ≠ severe storm automatically

ต้องใช้ environmental and storm-structure evidence เพิ่ม

## Rainfall input volume ≠ runoff volume

runoff ต้องมี hydrologic response

## Labeled threshold ≠ operational warning

threshold ใน teaching code หลายจุดมีไว้เพื่อ experimentation และต้องผ่าน validation ก่อน operational use

---

# Dataset Provenance

รายละเอียดแหล่งข้อมูลจริงของ release นี้อยู่ใน:

```text
data_provenance.csv
dataset_manifest.csv
README_DATASET.md
```

00A เป็นผู้ดาวน์โหลดและ freeze external sources ครั้งเดียว จากนั้นนิสิตใช้เฉพาะ canonical dataset จาก repository นี้ผ่าน 00B

แหล่งที่ใช้ในการสร้าง teaching dataset ปัจจุบันประกอบด้วย radar teaching source, DEM source, GIS administrative data, HydroBASINS และ pedagogical sounding ตามที่ระบุใน provenance ของ release

---

# Source and Attribution

ข้อมูลและ code จากแหล่งภายนอกยังคงอยู่ภายใต้เงื่อนไขของเจ้าของข้อมูลต้นทาง

ก่อนนำไปใช้ใน publication หรือ redistribution ควรตรวจ:

```text
license
attribution
data-use conditions
institutional policy
```

โดยเฉพาะข้อมูลเรดาร์ตรวจอากาศจากหน่วยงานผู้ให้ข้อมูล

---

# Suggested Repository Citation

ตัวอย่างทั่วไป:

```text
nattaponm. (2026). Teaching_RadarMet_TMD_Basic_Intermediate:
Open-source Python teaching materials for basic-to-intermediate
weather-radar processing using TMD radar data.
GitHub repository.
https://github.com/nattaponm/Teaching_RadarMet_TMD_Basic_Intermediate
```

สามารถปรับชื่อผู้แต่งและรูปแบบ citation ตาม metadata ที่ต้องการเผยแพร่จริง

---

# Recommended Uses

เหมาะสำหรับ:

```text
weather radar laboratory
environmental GIS laboratory
remote sensing course
physical geography
meteorology
hydrology
undergraduate project
master's research preparation
radar-data research prototype
```

---

# Possible Advanced Extensions

หลังจบ core course สามารถต่อยอด:

```text
radar mosaic
storm-object identification
storm tracking
VIL / VILD
echo-top products
hail detection
dual-pol QPE
gauge verification
ERA5 integration
radiosonde integration
severe-weather environments
machine learning
multi-radar GIS
operational-style quality monitoring
```

---

# Quick Start for Students

```text
1. Open 00B in Google Colab
2. Mount Google Drive
3. Download the 3 canonical ZIP packages
4. Verify SHA256
5. Wait for TMD RADAR COURSE DATA READY
6. Open Notebook 01
7. Continue sequentially to Notebook 13
```

[![START COURSE — Open 00B in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nattaponm/Teaching_RadarMet_TMD_Basic_Intermediate/blob/main/00B_get_radar_course_dataset_from_GitHub.ipynb)

---

# Repository Structure

```text
Teaching_RadarMet_TMD_Basic_Intermediate/
│
├── 00A_build_and_validate_radar_course_dataset.ipynb
├── 00B_get_radar_course_dataset_from_GitHub.ipynb
│
├── 01_lesson_z_Z_dBZ_ZR.ipynb
├── 02_lesson_pyart_basic_PPI.ipynb
├── 03_lesson_gate_filter_masking.ipynb
├── 04_lesson_gridding_interpolation.ipynb
├── 05_lesson_cross_section_RHI.ipynb
├── 06_lesson_maps_geographic_UTM_geotiff.ipynb
├── 07_lesson_polarimetric_QC_KDP_attenuation_HID.ipynb
├── 08_lesson_QPE_rainrate_accumulation.ipynb
├── 09_lesson_doppler_dealiasing.ipynb
├── 10_lesson_scan_strategy_beam_geometry_DEM.ipynb
├── 11_lesson_beam_blockage_DEM.ipynb
├── 12_lesson_capstone_zonal_statistics.ipynb
├── 13_lesson_spectrum_width_turbulence_EDR_PyTDA.ipynb
│
├── README.md
├── README_DATASET.md
│
├── TMD_Radar_Core_v1.zip
├── TMD_Radar_Metadata_v1.zip
├── TMD_Radar_Spatial_v1.zip
│
├── dataset_packages.csv
├── dataset_packages.sha256
├── dataset_manifest.csv
├── data_provenance.csv
├── build_acceptance_test.csv
├── final_acceptance_test.csv
├── final_build_summary.csv
└── github_ready_inventory.csv
```

---

# Maintainer

GitHub: [nattaponm](https://github.com/nattaponm)

Repository:

https://github.com/nattaponm/Teaching_RadarMet_TMD_Basic_Intermediate

---

> **Educational and scientific-use note**
>
> Repository นี้จัดทำเพื่อการเรียนการสอนและเป็นต้นแบบ workflow การประมวลผลข้อมูลเรดาร์ตรวจอากาศด้วยซอฟต์แวร์รหัสเปิด ผลิตภัณฑ์ที่สร้างจากแบบฝึกหัดไม่ควรถูกนำไปใช้เป็น operational warning, engineering decision หรือข้อสรุปเชิงสาเหตุโดยปราศจากการตรวจสอบ algorithm, calibration, validation และ uncertainty ที่เหมาะสม
