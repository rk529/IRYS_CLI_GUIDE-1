<div align="left">

##   **Introduction📔**

>The Irys CLI is a command-line tool for interacting with [Irys](https://irys.xyz/) , a decentralized data availability layer that lets you upload, manage, and retrieve data (files, JSON, metadata, etc.) on-chain or off-chain with permanent storage guarantees.

</div>

---

## Device/System Requirements 💻

>Not any specefic Requirements: should work on any minimal device:



# Install All Require Dependecies

```
sudo apt-get update && sudo apt-get upgrade -y
```

```
sudo apt install curl iptables build-essential git wget lz4 jq make protobuf-compiler cmake gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev screen ufw -y
```


## Install nodejs & npm

>{For Linux}

```
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash - && sudo apt install -y nodejs
```

>{For Mac}


```
brew install node
```

* Check Version

```
node -v
npm -v
```


---

## CLI Installation

```
sudo npm i -g @irys/cli
```

* Verify installation

```
irys 
```

---

## Parameters & Their Usage

| Option         | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| `-n`           | The network to check, `mainnet` or `devnet`, defaults to `mainnet`.         |
| `-t`           | The [token](https://docs.irys.xyz/build/d/features/supported-tokens) to use when funding.                                              |
| `-w`           | Your private key. (without 0x)                                                           |
| `--tags`       | Tags to include, format `<file_name> <file_format>`.                                   |
| `--provider-url` | RPC URL to use.   [FROM_HERE](https://chainlist.org/)                                                        |


---

## Fund Your wallet [Testnet/Devnet]

>Now, You have to deposit testnet tokens (any chain) 

```
irys fund 1000000 \
  -n devnet \
  -t ethereum \
  -w Private_Key \
  --provider-url RPC_URL
```

>Take Faucet: [Ethereum_Sepolia_Faucet](https://sepolia-faucet.pk910.de/) :: If u have to do in another chain then take faucet of that network:

>The fund amount is in `wei`

>Replace `Private_key` with your actual credential (Without 0x)

>Replace `RPC_URL` with your selected network: https://sepolia.drpc.org


<img width="1493" height="316" alt="image" src="https://github.com/user-attachments/assets/a5b83397-9be0-4204-89d9-b1c1fff419a8" />


---


## Check Balance 

```
irys balance WALLET_ADDRESS \
  -t ethereum \
  -n devnet \
  --provider-url RPC_URL
```


>Replace `WALLET_ADDRESS` with your actual one: & `RPC_URL` too:

---

## Upload a File

```
irys upload FILE_NAME \
  -n devnet \
  -t ethereum \
  -w PRIVATE_KEY \
  --tags FILE_NAME FILE_FORMAT \
  --provider-url RPC_URL
```


>Replace `FILE_NAME` with its actual one:

>Replace `PRIVATE_KEY` with your Credential

>Replace `FILE_NAME` & `FILE_FORMAT` (JPG,PNG)

>Replace `RPC_URL` with your selected Network

<img width="1038" height="211" alt="image" src="https://github.com/user-attachments/assets/a3a29264-ea9e-4872-9b4a-b7bf01a64b35" />

✔️✔️✔️

---
