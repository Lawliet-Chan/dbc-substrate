# Substrate


## 环境配置
### 安装 rust
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
### 安装 WASM
rustup target add wasm32-unknown-unknown --toolchain nightly-2020-03-09

### 安装 dbc-substrate
git clone https://github.com/Lawliet-Chan/dbc-substrate.git

## 编译
cd dbc-substrate/bin/node/cli && cargo build --release

## 运行
### 清空区块链存储 (每次启动链之前都要执行此操作)
cd ~/dbc-substrate/ && ./target/release/substrate purge-chain --dev -y
### 启动区块链
cd ~/dbc-substrate/ && ./target/release/substrate --dev

## 打开前端页面
在浏览器里输入 https://polkadot.js.org/apps/#/settings?rpc=ws://127.0.0.1:9944
点击左侧栏中的 `Transfer` 按钮即可看见

