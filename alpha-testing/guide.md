# Guide

### Download

Download the SDK from [Unibase Release](https://github.com/unibaseio/unibase-sdk-go).

### Explorer

{% embed url="https://www.explorer.unibase.io/" %}

### Faucet

* Gas token:  request Holesky ETH first, then send it to L1StandardBridgeProxy: [0x07205FEfD61E11C7AE3aeeb1656451Bad7896a84 ](https://holesky.etherscan.io/address/0x07205FEfD61E11C7AE3aeeb1656451Bad7896a84), you can claim Holesky ETH from the following faucet websites: [Google Faucet](https://cloud.google.com/application/web3/faucet/ethereum/holesky).
* It is advisable to have at least 1 holesky ETH available for transaction sending.
* Token Claim: Upon binary startup, the client automatically claims 100 UB tokens from the server.
* Transaction Costs: Each transaction costs 0.003 gas tokens; adding a piece costs 0.00017 gas tokens; adding a replica costs between 0.003 to 0.005 gas tokens.

### Stream Node

Initialize, defaults to \~/.stream directory, create account with password aidemo123

```bash
./stream init
```

Start daemon, defaults to port 8083, port 8083 must be accessible from the internet

```bash
./stream daemon run -b <BIND_PORT> -e <EXPOSE_URL>
```

Example with external IP 1.2.3.4

```bash
./stream daemon run -b 0.0.0.0:8083 -e http://1.2.3.4:8083
```

Check balance

```bash
./stream chain balance 
```

Check revenue

```bash
./stream chain stream revenue
```

Withdraw revenue&#x20;

```bash
./stream chain stream withdraw
```

### Storage Node

Initialize, defaults to \~/.store directory, create account with password aidemo123

```bash
./store-edge init
```

Start daemon, defaults to port 8082

```bash
./store-edge daemon run -b <BIND_PORT> -e <EXPOSE_URL>
```

Example with external IP 1.2.3.4, port 8082 accessible from the internet

```bash
./store-edge daemon run -b 0.0.0.0:8082 -e http://1.2.3.4:8082
```

Example: No external IP, port 8082 not accessible from the internet

```bash
./store-edge daemon run -b 127.0.0.1:8082
```

Check balance

```bash
./stream chain balance
```

Check revenue information

```bash
./store-edge chain store revenue
```

Withdraw storage revenue, updates available rewards

```bash
./store-edge chain store withdraw
```

Update storage rewards

```bash
./store-edge chain store updateReward
```

Withdraw storage rewards

```bash
./store-edge chain store withdrawReward
```

### Validator Node

Initialize, defaults to \~/.validator directory, create account with password aidemo123

```bash
./validator init
```

Start daemon, defaults to port 8085

```bash
./validator daemon run -b <BIND_PORT>
```

Example

```bash
./validator daemon run -b 127.0.0.1:8085
```

Check Balance

```bash
./validator chain balance
```



