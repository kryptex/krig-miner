<img width="1200" height="629" alt="krig-readme-v3" src="https://github.com/user-attachments/assets/2c38d034-71d1-4db9-b376-91b2dc58a0d4" />

# Krig miner
**Pearl (PRL)** miner for AMD GPUs by [pool.kryptex.com](https://pool.kryptex.com).

**Download** krig from [releases](https://github.com/kryptex/krig-miner/releases) and subscribe for updates.

## Hashrate

| GPU Model               | RDNA Version | Arch    | Backend | Hashrate      |
| ---------------------   | ------------ | ------- | ------- | ------------- |
| AMD Instinct MI355X     | CDNA 4       | gfx950  | ROCm    | ~550 TH/s     |
| AMD Instinct MI300X     | CDNA 3       | gfx942  | ROCm    | ~318 TH/s     |
| AMD Radeon RX 9070 XT   | RDNA 4       | gfx1201 | ROCm    | ~90.5 TH/s    |
| AMD Radeon RX 9060 XT   | RDNA 4       | gfx1200 | ROCm    | ~45 TH/s      |
| AMD Radeon RX 7900 XT   | RDNA 3       | gfx1100 | ROCm    | ~38 TH/s      |
| AMD Radeon RX 7600      | RDNA 3       | gfx1102 | ROCm    | ~14.7 TH/s    |
| AMD Radeon RX 6750 XT   | RDNA 2       | gfx1031 | ROCm    | ~14.5 TH/s    |
| AMD Radeon RX 6700 XT   | RDNA 2       | gfx1031 | ROCm    | ~13.5 TH/s    |
| NVIDIA GeForce RTX 5090 | Blackwell    | sm_120  | CUDA    | ~335 TH/s     |
| NVIDIA GeForce RTX 4090 | Ada Lovelace | sm_89   | CUDA    | ~254 TH/s     |

These are just examples. Other RDNA & CDNA GPUs are supported, too. See more GPUs there:  
https://pool.kryptex.com/device/gpu?brand=AMD&coin=PRL 

## Usage

```
usage: krig-miner [options]

options:
  -o, --url <url>          Pool endpoint: [scheme://]host[:port]
                             scheme: stratum+ssl:// (TLS only)
      --pool <url>         Alias for --url
  -u, --user <wallet>      Payout wallet
      --wallet <wallet>    Alias for --user
  -p, --password <pw>      Pool password
      --api-port <port>    Enable the Prometheus /metrics exposer on <port>
      --api-host <ip>      Bind interface for the exposer (optional; default *)
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
