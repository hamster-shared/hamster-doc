# Hamster Node

Hamster Nodes are the underlying chain nodes of the Hamster Network and provide services to the entire Hamster Network.

# 1. Overview

## 1.1 Node Responsibilities

Hamster node is a custom node built on Substrate framework . It provides basic functions such as provider registration, calculating market, and executing orders.

## 1.2 Hardware

Hamster nodes need to perform block-out and packetization transactions, so they have certain requirements on the system hardware. At the same time, since the block-out process and packaged transaction process require high network stability, we recommend that the block-out node use a fixed public IP, otherwise it will bring losses due to block-out instability and other situations.

# 2. Run

We offer two different ways to start the underlying chain, one as a docker and also by compiling the source code directly, we recommend the first one here

## 2.1 Docker

docker is the easiest way to build, we recommend using docker for building Hamster nodes

Points to note before run in docker：

- You need to install [docker][https://www.docker.com/] by yourself before starting, refer to docker official website for details

* You can choose to run your own test node with Docker. The docker build command is as follows, where YourDataDir is your local directory address, YourNodeName is your node name 

```bash
docker run -p 30333:30333 -p 9944:9944 -p 9933:9933 --restart=always -d -v <YourDataDir>:/tmp/db hamstershare/hamster:v1.0.0 /opt/ttchain/node-template --dev --name <YourNodeName> --ws-external --rpc-external --rpc-cors all --unsafe-rpc-external --rpc-methods unsafe --unsafe-ws-external --no-mdns
```

## 2.2 Binary

### Rust Setup

First, complete the [basic Rust setup instructions](https://github.com/hamster-shared/hamster/blob/main/docs/rust-setup.md).

### download

```bash
git clone https://github.com/hamster-shared/hamster.git && cd hamster
```

### Build

The `cargo run` command will perform an initial build. Use the following command to build the node
without launching it:

```sh
cargo build --release
```

### Embedded Docs

Once the project has been built, the following command can be used to explore all parameters and subcommands:

```bash
./target/release/node-template -h
```

### Run

```bash
./target/release/node-template --dev --ws-external --rpc-external --rpc-cors all --unsafe-rpc-external --rpc-methods unsafe --unsafe-ws-external --no-mdns
```

# 3. Create an account

## 3.1 Create accounts

First go to [polkadot.js.org](https://polkadot.js.org/apps/), click the icon on the top left corner, then select "DEVELOPMENT", click "Local Node", and finally click "Switch" to enter the blockchain browser interface

![image-20220221164251970](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220221164252.png)

Or, if your chain node has a public ip, you can enter your own ip in the address field below and click save.

![image-20220223141139131](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220223141139.png)



Then click on "Accounts", "Accounts", "Add account".

![image-20220221164436150](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220221164436.png)

Please make sure to save your own mnemonic seeds and click "Next". Enter name and password.

![image-20220221164601246](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220221164601.png)

## 3.2 transfer

All transactions on the chain require tokens, you can try a test account first and trade a certain amount of tokens into your account

![image-20220223141906963](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220223141907.png)

Select "send", select the account and amount, and click "Make Transfer"

![image-20220223142022730](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220223142022.png)

At this point, you have a test chain and the address on the test chain

