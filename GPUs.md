# Supported GPU families

Download the latest release:  
https://github.com/kryptex/krig-miner/releases/latest

Check our hashrate database:  
https://pool.kryptex.com/device/gpu

- **Version** = last performance/compatibility update
- **x No** = unsupported; 

## Pearl (PRL)

### NVIDIA

| Arch              | Family                               | Target          | Last update |
| ----------------- | ------------------------------------ | --------------- | ----------- |
| Blackwell         | RTX 5000 / RTX 6000 Series           | sm_120          | 1.4.0       |
| Blackwell ARM     | DGX Spark / GB10                     | sm_121          | 1.5.8       |
| Blackwell         | B200, GB200, B300, GB300             | sm_100, sm_103  | 1.5.3       |
| Hopper            | H100 / H200                          | sm_90           | 1.4.0       |
| Hopper            | GH200 / GH200 NVL2                   | sm_90           | 1.5.3       |
| Ada Lovelace      | RTX 4000 Series / RTX Ada / L-series | sm_89           | 1.4.0       |
| Ampere            | RTX 3000 Series / RTX A / A-series   | sm_80, sm_86    | 1.4.0       |
| Turing            | RTX 2000 Series / Quadro RTX / T4    | sm_75           | 1.4.0       |
| Turing            | GTX 1600 Series                      | sm_75           | 1.4.0       |
| Volta             | V100 / Quadro GV100 / TITAN V        | sm_70           | 1.4.0       |
| Pascal            | GTX 1000 Series / P-series           | sm_60, sm_61    | x           |
| Maxwell and older | GTX 900 Series and older             | sm_52 and older | x           |

### AMD

| Arch            | Family                               | Target                         | Last update |
| --------------- | ------------------------------------ | ------------------------------ | ----------- |
| CDNA 3 / 4      | MI300 Series                         | gfx942, gfx950                 | 1.4.0       |
| CDNA 1 / 2      | MI100 / MI200 Series                 | gfx908, gfx90a                 | x           |
| RDNA 4          | RX 9000 Series                       | gfx1200, gfx1201               | 1.4.0       |
| RDNA 3.5        | Ryzen AI APUs                        | gfx1150–gfx1152                | 1.5.2       |
| RDNA 3          | RX 7000 Series / Ryzen APUs          | gfx1100–gfx1103                | 1.5.2       |
| RDNA 2          | RX 6000 Series / selected Ryzen APUs | gfx1030-gfx1035                | 1.5.2       |
| RDNA 2          | Van Gogh / Raphael APUs              | gfx1033, gfx1036               | x           |
| RDNA 1          | Navi 12 / Navi 14                    | gfx1011, gfx1012               | 1.4.0       |
| RDNA 1          | Navi 10 / RDNA 1 APUs                | gfx1010, gfx1013               | x           |
| GCN 5 / Vega 20 | VII / MI50–MI60                      | gfx906                         | 1.5.1       |
| GCN 5 / Vega 10 | RX Vega / Vega APUs                  | gfx900, gfx902, gfx909, gfx90c | x           |
| GCN 3 / 4       | Fiji / Polaris                       | gfx803                         | x           |

### Intel

Not supported.

## Quantus (QTC)

### NVIDIA

| Arch              | Family                                       | Target          | Last update |
| ----------------- | -------------------------------------------- | --------------- | ----------- |
| Blackwell         | RTX 5000 / RTX 6000 Series                   | sm_120          | 1.5.10      |
| Blackwell ARM     | DGX Spark / GB10                             | sm_121          | 1.5.8       |
| Blackwell         | B200, GB200, B300, GB300                     | sm_100, sm_103  | 1.5.3       |
| Hopper            | H100 / H200                                  | sm_90           | 1.5.0       |
| Hopper            | GH200 / GH200 NVL2                           | sm_90           | 1.5.3       |
| Ada Lovelace      | RTX 4000 Series / L-series                   | sm_89           | 1.5.10      |
| Ampere            | RTX 3000 Series / RTX A / A-series           | sm_80, sm_86    | 1.5.10      |
| Turing            | RTX 2000 / GTX 1600 Series / Quadro RTX / T4 | sm_75           | 1.5.7       |
| Volta             | V100 / GV100 / TITAN V                       | sm_70           | x           |
| Pascal            | GTX 1000 Series / P-series                   | sm_60, sm_61    | 1.5.11      |
| Maxwell and older | GTX 900 Series and older                     | sm_52 and older | x           |

### AMD

| Arch              | Family                                  | Target                         | Last update |
| ----------------- | --------------------------------------- | ------------------------------ | ----------- |
| CDNA 1–4          | CDNA GPUs                               | gfx908, gfx90a, gfx942, gfx950 | x           |
| RDNA 4            | RX 9000 Series                          | gfx1200, gfx1201               | 1.5.9       |
| RDNA 3.5          | Ryzen AI APUs                           | gfx1150–gfx1152                | 1.5.2       |
| RDNA 3            | RX 7000 Series / Ryzen APUs             | gfx1100–gfx1103                | 1.5.9       |
| RDNA 2            | RX 6000 Series / selected Ryzen APUs    | gfx1030-gfx1035                | 1.5.11      |
| RDNA 2            | Van Gogh / Raphael APUs                 | gfx1033, gfx1036               | x           |
| RDNA 1            | RX 5000 Series / Pro / RDNA 1 APUs      | gfx1010–gfx1013                | 1.5.2       |
| GCN 5 / Vega 20   | VII / MI50–MI60                         | gfx906                         | 1.5.2       |
| GCN 5 / Vega 10   | RX Vega                                 | gfx900                         | 1.5.2       |
| GCN 5 / Vega APUs | Ryzen with Vega graphics                | gfx902, gfx909, gfx90c         | x           |
| GCN 3 / 4         | Fiji / Polaris (RX 400 / RX 500 Series) | gfx803                         | 1.5.2       |
| Older GCN         | Older GPUs / APUs                       | gfx6xx, gfx7xx, gfx801, gfx802 | x           |

### Intel

| Arch               | Family                                        | Target  | Last update |
| ------------------ | --------------------------------------------- | ------- | ----------- |
| Xe-HPG (Alchemist) | Arc A770 / A750 / A580, A770M / A730M / A550M | acm-g10 | 1.5.10      |
| Xe-HPG (Alchemist) | Arc A380 / A310, A370M / A350M, Pro A40 / A50 | acm-g11 | 1.5.10      |
| Xe-HPG (Alchemist) | Arc A570M / A530M, Pro A60                    | acm-g12 | 1.5.10      |
| Xe2 (Battlemage)   | Arc B500 Series                               | bmg-g21 | x           |

## Notes

- Intel Arc A-series is supported for Quantus only: the A750 on Linux, HiveOS and mmpOS since 1.5.8; all A-series GPUs and Windows since 1.5.10. The Intel GPU driver with Level Zero is required (`ze_loader.dll` on Windows, `libze_loader.so.1` on Linux). Use `--no-intel` to disable Intel GPUs.
- Use `--list-devices` to see which GPUs the installed driver exposes to the miner.
- AMD integrated GPUs are excluded by default. Use `--amd-igpu` to enable the supported APU architectures. 
- Legacy AMD GCN GPUs need a runtime that still supports their architecture. Linux ROCm 6 may be required.
- For NVIDIA + Linux, Ubuntu 24.04+ and a CUDA 13-compatible driver are recommended.
