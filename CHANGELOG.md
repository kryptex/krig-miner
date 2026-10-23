# Changelog

Download the latest release there:

https://github.com/kryptex/krig-miner/releases/latest

## 1.5.11

Faster hashrate:

Quantus (QTC):

- NVIDIA GPU Pascal family
- AMD GPU RDNA 2 family
- NVIDIA GeForce GTX 1080 72.94 MH/s (+124.9%) @ 174.89 W
- AMD RX 6750 XT 199.60 MH/s (+6.13%) @ 196 W
- AMD RX 6700 XT 186.326 MH/s (+1.35%) @ 149 W

## 1.5.10

Faster hashrate:

Quantus (QTC):

- NVIDIA GeForce RTX 5090 1766.12 MH/s (+2.17%) @ 575 W
- NVIDIA GeForce RTX 4090 1375.11 MH/s (+0.68%) @ 449 W
- NVIDIA GeForce RTX 3090 542.01 MH/s (+3.28%) @ 305 W
- NVIDIA CMP 90HX 365.851 MH/s (+3.86%) @ 248.99 W

Intel Arc for Quantus (QTC):

- Windows support
- All Intel Arc A-series GPUs: A770, A750, A580, A380, A310, mobile and Pro models
- New `--no-intel` flag disables Intel GPUs

## 1.5.9

Faster hashrate:

Quantus (QTC):

- AMD GPU RDNA 3 family
- AMD GPU RDNA 4 family
- AMD RX 9070 XT 312.504 MH/s (+66.29%) @ 304 W
- AMD RX 7900 XT 358.053 MH/s (+51.41%) @ 257 W

## 1.5.8

Faster hashrate:

Pearl (PRL):

- NVIDIA DGX Spark GB10 100.49 TH/s (+3.01%) @ 96 W

Quantus (QTC):

- NVIDIA DGX Spark GB10 460.04 MH/s (+54.67%) @ 95.73 W
- AMD RX 6700 XT 183.843 MH/s (+1.04%) @ 146 W
- Intel Arc A750 122.786 MH/s (+3.36%) @ 187.8 W

## 1.5.7

Quantus (QTC) higher hashrate:

- NVIDIA RTX PRO 6000 Blackwell Server Edition: 1881.10 MH/s @ 600.00 W
- NVIDIA GeForce RTX 5090: 1786.76 MH/s @ 574.99 W
- NVIDIA GeForce RTX 4090: 1317.97 MH/s @ 449 W
- NVIDIA RTX 6000 Ada Generation: 989.09 MH/s @ 299.66 W
- NVIDIA CMP 50HX: 377.875 MH/s @ 250 W
- NVIDIA CMP 90HX: 348.275 MH/s @ 320 W
- NVIDIA GeForce RTX 3060: 220.148 MH/s @ 169.25 W
- NVIDIA GeForce GTX 1660: 163.90 MH/s @ 128.92 W
- NVIDIA GeForce GTX 1650: 96.797 MH/s
- Intel Arc A750: 112.819 MH/s @ 187.96 W

## 1.5.6

Support for new regions of [Kryptex pool](https://pool.kryptex.com/)

## 1.5.5

Bugfix for Quantus pool protocol handling

## 1.5.4

Fixed HiveOS and mmpOS hashrate stats for Quantus coin

## 1.5.3

Added 3rd-party mining pools support:

- [Kryptex Pool](https://pool.kryptex.com/): 0% devfee
- 3rd-party pools: 3% devfee

Linux ARM64 miner for NVIDIA:

- DGX Spark (GB10)
- GH200
- GB200
- GB300

(Ubuntu 24.04 or newer with a CUDA 13 driver is required.)

## 1.5.2

Mining support for more GPU models:

Quantus (QTC):

- NVIDIA GeForce GTX 1080: 33.3 MH/s @ 167.66 W
- NVIDIA GeForce GTX 1660: 85.5 MH/s @ 115.65 W
- NVIDIA GeForce RTX 3090: 490.4 MH/s @ 370 W
- NVIDIA GeForce RTX 5090: 1339.7 MH/s @ 575 W
- AMD Radeon RX 6750 XT: 97.8 MH/s @ 191 W
- AMD Radeon RX 7600: 77.3 MH/s @ 144 W
- NVIDIA GTX 10xx/16xx
- AMD RX 400/500
- AMD Vega
- AMD RX 5000/6000/7000/9000
- AMD Ryzen APU support

Pearl (PRL):

- AMD Ryzen integrated GPUs (pass `--amd-igpu` to enable)

## 1.5.1

Quantus (QTC) mining improvements (mine with `--coin quantus`):

- AMD Radeon RX 7900 XT: 242.6 MH/s @ 255.3 W
- AMD Radeon RX 9070 XT: 155.8 MH/s @ 301.6 W
- NVIDIA GeForce RTX 3090: 438.9 MH/s @ 363.1 W

Fixed Pearl (PRL) mining startup failure on Linux for AMD Radeon VII, Radeon Pro VII, and Instinct MI50/MI60 GPUs.

## 1.5.0

Quantus (QTC) mining on NVIDIA GPUs with `--coin quantus`:

- NVIDIA GeForce RTX 4090: 967.4 MH/s @ 444.2 W
- NVIDIA RTX PRO 6000 Blackwell Server Edition: 1336.8 MH/s @ 559.3 W
- NVIDIA GeForce RTX 5090: 1284.6 MH/s @ 518.8 W
- NVIDIA L40S: 892.0 MH/s @ 348.6 W

## 1.4.3

- More NVIDIA monitoring information
- Error/warning logging improvements
- Fault tolerance to invalid CLI arguments: clear errors, ignore instead of exiting

## 1.4.2

- Overclocking (NVIDIA): `--gpu-cclock`, `--gpu-mclock`,
  `--gpu-coffset`, `--gpu-moffset`, `--gpu-plimit`, `--gpu-fan`,
  `--gpu-no-reset-oc`.
- Core and memory clock monitoring.
- Terminal UI: log scrolling with arrow keys, Page Up/Page Down, Home/End,
  and mouse wheel or trackpad.
- Linux AMD monitoring.
- Terminal UI bugfixes.

## 1.4.1

Log to a file: `--log-file <file>`.

Failover pools: add `--url` `--user` `--password` per pool,
or `--url` per pool and `--user` `--password` once.

## 1.4.0

Miner terminal UI for easy monitoring.

To disable, use `--no-tui`.

<img width="2359" height="1241" alt="image"
  src="https://github.com/user-attachments/assets/dca930e6-e49b-4c36-8ef8-0197bdb9828b" />

## Older releases

See [GitHub releases](https://github.com/kryptex/krig-miner/releases).
