<img width="1298" height="680" alt="krig-readme" src="https://github.com/user-attachments/assets/54974d80-9325-476b-b812-96637857228b" />

# Krig miner
**Pearl (PRL) & Quantus (QTC)** miner for AMD & NVIDIA GPUs by [pool.kryptex.com](https://pool.kryptex.com).

**Download** krig from [releases](https://github.com/kryptex/krig-miner/releases) and subscribe for updates.

Devfee: 0%.

## Pearl (PRL) Hashrate
### AMD

| GPU Model               | RDNA Version | Arch    | Backend | Hashrate      |
| ---------------------   | ------------ | ------- | ------- | ------------- |
| AMD Instinct MI355X     | CDNA 4       | gfx950  | ROCm    | ~550 TH/s     |
| AMD Instinct MI300X     | CDNA 3       | gfx942  | ROCm    | ~318 TH/s     |
| AMD Radeon RX 9070 XT   | RDNA 4       | gfx1201 | ROCm    | ~106 TH/s     |
| AMD Radeon RX 9060 XT   | RDNA 4       | gfx1200 | ROCm    | ~45 TH/s      |
| AMD Radeon RX 7900 XT   | RDNA 3       | gfx1100 | ROCm    | ~41.4 TH/s    |
| AMD Radeon RX 7600      | RDNA 3       | gfx1102 | ROCm    | ~15.4 TH/s    |
| AMD Radeon RX 6750 XT   | RDNA 2       | gfx1031 | ROCm    | ~17.8 TH/s    |
| AMD Radeon RX 6700 XT   | RDNA 2       | gfx1031 | ROCm    | ~15.9 TH/s    |
| AMD Radeon RX 5500 XT   | RDNA 1       | gfx1012 | ROCm    | TBD           |
| AMD Radeon RX 5500      | RDNA 1       | gfx1012 | ROCm    | TBD           |
| AMD Radeon RX 5300      | RDNA 1       | gfx1012 | ROCm    | TBD           |
| AMD Radeon Pro V520     | RDNA 1       | gfx1011 | ROCm    | TBD           |
| AMD Radeon Pro 5600M    | RDNA 1       | gfx1011 | ROCm    | TBD           |
| AMD Radeon VII          | GCN 5        | gfx906  | ROCm    | TBD           |
| AMD Radeon Pro VII      | GCN 5        | gfx906  | ROCm    | TBD           |
| AMD Instinct MI50/MI60  | GCN 5        | gfx906  | ROCm    | TBD           |

These are just examples. Other RDNA & CDNA GPUs are supported, too. See more GPUs there:  
https://pool.kryptex.com/device/gpu?brand=AMD&coin=PRL 

### Nvidia

| GPU Model               | RDNA Version | Arch    | Backend | Hashrate      |
| ---------------------   | ------------ | ------- | ------- | ------------- |
| NVIDIA B300             | Blackwell    | sm_103  | CUDA    | ~431 TH/s     |
| NVIDIA RTX PRO 6000     | Blackwell    | sm_120  | CUDA    | ~422 TH/s     |
| NVIDIA GeForce RTX 6000 | Blackwell    | sm_120  | CUDA    | ~402 TH/s     |
| NVIDIA GeForce RTX 5090 | Blackwell    | sm_120  | CUDA    | ~385 TH/s     |
| NVIDIA GeForce RTX 4090 | Ada Lovelace | sm_89   | CUDA    | ~292 TH/s     |
| NVIDIA L40S             | Ada Lovelace | sm_89   | CUDA    | ~259 TH/s     |
| NVIDIA RTX 6000 Ada     | Ada Lovelace | sm_89   | CUDA    | ~201 TH/s     |
| NVIDIA GeForce RTX 3090 | Ampere       | sm_86   | CUDA    | TBD           |

## Quantus (QTC) Hashrate

### Nvidia

| GPU Model                                  | Architecture | Arch   | Backend | Hashrate   | Power    |
| ------------------------------------------ | ------------ | ------ | ------- | ---------- | -------- |
| NVIDIA GeForce RTX 5090                    | Blackwell    | sm_120 | CUDA    | 1339.7 MH/s | 575 W    |
| NVIDIA RTX PRO 6000                        | Blackwell    | sm_120 | CUDA    | 1336.8 MH/s | 559.3 W  |
| NVIDIA GeForce RTX 4090                    | Ada Lovelace | sm_89  | CUDA    | 967.4 MH/s  | 444.2 W  |
| NVIDIA L40S                                | Ada Lovelace | sm_89  | CUDA    | 892.0 MH/s  | 348.6 W  |
| NVIDIA GeForce RTX 3090                    | Ampere       | sm_86  | CUDA    | 490.4 MH/s  | 370 W    |
| NVIDIA GeForce GTX 1660                    | Turing       | sm_75  | CUDA    | 85.5 MH/s   | 115.65 W |
| NVIDIA GeForce GTX 1080                    | Pascal       | sm_61  | CUDA    | 33.3 MH/s   | 167.66 W |

### AMD

| GPU Model             | Architecture | Arch    | Backend | Hashrate  | Power   |
| --------------------- | ------------ | ------- | ------- | --------- | ------- |
| AMD Radeon RX 7900 XT | RDNA 3       | gfx1100 | ROCm    | 242.6 MH/s | 255.3 W |
| AMD Radeon RX 9070 XT | RDNA 4       | gfx1201 | ROCm    | 155.8 MH/s | 301.6 W |
| AMD Radeon RX 6750 XT | RDNA 2       | gfx1031 | ROCm    | 97.8 MH/s  | 191 W   |
| AMD Radeon RX 7600    | RDNA 3       | gfx1102 | ROCm    | 77.3 MH/s  | 144 W   |

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

## Example
```
./krig-miner --url prl.kryptex.network:8048 --user WALLET/WORKER
```

## Support

Please contact us if you have any problems, questions, or suggestions: 
- support@kryptex.com
- https://t.me/kryptex

Also, feel free to open issues on Github. 
