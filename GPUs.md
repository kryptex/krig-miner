# Supported GPU families

Download the latest release:  
https://github.com/kryptex/krig-miner/releases/latest

Check our hashrate database:  
https://pool.kryptex.com/device/gpu

- **Version** = last performance/compatibility update
- **x No** = unsupported; 

## Pearl (PRL)

### NVIDIA

| Arch | Family | Target | Last update |
| --- | --- | --- | --- |
| Blackwell | RTX 50xx / RTX 6000 | sm_120 | 1.4.0 |
| Blackwell ARM | DGX Spark / GB10 | sm_121 | 1.5.3 |
| Blackwell | B200, GB200, B300, GB300 | sm_100, sm_103 | 1.5.3 |
| Hopper | H100 / H200 | sm_90 | 1.4.0 |
| Hopper | GH200 / GH200 NVL2 | sm_90 | 1.5.3 |
| Ada Lovelace | RTX 40xx / RTX Ada / L-series | sm_89 | 1.4.0 |
| Ampere | RTX 30xx / RTX A / A-series | sm_80, sm_86 | 1.4.0 |
| Turing | RTX 20xx / Quadro RTX / T4 | sm_75 | 1.4.0 |
| Turing | GTX 16xx | sm_75 | 1.4.0 |
| Volta | V100 / Quadro GV100 / TITAN V | sm_70 | 1.4.0 |
| Pascal | GTX 10xx / P-series | sm_60, sm_61 | x |
| Maxwell and older | GTX 9xx and older | sm_52 and older | x |

### AMD

| Arch | Family | Target | Last update |
| --- | --- | --- | --- |
| CDNA 3 / 4 | MI3xx | gfx942, gfx950 | 1.4.0 |
| CDNA 1 / 2 | MI1xx / MI2xx | gfx908, gfx90a | x |
| RDNA 4 | RX 9xxx | gfx1200, gfx1201 | 1.4.0 |
| RDNA 3.5 | Ryzen AI APUs | gfx1150–gfx1152 | 1.5.2 |
| RDNA 3 | RX 7xxx / Ryzen APUs | gfx1100–gfx1103 | 1.5.2 |
| RDNA 2 | RX 6xxx / selected Ryzen APUs | gfx1030-gfx1035 | 1.5.2 |
| RDNA 2 | Van Gogh / Raphael APUs | gfx1033, gfx1036 | x |
| RDNA 1 | Navi 12 / Navi 14 | gfx1011, gfx1012 | 1.4.0 |
| RDNA 1 | Navi 10 / RDNA 1 APUs | gfx1010, gfx1013 | x |
| GCN 5 / Vega 20 | VII / MI50–MI60 | gfx906 | 1.5.1 |
| GCN 5 / Vega 10 | RX Vega / Vega APUs | gfx900, gfx902, gfx909, gfx90c | x |
| GCN 3 / 4 | Fiji / Polaris | gfx803 | x |

## Quantus (QTC)

### NVIDIA

| Arch | Family | Target | Last update |
| --- | --- | --- | --- |
| Blackwell | RTX 50xx, RTX 6000 | sm_120 | 1.5.2 |
| Blackwell ARM | DGX Spark / GB10 | sm_121 | 1.5.3 |
| Blackwell | B200, GB200, B300, GB300 | sm_100, sm_103 | 1.5.3 |
| Hopper | H100 / H200 | sm_90 | 1.5.0 |
| Hopper | GH200 / GH200 NVL2 | sm_90 | 1.5.3 |
| Ada Lovelace | RTX 40xx / L-series | sm_89 | 1.5.0 |
| Ampere | RTX 30xx / RTX A / A-series | sm_80, sm_86 | 1.5.2 |
| Turing | RTX 20xx / GTX 16xx / Quadro RTX / T4 | sm_75 | 1.5.2 |
| Volta | V100 / GV100 / TITAN V | sm_70 | x |
| Pascal | GTX 10xx / P-series | sm_60, sm_61 | 1.5.2 |
| Maxwell and older | GTX 9xx and older | sm_52 and older | x |

### AMD

| Arch | Family | Target | Last update |
| --- | --- | --- | --- |
| CDNA 1–4 | CDNA GPUs | gfx908, gfx90a, gfx942, gfx950 | x |
| RDNA 4 | RX 9xxx | gfx1200, gfx1201 | 1.5.2 |
| RDNA 3.5 | Ryzen AI APUs | gfx1150–gfx1152 | 1.5.2 |
| RDNA 3 | RX 7xxx / Ryzen APUs | gfx1100–gfx1103 | 1.5.2 |
| RDNA 2 | RX 6xxx / selected Ryzen APUs | gfx1030-gfx1035 | 1.5.2 |
| RDNA 2 | Van Gogh / Raphael APUs | gfx1033, gfx1036 | x |
| RDNA 1 | RX 5xxx / Pro / RDNA 1 APUs | gfx1010–gfx1013 | 1.5.2 |
| GCN 5 / Vega 20 | VII / MI50–MI60 | gfx906 | 1.5.2 |
| GCN 5 / Vega 10 | RX Vega | gfx900 | 1.5.2 |
| GCN 5 / Vega APUs | Ryzen with Vega graphics | gfx902, gfx909, gfx90c | x |
| GCN 3 / 4 | Fiji / Polaris (RX 4xx/5xx) | gfx803 | 1.5.2 |
| Older GCN | Older GPUs / APUs | gfx6xx, gfx7xx, gfx801, gfx802 | x |

## Notes

- Use `--list-devices` to see which GPUs the installed driver exposes to the miner.
- AMD integrated GPUs are excluded by default. Use `--amd-igpu` to enable the supported APU architectures. 
- Legacy AMD GCN GPUs need a runtime that still supports their architecture. Linux ROCm 6 may be required.
- For NVIDIA + Linux, Ubuntu 24.04+ and a CUDA 13-compatible driver are recommended.
