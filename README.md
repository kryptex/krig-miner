# krig-miner
GPU miner for Pearl (PRL) by pool.kryptex.com

## Hashrate

| GPU Model             | RDNA Version | Arch    | Backend | Hashrate      |
| --------------------- | ------------ | ------- | ------- | ------------- |
| AMD Instinct MI300X   | CDNA 3       | gfx942  | ROCm    | ~318 TH/s     |
| AMD Radeon RX 9070 XT | RDNA 4       | gfx1201 | ROCm    | ~90.5 TH/s    |
| AMD Radeon RX 9060 XT | RDNA 4       | gfx1200 | ROCm    | ~45 TH/s      |
| AMD Radeon RX 7900 XT | RDNA 3       | gfx1100 | ROCm    | ~38 TH/s      |
| AMD Radeon RX 7600    | RDNA 3       | gfx1102 | ROCm    | ~14.7 TH/s    |
| AMD Radeon RX 6750 XT | RDNA 2       | gfx1031 | ROCm    | ~14.5 TH/s    |
| AMD Radeon RX 6700 XT | RDNA 2       | gfx1031 | ROCm    | ~13.5 TH/s    |

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
  -h, --help               Print this help and exit
  -V, --version            Print version and exit
```

## Example
```
./krig-miner --url prl.kryptex.network:8048 --user WALLET/WORKER
```

