# lp_ui

## 先决条件

- Docker
- NodeJS v14+

从这个 repo 的根目录运行以下命令

```bash
DOCKER_BUILDKIT=1 docker build --target node-export -f Dockerfile.proto -o type=local,dest=. .
DOCKER_BUILDKIT=1 docker build -f solana/Dockerfile.wasm -o type=local,dest=. solana
npm ci --prefix ethereum
npm ci --prefix sdk/js
npm run build --prefix sdk/js
```

The remaining steps can be run from this folder

## Install

```bash
npm ci
```

## Develop

```bash
npm start
```
