
# 1.Operation chain node

### 1.1 download

```bash
git clone https://github.com/hamster-shared/hamster.git && cd hamster
```

### 1.2 Build

The `cargo run` command will perform an initial build. Use the following command to build the node
without launching it:

```sh
cargo build --release
```
### 1.3 Run

```bash
./target/release/node-template --dev --ws-external --rpc-external --rpc-cors all --unsafe-rpc-external --rpc-methods unsafe --unsafe-ws-external --no-mdns
```
# 2.Operating the Gateway Client

### 2.1 download

```bash
git clone https://github.com/hamster-shared/hamster-gateway.git && cd hamster-gateway
```

### 2.2 build

```sh
go mod tidy
go build
```

### 2.3 run

```bash
./hamster-gateway daemon (windows The run command is hamster-gateway.exe)
```

# 3. Operate the gateway web application
### 3.1 download
```bash
git clone https://github.com/hamster-shared/hamster-gateway.git && cd hamster-gateway/frontend
```
### 3.2 Install dependencies
```bash
npm install
```

### 3.3 run
```bash
npm run server
```
### 3.4  address
```bash
http://localhost:3100
```
