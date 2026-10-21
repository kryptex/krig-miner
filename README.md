<img width="1298" height="680" alt="krig-readme" src="https://github.com/user-attachments/assets/54974d80-9325-476b-b812-96637857228b" />

# Krig miner
**Pearl (PRL) & Quantus (QTC)** miner for AMD & NVIDIA GPUs (Quantus also runs on Intel Arc A-series) by [pool.kryptex.com](https://pool.kryptex.com).

Quick start:
1. **Download** krig from [releases](https://github.com/kryptex/krig-miner/releases) and subscribe for updates.
2. Connect to Kryptex Pool:
   ```
   ./krig-miner --url prl.kryptex.network:8048 --user WALLET/WORKER
   ```
See [all the supported GPUs](GPUs.md) or check our [hashrate database](https://pool.kryptex.com/device/gpu?coin=PRL).

## Hashrate

These are just examples. Other AMD & NVIDIA GPUs are supported, too. Hashrate values may be outdated. 

### Pearl (PRL) Hashrate
#### AMD

| GPU Model               | Architecture | Arch    | Hashrate      |
| ---------------------   | ------------ | ------- | ------------- |
| AMD Instinct MI355X     | CDNA 4       | gfx950  | ~550 TH/s     |
| AMD Instinct MI300X     | CDNA 3       | gfx942  | ~318 TH/s     |
| AMD Radeon RX 9070 XT   | RDNA 4       | gfx1201 | ~106 TH/s     |
| AMD Radeon RX 9060 XT   | RDNA 4       | gfx1200 | ~45 TH/s      |
| AMD Radeon RX 7900 XT   | RDNA 3       | gfx1100 | ~41.4 TH/s    |
| AMD Radeon RX 7600      | RDNA 3       | gfx1102 | ~15.4 TH/s    |
| AMD Radeon RX 6750 XT   | RDNA 2       | gfx1031 | ~17.8 TH/s    |
| AMD Radeon RX 5500      | RDNA 1       | gfx1012 | Supported     |
| AMD Radeon VII          | GCN 5        | gfx906  | Supported     |
| AMD Instinct MI50/MI60  | GCN 5        | gfx906  | Supported     |

#### Nvidia

| GPU Model               | Architecture | Arch    | Hashrate      |
| ---------------------   | ------------ | ------- | ------------- |
| NVIDIA B300             | Blackwell    | sm_103  | ~431 TH/s     |
| NVIDIA RTX PRO 6000     | Blackwell    | sm_120  | ~422 TH/s     |
| NVIDIA GeForce RTX 6000 | Blackwell    | sm_120  | ~402 TH/s     |
| NVIDIA GeForce RTX 5090 | Blackwell    | sm_120  | ~385 TH/s     |
| NVIDIA GeForce RTX 4090 | Ada Lovelace | sm_89   | ~292 TH/s     |
| NVIDIA GeForce RTX 3090 | Ampere       | sm_86   | Supported     |
| NVIDIA L40S             | Ada Lovelace | sm_89   | ~259 TH/s     |
| NVIDIA RTX 6000 Ada     | Ada Lovelace | sm_89   | ~201 TH/s     |
| NVIDIA DGX Spark GB10   | Blackwell    | sm_121  | ~100 TH/s     |

### Quantus (QTC) Hashrate

#### Nvidia

| GPU Model               | Architecture | Arch   | Hashrate    | Power   |
| ----------------------- | ------------ | ------ | ----------- | ------- |
| NVIDIA RTX PRO 6000     | Blackwell    | sm_120 | 1881.1 MH/s | 600 W   |
| NVIDIA GeForce RTX 5090 | Blackwell    | sm_120 | 1766.1 MH/s | 575 W   |
| NVIDIA GeForce RTX 4090 | Ada Lovelace | sm_89  | 1375.1 MH/s | 449 W   |
| NVIDIA RTX 6000 Ada     | Ada Lovelace | sm_89  | 989.1 MH/s  | 299.7 W |
| NVIDIA L40S             | Ada Lovelace | sm_89  | 892.0 MH/s  | 348.6 W |
| NVIDIA GeForce RTX 3090 | Ampere       | sm_86  | 542.0 MH/s  | 305 W   |
| NVIDIA DGX Spark GB10   | Blackwell    | sm_121 | 460.0 MH/s  | 95.7 W  |
| NVIDIA CMP 50HX         | Turing       | sm_75  | 377.9 MH/s  | 250 W   |
| NVIDIA CMP 90HX         | Ampere       | sm_86  | 365.9 MH/s  | 249 W   |
| NVIDIA GeForce RTX 3060 | Ampere       | sm_86  | 220.1 MH/s  | 169.3 W |
| NVIDIA GeForce GTX 1660 | Turing       | sm_75  | 163.9 MH/s  | 128.9 W |
| NVIDIA GeForce GTX 1650 | Turing       | sm_75  | 96.8 MH/s   | 75 W    |
| NVIDIA GeForce GTX 1080 | Pascal       | sm_61  | 33.3 MH/s   | 167.7 W |

#### AMD

| GPU Model                       | Architecture | Arch    | Hashrate   | Power |
| ------------------------------- | ------------ | ------- | ---------- | ----- |
| AMD Radeon RX 7900 XT           | RDNA 3       | gfx1100 | 358.1 MH/s | 257 W |
| AMD Radeon RX 9070 XT           | RDNA 4       | gfx1201 | 312.5 MH/s | 304 W |
| AMD Radeon RX 6700 XT / 6750 XT | RDNA 2       | gfx1031 | 183.8 MH/s | 146 W |
| AMD Radeon RX 7600              | RDNA 3       | gfx1102 | 77.3 MH/s  | 144 W |

#### Intel

| GPU Model      | Architecture       | Arch    | Hashrate   | Power   |
| -------------- | ------------------ | ------- | ---------- | ------- |
| Intel Arc A750 | Xe-HPG (Alchemist) | acm-g10 | 122.8 MH/s | 187.8 W |

All Intel Arc A-series GPUs (A770, A750, A580, A380, A310, mobile and Pro models) are supported since 1.5.10 on Windows, Linux, HiveOS and mmpOS. The Intel GPU driver with Level Zero is required (`ze_loader.dll` on Windows, `libze_loader.so.1` on Linux). The hashrate above is measured on Linux; on Windows the A750 is currently about 25% slower. Use `--no-intel` to disable Intel GPUs.

## Usage

```
usage: krig-miner [options]

options:
  -o, --url <url>          Pool endpoint: [scheme://]host[:port]
                             pearl    stratum+ssl://
                             quantus  stratum+ssl://
      --coin <coin>        Coin to mine
                             pearl    default; aliases: prl, pearlhash
                             quantus  alias: qtc
      --algorithm <coin>   Alias for --coin
      --algo <coin>        Alias for --coin
      --pool <url>         Alias for --url
  -u, --user <wallet>      Payout wallet
      --wallet <wallet>    Alias for --user
  -p, --password <pw>      Pool password
  Failover pools: add --url --user --password per pool,
                  or --url per pool and --user --password once
      --api-port <port>    Enable the HTTP API on <port>
      --api-host <ip>      Bind interface for the API (optional; default 127.0.0.1)
                             e.g. --api-port 12000 --api-host 127.0.0.1
  -d, --devices <list>     Devices to mine on: comma-separated 0-based indices
                             (as shown by --list-devices), or 'all' (default —
                             every detected CUDA and ROCm device). e.g. -d 0,2
      --devices-pci <list> Devices to mine on, by PCI address: comma-separated
                             bus:device.function. e.g. --devices-pci 01:00.0,0a:00.0
      --amd-igpu           Include AMD integrated GPUs (APU/iGPU); excluded
                             by default. Affects -d and --list-devices indices.
      --no-cuda            Disable the CUDA backend (don't load CUDA DLLs or
                             enumerate NVIDIA GPUs). By default both backends
                             run and all CUDA + ROCm devices are mined.
      --no-rocm            Disable the ROCm backend (don't load HIP DLLs or
                             enumerate AMD GPUs)
      --no-intel           Disable the Intel Level Zero backend (don't load
                             ze_loader or enumerate Intel Arc GPUs; Quantus only)
      --rocm-runtime <6|7> Pin the HIP runtime major; by default 6 is tried
                             first, then 7
      --gpu-cclock <MHz>   Lock NVIDIA core clock
      --gpu-mclock <MHz>   Lock NVIDIA memory clock
      --gpu-coffset <MHz>  Set NVIDIA core clock offset (signed)
      --gpu-moffset <MHz>  Set NVIDIA memory clock offset (signed)
      --gpu-plimit <watts> Set NVIDIA board power limit
      --gpu-fan <percent>  Set every fan on each NVIDIA GPU (0-100)
                             One value applies to all selected NVIDIA GPUs;
                             lists follow selected-device order, '_' skips.
      --gpu-no-reset-oc    Keep NVIDIA settings on exit
  -l, --log-level <level>  Console verbosity: trace|debug|info|warn|error|
                             critical|none (default info). debug restores the
                             detailed per-job/per-share diagnostic output.
      --log-file <file>  log to a file
      --no-tui             Disable the interactive terminal UI and print logs
                             line by line (also automatic when redirected)
      --list-devices       List detected devices (index/name/pci) and exit
  -h, --help               Print this help and exit
  -V, --version            Print version and exit
```

## Support

Please contact us if you have any problems, questions, or suggestions: 
- support@kryptex.com
- https://t.me/kryptex

Also, feel free to open issues on Github. 
