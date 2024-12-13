# 毕业设计代码流程记录

## 环境配置

- Ubuntu 24.04.1 LTS
- Geth 1.14.12-stable
- Solidity 0.8.28+commit.7893614a.Linux.g++

### 问题记录

flag provided but not defined: --rpc
> 版本更新导致的命令行参数变化  
> 使用`--http`代替`--rpc`  
> 使用`--http.api`代替`--rpcapi`  
> 使用`--http.cordomain`代替`--rpccorsdomain`  
> 参考：[https://github.com/ethereum/go-ethereum/wiki/Command-Line-Options](https://github.com/ethereum/go-ethereum/wiki/Command-Line-Options)
